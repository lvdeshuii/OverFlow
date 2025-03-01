# Entwicklung von Geschäftsüberwachungsmetriken für Bank-IT-Systeme

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

Der Finanzsektor entwickelt sich ständig weiter, und mit ihm steigt die Komplexität der Bankdienstleistungen sowie die Vielfalt der Architekturen von Informationssystemen. Es wird immer schwieriger, Probleme durch ausschließlich technische Überwachungsregeln zu erkennen. Daher wächst der Bedarf an Überwachungsstrategien, die auf das Geschäft ausgerichtet sind und unabhängig von der verwendeten Technologie nur die Geschäftsabläufe abbilden. Mit umfangreichen praktischen Erfahrungen und tiefgehendem Wissen über die Überwachung von Geschäftsprozessen beleuchtet der Autor die entscheidenden Metriken und Regeln für eine effektive Geschäftsüberwachung.

### Evolution der Überwachungsmethoden

**Erste Stufe:** Das IT-Betriebspersonal legt manuell Überwachungsmetriken, Regeln und Parameter fest. Ein verbreiteter Ansatz ist die Konfiguration von Skripten in einem Überwachungssystem wie Zabbix, bei dem spezifische Alarmbedingungen auf der Basis von Schwellenwerten festgelegt werden. Wird ein Schwellenwert über- oder unterschritten, wird ein Alarm ausgelöst.

**Zweite Stufe:** Die Überwachungsmetriken und -regeln werden standardisiert. Das IT-Betriebspersonal ist für die Pflege der Betriebsparameter verantwortlich. Auf dieser Stufe werden die Überwachungskriterien organisiert und vereinheitlicht, um eine weitreichende Kompatibilität und Gleichförmigkeit über verschiedene Systeme hinweg zu gewährleisten.

**Dritte Stufe:** Das Überwachungssystem ermittelt selbstständig die Metriken, Regeln und optimalen Betriebsparameter durch die Analyse seiner eigenen Leistung sowie die der Produktionssysteme, wodurch der manuelle Aufwand für das IT-Personal minimiert wird.

Im Mittelpunkt dieser Diskussion steht die wichtige zweite Stufe, die einen Satz universeller Überwachungsmetriken und Alarmregeln vorstellt, die aus den operativen Erfahrungen mit Geschäftsprozessen gewonnen wurden.

### Wesentliche Kennzahlen und Warnregeln für das Monitoring von Bankdiensten

Bankinformationssysteme definieren sich über ihre Transaktionscodes oder Schnittstellen, die durch Rückgabecodes, Transaktionsvolumina und Reaktionszeiten charakterisiert sind. Dieser Leitfaden umreißt entscheidende Metriken und Warnregeln basierend auf diesen Eigenschaften und dient als Referenz für effektives Monitoring im Geschäftsbereich.

**1. Transaktionserfolgsrate**

Eine grundlegende Kennzahl in der Systemüberwachung ist die Transaktionserfolgsrate, die für die Beurteilung der Basisgesundheit eines Systems unerlässlich ist. Traditionelles Monitoring definiert eine Transaktion als erfolgreich, wenn keine systemischen Fehler vorliegen (z.B. Netzwerkprobleme oder Fehler beim Dateizugriff). Allerdings bedeutet das Fehlen solcher Fehler nicht, dass keine Probleme im Geschäftsprozess vorliegen. Betrachten wir zum Beispiel Transaktion A001, „Abfragebuchung“, die normalerweise „kein Datensatz gefunden“ bedeutet. Ein ungewöhnlicher Anstieg dieser Buchungen könnte auf ein Problem hinweisen, was die Notwendigkeit unterstreicht, zwischen System- und Geschäftserfolgsraten zu unterscheiden. Die Systemerfolgsrate bezieht sich auf technische Fehler, während die Geschäftserfolgsrate die Transaktionsergebnisse im Vergleich zu den erwarteten Geschäftsrückgabecodes bewertet. Dieser differenzierte Ansatz ermöglicht eine genauere Überwachung, die über die reine Erfolgsquote hinausgeht und spezifische erwartete Ergebnisse für jede Transaktion berücksichtigt.

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/MR8pzzoKXjZp8SC2icFBL32T5nicZc8Nn56cTG16anNEMp3ug4lF03nnh9vKEyp8aHLvoe5x0Fvibo1SDTlNmydeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

Abbildung 1: Übersicht zur Transaktionserfolgsrate

**2. Transaktionserfolgsrate im Dienstleistungssystem**

Ein besonderes Merkmal von Bankensystemen ist die deutliche Trennung zwischen aufrufenden Systemen und Dienstleistungssystemen bei jeder Transaktion. Das Verständnis der Leistung von Dienstleistungssystemen ist essentiell, um Probleme genau zu identifizieren. Es gilt festzustellen, ob und welches Dienstleistungssystem eine Transaktion initiiert. Die Analyse der Erfolgsraten von mit einem spezifischen Dienstleistungssystem verknüpften Transaktionen gibt Aufschluss über dessen Verlässlichkeit. Eine feinere Aufschlüsselung, wie zum Beispiel die Bewertung einzelner Transaktionscodes innerhalb des Dienstleistungssystems, ermöglicht eine noch präzisere Diagnose.

**3. Wenn Knoten verstummen: Der Alarm für ausbleibende Transaktionen**

