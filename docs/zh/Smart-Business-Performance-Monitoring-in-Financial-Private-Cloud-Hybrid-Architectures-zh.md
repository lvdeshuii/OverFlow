# 用户案例：金融私有云混合架构下的智能业务性能监控

**Other Languages**

+ [Chinese / 中文](/docs/zh/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-zh.md)
+ [English](/docs/en/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-en.md)
+ [Spanish / español / castellano](/docs/es/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-es.md)
+ [Japanese / 日本語](/docs/ja/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-ja.md)
+ [German / Deutsch](/docs/de/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-de.md)
+ [French / français](/docs/fr/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-fr.md)
+ [Arabic / al arabiya / العربية](/docs/ar/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-ar.md)
+ [Portuguese (Portugal)](/docs/pt/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-pt.md)
  
作为承载信息系统运行的核心底座，金融机构的IT基础设施也因此面临着来自数字化转型和技术自主的双重挑战，而金融私有云也渐渐成为了各金融机构应对挑战的选择之一。
近年来，某城商行致力于大力发展私有云作为金融科技赋能业务的新形态，联合先进的云厂商在金融云基础设施及服务、场景金融创新、云原生业务系统开发等领域开展联合研究与技术攻关，共同推进该城商行金融私有云技术架构的落地。最终，持续地将重要业务系统部署或者迁移到金融私有云上。此举已经带来了诸多的益处，比如：业务响应能力的提升、资源成本的优化、安全性能的提升等等，但同时也给运维管理带来了不小的挑战。
1、跨越云服务器/容器云等混合云架构，如何做到流量的统一采集和管理；
2、混合架构下，业务访问关系复杂，监控易出现盲区；
3、云环境下故障更为隐性，更难排查；
4、混合云架构下，如何做到统一运维，提升运维管理效率。
面对以上挑战，天旦与该城商行客户携手合作，共同打造了“金融私有云混合架构智能业务性能监控方案”，迎难而上，知难而进。

**挑战一：跨越混合云架构的流量采集难**

随着该城商行金融私有云的落地，部署和迁移到云服务器和容器云上的业务系统越来越多。如何安全有效地把混合云架构上的流量采集出来，甚至与云下传统环境流量汇聚到一起，并能够实现统一管理是面临的第一个难题。天旦根据用户实际场景，推出的多种探针部署（旁路探针+主机探针）组合方案完美实现了混合云架构的云网流量采集。同时，通过智能云网流量采集平台（Cloud Probe Manager）实现了采集器的统一管理，并最终将云下与混合云采集的流量汇聚至天旦业务性能管理BPC。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eicSYpc2jHwmXaszCfF6HXqPXXba4nFMFro0zT1qjp3Vzjz9b6vuojuw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*图 1：监控方案部署架构图*

**挑战二：跨越混合云架构的业务路径梳理难**

随着云上系统的不断丰富，在传统环境和云环境并存的架构下，业务路径梳理尤为重要。基于BPC解码出的互联数据自动探索业务流程，将全业务系统的服务路径实时可视化呈现，并可智能合并同节点应用，助力该城商行客户彻底厘清业务系统中每一个活动的服务节点与业务应用，排查每一条业务路径，扫清系统中的任何监控盲点，让科技部门对业务系统了如指掌。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eOnrHmIC2n9WcbibYwPFRPQPZ96KHdQiahRjibd6tGibHPuYzUFLbjV6thQ/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*图 2：SPVD自动梳理业务路径*

**挑战三：跨越混合云架构的故障排查难**

由于云架构的轻耦合、应用节点的动态变更等因素，云环境中的故障更加隐性，导致故障产生的原因更复杂。因此，与传统环境相比，云上业务系统故障更难排查。如果没有可靠的工具，故障告警不及时、定位不精准、分析不准确，将会对业务系统运行产生严重影响，进而波及前台业务。
为保障云上业务系统的稳定运行，天旦通过五大高频且典型的故障监控告警预设，监控了关键金融交易故障，再辅以自动故障定位和自动根因分析，分析故障影响程度。最终，定位到故障根源节点和异常指标，从而实现快速排障，让云上业务系统的运维响应效率与传统环境保持一致。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eZ07v3TGgWRswlTmhibicHKBdZia0OPxTMQxwHORfmGqvnMiahsTTYYJUuQ/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8ePCCCibQxF2DIvaTDHkIeTTBOTJs7MPO6BooPryicOAkZSsEcEYhXd1rw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*图 3：智能告警场景与告警触发*

**挑战四：跨越混合云架构的运维管理难**

随着该城商行与云厂商合作的逐步推进，该城商行的金融私有云已经步入了全新的阶段。随之，基于混合云架构的运维管理工作也成为了科技运维部门的重中之重。因此，一体化智能监控平台的建设也就势在必行。天旦业务性能管理BPC能够做到将混合云和传统环境纳入统一的监控界面，实现无盲区、端到端、全流程的监控覆盖，满足了该城商行的运维管理要求，大大提升了运维管理效率。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e7XjvzyrIL4l0ibJ9MQfBgGpdOMHve9iclMQvEicNURHvY5vx8kC9agXDg/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*图 4：全服务路径-云上云下一体化监控*

天旦业务性能管理BPC的多层追踪功能，帮助该城商行根据业务流水号在云上云下不同系统间做追踪，方便了客户对云上云下业务做全流程端到端监控。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e2FTsia5XDYUnrfSlSbyrjmAibyuG1Dxa3Fp29w1nJXbcNoh5MAVTVVyw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e2FTsia5XDYUnrfSlSbyrjmAibyuG1Dxa3Fp29w1nJXbcNoh5MAVTVVyw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*图5 ：多层追踪，实现单笔交易的端到端监控*

天旦业务性能管理BPC完善的应用性能指标组件能够将全业务系统状态实时呈现。图形化的界面能够高效呈现运维部门关心的各类指标信息，实现可视化的性能监控，并将应用性能监控的“5大黄金指标”以及多种业务维度用曲线、饼图、柱状图等方式实时呈现出来，其中包括应用层视图、应用层快照、多维统计、交易追踪等模块。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e7mMSVibHAvuc6M4icWmYcK574PkxXfXL2ibric5mkAcF1AibM1RwWLV3HdA/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*图 6：天旦BPC业务与性能分析*

***
At Netis, we're at the forefront of analyzing business(APM) and network performance(NPM), ensuring that over thirty billion transactions run smoothly every day. Our commitment to system and data security is paramount, and we pride ourselves on our ability to conduct real-time analysis through network traffic mirroring. This means we can get the job done without the need for any agents or disruptions to your existing operations. Based in Shanghai, China, Netis is a global software company known for its high-performance products and cost-effective solutions. Interested in what we offer? Don't hesitate to get in touch. We're excited about the possibility of working together and welcoming new partners.  
Discover more at: www.netis.com  
Or drop me a line directly: dennis.li@netis.com
