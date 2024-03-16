# Comment implémenter avec élégance la surveillance des performances d'affaires

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


À l'ère où l'on croule sous les outils de monitoring, comment peut-on faire simple tout en aidant les utilisateurs à mettre en place de façon élégante un suivi des performances d'affaires ?

### **1. Une perspective de monitoring axée sur le business**

Face à la diversité entre les indicateurs de surveillance et les objectifs de monitoring, les logiques d'alerte des solutions de surveillance de la performance applicative diffèrent aussi. On les classe généralement en deux types : les alertes dites "ascendantes", qui établissent des points d'alerte à partir de données de base telles que les headers des paquets, avant de remonter vers l'analyse de l'utilisation des applications et des services, pour finalement identifier les anomalies (comme des erreurs DNS ou des lenteurs de réponse). À l'opposé, les alertes "descendantes" se basent sur le monitoring des nœuds applicatifs et de certains nœuds réseau, fixant des critères d'alerte sur des données agrégées de haut niveau pour plonger ensuite dans l'analyse des données fondamentales. Les alertes ascendantes, avec leur volume élevé de fausses alertes et leur complexité de diagnostic, sont non seulement chronophages mais également peu précises. En revanche, le réglage des alertes descendantes permet une alerte rapide en cas de défaillance, jouant un rôle crucial dans une architecture opérationnelle centrée sur le business.

![002316seeudyfefdc8nldk.jpg](http://image.sciencenet.cn/album/201306/28/002316seeudyfefdc8nldk.jpg)

*Figure 1 : Schéma des niveaux de connaissance*

Netis BPC privilégie une approche de surveillance "descendante", offrant une vue d'ensemble grâce à une couverture de bout en bout, du macro au micro, centrée sur les enjeux d'affaires. Cette méthode transcende les frontières entre la gestion opérationnelle et les objectifs commerciaux, unifiant le monitoring et la perspective business pour garantir une analyse précise et intelligible des indicateurs d'alerte.

### **2. Un design pensé pour l'utilisateur**

Imaginer le temps sous forme de touches de piano et résumer les indicateurs clés d'affaires dans un carré à quatre segments constituent la quintessence du design de Netis BPC.

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyo1rZQMYRmK4Yfiambegqu7bWA3usmGboVBg1Ziav7DHAmztEEPeSWuh7Q/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Figure 2 : Les touches de piano et le carré à quatre segments, au cœur de la gestion des alertes et du diagnostic chez Netis BPC*

**Pourquoi une minute est-elle représentée par une touche de piano ?**

Afin de permettre aux utilisateurs de sentir le pouls de leurs opérations en temps réel, tout en rendant les tâches répétitives et stressantes aussi agréables qu'une pause musicale, Netis a opté pour les touches de piano comme symboles du temps. Chez BPC, le temps est segmenté en minutes, chaque segment étant coloré différemment pour refléter l'état des opérations. Les utilisateurs naviguent et interagissent avec les données comme s'ils effleuraient un clavier de piano. La touche sous le pointeur grossit pour mieux montrer le segment temporel ciblé, démontrant l'attention de Netis à fournir une information précise et facile à saisir.

Le choix de notifications minutées cherche à allier réactivité et économie. L'expérience avec des clients du secteur financier a montré à Netis que des alertes trop fréquentes surchargent sans apporter de nouvelle information, tandis que des alertes trop espacées perdent en pertinence et en temps. C'est pourquoi une minute a été choisie comme unité d'alerte, traduisant chaque minute par une touche de piano.

Malgré une couverture efficace pour de nombreux cas, ce modèle ne répond pas à tous les besoins, notamment dans les milieux où la réactivité est cruciale, comme chez les courtiers en valeurs mobilières. Pour eux, la rapidité est telle qu'un indicateur spécifique répété dix fois en une seconde ou une transaction dépassant 10 ms peut signaler un problème. C'est ainsi que Netis BPC a développé un second type d'alerte, basé sur la réaction à des caractéristiques d'événements en secondes, pour une surveillance encore plus affinée.

**La clé de la visualisation des indicateurs primordiaux**

Les spécialistes produits chez Netis ont établi un lien direct entre le volume des transactions et la charge de travail des applications, entre le taux de réponse et la santé du système, le taux de succès et la vitalité des opérations commerciales, ainsi qu'une corrélation inverse entre le temps de réponse des transactions et la qualité de l'expérience utilisateur. En prenant en compte les spécificités du domaine financier, ils ont mené une analyse comparative entre les métriques des Four Golden Signals, RED et USE, déterminant finalement que le volume des transactions, le taux de réponse, le temps de réponse et le taux de succès constituent les quatre indicateurs dorés de Netis BPC.

Face au défi de présenter ces quatre indicateurs essentiels de façon intuitive et évidente pour enrichir l'expérience utilisateur, l'équipe de Netis a entrepris un processus approfondi d'analyse, d'hypothèses, de tests et de validation, qui a abouti à l'innovation sectorielle du carré à quatre fenêtres.

L'idée du carré à quatre fenêtres a germé lors d'une visite au Musée d'Art Moderne de New York par Wizard, co-fondateur et chef produit chez Netis. Une exposition montrait une carte des États-Unis, illustrant des données géographiques et démographiques de manière claire grâce à un agencement en cases, qui évoquait les concepts de composants d'application et de réseau. Cette approche a révélé que l'essence de la transmission d'informations cruciales ne réside pas dans l'abondance des données, mais dans la précision avec laquelle les observateurs peuvent en extraire les éléments vitaux. Cette révélation, couplée à l'observation quotidienne des panneaux d'information, des signalétiques autoroutières et des icônes de guidage, a conduit à la conception du carré à quatre fenêtres, combinant efficacement le besoin d'accès rapide à l'information d'alerte avec la réalité de l'IT contemporain.

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq0zib9UrUva92PkicX1HbHqyo8icuiaU00eVBRmcY23lm9lq2fzViaRNFP7DiaiccI3GpszkEpyQFMf4TEQw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)

*Figure 3 : Le carré à quatre fenêtres emblématique du Musée d'Art Moderne de New York :*

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyoVNumuLZRlcb00S7bS3dP9oicnycxmmwSAGrvAukAunwnB6HePm1FFUg/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Figure 4 : Le carré à quatre fenêtres emblématique de Netis BPC :*

BPC est né d'une compréhension affinée des exigences des utilisateurs et d'une conception produit méticuleuse. En se plaçant dans la perspective du client pour saisir les besoins en alertes, en intégrant visuellement les indicateurs d'alerte dans la conception fonctionnelle, et en élaborant les touches de piano et le carré à quatre fenêtres à travers le prisme de l'expérience utilisateur, Netis allie une approche centrée sur l'individu et le service. Cette philosophie permet non seulement de cerner les difficultés rencontrées par les utilisateurs mais aussi de les accompagner dans l'usage du produit, fusionnant ainsi la valeur fonctionnelle avec l'intérêt utilisateur.

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
