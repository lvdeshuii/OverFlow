#  التحديات في تطبيق المراقبة الأعمال لأنظمة البنوك التكنولوجية

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

في مناقشتنا الأخيرة، سلطنا الضوء على أبرز المؤشرات الأعمال وقوانين المراقبة المتبعة. لكن، يواجه تنفيذ هذه الآليات تحديات متعددة، خاصة في المجالات الآتية:

**1. جمع معلومات المعاملات الأساسية**

لضمان مراقبة دقيقة للمعاملات، من الضروري أن يلتقط النظام بيانات كل عملية بشكل دقيق، تشمل: نظام الطلب، كود المعاملة، علامات المعاملات الرئيسية، نظام الخدمة، العقدة المعالجة، أوقات البدء والانتهاء، الرقم المسلسل، المؤسسة المالية، المبلغ، رمز الرد من نظام الخدمة، ورمز الرد من هذا النظام، إلى جانب تفاصيل أخرى. يصعب على العديد من الأنظمة تقديم هذه المعلومات بشكل كامل، خصوصاً رمز الرد من نظام الخدمة. إذا لم يكن النظام الإنتاجي مصممًا أساسًا لتسجيل هذه البيانات، يصبح توفيرها مهمة صعبة. من دون هذه المعلومات، تصبح عملية حساب نسبة نجاح معاملات نظام الخدمة غير ممكنة. علاوة على ذلك، تؤدي مشاركة بيانات التفاصيل المعاملاتية من جميع الأنظمة إلى نظام المراقبة إلى إنتاج كميات هائلة من البيانات، ما يشكل تحديًا لقدرات نظام المراقبة على المعالجة.

**2. المواصفات التطويرية للأنظمة الإنتاجية**

تخضع جميع الأنظمة الإنتاجية لقواعد المراقبة، مما يجعل توحيد وتنظيم تطوير هذه الأنظمة أمراً ضرورياً. على سبيل المثال، من الضروري الاعتماد بشكل كبير على معامل كود المعاملات. لتحقيق ذلك، ينبغي أن يضم معامل كود المعاملة مجموعة من التفاصيل مثل نظام الطلب، كود المعاملة، اسم المعاملة، نظام الخدمة، وعلامات مختلفة تشير إلى الحالة المالية وما إذا كان النظام مشغولاً أو في حالة خمول. يفضل أن يقوم كود معاملة محدد بوظيفة واحدة فقط. على سبيل المثال، يعاني كود المعاملة A009 من تجزئة وظيفية غير معيارية، مما يؤدي إلى استخدامه لحقل يشبه الفرعي للتفرع الوظيفي داخلياً. بالتالي، يمكن لكود المعاملة الواحد تنفيذ عدة وظائف تجارية، ما يجعل من الصعب وصف وظائف A009 التجارية بوضوح.

توحيد كود التطوير يمثل تحدياً كبيراً. تعتمد دقة تفعيلات التنبيهات على كود الاستجابة وتسجيل السجلات الذي تقدمه الأنظمة الإنتاجية. خلال عمل المؤلف في نظام التسوية المركزية لبنك X، واجه خطأ نظامياً كلاسيكياً يُعرف بكود 201999. هذا الخطأ يشير عادةً إلى عطل جسيم لا يمكن معالجته تقنياً. ومع ذلك، يتم إرجاع هذا الكود حوالي 800,000 مرة يومياً، مما ينتج عنه معدل نجاح للمعاملات يومياً أقل من 90%. أكواد العودة قد تُستخدم لأغراض متعددة؛ فعلى سبيل المثال، قد يعني كود العودة R00001 "لم يتم العثور على سجلات" أو "الرصيد غير كافي" وغير ذلك، ما يجعل من الصعب تحديد نجاح المعاملة. يصبح هذا الأمر أكثر تعقيداً في مراقبة الأعمال التي تصل إلى مستوى كود المعاملة، حيث أن حجم المعاملات أقل والحساسية للقيم المُرجعة أعلى. لذا، توحيد أكواد العودة يُعتبر ضرورياً بشكل عاجل.

كما يجب أن تتضمن مواصفات السجلات توحيد تسجيل سجلات الأخطاء. تعتمد دقة إنذارات مراقبة السجلات على تسجيل موحد للسجلات؛ وإلا، قد تكثر الإنذارات الكاذبة والمفقودة.

**3. تعديل العديد من المعايير التشغيلية**

بمجرد حل التحديات السابقة، يتوجب على فريق العمليات ضبط مجموعة متنوعة من المعايير التشغيلية باستمرار. للرصد بمستوى الأعمال التجارية، من الضروري تحديد إعدادات المعايير لكل كود معاملة، شاملةً معدل نجاح الأعمال، معدل نجاح النظام، نسبة الزيادة المفاجئة، نسبة الانخفاض، نسبة الانحراف عن المؤشر الأساسي، وعدد المعاملات غير الطبيعية. هذه المعايير توضح حالة تشغيل كود المعاملة. الأنظمة الكبرى تحوي عدداً هائلاً من أكواد المعاملات، مما يستلزم تعديلات مستمرة على عشرات الآلاف من المعايير التشغيلية لمجرد معايير كود المعاملة. لكن، بوضع قواعد لإعداد المعايير، يمكن تصميم خوارزمية لتعديل المعايير التشغيلية آليًا بناءً على الحالة التشغيلية الأساسية.

إنشاء نظام للرصد ليس بالأمر الصعب، إلا أن التحدي الحقيقي يكمن في ربط الرصد ارتباطاً وثيقاً بالأهداف التجارية، لتحقيق الاستفادة القصوى من قيمة الرصد التجاري، وتحفيز التحول من الصيانة الفنية إلى العمليات التقنية.

[المقال الأصلي](https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
