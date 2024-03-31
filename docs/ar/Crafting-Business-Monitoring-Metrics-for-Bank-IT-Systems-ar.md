#  وضع معايير مراقبة الأعمال لأنظمة البنوك الإلكترونية

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

مع نمو قطاع الخدمات المالية، أصبحت خدمات البنوك أكثر تعقيدًا، بالتوازي مع تنوع في أنظمة المعلومات. ظهرت تحديات في تحديد المشكلات عبر الأساليب التقنية الصرفة، مما أدى إلى زيادة الطلب على استراتيجيات مراقبة تركز على جوهر الأعمال بغض النظر عن التقنيات المستخدمة، لتسليط الضوء فقط على سير العمليات التجارية. يستعرض المؤلف، معتمدًا على خبرته الواسعة وفهمه العميق لمراقبة الأعمال، الأسس والمعايير الضرورية لمراقبة الأعمال بفاعلية.

### تطور آليات المراقبة

**المرحلة الأولى:** يدويًا، يحدد موظفو تكنولوجيا المعلومات معايير المراقبة والقواعد. تتضمن طريقة شائعة استخدام السكربتات في أنظمة مثل Zabbix، لإعداد إنذارات تنشط عند تجاوز حدود معينة، إما للأعلى أو للأسفل.

**المرحلة الثانية:** تتم توحيد معايير المراقبة والقواعد، حيث يكون على عاتق موظفي تكنولوجيا المعلومات مسؤولية الحفاظ على هذه المعايير. توسع هذه المرحلة على السابقة بتنظيم وتعميم معايير المراقبة لضمان التوافق والتجانس عبر مختلف الأنظمة.

**المرحلة الثالثة:** يقوم نظام المراقبة بنفسه بتحديد المعايير والقواعد والمعايير التشغيلية المثلى بناءً على تحليله لأدائه وأداء الأنظمة التشغيلية، مما يقلل من الحاجة إلى تدخل موظفي تكنولوجيا المعلومات.

هذه المناقشة تركز على المرحلة الثانية الأساسية، وتقترح مجموعة من المعايير العالمية للمراقبة وقواعد الإنذار المستنبطة من الخبرة التشغيلية في مجال الأعمال.

###  مقاييس وقواعد التنبيه الرئيسية لمتابعة خدمات البنوك

أنظمة المعلومات البنكية تتميز برموز المعاملات أو واجهاتها، وتبرز من خلال رموز الرجوع، حجم المعاملات، وزمن الاستجابة. يقدم هذا الدليل المقاييس الأساسية للمتابعة وقواعد الإنذار، استنادًا إلى هذه المميزات، ليكون دليلاً لمتابعة الأعمال بفعالية.

**1. نسبة نجاح المعاملات**

نسبة نجاح المعاملات هي مقياس أساسي في متابعة الأنظمة، ضرورية لتقييم صحة النظام الأساسية. المتابعة التقليدية لنسبة النجاح تعتبر المعاملة ناجحة إذا لم تواجه أخطاء نظامية، مثل مشاكل في الشبكة أو أخطاء في الوصول للملفات. لكن، غياب الأخطاء النظامية لا يضمن خلو المعاملات من المشكلات الإدارية. على سبيل المثال، المعاملة A001، التي تعني "استفسار عن المشاركات" والتي عادةً ما تشير إلى "عدم وجود سجل"، قد يدل ارتفاعها غير المعتاد على وجود مشكلة، مما يستلزم التفريق بين نسب نجاح النظام ونسب نجاح العمليات. نسبة نجاح النظام تقيم الفشل الفني، بينما نسبة نجاح الأعمال تقيس نتائج المعاملات مقارنةً برموز الرجوع المتوقعة للعمليات، ما يتيح متابعة أدق.

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/MR8pzzoKXjZp8SC2icFBL32T5nicZc8Nn56cTG16anNEMp3ug4lF03nnh9vKEyp8aHLvoe5x0Fvibo1SDTlNmydeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

الشكل 1: صفحة نسبة نجاح المعاملات

**2. نسبة نجاح معاملات نظام الخدمة**

ما يميز أنظمة البنوك هو الفصل الواضح بين الأنظمة الطالبة وأنظمة الخدمة لكل معاملة. من الضروري فهم أداء أنظمة الخدمة لتحديد المشكلات بدقة. يجب ببساطة تحديد ما إذا كانت المعاملة تستدعي نظام خدمة وما هو ذلك النظام. تحليل نسب نجاح المعاملات المتصلة بنظام خدمة محدد يكشف عن مدى موثوقيته. تقديم تحليل أكثر تفصيلاً لرموز المعاملات ضمن نظام الخدمة قد يعزز من القدرة على التشخيص.

**

**3. عندما تختفي الإشارات: إنذار بغياب المعاملات**

