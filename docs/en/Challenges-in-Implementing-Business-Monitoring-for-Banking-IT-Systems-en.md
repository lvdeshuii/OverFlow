# Challenges in Implementing Business Monitoring for Banking IT Systems

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

In our previous discussion, we identified common business indicators and monitoring rules. However, several difficulties arise during implementation, primarily in the following areas:

**1. Acquiring basic transaction information**

To effectively monitor transactions, the system must accurately collect data for each transaction, including the request system, transaction code, important transaction flags, service system, processing node, start and end times, serial number, institution, amount, service system return code, and this system's return code, among other details. Unfortunately, many systems cannot provide complete basic information, such as the service system return code. If the production system wasn't initially designed to record this field, it's challenging to provide it. Without this data, calculating the service system transaction success rate is impossible. Additionally, all systems provide transaction detail data to the monitoring system, resulting in large data volumes that challenge the monitoring system's processing performance.

**2. Development specifications for production systems**

Monitoring rules apply to all production systems, so standardization and normalization of production system development are essential. For example, there must be a strong dependence on the transaction code parameter. To achieve this, the transaction code parameter should include the request system, transaction code, transaction name, service system, financial flag, busy flag, and idle flag, among other details. Ideally, a single transaction code should perform only one function. For instance, transaction code A009 has non-standard functional decomposition, causing an atomic transaction code A009 program to use a sub_type-like field for functional branching internally. As a result, a single transaction code implements multiple business functions, making it difficult to clearly describe the business functionality of A009.

Standardizing development code is another significant challenge. The accuracy of alarm triggers depends on the response code and log recording provided by the production system. While working on Bank X's central clearing system, the author encountered a classic response code: 201999-System error. This error typically indicates a serious system fault that the program cannot process from a technical perspective or determine the cause. However, this response code is returned approximately 800,000 times daily, resulting in an overall daily transaction success rate of less than 90%. Moreover, return codes may have multiple uses. For example, return code R00001 should signify "No record found," but developers may customize it to mean "Insufficient balance," "Card number xxx error," "Address error," or even the opposite, like "Query returned xxx records." In such cases, the return code cannot determine whether a transaction is successful. This problem becomes more pronounced in business monitoring that drills down to the transaction code level, where transaction volume is smaller, and sensitivity to return values is higher. Standardizing return codes is urgently needed.

Log specifications should also include error log standardization. Accurate log monitoring alarms depend on standardized log recording; otherwise, false alarms and missed alarms may occur frequently.

**3. Setting numerous running parameters**

If the previous challenges are addressed, operations personnel must continuously fine-tune various running parameters. Business-class monitoring requires parameter settings for each transaction code, including business success rate, system success rate, surge ratio, drop ratio, indicator deviation baseline ratio, and the number of abnormal transactions. These parameters describe the transaction code's running situation. Larger systems have many transaction codes, requiring long-term adjustment of tens of thousands of running parameters for the transaction code parameter alone. However, if parameter setting rules are established, an algorithm can be designed to automatically modify running parameters based on the baseline running situation.

Designing a monitoring system is not difficult, but the challenge lies in making monitoring more relevant to the business, fully exploiting the value of business monitoring, and driving the transformation from IT maintenance to IT operations.

[Original article](https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
