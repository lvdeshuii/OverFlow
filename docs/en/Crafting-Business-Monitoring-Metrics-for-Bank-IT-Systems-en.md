# Crafting Business Monitoring Metrics for Bank IT Systems

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

As the financial sector evolves, banking services have grown in complexity alongside a diversification in information system architectures. The challenge of identifying issues through purely technical monitoring rules is escalating. There's a clear demand for business-centric monitoring strategies that are agnostic to technology architectures, focusing solely on depicting business operations. Drawing from extensive operational experience and a deep understanding of business monitoring, the author delves into the metrics and rules essential for effective business monitoring.

### Evolution of Monitoring Practices

**First Stage:** IT operations staff manually establish monitoring metrics, rules, and parameters. A common approach involves configuring scripts within a monitoring system like Zabbix, setting up specific alarm conditions based on thresholds, where crossing these thresholds (either above or below) triggers an alert.

**Second Stage:** Monitoring metrics and rules are standardized, with IT operations staff responsible for the upkeep of operational parameters. This stage builds upon the first by organizing and standardizing monitoring criteria to ensure broad compatibility and uniformity across various systems.

**Third Stage:** The monitoring system autonomously determines the metrics, rules, and optimal operational parameters by analyzing both its own performance and that of the production systems, minimizing the need for manual intervention by IT staff.

The focus of this discussion is the pivotal second stage, proposing a set of universal monitoring metrics and alert rules derived from operational insights into business activities.

### Key Metrics and Alert Rules for Monitoring Banking Services

Banking information systems are defined by their transaction codes or interfaces, characterized by return codes, transaction volumes, and response times. This guide outlines essential monitoring metrics and alert rules based on these characteristics, offering a reference for effective business monitoring.

**1. Transaction Success Rate**

A cornerstone metric in system monitoring is the transaction success rate, essential for assessing the basic health of a system. Traditional success rate monitoring deems a transaction successful in the absence of systemic errors (e.g., network issues or file access errors). Yet, a lack of systemic errors does not guarantee the absence of business process issues. Take transaction A001, "query posting", which normally indicates "no record found". An unusual spike in postings indicates a potential issue, suggesting a need for differentiating between system success rates and business success rates. The system success rate evaluates technical failures, while the business success rate measures transaction outcomes against expected business return codes. This nuanced approach allows for more precise monitoring, moving beyond mere success rates to consider specific expected outcomes for each transaction.

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/MR8pzzoKXjZp8SC2icFBL32T5nicZc8Nn56cTG16anNEMp3ug4lF03nnh9vKEyp8aHLvoe5x0Fvibo1SDTlNmydeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

Figure 1: Transaction Success Rate Page

**2. Service System Transaction Success Rate**

A unique aspect of banking systems is the clear distinction between calling and service systems for each transaction. Understanding the performance of service systems is crucial for pinpointing issues. Simply determine whether a transaction invokes a service system and which one it is. Analyzing the success rates of transactions linked to a specific service system provides insight into its reliability. Further granularity, such as assessing individual transaction codes within the service system, can offer deeper diagnostic capabilities.

**3. When Nodes Go Quiet: The No-Transaction Alarm**

In the whirlwind world of high-frequency trading, there's a clever trick: setting up an alarm for when, surprisingly, nothing happens. Imagine a bustling marketplace that suddenly goes silent. This alarm rings when a specific transaction doesn't occur within a set period at a particular node - think of it as a "missing action" alert. It's a bit like expecting a daily call from a friend and starting to worry when it doesn't come. However, figuring out when to expect the call (or transaction) isn't straightforward, as busy and quiet times vary, just like weekends and weekdays. It's about tracking every transaction's ebb and flow, picking out the ones that should be happening now. And so, we bring in the idea of "rush hours" and "down times" - for instance, marking weekdays from 8 a.m. to 7 p.m. as peak times. If transaction code A002 is buzzing all day, it's watched non-stop. But if A003 only wakes up during the rush, it gets a break during the lulls. And A004? If it barely whispers throughout the day, it's left alone, unmonitored.

**4. The Sudden Swings: Tracking Transaction Tsunamis**

Every day, transactions flow smoothly like a river through its channel. But when the system hits a snag, this flow can turn into a flood or a drought. Spotting these drastic changes is crucial. Imagine tracking a transaction, A005, during the afternoon rush. Comparing its activity to a "normal" day, we calculate the change. If it falls within the range of typical ups and downs (let's say, 0.8 to 1.2 times the norm), all's well. But if it plunges to 0.4 or soars to 1.6, it's time to sound the alarm. This method, however, stumbles a bit with the less frequent transactions, where even minor changes can seem like big waves.

**5. Monitoring the Pulse: Tracking Abnormal Transaction Volumes**

Diving into transaction success rates with a microscope, particularly at the granular level of individual codes, reveals a challenge: this approach doesn't play well with the extremes of low or ultra-high-frequency transactions. Picture this: low-frequency transactions end up setting off alarms like fireworks, while ultra-high-frequency ones might fly under the radar, missing the alert that trouble's brewing.

Take transaction A006, bustling with 10,000 transactions in just 10 minutes, 50 of which hit a snag. That nudges the success rate down by a mere 0.5%—seemingly minor yet potentially disastrous. Meanwhile, A007 logs just two transactions in the same timeframe, but given its heavyweight financial status, even a single hiccup is hard to ignore. The solution? Tailoring alert thresholds—over 10 misfires for A006, just one for A007—based on the beat of each transaction's rhythm, efficiently sidestepping the issue. And imagine a dashboard that lays out the nitty-gritty of all transactions gone awry, from the processing node to the service system, making emergency troubleshooting a breeze.

**6. The Time Crunch: Response Time Overshoots**

Bank systems, like any well-oiled machine, can sputter, slowing down or even stalling. Traditional monitoring might blink at response rates, but what about when delays linger just shy of the alarm threshold? Especially in high-traffic transactions, a slight delay doesn't always mean crossing the red line.

Here’s a fix: keep an eye on transactions straying from the norm in response times, cycle by cycle. For instance, if A008 typically wraps up in 300ms, stretching beyond 600ms or 900ms could signal trouble. A trio of these outliers within a cycle? Time to sound the alarm.

**7. Closing the Day, Keeping the Books**

The curtain call of a banking system's day, end-of-day processes, holds the key to a smooth opening act the next morning. Monitoring is straightforward: transactions tagged for day's end need to kick off and wrap up within set times, with a bow tied by a success signal. And when it comes to balancing the books, consistency is king—minor fluctuations in discrepancies are the green light for business as usual.

That wraps up our exploration into crafting smart, sensitive business monitoring tools. Stay tuned for a peek behind the curtain at the tech challenges that come with bringing these concepts to life.

Original article link: https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
