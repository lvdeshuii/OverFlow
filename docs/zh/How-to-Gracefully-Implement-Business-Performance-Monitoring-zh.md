# 如何优雅地实现业务性能监控

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/How-to-Gracefully-Implement-Business-Performance-Monitoring-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/How-to-Gracefully-Implement-Business-Performance-Monitoring-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/How-to-Gracefully-Implement-Business-Performance-Monitoring-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/How-to-Gracefully-Implement-Business-Performance-Monitoring-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/How-to-Gracefully-Implement-Business-Performance-Monitoring-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/How-to-Gracefully-Implement-Business-Performance-Monitoring-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/How-to-Gracefully-Implement-Business-Performance-Monitoring-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/How-to-Gracefully-Implement-Business-Performance-Monitoring-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/How-to-Gracefully-Implement-Business-Performance-Monitoring-ru.md)


在监控工具如此繁多的今天，如何化繁为简，帮助用户优雅地实现业务性能监控？

### **1. 以业务为中心的监控视角**

鉴于监控指标与监控意图的差异，应用性能监控产品的告警逻辑也不尽相同，一般被分为两类：一类被称作“自下而上”式的告警：在数据包头等底层数据中设计告警点，再向上排查应用与服务的利用率等，最后锁定哪些业务出现异常（譬如DNS错误、响应时间慢）等；另一类则被称作“自上而下”式的告警：通过监测业务的应用节点与部分网络节点，设定上层聚合数据的告警指标，从顶层的业务问题出发深入钻取底层数据。由于底层数据误告量大、不易排查，“自下而上”式的告警既耗时又不精准；而“自上而下”式的告警设置可以在系统或服务发生故障的瞬间快速告警，在以业务为核心的运维体系架构中显得尤为重要。

![002316seeudyfefdc8nldk.jpg](http://image.sciencenet.cn/album/201306/28/002316seeudyfefdc8nldk.jpg)

*图 1：知识层级图*

天旦BPC在技术上采取“自上而下”的监控方式，通过端到端的监控覆盖，拥有从宏观到微观的洞察能力，以业务为中心，打通运维与运营的屏障，统一监控与业务视角，充分保证告警指标分析的精准性、可读性。

### **2. 以用户为中心的设计理念**

用钢琴键代表时间，用四宫格呈现业务关键指标，是天旦BPC的关键设计。

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyo1rZQMYRmK4Yfiambegqu7bWA3usmGboVBg1Ziav7DHAmztEEPeSWuh7Q/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*图 2：钢琴键与四宫格在天旦BPC故障告警与定位中的运用*

**为什么1个钢琴键代表1分钟？**

为了让用户实时感知业务运行的状态，同时又能让重复、紧张的工作尽可能优雅放松，天旦选择用钢琴键来代表时间。BPC将一段时间具象为由1分钟片段组成的时间线，通过不同的颜色表达业务状态。使用者通过鼠标在钢琴键上移动进行信息交互，如同弹奏钢琴。当鼠标聚焦到某一个具体的时间片段，琴键随即放大。每一个细微的设计，都是确保用户能够精准获取信息的用心。

其次，采用分钟级的告警设置是为了满足告警实时性与成本的考量。基于大量金融客户的实践，天旦发现告警颗粒度过小，告警数量会海量增多，但告警事件基本重复的；而使用告警颗粒度过大，告警则不及时、甚至出现错漏和滞后。因此，天旦的产品专家最终决定将1分钟设为告警颗粒度，也意味着1个钢琴键代表1分钟。

尽管分钟级粒度的告警可以覆盖大多数场景，但部分行业的需求依然无法满足。例如券商的股票交易，股票交易监控实时性要求更高，当某类特征出现，即视为故障发生，比如可以将告警的触发条件定义为在1秒内连续出现10次特定事件、单笔交易时长超过10ms等。由此，天旦BPC诞生了第二类告警模式：根据事件特征秒级触发告警。

**如何展示黄金指标**

天旦的产品专家发现交易量与应用服务负载成正比，响应率与系统健康度成正比，成功率与业务健康度成正比，交易响应时间与客户体验成反比，并基于金融行业属性，横向比较分析Four Golden Signals、RED、USE指标，最终将交易量、响应率、响应时间、成功率作为天旦BPC的四大黄金指标。

站在以用户为中心的设计角度，如何为用户清晰直观地呈现四大黄金指标，创造更好的用户体验。为此，天旦的产品专家与用户体验设计师进行了大量分析、假设、实验与验证，最终诞生了业界首创的四宫格。

四宫格展示的灵感源自天旦联合创始人&首席产品官Wizard在纽约的现代艺术博物馆的一次参观。在展览中，有一张图呈现了当时美国的地理、人口等信息，通过方格形式清晰的展示指标，再将四个方格组成网格，与应用组件及网络的概念不谋而合。这让我们发现呈现最关键的信息，不在于全、而在于让观看者准确地获取最关键的信息。再放眼观察生活中无处不在的信息导览牌、高速公路指示牌、交通引导符号等。最终结合快速获取告警信息的用户需求与现实的IT环境，设计出了经典的四宫格。

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq0zib9UrUva92PkicX1HbHqyo8icuiaU00eVBRmcY23lm9lq2fzViaRNFP7DiaiccI3GpszkEpyQFMf4TEQw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)

*图 3：纽约现代艺术博物馆经典四宫格:*

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyoVNumuLZRlcb00S7bS3dP9oicnycxmmwSAGrvAukAunwnB6HePm1FFUg/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*图 4：天旦BPC经典四宫格:*

BPC产品源于对用户需求精准的理解与产品精准的设计。以客户视角洞察告警的需求，从功能设计中呈现告警指标，站在用户体验的角度设计出钢琴键与四宫格，以人、服务为中心的理念让天旦在创造软件产品的过程中既能理解用户痛点，又能帮助用户使用产品，实现产品功能价值与用户侧价值的统一。

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