In der rasenden Welt des Hochfrequenzhandels gibt es einen cleveren Kniff: die Einrichtung eines Alarms für den Fall, dass, wider Erwarten, nichts geschieht. Stellen Sie sich einen lebhaften Marktplatz vor, der plötzlich zur Ruhe kommt. Dieser Alarm ertönt, wenn eine spezifische Transaktion nicht innerhalb eines festgelegten Zeitraums an einem bestimmten Knoten stattfindet – es handelt sich quasi um einen Alarm für eine ausgebliebene Handlung. Es ähnelt der Situation, wenn man den täglichen Anruf eines Freundes erwartet und sich Sorgen macht, sollte dieser ausbleiben. Doch ist es nicht immer einfach zu bestimmen, wann dieser Anruf (oder die Transaktion) zu erwarten ist, da sowohl geschäftige als auch stille Zeiten variieren, ähnlich wie Wochenenden und Werktage. Es geht darum, den Fluss jeder Transaktion zu überwachen und jene zu identifizieren, die aktuell stattfinden sollten. So unterscheiden wir zwischen „Hochzeiten“ und „Flauten“ – wobei beispielsweise Werktage von 8 Uhr morgens bis 19 Uhr als Hauptverkehrszeiten gelten. Während der Transaktionscode A002 den ganzen Tag aktiv ist und kontinuierlich beobachtet wird, erhält A003 während der Stoßzeiten Aufmerksamkeit und kann in den Ruhephasen pausieren. Und A004? Wenn es den ganzen Tag über kaum Aktivität zeigt, bleibt es unbeachtet.

**4. Plötzliche Umschwünge: Das Verfolgen von Transaktionswellen**

Tagtäglich fließen Transaktionen gleichmäßig wie ein Fluss in seinem Bett. Doch trifft das System auf ein Hindernis, kann dieser Strom zu einer Überflutung oder zu einem Austrocknen führen. Es ist von großer Bedeutung, solche drastischen Änderungen frühzeitig zu erkennen. Nehmen wir an, wir beobachten eine Transaktion, A005, während der Stoßzeit am Nachmittag. Durch Vergleich ihrer Aktivität mit einem „normalen“ Tag lassen sich Veränderungen feststellen. Bewegt sich diese im Rahmen üblicher Schwankungen (etwa 0,8 bis 1,2-mal der Norm), ist alles in Ordnung. Weicht sie jedoch signifikant ab, etwa auf 0,4 oder steigt auf 1,6, so wird der Alarm ausgelöst. Diese Methode findet allerdings bei selteneren Transaktionen ihre Grenzen, wo selbst geringfügige Veränderungen bedeutend erscheinen können.

**5. Den Puls fühlen: Abweichende Transaktionsvolumen im Blick**

Ein genauer Blick auf die Erfolgsraten von Transaktionen, besonders auf der detaillierten Ebene einzelner Codes, offenbart eine Schwierigkeit: Dieser Ansatz passt nicht gut zu Transaktionen mit sehr niedriger oder extrem hoher Frequenz. Niedrigfrequente Transaktionen könnten Alarme wie Feuerwerke auslösen, während hochfrequente Transaktionen möglicherweise unbemerkt bleiben und so das Signal für aufkommende Probleme verpassen.

Betrachten wir zum Beispiel Transaktion A006, die in nur 10 Minuten mit 10.000 Transaktionen aufwartet, von denen 50 auf Probleme stoßen. Das senkt die Erfolgsrate um nur 0,5% – ein auf den ersten Blick geringfügiger, doch potenziell folgenschwerer Rückgang. Andererseits registriert A007 in derselben Zeitspanne nur zwei Transaktionen, doch angesichts seiner bedeutenden finanziellen Rolle ist selbst eine kleine Störung nicht zu übersehen. Die Lösung liegt in der individuellen Anpassung der Alarmgrenzen – mehr als 10 Fehler bei A006, aber nur einer bei A007 – basierend auf dem jeweiligen Transaktionsprofil, um das Problem effektiv zu umgehen. Und stellen Sie sich ein Dashboard vor, das Einblicke in alle problematischen Transaktionen bietet, vom Verarbeitungsknoten bis zum Service-System, was die Notfallbehebung erheblich erleichtert.

**6. Zeitdruck: Wenn Antwortzeiten sich ziehen**

Wie jede präzise arbeitende Maschine können auch Banksysteme ins Stocken geraten und langsamer werden oder sogar zum Stillstand kommen. Traditionelle Überwachungssysteme mögen bei Antwortzeiten aufmerken, doch was geschieht, wenn sich Verzögerungen knapp unter der Alarmgrenze halten? Insbesondere bei Transaktionen mit hohem Datenaufkommen bedeutet eine geringfügige Verzögerung nicht gleich das Überschreiten des kritischen Limits.

Ein Tipp: Behalten Sie Transaktionen im Auge, deren Antwortzeiten vom Normalfall abweichen – und das von Zyklus zu Zyklus. Sollte beispielsweise A008 normalerweise in 300 Millisekunden abgewickelt sein, deutet eine Ausdehnung auf 600 oder 900 Millisekunden auf ein mögliches Problem hin. Treten solche Ausreißer dreimal innerhalb eines Zyklus auf, ist es Zeit, Alarm zu schlagen.

**7. Tagesabschluss und Buchführung**

Der Abschluss eines Bankentages, die Vorgänge zum Tagesende, bildet den Schlüssel für einen reibungslosen Start in den nächsten Tag. Die Überwachung ist hierbei klar definiert: Transaktionen, die zum Tagesende gehören, müssen innerhalb festgelegter Zeiten starten und abschließen – gekrönt von einem Signal, das den Erfolg anzeigt. Beim Ausgleichen der Bücher gilt: Konstanz ist entscheidend. Geringe Abweichungen sind normal und kein Grund zur Beunruhigung.

Damit schließen wir unsere Betrachtung zur Entwicklung intelligenter und feinfühliger Instrumente für die Geschäftsüberwachung ab. Bleiben Sie dran für Einblicke in die technischen Herausforderungen, die bei der Realisierung dieser Konzepte auf uns zukommen.

Originalartikel-Link: https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
