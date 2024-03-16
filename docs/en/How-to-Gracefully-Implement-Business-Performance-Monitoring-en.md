# How to Gracefully Implement Business Performance Monitoring

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


In an era overflowing with monitoring tools, how can we streamline the complexity and assist users in gracefully implementing business performance monitoring?

### **1. A Business-Centric Monitoring Perspective**

Considering the disparities between monitoring metrics and intentions, application performance monitoring (APM) solutions offer varied alerting logics, broadly categorized into two types: "Bottom-up" alerting involves establishing alerts based on packet headers and other foundational data, then ascending to app and service utilization levels, ultimately identifying anomalies such as DNS errors or slow response times. On the flip side, "Top-down" alerting monitors business application nodes and select network nodes, setting alerts for high-level aggregated data. This approach starts with overarching business challenges and delves into underlying data. Due to the high false alarm rate and troubleshooting challenges of bottom-up data, it's not only time-consuming but also less precise. Conversely, top-down alerting can swiftly trigger alerts at the first sign of system or service failures, a crucial feature within a business-focused operational framework.
![002316seeudyfefdc8nldk.jpg](http://image.sciencenet.cn/album/201306/28/002316seeudyfefdc8nldk.jpg)

*Figure 1: Knowledge Hierarchy Diagram*

Netis BPC employs a "top-down" monitoring strategy, offering end-to-end coverage that enables a comprehensive view from the macro to the micro. By centering on business needs and bridging the divide between operations and management, it ensures unified monitoring and business perspectives, greatly enhancing the precision and clarity of alert analysis.

### **2. Designing with the User in Mind**

Imagine using piano keys to track time and a simple four-quadrant grid to display crucial business metrics. This innovative approach sits at the heart of Netis BPC's design ethos.
![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyo1rZQMYRmK4Yfiambegqu7bWA3usmGboVBg1Ziav7DHAmztEEPeSWuh7Q/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Figure 2: How piano keys and a four-quadrant grid play a role in Netis BPC's alert system and troubleshooting.*

**Why is each minute represented by a piano key?**

Netis BPC uses piano keys as a metaphor for time to give users a real-time sense of their business operations in a way that turns repetitive and stressful tasks into a more enjoyable experience. Each minute is a key on this timeline piano, with different colors conveying various states of business health. Interacting with these keys, users can "play" through their data, zooming in on specific moments with a mouse hover, much like enlarging a key under a pianist's finger. This attention to detail ensures users can easily and precisely access the information they need.

Furthermore, the choice of minute-level alerts strikes a balance between promptness and practicality. From extensive experience with financial clients, Netis learned that too detailed an alert system overwhelms with repetition, while too broad a system risks delays and oversights. Thus, setting alerts to minute intervals—each piano key—was a deliberate choice for efficiency and effectiveness.

However, minute granularity doesn't fit every scenario. For instance, in stock trading, where the pace is faster and stakes higher, even seconds matter. A transaction delay of more than 10ms or 10 specific events within a second can trigger alerts in this high-speed context. Thus, Netis BPC also offers second-level alerting, a faster, more sensitive detection system tailored for such critical needs.

**Displaying the Golden Signals**

Netis has distilled the essence of business monitoring into four golden signals: transaction volume mirrors application load, response rate echoes system health, success rate reflects business well-being, and transaction response time inversely indicates customer satisfaction. This revelation came from analyzing and comparing industry metrics like the Four Golden Signals, RED, and USE, tailoring them specifically for the financial sector's unique needs.

But how do you make these critical indicators clear and engaging for users? Netis's breakthrough came from marrying thorough analysis with creative design, resulting in the pioneering four-quadrant grid.

This design leap was inspired during a visit to New York's Museum of Modern Art by Netis co-founder & Chief Product Officer, Wizard. A piece showcasing America's geography and population through a clear, grid-based diagram sparked the idea. It showed that the power of information lies not in its volume but in the precision of its presentation. From highway signs to information guideboards, clarity reigns supreme. This insight, coupled with the need for quick, clear alert information in IT, birthed the iconic four-quadrant grid.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq0zib9UrUva92PkicX1HbHqyo8icuiaU00eVBRmcY23lm9lq2fzViaRNFP7DiaiccI3GpszkEpyQFMf4TEQw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)

*Figure 3: New York's Museum of Modern Art's classic four-quadrant grid:*

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyoVNumuLZRlcb00S7bS3dP9oicnycxmmwSAGrvAukAunwnB6HePm1FFUg/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Figure 4: Netis BPC's signature four-quadrant grid:*

At its core, BPC's product philosophy is about deeply understanding user needs and designing solutions that meet those needs precisely. By embedding the users' perspective into the design, notably with the piano keys and the four-quadrant grid, Netis champions a user and service-centered approach. This philosophy not only addresses user pain points but also bridges the gap between product functionality and user value.

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
