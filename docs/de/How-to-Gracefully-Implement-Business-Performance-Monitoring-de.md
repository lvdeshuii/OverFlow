# Elegante Monitoring-Lösungen für Geschäftsprozesse

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


Wie schafft man es in einer Welt voller Monitoring-Tools, Komplexität zu reduzieren und Anwendern zu ermöglichen, ihr Geschäftsmonitoring elegant zu gestalten?

### **1. Der geschäftsorientierte Monitoring-Ansatz**

Die Alarmlogik von Tools zur Überwachung der Anwendungsperformance unterscheidet sich, basierend auf den Differenzen zwischen Überwachungskriterien und -zielen, signifikant. Generell teilt man sie in zwei Hauptansätze auf: den "Bottom-up"-Alarm, der Alarme auf Basis von niedrigstufigen Daten wie Datenpaketen setzt und sich dann zu höheren Ebenen wie der Nutzung von Anwendungen und Diensten vorarbeitet, um schließlich Probleme wie DNS-Fehler oder langsame Reaktionszeiten zu identifizieren. Dem gegenüber steht der "Top-down"-Alarm, der durch Monitoring der geschäftskritischen Anwendungs

- und Netzwerkknoten auf höherstufigen Aggregatdaten basiert und von oberflächlichen Geschäftsproblemen aus tiefer in die Datenebene eindringt. Da "Bottom-up"-Alarme oft zeitaufwendig und unpräzise sind, zeichnen sich "Top-down"-Alarme durch ihre Fähigkeit aus, bei System- oder Serviceausfällen sofort zu alarmieren, was sie zu einem unverzichtbaren Werkzeug in einem geschäftsorientierten IT-Operations-Framework macht.
![002316seeudyfefdc8nldk.jpg](http://image.sciencenet.cn/album/201306/28/002316seeudyfefdc8nldk.jpg)

*Abbildung 1: Wissenshierarchie-Diagramm*

Netis BPC setzt technologisch auf den "Top-down"-Monitoring-Ansatz, bietet durch eine End-to-End-Monitoringabdeckung tiefgreifende Einblicke von Makro bis Mikro. Indem es das Geschäft in den Mittelpunkt stellt und die Barrieren zwischen Betrieb und Management niederreißt, schafft es eine einheitliche Sichtweise auf Monitoring und Geschäftsprozesse und gewährleistet damit höchste Präzision und Verständlichkeit in der Analyse von Alarmindikatoren.

### **2. Designkonzept mit dem Nutzer im Mittelpunkt**

Das Herzstück von Netis BPC bildet ein innovatives Design, bei dem Klaviertasten die Zeit symbolisieren und ein Vier-Felder-Raster die Kernindikatoren des Geschäfts visualisiert.
![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyo1rZQMYRmK4Yfiambegqu7bWA3usmGboVBg1Ziav7DHAmztEEPeSWuh7Q/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Abbildung 2: Einsatz von Klaviertasten und dem Vier-Felder-Raster in Netis BPC für effiziente Fehleralarmierung und -lokalisierung*

**Warum repräsentiert eine Klaviertaste genau eine Minute?**

Netis BPC hat sich zum Ziel gesetzt, Nutzern eine intuitive und zeitnahe Einsicht in den Betriebszustand ihres Geschäfts zu ermöglichen und dabei Routinearbeiten möglichst angenehm zu gestalten. Die Zeit wird durch Klaviertasten dargestellt, wobei jede Taste für eine Minute steht. Dies ermöglicht eine dynamische Interaktion: Nutzer können durch Bewegen der Maus über die Tasten, ähnlich wie beim Klavierspielen, mit den Daten interagieren. Der Fokus auf ein spezifisches Zeitsegment bewirkt eine Vergrößerung der entsprechenden Taste - ein Design, das präzise Informationsabfrage unterstützt.

Die Entscheidung für minutengenaue Alarme berücksichtigt sowohl die Notwendigkeit der Echtzeitreaktion als auch die Kosten. Die Erfahrung mit Finanzkunden zeigt, dass eine zu detaillierte Alarmierung zu einer Überflutung mit meist redundanten Warnungen führt, während zu grobe Einstellungen die Reaktionsfähigkeit beeinträchtigen. Daher wurde die Minutengranularität als optimaler Kompromiss gewählt.

Für spezifische Branchenanforderungen, wie den hochsensiblen Aktienhandel, wurde ein zweiter, auf Sekunden basierender Alarmmodus entwickelt. Hier ermöglicht die Definition spezifischer Triggerkriterien, wie zehn bestimmte Ereignisse innerhalb einer Sekunde oder Transaktionszeiten über 10ms, eine noch präzisere Fehlererkennung und -reaktion.

**Präsentation der Schlüsselindikatoren**

Das Team von Netis hat entdeckt, dass Handelsvolumen und Anwendungslast, Antwortgeschwindigkeit und Systemstabilität sowie Erfolgsraten und Geschäftsleistung direkt zusammenhängen, während die Zeit bis zur Reaktion auf Anfragen invers zur Kundenzufriedenheit steht.Nach einem Vergleich der Four Golden Signals, RED und USE-Indikatoren, speziell für den Finanzsektor, kristallisierten sich Handelsvolumen, Antwortrate, Antwortzeit und Erfolgsrate als die vier zentralen Indikatoren für Netis BPC heraus.

Wie lässt sich dies nun Nutzern klar und intuitiv vermitteln, um ihre Erfahrung zu optimieren? Nach umfangreicher Analyse und zahlreichen Tests hat das Netis-Team den ersten Vier-Felder-Raster der Branche entwickelt.

Die Inspiration für dieses Layout kam Wizard, dem Mitgründer und Produktchef von Netis, bei einem Besuch des Museum of Modern Art in New York. Eine Ausstellung zeigte eine Karte der USA, die Informationen in einem klaren und strukturierten Raster darstellte. Diese Art der Präsentation, die wichtige Informationen fokussiert und leicht zugänglich macht, wurde zur Basis für den Vier-Felder-Raster von Netis.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq0zib9UrUva92PkicX1HbHqyo8icuiaU00eVBRmcY23lm9lq2fzViaRNFP7DiaiccI3GpszkEpyQFMf4TEQw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)

*Abbildung 3: Inspirierender Vier-Felder-Raster im Museum of Modern Art in New York*

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyoVNumuLZRlcb00S7bS3dP9oicnycxmmwSAGrvAukAunwnB6HePm1FFUg/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Abbildung 4: Der Vier-Felder-Raster von Netis BPC*

Die Entwicklung des BPC-Produkts basiert auf einem tiefen Verständnis der Nutzerbedürfnisse und einem zielgerichteten Designansatz. Indem wir aus der Perspektive unserer Kunden die Notwendigkeit von präzisen Alarmmeldungen betrachten und die Indikatoren im Designprozess berücksichtigen, haben wir ein System geschaffen, das nicht nur den Anforderungen der Nutzer gerecht wird, sondern auch deren Anwendungserfahrung verbessert.

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
