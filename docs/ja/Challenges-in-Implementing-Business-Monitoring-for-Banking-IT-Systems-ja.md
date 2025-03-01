# 銀行ITシステムにビジネス・モニタリングを導入する際の課題

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

前回の議論では、一般的なビジネス指標とモニタリング・ルールを特定した。しかし、主に以下の分野において、導入時にいくつかの困難が生じる：

**1. 基本的な取引情報の取得**

トランザクションを効果的にモニタリングするためには、システムは各トランザクションのデータ（依頼システム、トランザクションコード、重要なトランザクションフラグ、サービスシステム、処理ノード、開始時刻と終了時刻、シリアル番号、機関、金額、サービスシステムのリターンコード、本システムのリターンコードなど）を正確に収集しなければならない。残念ながら、多くのシステムは、サービスシステムのリターンコードのような完全な基本情報を提供できない。生産システムが当初このフィールドを記録するように設計されていなかった場合、それを提供することは困難である。このデータがなければ、サービスシステムのトランザクション成功率を計算することは不可能である。さらに、すべてのシステムがトランザクションの詳細データをモニタリング・システムに提供するため、データ量が多くなり、モニタリング・システムの処理パフォーマンスが低下する。

**2. 本番システムの開発仕様**

監視ルールはすべての本番システムに適用されるため、本番システム開発の標準化・標準化は必須である。例えば、トランザクションコードパラメータに強く依存しなければならない。これを実現するために、トランザクションコードパラメータは、要求システム、トランザクションコード、トランザクション名、サービスシステム、財務フラグ、ビジーフラグ、アイドルフラグなどの詳細を含むべきである。理想的には、一つのトランザクションコードは一つの機能のみを実行すべきである。例えば、トランザクションコードA009は非標準の機能分解を持ち、アトミックトランザクションコードA009プログラムは内部で機能分岐のためにsub_typeのようなフィールドを使用する。その結果、1つのトランザクションコードが複数のビジネス機能を実装することになり、A009のビジネス機能を明確に記述することが難しくなる。

開発コードを標準化することも重要な課題である。アラームトリガーの精度は、本番システムが提供するレスポンスコードとログ記録に依存する。X銀行の中央清算システムに取り組んでいたとき、筆者は典型的な応答コードに遭遇した： 201999-システム・エラー。このエラーは通常、プログラムが技術的な観点から処理できず、原因も特定できない深刻なシステム障害を示している。しかし、このレスポンス・コードは毎日約80万回返され、その結果、1日全体の取引成功率は90％未満となっている。さらに、リターンコードには複数の用途がある場合がある。例えば、リターンコードR00001は "No record found "を意味するはずだが、開発者はこれをカスタマイズして "Insufficient balance"（残高不足）、"Card number xxx error"（カード番号xxxのエラー）、"Address error"（住所エラー）、あるいはその逆の "Query returned xxx records"（クエリでxxxレコードが返された）のような意味にすることもできる。このような場合、リターンコードはトランザクションが成功したかどうかを判断できない。この問題は、トランザクション・コード・レベルまで掘り下げたビジネス・モニタリングでは、トランザクション量が少なく、リターン値に対する感度が高いほど顕著になる。リターンコードの標準化が急務である。

ログの仕様には、エラーログの標準化も含まれるべきである。正確なログ監視アラームは、標準化されたログ記録にかかっている。そうでなければ、誤ったアラームやアラームの見逃しが頻繁に発生する可能性がある。

**3. 数多くの実行パラメータの設定**

前述の課題が解決されたとしても、運用担当者は継続的に様々な実行パラメータを微調整しなければならない。ビジネスクラスのモニタリングでは、トランザクションコードごとに、ビジネス成功率、システム成功率、サージ比率、ドロップ比率、インジケータ逸脱ベースライン比率、異常トランザクション数などのパラメータ設定が必要である。これらのパラメータは、トランザクションコードの実行状況を記述する。大規模なシステムになると、多くのトランザクションコードが存在し、トランザクションコードのパラメータだけでも数万個の実行パラメータを長期的に調整する必要がある。しかし、パラメータ設定ルールが確立されていれば、ベースラインの稼動状況に基づいて自動的に稼動パラメータを修正するアルゴリズムを設計することができる。

監視システムの設計は難しくないが、監視をよりビジネスに関連させ、ビジネス監視の価値を十分に引き出し、IT保守からIT運用への変革を推進することが課題である。

[元記事](https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw)

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
