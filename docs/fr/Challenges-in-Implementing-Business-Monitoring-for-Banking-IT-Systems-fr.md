# Défis de l'implémentation de la surveillance des affaires pour les systèmes informatiques bancaires

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

Dans notre discussion précédente, nous avons identifié des indicateurs d'affaires courants et des règles de surveillance. Néanmoins, plusieurs difficultés émergent lors de l'implémentation, principalement dans les domaines suivants :

**1. Acquisition des informations fondamentales sur les transactions**

Pour une surveillance efficace des transactions, le système doit recueillir précisément les données de chaque transaction, incluant le système requérant, le code de la transaction, les drapeaux importants de la transaction, le système de service, le nœud de traitement, les horaires de début et de fin, le numéro de série, l'institution, le montant, le code de retour du système de service, et celui de ce système, parmi d'autres détails. Malheureusement, beaucoup de systèmes ne peuvent pas fournir toutes les informations de base nécessaires, comme le code de retour du système de service. Si le système de production n'était pas initialement conçu pour enregistrer cette donnée, il est difficile de la fournir. Sans cette information, il est impossible de calculer le taux de réussite des transactions du système de service. En outre, tous les systèmes fournissent des détails sur les transactions au système de surveillance, générant un volume de données élevé qui met au défi la capacité de traitement du système de surveillance.

**2. Normes de développement pour les systèmes de production**

Les règles de surveillance s'appliquent à tous les systèmes de production, donc la standardisation et la normalisation du développement des systèmes de production sont cruciales. Il est essentiel, par exemple, qu'il y ait une forte dépendance vis-à-vis du paramètre de code de transaction. Pour y parvenir, le paramètre du code de transaction devrait comprendre le système requérant, le code de transaction, le nom de la transaction, le système de service, le marqueur financier, le drapeau d'activité, et le drapeau d'inactivité, entre autres. Idéalement, un seul code de transaction devrait exécuter une seule fonction. Par exemple, le code de transaction A009 présente une décomposition fonctionnelle non standard, ce qui conduit un programme de code de transaction atomique A009 à utiliser un champ semblable à un sous-type pour une bifurcation fonctionnelle interne. En conséquence, un unique code de transaction implémente plusieurs fonctions d'affaires, rendant la description claire de la fonctionnalité commerciale de A009 difficile.

La standardisation du code de développement représente un autre défi majeur. La précision des alertes dépend du code de réponse et de l'enregistrement des logs fournis par le système de production. Lors du travail sur le système central de compensation de la Banque X, l'auteur a rencontré un code de réponse classique : 201999 - Erreur système. Cette erreur indique généralement un défaut sérieux du système que le programme ne peut pas traiter d'un point de vue technique ou dont il ne peut déterminer la cause. Cependant, ce code de réponse est retourné environ 800 000 fois par jour, aboutissant à un taux de réussite des transactions quotidien inférieur à 90 %. De plus, les codes de retour peuvent être utilisés de multiples façons. Par exemple, le code de retour R00001 devrait signifier « Aucun enregistrement trouvé », mais il peut être personnalisé pour signifier « Solde insuffisant », « Erreur sur le numéro de carte xxx », « Erreur d'adresse », ou même l'inverse, comme « La requête a retourné xxx enregistrements ». Dans ces cas, le code de retour ne permet pas de déterminer si une transaction est réussie. Ce problème est d'autant plus marqué dans la surveillance des affaires qui se concentre sur le niveau du code de transaction, où le volume des transactions est plus faible et la sensibilité aux valeurs de retour est plus élevée. La standardisation des codes de retour est donc une nécessité urgente.

La standardisation des logs d'erreurs est également cruciale. Les alarmes précises de surveillance des logs dépendent d'un enregistrement standardisé des logs ; sans cela, les fausses alertes et les omissions d'alertes peuvent se produire fréquemment.

**3. Ajustement de nombreux paramètres d'exécution**

Une fois les défis précédents relevés, le personnel opérationnel doit continuellement peaufiner divers paramètres d'exécution. La surveillance à caractère commercial exige des paramètres pour chaque code de transaction, y compris le taux de succès commercial, le taux de succès du système, le ratio de hausse, le ratio de baisse, le ratio de déviation de l'indicateur de base, et le nombre de transactions anormales. Ces paramètres décrivent la situation d'exécution du code de transaction. Dans les systèmes plus importants, de nombreux codes de transaction nécessitent un ajustement à long terme de dizaines de milliers de paramètres d'exécution rien que pour le paramètre du code de transaction. Cependant, si des règles de paramétrage sont établies, un algorithme peut être conçu pour ajuster automatiquement les paramètres d'exécution en fonction de la situation d'exécution de base.

Concevoir un système de surveillance n'est pas compliqué, mais le véritable défi réside dans la capacité à rendre la surveillance plus pertinente pour les affaires, à maximiser la valeur de la surveillance des affaires et à piloter la transformation de la maintenance IT vers les opérations IT.

[Article original](https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
