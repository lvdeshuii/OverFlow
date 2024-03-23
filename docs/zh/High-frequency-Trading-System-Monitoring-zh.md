# 极速交易系统监控

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/High-frequency-Trading-System-Monitoring-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/High-frequency-Trading-System-Monitoring-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/High-frequency-Trading-System-Monitoring-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/High-frequency-Trading-System-Monitoring-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/High-frequency-Trading-System-Monitoring-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/High-frequency-Trading-System-Monitoring-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/High-frequency-Trading-System-Monitoring-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/High-frequency-Trading-System-Monitoring-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/High-frequency-Trading-System-Monitoring-ru.md)

在交易系统的发展过程中，交易者对快的追求始终如一。随着量化交易的逐渐流行，交易者对极速系统的需求愈加强烈。

### 极速交易系统面临的监控挑战

极速交易系统的出现，进一步加剧了应用运维的管理难度，对运维监控工具的监测精度、产品性能与稳定性提出了极高要求。

- 纳秒级的监测精度需求：极速交易需要更快速地处理订单、低延迟地反馈行情，交易处理速度一般维持在微秒范围内。传统监控工具难以实现微秒甚至纳秒级的测量精度，无法满足极速交易系统的“奔跑”需求。
- 专业的协议解码需求：传统监控工具缺乏丰富的业务系统解码能力，无法全面支持所有主流极速交易系统的自动解码。
- 减少对系统性能的影响：传统日志类、插码类工具消耗系统性能，影响系统稳定性，无法对极速交易系统实现精准监控。

因此，应用运维部门需要采用高精度、高性能、解码能力强的监控工具，通过比极速交易“更极速”的监控能力，解决故障排查难、定位难、分析难等一系列运维难题，保障极速交易系统极速“奔跑”。

### BPC极速交易版

多年来，天旦BPC持续保障证券机构用户的业务连续性。通过旁路部署获取网络流量，天旦BPC所提供的四大黄金指标、智能告警、单笔交易追踪、多维统计分析等功能。天旦升级发布“BPC极速交易版”，提供纳秒级监控能力，为极速交易系统提供全方位的运维保障。

**纳秒级的时间戳技术**

极速交易系统的核心穿透时延、上行时延、全链路穿透时延大多以微秒为单位，这就要求运维监控产品的时延监测精度需控制在微秒、甚至纳秒范围内。“BPC极速交易版”将监测精度从“微秒级”提升至“纳秒级”，通过纳秒级的高精度时间戳，可快速计算各交易环节耗时与全链路交易耗时；基于精准的时延测度，一旦单笔订单时延过大，即刻进行智能告警；通过呈现时延与吞吐量对应关系、一键追踪等功能，精准定位故障根因。

**以业务为中心的监控视角**

“BPC极速交易版”根据实际业务路径，以服务为向导，智能梳理系统间的逻辑访问关系。通过服务路径图实时监控核心中间件、交易所组件状态，提供交易量、响应时间、响应率、成功率等四大黄金指标，帮助运维人员快速定位问题。

![%E6%99%BA%E8%83%BD%E6%95%85%E9%9A%9C%E5%91%8A%E8%AD%A6-scaled.jpg](https://www.netis.com/wp-content/uploads/2022/05/%E6%99%BA%E8%83%BD%E6%95%85%E9%9A%9C%E5%91%8A%E8%AD%A6-scaled.jpg)

*图 1：service path view*

**多段交易追踪功能**

通过多段交易追踪功能，将单笔订单在全交易链路上、各关键节点的数据进行智能关联；一键点击，便能直观分析每笔订单在各节点的处理耗时等具体情况。

“BPC极速交易版”将极速交易订单请求、订单内部响应、订单交易所响应报文等进行全量、极速解析；通过高性能网卡的高精度时间戳，计算出全链路耗时（订单请求与订单交易所响应）、中间件处理耗时（订单请求、订单内部响应）等各项指标，辅助运维人员进行具体分析；并基于实际运维场景，灵活构建证券秒级监控视图。

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq19VyEficPiaZ2k9iaJhBWWYicHSHVWKyCm89sMW99ER72MfE1GBUsmQob7o6hmpjQvUD3BrDsFV33zlQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

*图 2：多段交易追踪功能*

**全面支持主流极速交易系统，极速监控即刻落地**

基于天旦业界领先的解码能力，目前，“BPC极速交易版”已全面适配恒生、华锐、顶点等众多主流极速交易系统，并广泛支持上交所组播、深交所组播等交易所行情系统和私有行情分发系统等。BPC支持灵活定制解码，可快速适配第三方协议解码需求。

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
