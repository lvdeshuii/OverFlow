# Herausforderungen bei der Implementierung von Business Monitoring für Banken-IT-Systeme

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

In unserer vorherigen Diskussion haben wir gemeinsame Geschäftsindikatoren und Überwachungsregeln identifiziert. Bei der Umsetzung treten jedoch mehrere Schwierigkeiten auf, hauptsächlich in den folgenden Bereichen:

**1. Beschaffung grundlegender Transaktionsinformationen**

Damit Transaktionen effektiv überwacht werden können, muss das System für jede Transaktion genaue Daten sammeln. Dazu gehören Informationen wie das Anforderungssystem (das System, das die Transaktion anfordert), der Transaktionscode, wichtige Transaktionsflags (Statusindikatoren), das Dienstsystem (das System, das die Transaktion verarbeitet), der Verarbeitungsknoten, die Start- und Endzeiten, die Seriennummer, die Einrichtung, der Betrag, der Rückgabecode des Dienstsystems und der Rückgabecode dieses Systems. Leider können viele Systeme keine vollständigen Grundinformationen bereitstellen, wie z.B. den Rückgabecode des Dienstsystems. Wenn das Produktionssystem nicht ursprünglich so konzipiert wurde, dass es dieses Feld aufzeichnet, ist es schwierig, es bereitzustellen. Ohne diese Daten ist es unmöglich, die Erfolgsquote der Dienstsystemtransaktionen zu berechnen. Darüber hinaus stellen alle Systeme Transaktionsdetaildaten dem Überwachungssystem zur Verfügung, was zu großen Datenmengen führt, die die Verarbeitungsleistung des Überwachungssystems herausfordern.

**2. Entwicklungsspezifikationen für Produktionssysteme**

Überwachungsregeln gelten für alle Produktionssysteme, daher ist die Standardisierung und Normalisierung der Entwicklung von Produktionssystemen unerlässlich. Beispielsweise muss es eine starke Abhängigkeit vom Transaktionscodeparameter geben. Um dies zu erreichen, sollte der Transaktionscodeparameter das Anforderungssystem, den Transaktionscode, den Transaktionsnamen, das Dienstsystem, den Finanzflag (einen Indikator für finanzielle Transaktionen), den Belegungsflag (ein Indikator, ob das System beschäftigt ist) und den Leerlaufflag (ein Indikator, ob das System inaktiv ist), unter anderem, enthalten. Idealerweise sollte ein einzelner Transaktionscode nur eine Funktion ausführen. Beispielsweise hat der Transaktionscode A009 eine nicht standardmäßige funktionale Zerlegung, wodurch ein atomarer Transaktionscode A009-Programm ein sub_type-ähnliches Feld für die funktionale Verzweigung intern verwendet. Als Ergebnis implementiert ein einzelner Transaktionscode mehrere Geschäftsfunktionen, was es schwierig macht, die Geschäftsfunktionalität von A009 klar zu beschreiben.

Die Standardisierung von Entwicklungscode ist eine weitere große Herausforderung. Die Genauigkeit der Alarmauslösung hängt von dem Rückgabecode und der Protokollaufzeichnung ab, die vom Produktionssystem bereitgestellt werden. Während der Arbeit am zentralen Clearing-System der Bank X stieß der Autor auf einen klassischen Rückgabecode: 201999-Systemfehler. Dieser Fehler deutet normalerweise auf einen schwerwiegenden Systemfehler hin, den das Programm aus technischer Sicht nicht verarbeiten oder die Ursache bestimmen kann. Dieser Rückgabecode wird jedoch täglich etwa 800.000 Mal zurückgegeben, was zu einer Gesamterfolgsquote der täglichen Transaktionen von weniger als 90 % führt. Darüber hinaus können Rückgabecodes mehrere Verwendungszwecke haben. Beispielsweise sollte der Rückgabecode R00001 "Kein Datensatz gefunden" bedeuten, Entwickler können ihn jedoch anpassen, um "Unzureichender Saldo", "Kartennummer xxx Fehler", "Adressfehler" oder sogar das Gegenteil, wie "Abfrage zurückgegebene xxx Datensätze", zu bedeuten. In solchen Fällen kann der Rückgabecode nicht bestimmen, ob eine Transaktion erfolgreich ist. Dieses Problem wird in der Geschäftsüberwachung, die auf die Ebene des Transaktionscodes heruntergebrochen wird, noch deutlicher, wo das Transaktionsvolumen kleiner ist und die Empfindlichkeit gegenüber Rückgabewerten höher ist. Die Standardisierung von Rückgabecodes ist dringend erforderlich.

Auch die Protokollspezifikationen sollten die Standardisierung von Fehlerprotokollen umfassen. Genauere Protokollüberwachungsalarme erfordern eine standardisierte Protokollaufzeichnung; sonst können falsche Alarme und verpasste Alarme häufig auftreten.

**3. Einstellen zahlreicher Betriebsparameter**

Wenn die vorherigen Herausforderungen angegangen werden, müssen die Betriebspersonal kontinuierlich verschiedene Betriebsparameter feinabstimmen. Die Geschäftsklassenüberwachung erfordert Parametereinstellungen für jeden Transaktionscode, einschließlich Geschäftserfolgsrate, Systemerfolgsrate, Anstiegsverhältnis, Abbruchverhältnis, Indikatorabweichungs-Basisverhältnis und die Anzahl der ungewöhnlichen Transaktionen. Diese Parameter beschreiben die Betriebssituation des Transaktionscodes. Größere Systeme haben viele Transaktionscodes, was eine langfristige Anpassung von Zehntausenden von Betriebsparametern für den Transaktionscodeparameter erfordert. Wenn jedoch Regeln für die Parametereinstellung festgelegt werden, kann ein Algorithmus entwickelt werden, um die Betriebsparameter automatisch basierend auf der Basisbetriebssituation zu ändern.

Die Gestaltung eines Überwachungssystems ist nicht schwierig, aber die Herausforderung besteht darin, die Überwachung für das Geschäft relevanter zu machen, den Wert der Geschäftsüberwachung voll auszuschöpfen und den Übergang von der IT-Wartung zu den IT-Betriebsabläufen voranzutreiben.

[Originalartikel](https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
