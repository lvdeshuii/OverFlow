
# Whitepaper zur Sammlung und Analyse von Cloud-Netzwerkverkehr (2022)

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

Eine Studie von IDC zeigt, dass in den nächsten zwei Jahren die meisten Unternehmen auf Hybrid- und Multi-Cloud-Strategien setzen werden, um cloud-native Plattformen zu entwickeln. Angesichts der wachsenden Vielfalt von Anwendungsszenarien in der Cloud stellt der interne (Ost-West-)Verkehr eine weit größere Herausforderung dar als ursprünglich erwartet. Die präzise Erfassung und Verwaltung dieses Verkehrs stellt Unternehmen vor eine gemeinsame Herausforderung. Gartner empfiehlt daher, dass IT-Entscheidungsträger in Unternehmen ihre Methoden zur Erfassung und Analyse des Verkehrs überdenken sollten, um die notwendige Transparenz in Hybrid-Cloud-Umgebungen zu schaffen und so zukünftige Leistungsüberwachung und -management zu ermöglichen.

Netis ist der Meinung, dass die Analyse der Beobachtbarkeit des Cloud-Netzwerkverkehrs eine der effektiven Methoden darstellt, um die Herausforderungen der Leistungsüberwachung und des Managements in cloud-nativen und Hybrid-Cloud-Umgebungen anzugehen. Durch die Anwendung von Technologien zur le

istungsstarken, umfassenden und nicht-invasiven Erfassung und Verarbeitung des Verkehrs kann eine Cloud-Netzwerkverkehrsvisualisierung über verschiedene Umgebungen und Architekturen hinweg realisiert werden, was letztendlich zu einer umfassenden Beobachtbarkeit des Cloud-Netzwerks führt. Um Unternehmen bei der Bewältigung dieser Herausforderungen zu unterstützen, hat Netis das "Whitepaper zur Sammlung und Analyse von Cloud-Netzwerkverkehr (2022)" herausgegeben. Das Dokument ist in sechs Abschnitte gegliedert: Herausforderungen der Cloud-Ära, der Wert der Cloud-Netzwerkverkehrsbeobachtbarkeit, Architektur und Technologie für die Sammlung und Analyse der Verkehrsbeobachtbarkeit, Lösungsstrategien, typische Anwendungsfälle und branchenspezifische Best Practices. Es bietet Nutzern aus allen Branchen optimale Cloud-Lösungen.

Die Hauptpunkte des Whitepapers sind wie folgt:

**1. Kernkompetenzen**

- Vielfältige Umgebungen:

  Breite Unterstützung: Kompatibilität mit führenden Betriebssystemen, Chipsätzen, Virtualisierungs- und Containerumgebungen gewährleistet.

  Mikroservice-Unterstützung: Ermöglicht vielfältige Bereitstellungsarten innerhalb von Mikroservice-Architekturen und unterstützt diverse Container-Laufzeiten.

- Umfangreiche Fähigkeiten:

  Datenpaket-Management: Bietet umfassende Funktionen wie Sammeln, Filtern, Verteilen, Zuschneiden und Entfernen von Duplikaten bei Datenpaketen.

  Flow- und Telemetrie-Funktionen: Notwendige Vorverarbeitung gesammelter Datenpakete zur Visualisierung des Cloud-Netzwerkverkehrs, inklusive Erstellung von Flow-Logs und Telemetrie-Unterstützung.

  Markierungsfunktion: Erlaubt das Hinzufügen spezifischer Informationen zu Geschäfts-, Netzwerk- und Sicherheitsaspekten in die gesammelten Datenpakete.

  TCP-Unterstützung: Sichert die Zuverlässigkeit der Datenübertragung durch Nutzung des TCP-Protokolls.

- Geschäftsneutralität: Keine Eingriffe oder Änderungen am bestehenden Geschäftsbetrieb notwendig.

- Eigenverwaltung: Umfasst Anbindung an das Verwaltungsdashboard, Überwachung des Betriebsstatus der Sammeltools, Selbstüberwachung, Fehlerisolierung, Selbstheilung und Visualisierungsfeatures.

- Modulare Struktur: Unterstützt flexible Anpassung und Skalierung.

**2. Schlüsseltechniken**

