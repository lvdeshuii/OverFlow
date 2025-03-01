# الطريقة الأنيقة لرصد أداء الأعمال

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


في عصر تكثر فيه أدوات الرصد، كيف يمكننا التبسيط لتمكين المستخدمين من رصد أداء أعمالهم بسلاسة؟

### **1. رؤية الرصد بعيون الأعمال**

أمام تباين مقاييس وأهداف الرصد، تختلف أساليب التنبيه في منتجات رصد أداء التطبيقات، حيث تنقسم إلى نوعين: النوع الأول هو التنبيه "من الأسفل إلى الأعلى"، الذي يتم فيه تحديد نقاط التنبيه في المعلومات الأساسية مثل رؤوس الحزم، ثم تتبع استخدام التطبيق والخدمات للوصول إلى تحديد الإشكاليات في العمليات مثل أخطاء DNS أو تأخر الاستجابة. النوع الثاني، التنبيه "من الأعلى إلى الأسفل"، يرتكز على مراقبة نقاط تطبيقية وشبكية محددة، مع التركيز على المقاييس المجمعة للتنبيه من القضايا العليا إلى البيانات الأساسية. بما أن البيانات الأساسية غالبا ما تكون مضللة وصعبة التتبع، فإن التنبيهات "من الأسفل إلى الأعلى" قد تكون غير دقيقة وتستهلك وقتا طويلا. في المقابل، يعتبر التنبيه "من الأعلى إلى الأسفل" سريعًا في الإشارة إلى الأعطال، ويحظى بأهمية كبيرة في الأنظمة التي تتمحور حول الأعمال.

