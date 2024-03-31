# Creando Métricas de Monitoreo Empresarial para Sistemas Bancarios de TI

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

Con la evolución del sector financiero, los servicios de banca se han vuelto más complejos, así como la diversificación en las arquitecturas de sus sistemas de información. Identificar incidencias solo con reglas de monitoreo técnico es cada vez más desafiante. Surge, entonces, la necesidad de estrategias de monitoreo que pongan el negocio en el centro, independientes de la arquitectura tecnológica, y que se enfoquen en reflejar las operaciones comerciales. Apoyándose en una rica experiencia operacional y un conocimiento profundo del monitoreo de negocios, el autor explora las métricas y reglas clave para un monitoreo empresarial efectivo.

### Evolución de las Prácticas de Monitoreo

**Primera Fase:** El equipo de operaciones de TI configura manualmente las métricas, reglas y parámetros de monitoreo. Un método común incluye el uso de scripts en sistemas de monitoreo como Zabbix para definir condiciones específicas de alerta basadas en límites, donde superar estos límites, ya sea hacia arriba o hacia abajo, activa una notificación.

**Segunda Fase:** Se estandarizan las métricas y reglas de monitoreo, quedando el personal de operaciones de TI a cargo de mantener los parámetros operativos. Esta fase mejora la anterior organizando y unificando los criterios de monitoreo para garantizar compatibilidad y coherencia en los distintos sistemas.

**Tercera Fase:** El sistema de monitoreo automáticamente ajusta las métricas, reglas y parámetros operativos óptimos, analizando su rendimiento y el de los sistemas en producción, lo que reduce significativamente la intervención manual del personal de TI.

El enfoque de esta discusión se centra en la crucial segunda fase, proponiendo un conjunto de métricas de monitoreo universales y reglas de alerta, basadas en la comprensión profunda de las operaciones y actividades empresariales.

### Métricas y Reglas de Alerta Claves para el Monitoreo de Servicios Bancarios

Los sistemas de información bancaria se definen por sus códigos de transacción o interfaces, caracterizados por códigos de retorno, volúmenes de transacción y tiempos de respuesta. Esta guía detalla las métricas de monitoreo esenciales y las reglas de alerta basándose en estas características, ofreciendo una referencia para un monitoreo empresarial efectivo.

**1. Tasa de Éxito de Transacciones**

Una métrica esencial en el monitoreo de sistemas es la tasa de éxito de transacciones, crucial para evaluar la salud básica de un sistema. El monitoreo tradicional de la tasa de éxito considera exitosa una transacción si no hay errores sistémicos (como problemas de red o errores de acceso a archivos). No obstante, la ausencia de errores sistémicos no asegura que no haya problemas en los procesos de negocio. Por ejemplo, la transacción A001, "consulta de publicaciones", que normalmente indica "registro no encontrado". Un aumento inusual en estas consultas puede señalar un problema, resaltando la importancia de diferenciar entre tasas de éxito del sistema y tasas de éxito de negocio. La tasa de éxito del sistema evalúa fallos técnicos, mientras que la tasa de éxito de negocio mide los resultados de las transacciones contra los códigos de retorno empresariales esperados, permitiendo un monitoreo más detallado y preciso.

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/MR8pzzoKXjZp8SC2icFBL32T5nicZc8Nn56cTG16anNEMp3ug4lF03nnh9vKEyp8aHLvoe5x0Fvibo1SDTlNmydeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

Figura 1: Página de Tasa de Éxito de Transacciones

**2. Tasa de Éxito en el Sistema de Servicios**

Un rasgo distintivo de los sistemas bancarios es la clara distinción entre los sistemas de llamadas y de servicios en cada transacción. Comprender el rendimiento de los sistemas de servicios es clave para identificar problemas. Basta con determinar si una transacción utiliza un sistema de servicio y cuál es. Analizar las tasas de éxito de las transacciones relacionadas con un sistema de servicio específico aporta perspectivas sobre su fiabilidad. Una mirada más detallada, evaluando los códigos de transacción individuales dentro del sistema de servicio, puede mejorar el diagnóstico.

**3. Cuando los Nodos Enmudecen: La Alarma de No-Transacción**

