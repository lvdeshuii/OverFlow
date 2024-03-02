# Livre Blanc sur l'Analyse et la Collecte du Trafic dans le Cloud et les Réseaux (2022)

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

D'après une étude d'IDC, dans les prochaines années, la majorité des entreprises se tourneront vers des solutions de cloud hybride et multi-cloud pour développer leurs plateformes cloud natives. Face à la multiplication des applications sur le cloud, le trafic interne, dit est-ouest, excède largement les prévisions. La précision dans la collecte et la gestion de ce trafic représente donc un défi majeur pour les entreprises. Gartner suggère ainsi que les responsables IT repensent les stratégies de collecte et d'analyse du trafic afin d'offrir la transparence nécessaire dans les environnements hybrides, essentielle pour le contrôle et la gestion des performances à venir.

Netis estime que l'analyse de l'observabilité du trafic dans les réseaux et le cloud représente une solution clé pour le suivi et la gestion des environnements cloud natifs et hybrides. Grâce à des technologies de collecte et de traitement du trafic avancées, non intrusives et adaptées à tous les scénarios, il est possible de créer une visualisation du trafic adaptée à divers environnements et architectures, permettant une observabilité complète du réseau et du cloud. Pour accompagner les entreprises dans ces défis, Netis a lancé le "Livre Blanc sur l'Analyse et la Collecte du Trafic dans le Cloud et les Réseaux (2022)". Ce document, structur

é en six parties, aborde les défis du cloud moderne, l'intérêt de l'observabilité du trafic, les approches et technologies pour l'analyse du trafic et sa collecte, les stratégies de mise en œuvre, ainsi que des études de cas et des pratiques d'excellence sectorielles, offrant ainsi des solutions optimales pour la transition cloud de diverses industries.

Points clés du livre blanc :

**1. Compétences principales**

- Multienvironnemental :

  Compatibilité étendue : Prise en charge des systèmes d'exploitation majeurs, des chipsets dominants, ainsi que des technologies de virtualisation et conteneurisation courantes.

  Adaptation aux microservices : Supporte diverses configurations de déploiement sous architecture microservices et différents environnements de conteneurs.

- Polyvalence :

  Gestion des paquets de données : Capacités de collecte, de filtrage, de répartition, de découpage et de déduplication des paquets.

  Fonctionnalités Flow et Telemetry : Nécessité de prétraiter les paquets collectés pour générer des logs Flow et offrir un support Telemetry pour visualiser le trafic réseau et cloud.

  Marquage des données : Possibilité de marquer les paquets avec des informations spécifiques aux contextes d'application, de réseau et de sécurité.

  Transmission TCP : Utilisation du protocole TCP pour assurer une transmission fiable des données collectées.

- Non-intrusif : Intégration transparente sans nécessiter de modifications dans les opérations commerciales.

- Autonomie : Inclut l'intégration avec le tableau de bord, la surveillance de l'état de fonctionnement des collecteurs, l'autodiagnostic, le système de disjonction, l'auto-réparation et la visualisation.

- Scalabilité : Capacité à s'adapter dynamiquement à l'augmentation ou à la réduction des besoins.

**2. Techniques essentielles**

- Méthodes de collecte :

  Approches : On distingue principalement deux environnements : le cloud public et le cloud privé, et du côté technique, cela se divise en VM (machines virtuelles) et technologies de conteneurs.

  Compétences requises : Il est crucial que la collecte de données soit adaptative à différents scénarios, utilisant des techniques spécifiques pour chaque cas. De plus, dans un cadre hybride, une plateforme unifiée pour la gestion des données collectées est indispensable.

- Traitement multi-niveaux/vTAP : Selon Netis, le traitement des données du cloud doit se faire de manière stratifiée, en assurant la collecte, le traitement, la modification et la gestion par niveaux, afin de maintenir une construction d'observabilité exhaustive et précise, même en présence d'un grand nombre d'éléments à surveiller et d'un volume de trafic élevé.

- Technologie de collecte avancée : Face à la diversité et la complexité des environnements cloud, il est essentiel de sélectionner les technologies de collecte les plus adaptées pour optimiser performance et efficacité.

- Autonomie des environnements : Il est essentiel de supporter des serveurs autonomisés, y compris ceux basés sur des architectures CPU ARM et des systèmes d'exploitation sur mesure.

- Prise en charge de Flow : Les statistiques de flux basées sur des scénarios spécifiques permettent de répondre efficacement aux défis des réseaux et des applications, notamment en termes de sécurité, tout en équilibrant les coûts liés au trafic cloud.

- Capacités Telemetry : L'intégration des fonctionnalités d'Open Telemetry permet d'accroître l'observabilité tout en minimisant la consommation de ressources de trafic dans le cloud.

**3. Stratégies de déploiement**

Nous abordons ici cinq stratégies principales : le déploiement intégral du collecteur, la collecte de trafic sur les machines hôtes, la collecte de trafic sur les machines virtuelles, la collecte de trafic dans des environnements de conteneurs, et le détournement de trafic par vTAP. Chacune de ces stratégies est expliquée en détail dans notre livre blanc.

**4. Scénarios d'application typiques**

- Scénarios de sécurité : Uniquement avec un système de collecte de trafic réseau fiable, il est possible d'effectuer une extraction précise et dynamique du trafic des serveurs d'affaires dans le cloud.

  Conscience situationnelle : Pour une perception affinée des situations dans le cloud, compte tenu de la migration des charges de travail vers le cloud, il est crucial de comprendre la sécurité interne des services, en s'appuyant sur l'analyse précise du trafic cloud via des sondes de sécurité et des moteurs de sécurité dédiés.

  Protection niveau 2.0 : L'extraction précise et dynamique du trafic des serveurs d'affaires cloud par un système de collecte fiable est cruciale pour répondre aux exigences de la protection de niveau 2.0 sur le cloud.

- BPM/APM : Netis considère que le BPM permet une identification et localisation rapides des problèmes d'expérience utilisateur grâce à l'analyse du trafic réseau. Associé à l'analyse du code d'application par l'APM, cette approche facilite l'analyse des causes racines, offrant une nouvelle perspective pour l'observabilité dans le cloud.

- NPMD : Dans le cloud, à la différence des environnements traditionnels, la surveillance réseau doit intégrer des informations comme AZ, VPC, service, etc., et renforcer l'analyse topologique et le suivi de session à plusieurs niveaux.

  Analyse topologique dans le cloud : Pour suivre la topologie réseau du cloud, la surveillance réseau du cloud est essentielle, appuyée par la technologie de collecte de visibilité du trafic, s'adaptant aux dynamiques changeantes du cloud. Il est également nécessaire de compresser le trafic pour éviter la congestion.

  Suivi de session multi-niveaux : Pour l'analyse réseau dans le cloud, la capacité de suivi de session nécessite la technologie de visibilité du trafic pour un suivi à plusieurs niveaux.

- Gestion et sécurité des bases de données : Avec l'apparition des architectures de bases de données distribuées, de nouvelles exigences sont posées pour la surveillance traditionnelle. Les interactions fréquentes et les problèmes potentiels entre les nœuds de données et d'accès nécessitent l'utilisation de la collecte de visibilité du trafic dans le cloud pour une meilleure surveillance des bases de données distribuées.

[**Cliquez pour télécharger**](https://open.netis.com/datacenter/white-papers/天旦云网流量采集分析白皮书（2022）)
***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
