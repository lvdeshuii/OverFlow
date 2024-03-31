# Concevoir des Indicateurs de Performance pour les Systèmes IT des Banques

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

Avec l'évolution du secteur financier, la complexité des services bancaires et la diversification des architectures des systèmes d'information vont de pair. Identifier les problèmes uniquement sur la base de règles de surveillance technique devient un véritable défi. D'où l'émergence d'un besoin en stratégies de surveillance orientées vers les besoins réels du business, indépendantes des architectures technologiques et centrées sur la cartographie des processus d'affaires. Fort de son expérience opérationnelle et de sa compréhension approfondie du suivi des activités, l'auteur se penche sur les indicateurs et les règles clés pour une surveillance business efficace.

### L'évolution des pratiques de surveillance

**Première phase :** Les équipes IT mettent en place manuellement des indicateurs de performance, des règles et des paramètres de surveillance. Cela peut impliquer la configuration de scripts dans des systèmes comme Zabbix, avec des alertes se déclenchant lorsque certains seuils sont franchis.

**Deuxième phase :** La standardisation des indicateurs et des règles de surveillance, avec une responsabilité maintenue par les équipes opérationnelles IT pour la gestion des paramètres. Cette phase approfondit la première, harmonisant les critères de surveillance pour garantir une cohérence et une compatibilité étendue entre les différents systèmes.

**Troisième phase :** Le système de surveillance s'auto-régule, définissant les meilleurs indicateurs, règles et paramètres opérationnels en analysant ses performances et celles des systèmes en production, réduisant ainsi le besoin d'intervention manuelle.

Ce dialogue se concentre sur la phase intermédiaire essentielle, suggérant une série d'indicateurs de performance universels et de règles d'alerte, fruits d'une analyse approfondie des activités business.

### Indicateurs clés et règles d'alerte pour le suivi des services bancaires

Les systèmes informatiques bancaires se définissent par leurs codes de transaction ou interfaces, marqués par des codes de réponse, volumes de transactions et délais de réponses. Ce guide met en lumière les indicateurs de suivi cruciaux et les règles d'alerte, basés sur ces aspects, pour une surveillance opérationnelle efficace.

**1. Taux de succès des transactions**

Un indicateur essentiel dans le suivi des systèmes est le taux de succès des transactions, vital pour juger de la santé fondamentale d'un système. Traditionnellement, on considère qu'une transaction est réussie si aucune erreur système n'est présente (comme des soucis de réseau ou des erreurs d'accès aux fichiers). Cependant, l'absence d'erreurs système n'assure pas qu'il n'y ait pas de problèmes au niveau des processus métiers. Prenons la transaction A001, "interrogation de publication", qui signale normalement "aucun enregistrement trouvé". Une augmentation inattendue de ces interrogations pourrait signaler un souci, soulignant l'importance de distinguer les taux de succès système des taux de succès métier. Le taux de succès système se concentre sur les défaillances techniques, tandis que le taux de succès métier évalue le résultat des transactions par rapport aux codes de retour métiers attendus. Cette distinction permet un suivi plus précis, en se concentrant sur les résultats spécifiquement attendus de chaque transaction.

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/MR8pzzoKXjZp8SC2icFBL32T5nicZc8Nn56cTG16anNEMp3ug4lF03nnh9vKEyp8aHLvoe5x0Fvibo1SDTlNmydeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

Figure 1: Page du Taux de Succès des Transactions

**2. Taux de succès des transactions des systèmes de service**

Une particularité des systèmes bancaires réside dans la distinction nette entre les systèmes d'appel et les systèmes de service pour chaque transaction. Il est crucial de comprendre les performances des systèmes de service pour cibler les problèmes. Déterminez simplement si une transaction fait appel à un système de service et lequel. L'analyse des taux de succès liés à un système de service particulier révèle sa fiabilité. En examinant de plus près les codes de transactions spécifiques au sein du système de service, on peut obtenir une vision plus détaillée pour le diagnostic.

This reinterpreted version aims to make the content more approachable and easier to understand for readers of French science and technology blogs, while still conveying the original's factual content and maintaining its structural integrity.

**3. Quand les Nœuds Deviennent Silencieux : L'Alarme de Non-Transaction**

