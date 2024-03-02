# Análisis y Recolección de Tráfico en Redes Nube - Informe Blanco (2022)

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

De acuerdo con estudios de IDC, en los próximos dos años, la mayoría de las empresas adoptarán enfoques de nube híbrida y multicloud para desarrollar plataformas nativas en la nube. A medida que los escenarios de aplicación empresarial en la nube aumentan, el tráfico interno de la nube, conocido como tráfico este-oeste, supera las expectativas. Enfrentar el desafío de recolectar y administrar este tráfico de manera precisa se ha convertido en una preocupación común entre las empresas. Por ello, Gartner sugiere: "Los responsables de TI empresariales deberían replantearse las estrategias de recopilación y análisis de tráfico para proporcionar el nivel de visibilidad necesario en ambientes de nube híbrida, facilitando así la futura supervisión y gestión del rendimiento".

Netis cree que el análisis de la observabilidad del tráfico de red en entornos de nube es una de las estrategias más efectivas para abordar la supervisión y gestión del rendimiento en contextos de nube híbrida y nativa. Mediante el uso de tecnologías de captura y procesamiento de tráfico de alto rendimiento, que abarcan todos los escenarios y son no invasivas para las aplicaciones, es posible crear una visualización del tráfico en múltiples entornos y estructuras de red en la nube,

 logrando así una observabilidad de red completa. Para asistir a las empresas con los desafíos mencionados, Netis ha publicado el "Informe Blanco de Análisis y Recolección de Tráfico en Redes Nube (2022)". Este documento se estructura en seis secciones: desafíos de la era de la nube, valor de la observabilidad del tráfico de red, estructuras y tecnologías de recopilación y análisis de tráfico, estrategias de implementación, ejemplos de casos de uso y prácticas óptimas del sector, ofreciendo soluciones avanzadas para las empresas de diversos sectores que están migrando a la nube.

Los puntos clave del informe son los siguientes:

**1. Habilidades Clave**

- Multientorno:

  Soporte integral de entornos: Compatible con los principales sistemas operativos, chips y entornos de virtualización y contenedores.

  Apoyo a microservicios: Facilita diversas configuraciones de despliegue en arquitecturas de microservicios y soporta diferentes ambientes de ejecución de contenedores.

- Polivalencia:

  Manejo de paquetes de datos: Capacidad para gestionar paquetes de datos realizando acciones como recolección, filtrado, distribución, recorte y eliminación de duplicados.

  Capacidades de Flow y Telemetry: Esencial para la visualización del tráfico en redes nube, permite el preprocesamiento de paquetes de datos recogidos, la generación de registros de Flow y soporta funcionalidades de Telemetry.

  Función de marcado: Permite etiquetar paquetes de datos recogidos, integrando datos de escenarios comerciales, de red y de seguridad.

  Soporte de transmisión TCP: Emplea el protocolo TCP para asegurar la transmisión fiable de los paquetes de datos recolectados.

- Impacto nulo en la operativa empresarial: No interfiere con las operaciones del negocio, evitando la necesidad de realizar cambios.

- Autogestión: Incluye la integración con paneles de control, monitoreo del estado de los recolectores, autodiagnóstico, protección ante fallos, recuperación automática y funciones de visualización.

- Escalabilidad: Permite una ampliación y reducción dinámicas según las necesidades.

**2. Tecnologías Clave**

- Técnicas de Recolección:

  Escenarios soportados: Se clasifican en nubes públicas y privadas desde el ángulo de aplicación; y en tecnologías VM y Container desde una perspectiva técnica.

  Habilidades de apoyo: Es crucial que la captura de tráfico abarque diversos contextos y emplee estrategias específicas para cada uno. Además, tras la captura en ambientes mixtos, es imprescindible una plataforma que centralice su gestión.

- Procesamiento Multinivel/vTAP: Netis propone que la estrategia de captura de tráfico en la nube consiste en un enfoque escalonado para la recolección, procesamiento y gestión, garantizando un análisis detallado y completo incluso ante volúmenes de tráfico y número de objetos gestionados enormes.

- Tecnología de Captura Base: Ante la diversidad y complejidad de los ambientes en la nube, es vital seleccionar la tecnología de captura más eficiente para cada situación específica.

- Apoyo a Ambientes Independientes: La captura y análisis del tráfico de red en la nube debe ser compatible con servidores independientes, como aquellos basados en CPUs de arquitectura ARM o con sistemas operativos personalizados.

- Soporte de Flow: Utilizando estadísticas detalladas de flujo basadas en el escenario de uso, aplicables en contextos de red, aplicaciones y seguridad, se puede equilibrar de manera efectiva entre el valor generado y los costos de la red en la nube.



- Capacidad de Telemetría: A través de la integración con Open Telemetry, es posible ampliar la capacidad de observación minimizando al mismo tiempo el uso de recursos de tráfico en la red en la nube.

**3. Estrategias de Implementación**

Incluye principalmente cinco enfoques: estrategia integral de implementación de recolectores, estrategia para la

 captura de tráfico en servidores físicos, estrategia para la captura de tráfico en máquinas virtuales, estrategia para la captura de tráfico en entornos de contenedores, y vTAP para el enrutamiento del tráfico. Cada estrategia se explica detalladamente en el informe.

**4. Escenarios de Uso Comunes**

- En el ámbito de la seguridad: Solamente con un sistema eficaz de captura de tráfico en la nube se puede lograr una extracción precisa y dinámica del tráfico de servidores empresariales en la nube.

  Percepción de la situación: En la nube, comprender a fondo la seguridad interna del negocio es crucial debido a la carga de trabajo virtualizada, y depende del análisis exacto del tráfico en la nube por parte de las sondas y motores de seguridad subyacentes.

  Protección de nivel avanzado 2.0: La captura eficaz del tráfico en la nube permite una extracción precisa y actualizada del tráfico de los servidores empresariales, cumpliendo con los requisitos de la versión avanzada de protección en la nube 2.0.

- BPM/APM: Según Netis, BPM permite identificar y localizar rápidamente problemas de experiencia del usuario mediante el análisis de tráfico de red, y, al integrarlo con las capacidades de análisis de código de aplicación de APM, se facilita un diagnóstico profundo de los problemas, abriendo nuevos caminos para lograr una observabilidad eficaz en la nube.

- NPMD: A diferencia de los entornos tradicionales, la monitorización de redes en la nube debe incluir datos específicos como AZ, VPC, servicios, etc., y mejorar la capacidad para analizar la topología en la nube y realizar seguimientos detallados de las sesiones a múltiples niveles.

  Análisis de topología en la nube: Es vital tener un conocimiento actualizado de la estructura de la red en la nube, lo cual requiere de tecnologías de captura de tráfico en la nube que permitan adaptarse a los cambios dinámicos. Además, es importante minimizar el tráfico para evitar saturaciones mediante la optimización de la captura y análisis de datos.

  Seguimiento detallado de sesiones: Para una análisis de red en la nube efectivo, se requiere de un seguimiento detallado a varios niveles, lo cual es posible mediante tecnologías especializadas de captura de tráfico.

- Mantenimiento y seguridad de bases de datos: Con la emergencia de arquitecturas de bases de datos distribuidas en la nube, se necesitan nuevos enfoques para su monitorización. La frecuencia y complejidad de las interacciones entre los nodos de datos incrementan los desafíos, por lo que un enfoque basado en la captura de tráfico en la nube ofrece una solución más efectiva.

[**Descarga aquí**](https://open.netis.com/datacenter/white-papers/天旦云网流量采集分析白皮书（2022）)
***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
