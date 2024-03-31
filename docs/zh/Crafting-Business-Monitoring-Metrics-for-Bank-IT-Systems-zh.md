# 银行信息系统业务类监控的指标设定

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Crafting-Business-Monitoring-Metrics-for-Bank-IT-Systems-ru.md)

随着金融业的发展，银行业务功能变得越来越复杂，信息系统技术架构也变得多种多样，单纯从技术层面来设置监控规则越来越难以发现问题，迫切需要一套不区分技术架构，仅以描述业务运行情况为目的的业务类监控。笔者结合自己运维经验及对业务监控的理解，讨论一下业务类监控的指标和监控规则。

### 监控发展的三个阶段

第一阶段：需要运维人员自行设定监控指标、规则、运行参数。我们最常见的监控模式是：在某监控系统中配置脚本，设置一个具体报警项，然后在服务器运行脚本获取一个特定值，设一个阈值，高于或低于阈值即触发告警，比较典型的是zabbix监控系统。

第二阶段：为监控系统约定监控指标、规则，运维人员维护运行参数。监控指标和报警规则应在第一阶段的基础上进行归纳整理，设置尽量具有统一性，尽量兼容所有系统的运行情况。

第三阶段：由监控系统约定监控指标、规则，同时根据监控自身和生产系统运行情况计算出最佳的运行参数，运维人员基本不参与维护。

本文重点对第二阶段进行分析，并根据业务运行情况，给出一些普遍的监控指标和报警规则。

### 业务监控的指标和报警规则

银行信息系统最小业务功能单位是交易码或接口，每一支交易共有的特征是返回码、交易量、响应时间，笔者围绕这几个特征尝试设置一些通用监控指标和报警规则，以供大家作为参考。

**1、交易成功率**

该指标是监控系统最实用、最基本的一个指标。一般的成功率监控，在系统不返回系统级别错误，例如网络不通，文件未打开等系统级别异常时，均认为交易成功。但没有返回该类错误并不意味着业务处理没有问题。例如交易A001的功能是“查询挂账”，正常情况下返回“查无记录”，在交易异常产生挂账时返回挂账交易信息。如果A001某天大量返回挂账，监控是否应该感知到该种情况呢？理想中是的。所以可以引入系统成功率和业务成功率，系统成功率用于计算生产系统技术层面失败率，业务成功率计算每支交易在返回某种业务返回码时的成功率。每支交易每天返回返回码量的量和比率都是基本固定的，甚至可以针对每一个交易码设定返回码的比率范围，而不拘泥于成功率。


![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/MR8pzzoKXjZp8SC2icFBL32T5nicZc8Nn56cTG16anNEMp3ug4lF03nnh9vKEyp8aHLvoe5x0Fvibo1SDTlNmydeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

图 1：交易成功率页面

**2、服务系统交易成功率**

银行系统的特点之一，是每一笔交易都有确定的调用系统和服务系统，如果我们可以感知服务系统是否正常，对于确定故障点是非常有用的。这一项的实现很简单，只要确定每一支交易有无调用服务系统，确定调用的服务系统是哪一个，将调用到该服务系统所有交易确定为计算样本，对服务系统给定的返回码进行成功率计算，即可得到该服务系统的成功率。如果维度更细致一些，可以计算服务系统的哪一个交易码成功率低。

**3、节点无交易发生**

对于高频交易，可以设定在一个统计周期内，如果没有指定交易发生，可判定触发无交易发生报警（可细化到某节点无xx交易发生）。但细想的话，经验老到的运维同事应该能想到，还是有点复杂的，因为交易的发生情况在高峰期和低峰期不同，工作日和节假日不同。这需要针对每一支交易进行交易量的统计分析，选定在当前条件内符合条件的交易码。我们可以引入“忙时”、“闲时”的概念。举例：可以设定工作日早8点至晚19点为忙时，其余时间段及节假日全天为闲时，统计后发现交易码A002全天交易都很多，那么就设置为忙时、闲时均进行监控；交易码A003只有高峰期交易量多，闲时交易量很少甚至无交易，就设置为忙时监控、闲时不监控；交易码A004全天交易量都很少，断断续续只有很少的交易量，那么就设置为忙时、闲时均不监控。

**4、交易量环比骤变**

在日常工作中会发现，系统正常时，同一支交易在同时段交易量不会有太大起伏，在系统异常时，交易量也会随之产生变化。我们需要一种手段来发现交易量的突增或突减。可以计算指定交易码的交易量环比，如果起伏太大，则可以判断系统发生了一些需要管理员注意的情况。举例：A005交易，目前15点08分属于忙时，参数为忙时有效，符合条件，计算14点08分至当前时间点15点08分A005交易发生量为a，该交易码基线工作日14点08分至15点08分交易总量为b，则环比比率c = a / b ，如果c在0.8~1.2之间（上限、下限均可调），可认定为正常，如果c=0.4或c=1.6，认定为交易量偏低或偏高，给出报警。

该指标对低频交易无效，交易量数值小会造成比率起伏较大。

**5、异常交易每周期笔数**

如果交易成功率指标下探至交易码级别，对于低频交易或超高频交易适用度都不高。低频交易会频繁触发报警，而超高频交易可能感知不到问题已经发生。

例如A006交易10分钟交易量10000笔，其中50笔有问题，成功率仅仅下降了0.5%，但50笔足以引起很大问题。例如A007交易10分钟交易量2笔，而且它是重要金融交易，就比较难设定成功率。这时候我们可以设A006一个周期内失败10笔以上，A007失败1笔以上，其他交易码根据交易量统计结果各自给定报警笔数，即可解决这个问题。而且，可以专门设计一个页面，显示出所有异常交易的基础交易信息，例如：处理节点、流水号、请求系统、交易码、服务系统、返回码等，在应急处置中加快定位到故障点。

**6、响应时间超时每周期笔数**

银行系统在发生故障时，可能会降低系统性能，造成响应时间拉长或者技术层面判为超时。某些监控依靠响应率应对这种现象，但响应率无法发现响应时间拉长但又短于监控等待时间的情况，另外对于较高频交易，部分交易异常不一定能够突破响应率阈值。

同异常交易一样，可以对响应时间异常的交易进行每周期笔数监控。例：交易A008，从基线中统计得到响应时间一般在300ms，那么设定超时时间over_time为600ms或900ms。如果有某一笔A008响应时间超过over_time，可以认定该笔交易超时，1个统计周期内超时超过3笔（可修改），给出报警。

**7、日终、对账**

日终对于银行系统的重要不言而喻，某些步骤直接影响次日的开门营业，需要专门的指标来监控。只要指定为日终步骤的交易码，在指定的最晚开始时间前开始，指定的时长内完成，且在最晚完成时间前返回成功即可。对于有对账需求的系统，在指定的时间内，发生指定类型的对账，且对账不一致的笔数、金额与往期相比没有太大浮动，可认为正常。

以上就是我关于业务类监控指标设定的思考，下次我们将讨论业务类监控的实现难点。

原文链接：https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