في عالم التداول السريع كالإعصار، هناك استراتيجية ذكية تتمثل في إعداد إنذار للأوقات التي، بشكل مفاجئ، لا تحدث فيها معاملات. تصور سوقًا مزدحمًا يهدأ فجأة. هذا الإنذار يُفعّل عند عدم حدوث معاملة محددة خلال فترة زمنية معينة في نقطة تحويل محددة، كإشارة لفقدان حدث متوقع. كأنك تتوقع مكالمة يومية من صديق وتبدأ بالقلق عند عدم وصولها. لكن، تحديد موعد هذه المكالمة (أو المعاملة) ليس بالأمر اليسير، إذ تختلف الفترات بين النشاط والهدوء، كالفرق بين الأسبوع ونهاية الأسبوع. يعتمد الأمر على رصد تدفقات المعاملات بدقة، وتحديد تلك التي كان يجب أن تتم في الوقت الحالي. نعتمد هنا على تمييز "أوقات الذروة" و"أوقات الراحة"، مثل اعتبار أيام العمل من الـ8 صباحًا حتى الـ7 مساءً كأوقات ذروة. إذا كانت المعاملة بالرمز A002 نشطة طوال اليوم، فهي تحت المراقبة المستمرة. أما A003 التي تنشط فقط خلال الذروة، فيتم إعفاؤها خلال الفترات الأقل نشاطًا. وبالنسبة لـA004، إذا كان نشاطها خافتًا طوال اليوم، فلا يتم مراقبتها.

**4. التغيرات المفاجئة: رصد أمواج المعاملات العاتية**

يوميًا، تسير المعاملات بانسيابية كمجرى نهر. لكن، عندما تظهر مشكلة في النظام، يمكن لهذا الانسياب أن يتحول إلى فيضان أو جفاف مفاجئ. القدرة على اكتشاف هذه التحولات الجذرية تعتبر حيوية. تخيل أنك تراقب معاملة A005 في ذروة فترة ما بعد الظهر. بمقارنة نشاطها بيوم عادي، نقوم بحساب التغيير. إذا كان ضمن نطاق التقلبات المعتادة (أي، 0.8 إلى 1.2 مرة المعدل الطبيعي)، فكل شيء تحت السيطرة. لكن، إذا انخفضت إلى 0.4 أو قفزت إلى 1.6، يُعد ذلك إشارة لضرورة التحرك. ولكن، هذه الطريقة قد تواجه تحديات مع المعاملات الأقل تواترًا، حيث يمكن أن تبدو التغييرات البسيطة كتقلبات كبيرة.

**5. رصد النبض: متابعة حجوم المعاملات الشاذة**

عندما ندقق في معدلات نجاح المعاملات بدقة عالية، لا سيما عند النظر إلى الأكواد الفردية، نجد أنفسنا أمام تحدي: هذه الطريقة لا تتعامل بفعالية مع المعاملات ذات التواتر النادر أو الشديد الكثافة. فكّر في الأمر: المعاملات قليلة التواتر تثير الإنذارات بطريقة مبالغ فيها، بينما تلك ذات التواتر المرتفع جداً قد تمر مرور الكرام دون لفت الانتباه إلى وجود مشكلة محتملة.

خذ لنا مثالاً المعاملة A006، التي تضم 10,000 معاملة في عشر دقائق فقط، و50 منها تصادف مشاكل. هذا يخفض معدل النجاح بنسبة ضئيلة قدرها 0.5%—رقم يبدو صغيراً ولكن يحمل في طياته مخاطر جمّة. من جهة أخرى، تُسجل المعاملة A007 معاملتين فقط في نفس الفترة الزمنية، لكن بالنظر إلى أهميتها المالية الكبيرة، فإن أي تعثر مهما كان صغيراً يستحق الانتباه. الحل يكمن في تفصيل عتبات الإنذار بعناية—أكثر من 10 أخطاء لـ A006 وخطأ واحد فقط لـ A007—معتمدين على وتيرة كل معاملة، ما يتيح تجاوز المشكلة بفعالية. ولنتصور لوحة تحكم تظهر تفصيلات كل المعاملات الفاشلة، من نقطة المعالجة إلى نظام الخدمة، لتسهيل عملية التدخل السريع عند الحاجة.

**6. ضغط الوقت: تجاوز وقت الاستجابة**

أنظمة البنوك، كأي نظام متقن، قد تواجه تباطؤاً أو تعثراً. المراقبة التقليدية قد ترصد سرعات الاستجابة، لكن ماذا عن التأخيرات التي تقع قريباً من حد التنبيه دون تجاوزه؟ خاصة في المعاملات ذات الحركة الكبيرة، حيث أن تأخيراً بسيطاً لا يعني بالضرورة مشكلة كبيرة.

الحل هنا هو متابعة المعاملات التي تخرج عن المعدل الطبيعي لأوقات الاستجابة، دورة تلو الأخرى. على سبيل المثال، إذا كانت المعاملة A008 عادة ما تنتهي خلال 300 مللي ثانية، فإن تجاوزها لـ600 مللي ثانية أو 900 قد يشير إلى وجود مشكلة. إذا حدثت ثلاث حالات مماثلة خلال دورة واحدة، فقد حان وقت إطلاق التحذير.

**7. إغلاق اليوم، الحفاظ على السجلات**

نهاية اليوم في نظام البنك، والعمليات التي تجري في هذا الوقت، تضمن بداية سلسة في اليوم التالي. المراقبة هنا واضحة: يجب أن تبدأ المعاملات المخصصة لنهاية اليوم وتنتهي في الأوقات المحددة، ويتم تأكيدها بإشارة نجاح. وبالنسبة لموازنة السجلات، فإن الثبات هو الأساس - الاختلافات الصغيرة في الأرقام تعني استمرار العمل كالمعتاد.

نختتم هنا جولتنا في إنشاء أدوات مراقبة ذكية وحساسة للأعمال. كونوا على انتظار لمزيد من الاطلاع على التحديات التكنولوجية المرتبطة بتطبيق هذه المفاهيم.

رابط المقالة الأصلية: https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com