![002316seeudyfefdc8nldk.jpg](http://image.sciencenet.cn/album/201306/28/002316seeudyfefdc8nldk.jpg)

*الشكل 1: هرم المعرفة*

تستخدم Netis BPC استراتيجية "من الأعلى إلى الأسفل" في التقنية، مما يوفر تغطية شاملة من النهاية إلى النهاية ورؤية عميقة من العموم إلى التفاصيل. بتركيزها على الأعمال، تسهل الانتقال بين العمليات والأسواق، موحدة بين منظور الرصد وأهداف الأعمال، وتضمن بذلك دقة وقابلية تحليل إشارات التنبيه.

### **2. الفلسفة التصميمية بعين المستخدم**

تمثيل الزمن بمفاتيح البيانو وعرض المقاييس الأساسية للأعمال في شكل شبكة رباعية يشكل جوهر تصميم Netis BPC.

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyo1rZQMYRmK4Yfiambegqu7bWA3usmGboVBg1Ziav7DHAmztEEPeSWuh7Q/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*الشكل 2: تطبيق مفاتيح البيانو وشبكة الرباعية في تنبيهات وتحديد مشاكل Netis BPC*

**لماذا يُستخدم مفتاح البيانو لتمثيل دقيقة واحدة؟**

بهدف إيصال حالة أداء الأعمال بشكل فوري للمستخدمين، وجعل الأعمال المتكررة والمجهدة أكثر ارتياحًا وأناقة، قررت Netis استخدام مفاتيح البيانو كرموز للزمن. BPC تحول الزمن إلى سلسلة من اللحظات المتوالية، كل دقيقة تُمثل بمفتاح، وتُستخدم الألوان لتمييز حالات العمل المختلفة. يتم التفاعل مع هذه البيانات بواسطة الماوس، بطريقة تُحاكي عزف البيانو، حيث يُظهر التركيز على لحظة زمنية محددة تكبير للمفتاح المقابل. كل جزئية من هذا التصميم مهيأة لتمكين المستخدم من الحصول على المعلومات بكل دقة.كذلك، تم اختيار دقة التنبيه بالدقي

قة لتحقيق التوازن المثالي بين استجابة التنبيهات والتكلفة المعقولة. استنادًا إلى خبرة العديد من العملاء في القطاع المالي، وجدت Netis أن دقة التنبيه الزائدة تؤدي إلى تكرار الإشارات وزيادة عددها بشكل كبير، في حين أن التنبيهات ذات الدقة الأقل قد تفتقد للفورية وتؤدي إلى تأخيرات. لذا، استقر رأي متخصصي المنتج في Netis على جعل الدقيقة الواحدة مقياسًا للتنبيه، بمعنى أن كل مفتاح بيانو يُعادل دقيقة واحدة.

رغم أن التنبيهات بدقة الدقيقة تناسب العديد من السياقات، فإن بعض القطاعات كقطاع التداول في الأوراق المالية تتطلب دقة أعلى بكثير. في هذه الحالات، يُعتبر ظهور ميزات محددة كإشارة لوقوع مشكلة، كتعريف التنبيه لينشط عند حدوث عدة أحداث معينة خلال ثانية واحدة أو تجاوز مدة المعاملة لـ 10 مللي ثانية. وعليه، طورت Netis BPC نمطًا ثانيًا للتنبيه يستند إلى الثواني حسب خصائص الحدث.

**عرض المؤشرات الذهبية ببراعة**

اكتشف خبراء Netis العلاقة بين حجم التجارة وحمل الخدمات، وكذلك بين معدلات الاستجابة وصحة النظام والعمليات التجارية، ووجدوا أن زمن استجابة العمليات يؤثر سلبًا على تجربة العملاء. بعد دراسة معمقة ومقارنات للمؤشرات المالية الرئيسية، حددوا أربعة مؤشرات رئيسية: حجم التجارة، معدل الاستجابة، زمن الاستجابة، ومعدل النجاح كالدعائم الأساسية لـ Netis BPC.

من منظور تركيز التصميم على المستخدم، كان التحدي هو كيفية تقديم هذه المؤشرات بطريقة واضحة وجذابة. الحل جاء من خلال التعاون المكثف بين متخصصي المنتجات ومصممي تجربة المستخدم، والذي أثمر عن ابتكار شبكة الرباعيات، أولى من نوعها في الصناعة.

فكرة شبكة الرباعيات استوحيت من زيارة Wizard، أحد المؤسسين المشاركين والمدير التنفيذي للمنتج في Netis، لمتحف الفن الحديث بنيويورك. هناك، تأثر بتصميم معين يقدم معلومات جغرافية وسكانية بأسلوب واضح. تماشى هذا التصميم مع فكرة مكونات التطبيق والشبكة، مؤكدًا على الأهمية ليس في الكم، بل في القدرة على تقديم المعلومات الجوهرية بدقة. تم البناء على هذه الفكرة، مع أخذ إلهام من اللافتات الإرشادية وعلامات التوجيه، لتطوير شبكة الرباعيات التي تخدم احتياجات المستخدمين في الحصول بسرعة على المعلومات الضرورية.

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq0zib9UrUva92PkicX1HbHqyo8icuiaU00eVBRmcY23lm9lq2fzViaRNFP7DiaiccI3GpszkEpyQFMf4TEQw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)

*الشكل 3: شبكة الرباعيات الكلاسيكية بمتحف الفن الحديث بنيويورك:*

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyoVNumuLZRlcb00S7bS3dP9oicnycxmmwSAGrvAukAunwnB6HePm1FFUg/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*الشكل 4: شبكة الرباعيات الكلاسيكية في Netis BPC:*

منتج BPC هو ثمرة فهم عميق لمتطلبات المستخدمين وتصميم دقيق للمنتج. من خلال رؤية احتياجات التنبيه من منظور العميل، وتجسيد مؤشرات التنبيه في التصميم، ومن خلال تصميم مفاتيح البيانو وشبكة الرباعيات من منظور تجربة المستخدم، تنجح Netis في فهم التحديات التي يواجهها المستخدمون ومساعدتهم على استخدام المنتج بفعالية، محققة بذلك تكاملًا بين القيمة الوظيفية للمنتج والقيمة المقدمة للمستخدمين.

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
