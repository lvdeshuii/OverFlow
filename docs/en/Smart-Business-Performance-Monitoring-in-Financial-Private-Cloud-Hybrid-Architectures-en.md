# User Case: Smart Business Performance Monitoring in Financial Private Cloud Hybrid Architectures

**Other Languages**

+ [Chinese / 中文](/docs/zh/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-zh.md)
+ [English](/docs/en/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-en.md)
+ [Spanish / español / castellano](/docs/es/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-es.md)
+ [Japanese / 日本語](/docs/ja/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-ja.md)
+ [German / Deutsch](/docs/de/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-de.md)
+ [French / français](/docs/fr/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-fr.md)
+ [Arabic / al arabiya / العربية](/docs/ar/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-ar.md)
+ [Portuguese (Portugal)](/docs/pt/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-pt.md)

As the foundational platform supporting the operation of information systems, financial institutions' IT infrastructures face the twin challenges of digital transformation and technological autonomy. Consequently, the financial private cloud has emerged as a preferred solution for many financial institutions to address these challenges.
In recent years, a city commercial bank has dedicated itself to the vigorous development of private clouds as a new embodiment of fintech-enabled business. It has partnered with leading cloud service providers for joint research and breakthroughs in financial cloud infrastructure and services, financial scenario innovation, and the development of cloud-native business systems, collaboratively advancing the deployment of the bank's financial private cloud technology architecture. This strategy of consistently deploying or migrating critical business systems to the financial private cloud has yielded numerous benefits, such as enhanced business agility, cost optimization, and improved security. However, it has also introduced significant challenges to operational management, including:

1. Achieving unified traffic collection and management across hybrid cloud architectures like cloud servers and container clouds;
2. Navigating complex business access relationships and monitoring blind spots in hybrid architectures;
3. Dealing with more concealed failures in cloud environments, complicating troubleshooting efforts;
4. Streamlining operations to enhance efficiency under the hybrid cloud architecture.
   In response to these challenges, Netis and the city commercial bank have collaboratively developed the "Financial Private Cloud Hybrid Architecture Intelligent Business Performance Monitoring Solution," bravely confronting and advancing through these difficulties.

**Challenge One: Overcoming Traffic Collection Hurdles in Hybrid Cloud Architectures**

As the city commercial bank embraces its financial private cloud, an increasing number of business systems find their new homes on cloud servers and container clouds. The first hurdle is how to efficiently and securely gather traffic across this mixed cloud setup, merge it with traffic from traditional setups, and manage it all under one roof. Netis has ingeniously addressed this by introducing a suite of probe deployment strategies (involving both bypass and host probes) tailored to user scenarios. This approach not only facilitates comprehensive traffic collection within the hybrid cloud framework but also, through the Cloud Probe Manager, ensures centralized control over these collections. The culmination of this effort is the integration of traffic data, both from traditional and hybrid cloud sources, into Netis's Business Performance Management (BPC) system.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eicSYpc2jHwmXaszCfF6HXqPXXba4nFMFro0zT1qjp3Vzjz9b6vuojuw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*Figure 1: Deployment architecture of the monitoring solution.*

**Challenge Two: Navigating Business Path Analysis in Hybrid Cloud Architectures**

As cloud-based systems proliferate, delineating business paths becomes increasingly crucial within architectures that blend traditional and cloud environments. Leveraging wire data decoded by BPC, the system autonomously navigates business processes, rendering the entire business system's service paths in a visually accessible format. This not only facilitates real-time visibility but also enables the intelligent amalgamation of applications at identical nodes. This comprehensive visibility aids city commercial bank clients in demystifying the service nodes and applications across their operations, allowing for meticulous path analysis and the elimination of monitoring blind spots. This ensures that the tech department can masterfully manage and understand the business system's intricacies.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eOnrHmIC2n9WcbibYwPFRPQPZ96KHdQiahRjibd6tGibHPuYzUFLbjV6thQ/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*Figure 2: SPVD's automated business path analysis.*

**Challenge Three: Navigating Troubleshooting in Hybrid Cloud Architectures**