Dans le tourbillon du trading haute fréquence, une astuce ingénieuse se démarque : l'installation d'une alarme pour les moments, étonnamment, de silence total. Imaginez un marché foisonnant qui, subitement, s'immobilise. Cette alarme retentit lorsqu'une transaction précise n'est pas effectuée dans un délai déterminé sur un nœud spécifique, agissant comme une alerte pour une "action absente". C'est comme si l'absence d'un appel quotidien d'un ami suscitait votre inquiétude. Toutefois, anticiper cet appel (ou cette transaction) s'avère complexe, les périodes d'activité et de calme fluctuant, à l'instar des différences entre semaines et week-ends. Il est essentiel de cartographier le va-et-vient de chaque transaction pour identifier celles attendues à l'instant T. Nous différencions alors les "périodes de pointe" des "périodes creuses", les jours ouvrés de 8h à 19h étant considérés comme les plus chargés. Si le code transactionnel A002 est en effervescence constante, il est sous surveillance continue. A003, s'animant uniquement aux heures de pointe, bénéficie d'une pause en dehors. Quant à A004, murmurant à peine, elle reste discrète et sans surveillance.

**4. Fluctuations Brusques : À la Poursuite des Tsunamis Transactionnels**

Les transactions s'écoulent avec fluidité au quotidien, telles une rivière suivant son cours. Cependant, face à un obstacle, ce flux peut se muer en inondation ou en sécheresse. Il est vital de détecter ces transformations radicales. Suivons par exemple la transaction A005 durant l'affluence de l'après-midi. En la comparant à une journée type, nous mesurons l'écart. Si ce dernier se situe dans un intervalle attendu de fluctuations (par exemple, entre 0,8 et 1,2 fois la normale), tout est en ordre. Mais une chute à 0,4 ou une montée à 1,6 déclenche l'alarme. Cette méthode révèle ses limites avec les transactions sporadiques, où de légères variations peuvent sembler significatives.

**5. Sur la Trace du Pouls : Surveillance des Volumes de Transactions Atypiques**

Examiner les taux de réussite des transactions à la loupe, surtout à l'échelle des codes individuels, expose un défi : cette stratégie peine à gérer les extrêmes des transactions peu fréquentes ou à très haute fréquence. Les transactions rares déclenchent des alarmes à tout-va, tandis que les plus fréquentes pourraient ne pas éveiller l'attention nécessaire, occultant ainsi l'imminence d'un problème.

Considérons la transaction A006, avec ses 10 000 opérations en 10 minutes, dont 50 rencontrent un obstacle. Cela réduit le taux de réussite de juste 0,5 %, un détail en apparence anodin, mais potentiellement critique. D'autre part, A007, avec seulement deux transactions dans le même intervalle, mais d'une importance financière majeure, ne peut se permettre aucune erreur. La clé ? Ajuster les seuils d'alerte — plus de 10 échecs pour A006, un seul suffit pour A007 — en s'adaptant au rythme de chaque transaction, écartant ainsi efficacement le problème. Et envisagez un tableau de bord détaillant chaque transaction problématique, du nœud de traitement au système de service, simplifiant grandement le dépannage urgent.

**6. La Contrainte Temporelle : Quand le Temps de Réponse Explose**

Les systèmes bancaires, pareils à des mécanismes parfaitement huilés, peuvent connaître des faiblesses, se ralentir ou même s'arrêter. La surveillance habituelle peut surveiller les taux de réponse, mais que faire si les retards demeurent légèrement en dessous du seuil critique ? Dans le cas de transactions très fréquentées, un petit retard ne signale pas nécessairement le franchissement d'une limite critique.

Solution : surveillez les transactions dont les temps de réponse s'éloignent de l'ordinaire, à chaque cycle. Si, par exemple, A008 se conclut normalement en 300 ms, un allongement au-delà de 600 ms ou 900 ms pourrait indiquer un souci. Trois anomalies de ce type dans un cycle ? Il est temps d'alerter.

**7. Fermeture du Rideau, Équilibrage des Comptes**

Le clap de fin pour la journée d'un système bancaire, avec les procédures de clôture, est crucial pour assurer un démarrage sans accroc le lendemain. La surveillance est directe : les transactions prévues pour la clôture doivent être lancées et conclues dans des temps impartis, avec une confirmation de succès. Quant à l'équilibrage des comptes, la régularité est primordiale - des variations mineures dans les anomalies sont tout à fait normales.

Nous achevons ici notre voyage à travers la conception d'outils de surveillance des affaires à la fois intelligents et sensibles. Restez branchés pour découvrir les défis techniques liés à la concrétisation de ces idées.

Lien vers l'article original : https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
