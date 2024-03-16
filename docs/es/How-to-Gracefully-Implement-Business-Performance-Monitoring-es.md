# Elegancia en la monitorización del rendimiento empresarial: Una guía

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


¿Cómo podemos hacer más sencillo el complejo mundo de las herramientas de monitorización para mejorar el rendimiento empresarial de forma elegante?

### **1. Enfocándonos en el negocio para una mejor monitorización**

Las herramientas de monitorización del rendimiento de aplicaciones tienen diferentes lógicas de alerta debido a las variadas necesidades y objetivos. Podemos clasificar estas lógicas de alerta principalmente en dos enfoques: el primero es el enfoque "de abajo hacia arriba", que empieza con la detección de anomalías en datos fundamentales, como los encabezados de paquetes, para luego escalar hasta analizar la utilización de aplicaciones y servicios, identificando finalmente problemas específicos en los negocios, como errores DNS o lentitud en las respuestas. El segundo enfoque es el "de arriba hacia abajo", que comienza por monitorear los aspectos críticos de los negocios y la red para establecer indicadores de alerta basados en datos agregados, permitiendo una rápida detección de problemas desde una perspectiva empresarial superior. Las alertas "de abajo hacia arriba" suelen ser tediosas y propensas a errores debido a la dificultad de filtrar falsas alarmas, mientras que las "de arriba hacia abajo" ofrecen una manera rápida y precisa de identificar fallos críticos, siendo cruciales en un entorno operativo que prioriza el negocio.

![002316seeudyfefdc8nldk.jpg](http://image.sciencenet.cn/album/201306/28/002316seeudyfefdc8nldk.jpg)

*Figura 1: Jerarquía del Conocimiento*

Netis BPC se destaca por su estrategia de monitorización "de arriba hacia abajo", abarcando desde una visión global hasta el detalle más fino, centrada en el negocio para fusionar operaciones y estrategias comerciales, logrando una visión unificada que asegura la precisión y claridad en el análisis de alertas.

### **2. Diseño innovador centrado en el usuario**

Convertir las teclas de piano en representaciones del tiempo y utilizar un cuadrante para mostrar los indicadores clave del negocio son las ingeniosas estrategias de diseño de Netis BPC.
![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyo1rZQMYRmK4Yfiambegqu7bWA3usmGboVBg1Ziav7DHAmztEEPeSWuh7Q/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Figura 2: Aplicación de teclas de piano y cuadrantes en la detección y diagnóstico de fallos en Netis BPC*

**¿Por qué una tecla de piano simboliza un minuto?**

Netis ha ideado usar teclas de piano para simbolizar el tiempo, buscando que los usuarios sientan el pulso del negocio en tiempo real de una manera que transforme el estrés y la repetición en una experiencia más relajante y estilizada. BPC convierte un lapso de tiempo en una línea compuesta por segmentos de un minuto, cada uno coloreado diferentemente para reflejar el estado del negocio. La interacción es intuitiva: deslizar el ratón sobre las teclas como si se estuviera tocando un piano, donde enfocarse en un segmento hace que se destaque. Esta meticulosidad en el diseño garantiza una precisa adquisición de información por parte de los usuarios.

Además, la decisión de configurar alertas por minuto surge de un deseo de balancear la prontitud de la alerta con su coste operativo. La experiencia con clientes del sector financiero llevó a Netis a concluir que una granularidad de alerta menor a un minuto genera un volumen excesivo de alertas redundantes, mientras que una mayor dilata la respuesta. Así, establecer la duración de un minuto por alerta optimiza este equilibrio, simbolizado por la tecla de un piano.

Sin embargo, este enfoque no cubre todas las necesidades, especialmente en sectores como el de corredurías de bolsa, donde la demanda de inmediatez es crítica. Por ejemplo, detectar un fallo puede depender de que se produzca una secuencia específica de eventos 10 veces en un segundo o que una operación exceda los 10 ms de duración. Esta necesidad dio lugar a un nuevo modelo de alerta en Netis BPC: el desencadenamiento de alertas en segundos basado en características específicas de eventos.

**Revelando los Indicadores Dorados**

En el mundo de Netis, un descubrimiento clave ha sido la correlación directa entre el volumen de transacciones y la carga sobre los servicios de aplicación; la relación entre la tasa de respuesta y la salud del sistema; cómo la tasa de éxito refleja la salud empresarial; y el inverso impacto del tiempo de respuesta de las transacciones en la experiencia del cliente. A través de una comparación meticulosa con los indicadores de Four Golden Signals, RED y USE propios del sector financiero, Netis BPC ha destilado su esencia en cuatro indicadores dorados: volumen de transacciones, tasa de respuesta, tiempo de respuesta y tasa de éxito.

Con el usuario en el corazón del diseño, el desafío fue cómo visualizar estos cuatro indicadores dorados de manera intuitiva, elevando la experiencia de usuario a nuevas alturas. Un viaje de exploración, hipótesis, experimentación y validación llevado a cabo por los expertos de producto y diseñadores de UX de Netis, culminó en la innovadora cuadrícula de cuatro cuadrantes, una primicia en la industria.

Esta cuadrícula se inspiró en una visita al Museo de Arte Moderno de Nueva York por Wizard, co-fundador y CPO de Netis. Un gráfico exhibido, que mostraba de forma clara y concisa datos geográficos y demográficos de EE.UU. mediante cuadrados, plantó la semilla de esta idea. La disposición de cuatro cuadrados en una matriz resonaba con la estructura de componentes de aplicaciones y redes, demostrando que la clave para transmitir información crítica no reside en la cantidad, sino en la precisión. Inspirados por la señalética cotidiana, desde las señales de tráfico hasta los íconos de navegación, este concepto se fusionó con la necesidad de capturar alertas rápidamente en el dinámico entorno IT, dando vida a la emblemática cuadrícula de cuatro cuadrantes.
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq0zib9UrUva92PkicX1HbHqyo8icuiaU00eVBRmcY23lm9lq2fzViaRNFP7DiaiccI3GpszkEpyQFMf4TEQw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)

*Figura 3: Inspiración: Cuadrícula de cuatro cuadrantes en el Museo de Arte Moderno de Nueva York.*

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyoVNumuLZRlcb00S7bS3dP9oicnycxmmwSAGrvAukAunwnB6HePm1FFUg/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*Figura 4: Aplicación: Cuadrícula de cuatro cuadrantes de Netis BPC.*

La esencia de BPC yace en una interpretación precisa de las necesidades del usuario, conjugada con un diseño igualmente preciso. Al presentar los indicadores de alerta con un diseño funcional y creativo, como las teclas de piano y la cuadrícula de cuatro cuadrantes, desde una óptica centrada en el usuario, Netis no solo aborda los desafíos de sus usuarios, sino que facilita su solución, logrando una armonía entre el valor funcional del producto y el valor percibido por el usuario.

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
