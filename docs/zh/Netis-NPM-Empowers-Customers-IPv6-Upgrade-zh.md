# 天旦NPM助力客户IPV6改造

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Netis-NPM-Empowers-Customers-IPv6-Upgrade-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Netis-NPM-Empowers-Customers-IPv6-Upgrade-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Netis-NPM-Empowers-Customers-IPv6-Upgrade-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Netis-NPM-Empowers-Customers-IPv6-Upgrade-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Netis-NPM-Empowers-Customers-IPv6-Upgrade-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Netis-NPM-Empowers-Customers-IPv6-Upgrade-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ru.md)

**案例背景**

中国中央网信办、国家发展改革委、工业和信息化部于2021年7月联合印发《关于加快推进互联网协议第六版（IPv6）规模部署和应用工作的通知》，《通知》明确提出将 **“深入推进金融机构IPv6改造，持续提高金融服务机构面向公众服务的互联网应用系统IPv6支持能力，健全IPv6监控运维体系。”** 作为IPv6规模部署和应用的重点任务。

**案例简述**

某银行积极响应三部委号召，全力落实IPv6改造工作。截止2022年初，面向互联网的网络分区建立IPv4+IPv6双栈承载网络，门户网站、网上银行、手机银行、微信银行等面向公众服务的应用系统增加对IPv6支持能力。为提高IPv4+IPv6双栈网络运维能力，健全双栈运维体系，该银行在传统网络运维基础上，引入业界先进的全流量网络分析系统（天旦NPM），对互联网相关应用及重要网络分区的网络流量进行实时监控。

**案例价值**

- 网络流量可视化：快速直观展现网络拓扑结构及内容，为后期挖掘网络内部商业价值奠定基础。
- 业务视角服务路径图：打破传统网络运维和应用运维的竖井；
- 互联网应用IPv4与IPv6对比视图：及时了解IPv4与IPv6应用的访问量、网络性能指标，动态调整相关网络资源，快速响应应用需求；
- 网络异常准确定位、快速告警：缩短故障处理时间，提高网络服务质量；

**1. 天旦NPM，一体化网络流量管理平台**

全流量网络分析系统基于成熟的网络镜像技术，实时将网络流量复制到网络分流器（TAP），再利用TAP的流量汇聚、打标签、分发等功能，把指定的流量分别送到不同的后端探针设备。探针设备对网络流量进行分析处理后，通过一体化管理平台进行统一管理和展现。

![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdmOY8s0Zx1QLXLJAwZPCTCVweXBzFohlQVec4ZWSD75iafRL0nuxPedQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

*图 1：天旦NPM逻辑部署架构*



通过对互联网出口专线、安全设备前后交换机进行全流量分析，建立IPv4和IPv6独立的可视化视图，对网络状态进行实时监测，运维人员可以快速及时地了解网络日常状态。

![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdzV9UeJb7j2j2MdKqialiaWyAg8aaWdNAnxxkH5ibOpcL3mykCg1G68bPA/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

*图 2：某IPv4专线出口链路视图-应用性能指标*

![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdLebyqoTAYIJEwomHz2EAtVUYrickXjJ57I8POcGUIXDL3wg7TzyibD6w/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

*图 3：某IPv4专线出口链路视图-网络负载*

![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdNd5IJZE9kThvyGBOKXnLbicb8h9yHh7gQZXriboIntLgvIXEjXSFLUrQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

*图 4：某IPv6专线出口链路视图-网络负载*

**2. 独创SPV，从应用角度看网络**

日常运维工作中网络和应用分属不同团队负责，在业务出现问题时，各自为战，严重影响故障定位和处理的速度。天旦NPM另辟蹊径，独创的服务路径图（SPV）技术基于业务视角建立全链路端到端的监控体系，从应用角度看网络。SPV从负载量、网络性能、应用性能、应用可用性四大维度展现应用的网络状态，协助运维人员在应用出现问题时可以准确定位快速排障。

![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrd7ibZGpAdR6x5s4JPYOrSQqgibTXTVoK53cRxPSawqYnplztwXVAiaNIFQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

*图 5：天旦NPM基于业务视角的服务路径图*

**3. 一屏看清：IPv4和IPv6网络指标对比**

在互联网出口，某银行基于天旦NPM专业大屏，定制出口专线IPv4和IPv6网络指标对比大屏，实时掌握互联网出口状态，有效提升用户体验。

![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrd0icN9vsmAf2Tp1gks2V2Z3nx266D6ia02XqbTP9Jvu1srs0ve7xFa2Dw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

*图 6：天旦NPM大屏*

针对面向公众的重要业务系统，定制日报、周报、月报等级别的报表，按需求报送相关监管部门。

![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdIngXzdI72uJ9mrwpx0LHnmpWslsam5qu2s1R5ADQDcTos941Xz4vXg/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

*图 7：重要业务的周报报表*

天旦产品全面支持IPv6业务分析，有效保障客户IPv6业务稳定运行。
***
At Netis, we're at the forefront of analyzing business(APM) and network performance(NPM), ensuring that over thirty billion transactions run smoothly every day. Our commitment to system and data security is paramount, and we pride ourselves on our ability to conduct real-time analysis through network traffic mirroring. This means we can get the job done without the need for any agents or disruptions to your existing operations. Based in Shanghai, China, Netis is a global software company known for its high-performance products and cost-effective solutions. Interested in what we offer? Don't hesitate to get in touch. We're excited about the possibility of working together and welcoming new partners.  
Discover more at: www.netis.com/en/  
Or drop me a line directly: dennis.li@netis.com