En el ajetreado mundo del comercio de alta frecuencia, existe un truco astuto: establecer una alarma para cuando, inesperadamente, no pasa nada. Imagina un mercado bullicioso que de repente queda en silencio. Esta alarma se activa cuando una transacción específica no se realiza dentro de un periodo determinado en un nodo específico, actuando como una alerta de "acción ausente". Es como si esperaras una llamada diaria de un amigo y empezaras a preocuparte cuando no se produce. Determinar cuándo esperar la transacción no es sencillo, ya que los periodos de actividad y calma varían, similar a los fines de semana y días laborables. Se trata de seguir el flujo de cada transacción, identificando aquellas que deberían estar ocurriendo. Así, diferenciamos entre "horas pico" y "periodos de baja actividad", por ejemplo, considerando los días laborables de 8 a.m. a 7 p.m. como los más activos. Si el código de transacción A002 está activo todo el día, se mantiene bajo vigilancia constante. Pero si A003 solo se activa en las horas pico, entonces se relaja en los momentos tranquilos. ¿Y A004? Si apenas se manifiesta a lo largo del día, se deja sin supervisión.

**4. Olas Gigantes en el Mundo de las Transacciones: Detectando Cambios Abruptos**

Cada día, las transacciones circulan fluidamente, semejante a un río en su cause. No obstante, cuando el sistema enfrenta obstáculos, este flujo puede transformarse en una avalancha o sequía. Es crucial identificar estos cambios repentinos. Imagine seguir la transacción A005 en plena hora pico. Al comparar su actividad con un día ordinario, calculamos la variación. Si se mantiene en el rango habitual de fluctuaciones (por ejemplo, de 0.8 a 1.2 veces lo normal), todo marcha bien. Pero si se reduce a 0.4 o incrementa a 1.6, es momento de activar la alarma. Sin embargo, este método enfrenta dificultades con transacciones esporádicas, donde cambios mínimos pueden parecer enormes.

**5. Escaneando el Pulso: Identificando Volumen Anormal en Transacciones**

Analizar minuciosamente las tasas de éxito de las transacciones, particularmente a nivel de códigos específicos, presenta un reto: esta metodología no es efectiva para transacciones de muy baja o altísima frecuencia. Por ejemplo, las transacciones de baja frecuencia pueden generar alarmas constantemente, mientras que las de alta frecuencia podrían no detectar señales de problemas inminentes.

Consideremos la transacción A006, con 10,000 operaciones en tan solo 10 minutos, 50 de las cuales presentan problemas. Esto solo reduce la tasa de éxito en un 0.5%—un cambio aparentemente insignificante pero potencialmente crítico. Por otro lado, A007 realiza apenas dos transacciones en el mismo periodo, pero su importancia financiera es tal que cualquier fallo es imposible de ignorar. ¿La solución? Ajustar los límites de alerta—más de 10 errores para A006, solo uno para A007—según el ritmo propio de cada transacción, solucionando eficazmente el dilema. Y visualice un panel de control que detalle cada transacción problemática, desde el nodo de procesamiento hasta el sistema de servicio, facilitando enormemente la resolución de emergencias.

**6. Contra Reloj: Demoras en el Tiempo de Respuesta**

Los sistemas bancarios, cual maquinarias engrasadas, pueden fallar, ralentizándose o incluso parándose. La supervisión convencional podría no percatarse de tasas de respuesta lentas, especialmente si los retrasos no alcanzan el umbral de alarma. En transacciones con alta demanda, un pequeño retraso no necesariamente significa una alerta roja.

Una solución es monitorear las transacciones que se desvían del tiempo de respuesta habitual, ciclo tras ciclo. Por ejemplo, si A008 normalmente finaliza en 300ms, un aumento a 600ms o 900ms podría indicar un problema. Si esto ocurre tres veces en un ciclo, es hora de alertar.

**7. Fin de Jornada: Cuadrando Cuentas**

El cierre del día en un sistema bancario, y los procesos de finalización, son cruciales para un inicio fluido al día siguiente. El monitoreo es directo: las transacciones programadas para el cierre deben empezar y finalizar en los tiempos asignados, culminando exitosamente. En cuanto a la conciliación de cuentas, la regularidad es fundamental—pequeñas variaciones son normales y no suponen problema alguno.

Con esto concluimos nuestra incursión en el desarrollo de herramientas de monitoreo empresarial inteligentes y sensitivas. Próximamente, exploraremos los retos tecnológicos asociados con la implementación de estos conceptos.

Enlace al artículo original: https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
