# Вызовы при внедрении систем мониторинга бизнес-процессов в банковские ИТ-системы

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

В ходе нашего последнего обсуждения мы выделили ключевые бизнес-показатели и правила для их отслеживания. Однако на практике возникают определенные сложности, особенно в следующих аспектах:

**1. Сбор основных данных о транзакциях**

Чтобы мониторинг транзакций был эффективным, система должна в точности собирать информацию по каждой транзакции. Это включает в себя данные о системе-инициаторе, коде транзакции, ключевых метках, системе обслуживания, обработчике, времени начала и завершения операции, серийном номере, учреждении, сумме, коде ответа системы обслуживания и собственном коде ответа. Нередко системы не способны предоставить полный набор базовых данных, например, код ответа системы обслуживания. Если первоначально система не была настроена на фиксацию этого параметра, его документирование становится проблематичным. Отсутствие таких данных делает невозможным анализ эффективности транзакций системы обслуживания. Более того, объемы данных о транзакциях, поступающих в систему мониторинга от всех систем, могут быть настолько велики, что обработка этих данных ставит под сомнение производительность системы мониторинга.

**2. Стандарты разработки для производственных систем**

Все производственные системы подлежат мониторингу, поэтому важно стандартизировать и упорядочить их разработку. К примеру, необходимо чётко следовать параметрам кода транзакции, который должен включать систему запроса, сам код транзакции, название, систему обслуживания, признаки финансовой операции, занятости и простоя среди прочего. В идеальном случае, каждый код транзакции исполняет только одну задачу. Например, использование кода A009 в нарушение стандарта, когда одна программа с этим кодом выполняет несколько функций через внутреннюю ветвистую логику, усложняет понимание её бизнес-логики.

Одной из серьёзных задач является стандартизация кодов разработки. Точность определения проблем в системе зависит от кодов ответов и записей в логах. Работая с системой центрального клиринга Банка X, был выявлен типичный код ошибки 201999, указывающий на серьезные сбои в системе. Этот код возвращался около 800 000 раз в день, снижая дневную эффективность транзакций до менее 90%. Сложности возникают и с многозначностью кодов возврата. Например, код R00001 могут использовать для разных ситуаций, от "Запись не найдена" до "Недостаточно средств", что затрудняет оценку успеха операции. Необходима стандартизация кодов возврата для повышения эффективности бизнес-мониторинга.

Важно также стандартизировать записи ошибок в логах. Без этого могут возникать ошибочные или пропущенные сигналы тревоги.

**3. Настройка множества операционных параметров**

Решив начальные задачи, специалисты должны тщательно настраивать разнообразные операционные параметры. Для мониторинга на уровне бизнеса необходимо определить настройки для каждого типа операций, включая показатели успешности бизнеса и системы, скорость роста и падения операций, отклонение от обычных значений, а также число нестандартных операций. Эти настройки помогают понять, как функционирует каждая операция. В больших системах с множеством типов операций необходима постоянная корректировка тысяч настроек. Но создав правила для этих настроек, можно автоматизировать процесс, позволяя алгоритмам адаптировать параметры в зависимости от текущей ситуации.

Создать систему мониторинга не сложно, главное — сделать её максимально полезной для бизнеса. Это позволит не только отслеживать текущее состояние, но и направлять процесс с технической поддержки на управление ИТ-операциями.

[Оригинальная статья](https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