The nature of cloud architectures—characterized by their flexible connections and ever-changing application nodes—means that failures within the cloud are sneakier and their causes more complex than ever. This complexity turns troubleshooting in cloud-based business systems into a formidable task. Without the right tools, delays in failure notifications, imprecise fault localization, and inaccurate analyses can seriously disrupt business operations, potentially impacting customer-facing services.

To safeguard the smooth operation of cloud-based systems, Netis has implemented a strategy using five sets of alarm presets, specifically designed to monitor for common yet critical financial transaction failures. This system is bolstered by automated fault localization and root cause analysis, enabling a thorough evaluation of the failure's impact. The end goal? To quickly identify the root cause and any abnormal performance metrics, facilitating swift resolution. This approach ensures that the maintenance response times of cloud-based systems are on par with those of traditional setups.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eZ07v3TGgWRswlTmhibicHKBdZia0OPxTMQxwHORfmGqvnMiahsTTYYJUuQ/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8ePCCCibQxF2DIvaTDHkIeTTBOTJs7MPO6BooPryicOAkZSsEcEYhXd1rw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*Figure 3: Illustration of intelligent alarm scenarios and triggers.*

**Challenge Four: Overcoming Operational Management Hurdles in Hybrid Cloud Architectures**

The city commercial bank's financial private cloud has embarked on a groundbreaking journey, thanks to its evolving partnership with cloud service providers. This evolution has propelled operational management, especially within a hybrid cloud framework, to the forefront of the technology operations department's agenda. Consequently, the deployment of a unified intelligent monitoring platform has become a necessity. Netis Business Performance Management (BPC) stands out by seamlessly integrating hybrid and traditional environments into one monitoring interface, ensuring comprehensive, end-to-end coverage without any blind spots. This achievement not only aligns with the operational management goals of the city commercial bank but also significantly boosts efficiency in this domain.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e7XjvzyrIL4l0ibJ9MQfBgGpdOMHve9iclMQvEicNURHvY5vx8kC9agXDg/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*Figure 4: Comprehensive Service Path - Unified Monitoring Across Cloud and On-Premises Environments*

Through its sophisticated multi-layer tracking, Netis BPC empowers the bank to seamlessly track transactions across cloud and on-premises systems using business transaction numbers. This capability simplifies the task of achieving thorough, end-to-end monitoring of services, irrespective of their location.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e2FTsia5XDYUnrfSlSbyrjmAibyuG1Dxa3Fp29w1nJXbcNoh5MAVTVVyw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e9mAK5j45wGqhT1bMceXP5BV6pcDiaKHv5fa0LRTib5O3VCtW49mSfMWQ/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*Figure 5: Multi-Layer Tracking - End-to-End Monitoring for Individual Transactions*

Netis BPC's advanced application performance metrics component vividly displays the real-time status of the entire business system. Its intuitive graphical interface efficiently showcases various key metrics, facilitating visualized performance monitoring. The platform adeptly presents essential application performance metrics, including the "Five Golden Metrics," along with a wide range of business dimensions through dynamic curves, pie charts, and bar graphs. This includes detailed views of application layers, snapshots, multi-dimensional statistics, and transaction tracking features.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e7mMSVibHAvuc6M4icWmYcK574PkxXfXL2ibric5mkAcF1AibM1RwWLV3HdA/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*Figure 6: Netis BPC - Bridging Business and Performance Analysis*

***
At Netis, we're at the forefront of analyzing business(APM) and network performance(NPM), ensuring that over thirty billion transactions run smoothly every day. Our commitment to system and data security is paramount, and we pride ourselves on our ability to conduct real-time analysis through network traffic mirroring. This means we can get the job done without the need for any agents or disruptions to your existing operations. Based in Shanghai, China, Netis is a global software company known for its high-performance products and cost-effective solutions. Interested in what we offer? Don't hesitate to get in touch. We're excited about the possibility of working together and welcoming new partners.​  
Discover more at: www.netis.com​  
Or drop me a line directly: dennis.li@netis.com