- Erfassungstechnologie:

  Einsatzgebiete: Es gibt zwei Hauptanwendungsbereiche: die öffentliche und die private Cloud; technisch gesehen unterteilen sich diese in VM- und Container-Technologien.

  Fähigkeiten: Die Datenerfassung sollte sich erstens auf vielfältige Szenarien erstrecken und unterschiedliche Methoden je nach Kontext anwenden. Zweitens erfordert die Erfassung in gemischten Umgebungen eine zentrale Verwaltungsplattform.

- Mehrschichtiges Verarbeiten/vTAP: Netis ist der Ansicht, dass die Technik zur Erfassung des Cloud-Verkehrs mit einem schichtenweisen Ansatz – Erfassen, Verarbeiten, Verfeinern und Verwalten – sicherstellt, dass auch bei enormem Datenverkehr und vielen Verwaltungsobjekten eine gründliche und umfassende Überwachbarkeit gewährleistet ist.

- Grundlegende Erfassungstechniken: Aufgrund der Vielfalt und Komplexität der Basisschichten der Cloud müssen spezifische, auf die jeweilige Umgebung zugeschnittene Erfassungstechniken gewählt werden, um die höchstmögliche Leistung und Effizienz zu erreichen.

- Unterstützung unabhängiger Umgebungen: Für

 die Erfassung und Analyse des Cloud-Netzwerkverkehrs müssen unabhängige Server unterstützt werden, beispielsweise CPUs basierend auf der ARM-Architektur oder angepasste Betriebssysteme.

- Flow-Unterstützung: Durch detaillierte Flow-Statistiken, die auf spezifische Nutzerszenarien abgestimmt sind und in Bereichen wie Netzwerk, Anwendungen und Sicherheit eingesetzt werden, können Entscheidungen zwischen Mehrwert und Cloud-Netzwerkkosten effektiv getroffen werden.

- Telemetriefunktion: Durch die Integration von Open Telemetry kann die Überwachungsleistung verbessert werden, während gleichzeitig der Ressourcenverbrauch des Cloud-Netzwerkverkehrs deutlich reduziert wird.

**3. Implementierungspläne**

Es gibt hauptsächlich fünf Arten: Gesamtlösungen

 für Sammler, Verkehrserfassungssysteme für Hosts, für virtuelle Maschinen, für Containerumgebungen und vTAP-Umleitungen. Diese Pläne werden im Weißbuch ausführlich erläutert.

**4. Typische Anwendungsbeispiele**

- Sicherheit: Eine präzise und dynamische Erfassung des Cloud-internen Verkehrs ist nur mit einem zuverlässigen Cloud-Netzwerkverkehrserfassungssystem möglich.

  Situationsbewusstsein: Für das Verständnis der internen Sicherheitslage in der Cloud ist eine genaue Analyse des Cloud-Verkehrs notwendig.

  Schutzlevel 2.0: Die Erfüllung der Cloud-Sicherheitsstandards setzt eine genaue Erfassung des Netzwerkverkehrs voraus.

- BPM/APM: Netis sieht in der schnellen Identifikation und Lokalisierung von Benutzererfahrungsproblemen durch BPM in Kombination mit der Codeanalyse durch APM eine innovative Lösung für die Überwachung in der Cloud.

- NPMD: Cloud-basierte Netzwerküberwachung unterscheidet sich von traditionellen Ansätzen und erfordert eine detaillierte Analyse inklusive Cloud-spezifischer Informationen wie AZ und VPC sowie erweiterte Fähigkeiten zur Topologieanalyse und zur Nachverfolgung von Sitzungen über mehrere Ebenen.

  Cloud-Topologieanalyse: Um die Dynamik der Cloud-Strukturen zu bewältigen, ist eine fortlaufende Überwachung mit Unterstützung durch spezielle Sammeltechniken notwendig.

  Tiefgehende Sitzungsverfolgung: Eine mehrschichtige Verfolgung von Sitzungen in der Cloud erfordert fortschrittliche Technologien zur Datenerfassung.

- Datenbankmanagement und -sicherheit: Neue Herausforderungen für das Monitoring traditioneller Datenbanken entstehen durch die Verbreitung von Cloud-basierten verteilten Architekturen. Ein Cloud-basiertes Überwachungssystem, das durch Verkehrserfassungstechnologien unterstützt wird, bietet hier eine optimale Lösung.

[**Download hier**](https://open.netis.com/datacenter/white-papers/天旦云网流量采集分析白皮书（2022）)
***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
