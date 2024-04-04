# 银行信息系统业务类监控的实现难点

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Challenges-in-Implementing-Business-Monitoring-for-Banking-IT-Systems-ru.md)

经过上期的讨论，我们已经明确了一些通用的业务指标和监控规则，后面似乎只需要维护好描述业务运行的参数就可以了，但在实现过程中还会碰到诸多难点，主要集中在以下几方面：

**1、基础交易信息的获取**

想要实现上述功能，需要监控系统准确采集每一笔交易信息，信息至少要包括请求系统、交易码、重要交易标志、服务系统、处理节点、交易开始时间、交易结束时间（或处理时长）、流水号、机构、金额、服务系统返回码、本系统返回码、返回信息等。

这些基础信息很多系统都无法完整提供，例如服务系统返回码，如果在生产系统设计之初没有考虑记录这个字段，就很难提供，没有该数据，服务系统交易成功率无法计算。例如全局流水号。此外，所有系统均向监控系统提供交易明细数据，数据量非常大，非常考验监控系统的处理性能。

**2、生产系统开发规范**

监控规则会覆盖至所有生产系统，因此，对生产系统开发的标准化、规范化是有要求的。例如需要强依赖交易码参数。为了实现上述功能，交易码参数至少要包含请求系统、交易码、交易名称、服务系统、金融标志（重要交易标志）、忙时标志、闲时标志等，单一交易码最好只完成单一功能。例如交易码A009，因功能拆分不标准，一个原子交易码A009程序内部用do_type之类的字段做了功能分支，一个交易码实现了多个业务功能，这种情况很难说清A009的业务功能，到底是查询交易还是金融交易。

开发代码的规范性也是一个较大的问题。报警触发是否准确，与生产系统给定的响应码、日志记录等紧密相关。笔者曾在X行集中清算系统工作，该系统有一个非常经典的响应码：201999-系统错误。一般认为在系统严重故障，程序无法从技术层面处理又无法判定原因时给定该报错。但实际此响应码一天约返回80万笔，据此计算该系统每日整体交易成功率不足90%。此外还存在返回码一码多用的情况。例如返回码R00001，应指定一个标准含义如“查无记录”，但实际使用可能被开发人自定义为“余额不足”或“卡号xxx错误”，“地址错误”之类，甚至截然相反的含义，如“查询返回xxx条”。此时这个返回码已经无法界定一笔交易成功与否了。业务监控下探到交易码级别，这个问题会更加突出，指定交易码后交易量会比较小，对返回值会更加敏感，迫切需要推进返回码规范化的工作。

错误日志标准化是日志规范比较典型的问题。日志记录是否规范直接决定日志监控报警是否准确，否则会导致大量误报和漏报。

**3、大量的运行参数设置**

上述两点如果能够克服，剩下的就是运维人员长期对各种运行参数进行打磨。业务类监控，需要针对每一个交易码进行参数设定，每一个交易码至少要包含业务成功率、系统成功率、突增比率、突降比率、指标偏离基线比率、异常交易笔数等参数，据此描述该交易码的运行情况。规模比较大的系统交易码的数量很多，这意味着仅交易码参数一项要长期调整上万条运行参数。不过，在参数设置规则确定的情况下，可以设计算法，根据基线的运行情况自动修改运行参数。

设计一个监控系统并不难，难点在于如何让监控更贴近业务，充分挖掘业务监控的价值，推动IT运维向IT运营转变。

原文链接：https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
