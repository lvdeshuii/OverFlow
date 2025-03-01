# 云网流量采集分析白皮书（2022）

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ru.md)

据IDC调研发现，未来两年，大多数企业将会选择混合云和多云的方式构建云原生平台。随着企业云上应用场景的不断丰富，云内的东西流量远超预期，如何精准地采集与管理流量是企业面临的共同挑战。为此，Gartner提出：“企业的IT决策者应该重新考虑流量采集与分析的方法，通过提供混合云环境所需要的可视化水平，实现未来的性能监控与管理”。

天旦认为云网流量可观测性分析是破解云原生、混合云环境性能监控与管理的有效手段之一。运用高性能、全场景、对应用无侵入的流量采集与处理技术，可以构建多环境、多架构下的云网流量可视化，最终实现全方位的云网可观测。为帮助企业解决以上难题，天旦推出《云网流量采集分析白皮书（2022）》。白皮书共分为六个章节，包括：云时代挑战、云网流量可观测性价值、云网流量采集与可观测性分析架构与技术、部署落地方案、典型场景案例与行业最佳实践案例等，为千行百业的用户上云提供最优解决方案。

白皮书主要观点如下：

**1. 关键能力**

- 多环境：

  各类环境支持：支持主流的操作系统、主流的芯片、主流的虚拟化、容器化环境。

  微服务支持：支持微服务架构下的各类部署形态、支持各种容器运行时。

- 多能力：

  数据包处理能力：支持对数据包进行：采集、过滤、分发、裁切、去重等各类关键能力。 

  Flow 与Telemetry 能力：云网流量可视化，需要支持对采集的原始数据包进行预处理，输出 Flow 日志，并具备 Telemetry 支持能力。

  染色能力：支持对采集的原始数据包进行数据包染色，将业务场景、网络场景、安全场景的信息植入数据包。

  TCP传输支持：采用TCP协议传输采集的数据包保障传输的可靠性。

- 业务零侵入：对业务零侵入，无需业务做任何更改。

- 自管理：主要包括：管理台对接、采集器运行状态感知、自监控、熔断、自恢复与可视化。

- 分层：支持动态扩缩。

**2. 关键技术**

- 采集技术：

  支持场景：从应用场景角度，分为公有云与私有云等两大应用场景；从技术角度，分为VM和Container 技术两大类。

  支持能力：首先，流量采集应该覆盖多种不同场景，且在不同场景中采取不同的采集器手段；其次，混合环境分层采集流量后，需要统一的管理平台。

- 多层处理/vTAP：天旦认为云流量采集技术通过“云上来、云上去”的思路，进行分层采集、分层处理、分层加工、分层管理，以保证在面对海量被管对象、超大流量的情况下，能够完成更细致、更全面的可观测性建设。

- 底层采集技术：云的底层环境多而复杂，为获得最大化的采集性能和效率，针对不同的环境需要选择最适合的采集技术。

- 自主环境支持：云网流量采集与可观测性分析需要支持自主化服务器，比如ARM架构CPU、定制化操作系统等。

- Flow支持：基于消费场景的精细 Flow 流统计能力，应用于网络、应用、安全等相关应用场景，能够有效解决价值与云网开销间的选择问题。

- Telemetry能力：结合 Open Telemetry 能力，可以在大幅缩小云网流量资源消耗的情况下提升可观测性能力。

**3. 部署方案**

主要包括以下5种：采集器整体部署方案、宿主机流量采集方案、虚拟机流量采集方案、容器环境流量采集方案、vTAP分流，在白皮书中详细介绍了每种部署方案。

**4. 典型应用场景**

- 安全场景:只有通过可靠的云网流量采集系统，才能够做到对云内业务主机流量的精准、动态提取。

  态势感知：云上态势感知，由于工作负载云化，需要深入了解业务内部的安全情况，在其所依赖的下层安全探针/安全引擎中，依赖于云流量的精准分析。

  等级保护2.0：通过可靠的云网流量采集，对云内业务主机流量的精准、动态提取，是满足云上等级保护2.0的要求。

- BPM/APM：天旦认为，BPM通过网络流量可快速发现用户体验问题并快速定位，再结合APM的应用代码分析能力对问题进行根因分析，为实现云上可观测提供了全新的解决思路。

- NPMD ：与传统环境不同，云上网络监控需要加入AZ、VPC、service等信息，需要增强云上拓扑分析与多层穿透会话级追踪的能力。

  云上拓扑分析：随时掌握云网拓扑，就需要云网监控，需要云流量可观测性采集的染色技术支持才能适应云上的动态变化。同时，需要云流量可观测性采集中继层输出流数据，进一步压缩流量，避免流量拥堵。

  多层穿透会话级追踪：云上网络分析穿透会话级追踪能力，需要云流量可观测性采集的染色技术进行多层追踪。

- 数据库运维与安全：云上数据库由于分布库架构的出现，对传统数据库监控提出了新要求。数据库数据节点和接入节点的互访更频繁，也更容易发生问题。通过云流量可观测性采集构建云上分布数据库监控，是一种更好的选择。

[**点击下载**](https://open.netis.com/datacenter/white-papers/天旦云网流量采集分析白皮书（2022）)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
