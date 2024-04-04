# Desafíos en la implementación de monitoreo comercial para sistemas de información bancaria

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

En nuestra discusión anterior, identificamos indicadores comerciales comunes y reglas de monitoreo. Sin embargo, surgen varias dificultades durante la implementación, principalmente en las siguientes áreas:

**1. Adquisición de información de transacciones básicas**

Para monitorear efectivamente las transacciones, el sistema debe recopilar con precisión los datos de cada transacción, incluidos el sistema de solicitud, el código de transacción, las banderas de transacción importantes, el sistema de servicio, el nodo de procesamiento, las horas de inicio y finalización, el número de serie, la institución, el monto, el código de devolución del sistema de servicio y el código de devolución de este sistema, entre otros detalles. Desafortunadamente, muchos sistemas no pueden proporcionar información básica completa, como el código de devolución del sistema de servicio. Si el sistema de producción no estaba diseñado inicialmente para registrar este campo, es difícil proporcionarlo. Sin estos datos, es imposible calcular la tasa de éxito de la transacción del sistema de servicio. Además, todos los sistemas proporcionan datos detallados de transacciones al sistema de monitoreo, lo que resulta en grandes volúmenes de datos que desafían el rendimiento de procesamiento del sistema de monitoreo.

**2. Especificaciones de desarrollo para sistemas de producción**

Las reglas de monitoreo se aplican a todos los sistemas de producción, por lo que la estandarización y normalización del desarrollo del sistema de producción son esenciales. Por ejemplo, debe haber una fuerte dependencia del parámetro de código de transacción. Para lograr esto, el parámetro de código de transacción debe incluir el sistema de solicitud, el código de transacción, el nombre de la transacción, el sistema de servicio, la bandera financiera, la bandera ocupada y la bandera inactiva, entre otros detalles. Idealmente, un solo código de transacción debe realizar solo una función. Por ejemplo, el código de transacción A009 tiene una descomposición funcional no estándar, lo que hace que un programa de código de transacción atómica A009 use un campo similar a sub_type para el ramificado funcional interno. Como resultado, un solo código de transacción implementa múltiples funciones comerciales, lo que dificulta describir claramente la funcionalidad comercial de A009.

La estandarización del código de desarrollo es otro desafío importante. La precisión de los disparadores de alarmas depende del código de respuesta y el registro de registros proporcionados por el sistema de producción. Al trabajar en el sistema de compensación central del Banco X, el autor se encontró con un código de respuesta clásico: 201999-Error del sistema. Este error generalmente indica una falla grave del sistema que el programa no puede procesar desde una perspectiva técnica o determinar la causa. Sin embargo, este código de respuesta se devuelve aproximadamente 800,000 veces al día, lo que resulta en una tasa general de éxito de transacciones diarias de menos del 90%. Además, los códigos de retorno pueden tener múltiples usos. Por ejemplo, el código de retorno R00001 debería significar "No se encontró registro", pero los desarrolladores pueden personalizarlo para significar "Saldo insuficiente", "Error en el número de tarjeta xxx", "Error en la dirección" o incluso lo contrario, como "Consulta devolvió xxx registros". En tales casos, el código de retorno no puede determinar si una transacción es exitosa. Este problema se vuelve más pronunciado en el monitoreo comercial que perfora hasta el nivel del código de transacción, donde el volumen de transacciones es menor y la sensibilidad a los valores de retorno es mayor. Se necesita urgentemente la estandarización de los códigos de retorno.

Las especificaciones de registro también deben incluir la estandarización de registros de errores. El monitoreo preciso de alarmas de registro depende de registros de registro estandarizados; de lo contrario, pueden ocurrir falsas alarmas y alarmas perdidas con frecuencia.

**3. Configuración de numerosos parámetros de ejecución**

Si se abordan los desafíos anteriores, el personal de operaciones debe ajustar continuamente varios parámetros de ejecución. El monitoreo comercial requiere configuraciones de parámetros para cada código de transacción, incluidos la tasa de éxito comercial, la tasa de éxito del sistema, la relación de aumento, la relación de caída, la relación de desviación de la línea base del indicador y el número de transacciones anormales. Estos parámetros describen la situación de ejecución del código de transacción. Los sistemas más grandes tienen muchos códigos de transacción, lo que requiere un ajuste a largo plazo de decenas de miles de parámetros de ejecución para el parámetro de código de transacción solo. Sin embargo, si se establecen reglas de configuración de parámetros, se puede diseñar un algoritmo para modificar automáticamente los parámetros de ejecución según la situación de ejecución de la línea base.

Diseñar un sistema de monitoreo no es difícil, pero el desafío radica en hacer que el monitoreo sea más relevante para el negocio, explotar plenamente el valor del monitoreo comercial y conducir la transformación del mantenimiento de TI a las operaciones de TI.

[Artículo original](https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
