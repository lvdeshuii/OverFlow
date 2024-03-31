# 銀行ITシステム向けビジネスモニタリング指標の構築

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

金融業界が成長し続ける中、銀行のサービスや情報システムの構成が複雑化しています。技術だけに頼ったモニタリングでは問題の特定が難しくなっており、ビジネスの動きを直接反映する技術非依存のモニタリング戦略への需要が高まっています。運用の実績とビジネスモニタリングへの深い理解に基づき、著者はビジネスモニタリングに不可欠な指標とルールに焦点を当てています。

### モニタリングの進化

**初期段階:** IT運用チームがモニタリングの指標、ルール、パラメータを手動で設定します。よくある方法は、Zabbixのようなシステムでスクリプトを設定し、特定の閾値を基準にアラートを発することです。

**標準化段階:** モニタリングの指標とルールが標準化され、IT運用チームが運用パラメータの管理を行います。この段階では、様々なシステム間での互換性と一貫性を確保するために、モニタリングの基準を組織化し、標準化します。

**自動化段階:** モニタリングシステムが自動的に指標、ルール、最適な運用パラメータを決定します。これは、システム自体と生産システムのパフォーマンス分析に基づき、ITスタッフの手動介入を減らします。

この議論では、ビジネス活動への洞察から導かれた汎用的なモニタリング指標とアラートルールの設定を、特に重要な標準化段階に焦点を当てて提案しています。

### 銀行サービス監視のためのキーメトリクスとアラートルール

銀行情報システムは、そのトランザクションコードやインターフェースによって定義され、リターンコード、トランザクション量、応答時間といった特徴があります。本ガイドでは、これらの特性に基づく重要な監視指標とアラートルールを紹介し、効果的なビジネス監視のための参考情報を提供します。

**1. トランザクション成功率**

システム監視における基本となるメトリクスはトランザクションの成功率で、システムの基本的な健康状態を評価するのに不可欠です。従来の成功率の監視では、システム的なエラー（例えば、ネットワークの問題やファイルアクセスのエラーなど）がない場合にトランザクションを成功とみなします。しかし、システムエラーがないからといって、ビジネスプロセスの問題がないとは限りません。例えば、トランザクションA001「クエリポスティング」は通常「レコード未発見」を示しますが、ポスティングの異常な増加は潜在的な問題を示唆します。これは、システムの成功率とビジネスの成功率を区別する必要があることを示しています。システムの成功率は技術的な失敗を評価し、ビジネスの成功率は期待されるビジネスリターンコードとのトランザクション結果を測定します。この細かい視点により、単純な成功率を超え、各トランザクションに対する特定の期待結果を考慮に入れたより正確な監視が可能になります。

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/MR8pzzoKXjZp8SC2icFBL32T5nicZc8Nn56cTG16anNEMp3ug4lF03nnh9vKEyp8aHLvoe5x0Fvibo1SDTlNmydeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

図1: トランザクション成功率ページ

**2. サービスシステムトランザクション成功率**

銀行システムの特徴的な点は、各トランザクションに対して呼び出しシステムとサービスシステムがはっきりと区別されていることです。サービスシステムのパフォーマンスを把握することは、問題の特定に不可欠です。トランザクションがどのサービスシステムを呼び出しているかを単に特定することから始めます。特定のサービスシステムに関連するトランザクションの成功率を分析することで、その信頼性に関する洞察が得られます。サービスシステム内の個々のトランザクションコードを評価することで、さらに詳細な診断が可能になります。

**3. ノードが静かになるとき：トランザクションなしアラーム**

高頻度取引の世界では、驚くべきことに何も起こらない時に警告を設定する賢い方法があります。賑わう市場が突然静まり返ることを想像してみてください。このアラームは、特定のノードで設定された期間内に特定のトランザクションが発生しない場合に鳴ります。これは「行動の欠如」警告のようなものです。毎日友人からの連絡を期待していて、それが来ないと心配するようなものです。しかし、いつその連絡（またはトランザクション）を期待するかを把握するのは簡単ではありません。忙しい時間帯と静かな時間帯は、週末と平日のように異なります。すべてのトランザクションの流れを追跡し、今起こるべきものを見つけ出すことが重要です。こうして、「ラッシュアワー」と「オフタイム」の概念が導入されます。例えば、平日の午前8時から午後7時をピークタイムとして設定します。トランザクションコードA002が一日中活発な場合、休むことなく監視されます。しかし、A003がラッシュ時間にのみ活動する場合、静かな時間には休息が与えられます。そして、A004は？もし一日中ほとんど活動がなければ、監視されずに放置されます。

**4. 突然の変動：取引量の津波を検知**

取引は通常、川の流れのように円滑に進みます。しかし、システムに問題が発生すると、この流れは洪水か干ばつに変わることがあります。こうした急激な変化を素早く察知することが非常に重要です。例えば、午後の忙しい時間に取引A005の動きを追跡し、「通常の」日と比較して変化を計測します。変化が通常の範囲（0.8から1.2倍程度）内であれば問題ありませんが、0.4に落ち込んだり1.6に急上昇したりすると、警報を発する必要があります。ただし、頻度が低い取引では、小さな変動でも大きな波のように感じられることがあります。

**5. 脈拍のモニタリング：異常な取引量の追跡**

個々のコードのレベルで取引の成功率を詳細に調べると、低頻度または非常に高頻度の取引では、この方法がうまく機能しないことがわかります。低頻度の取引では警報が頻繁に発生し、超高頻度の取引では問題が見逃されがちです。

例えば、10分間に10,000回の取引を行うA006は、50回の障害で成功率が0.5%低下するかもしれませんが、これは表面上小さな変動ですが、重大な問題を引き起こす可能性があります。一方、同じ期間に2回の取引を行うA007では、たとえ1回の障害でも重大な影響を与える可能性があります。解決策として、各取引の特性に応じて警告の閾値を設定します—A006は10回以上の問題で、A007は1回の問題で警告します。また、処理ノードからサービスシステムまで、問題のあった取引の詳細を一覧表示するダッシュボードがあれば、緊急時の問題解決が格段に容易になります。

**6. 時間の制約：予想を超える応答時間の遅延**

銀行システムは、いかによく機能する機械であっても、遅れたり、停止することがあります。従来の監視では応答速度に注目しますが、アラームの基準値ギリギリでの遅延はどうでしょうか？特に高トラフィックの取引では、わずかな遅延も必ずしも問題を示すわけではありません。

解決策としては、通常から逸脱する応答時間を持つ取引に注目し、サイクルごとにチェックしましょう。例えば、A008が通常300msで処理される場合、600msや900msまで時間がかかると問題があるかもしれません。一つのサイクルでこのような例外が3回発生したら、警告を発する時期かもしれません。

**7. 終日処理と帳簿管理**

銀行システムの日の終わりの幕引きとしての終日プロセスは、翌朝のスムーズなスタートのための鍵です。監視は簡単です：日末に設定された取引は、決められた時間内に開始し、成功を示すシグナルで終了する必要があります。そして、帳簿を正確に保つことについては、一貫性が最も重要です。わずかな数値の不一致は、通常業務を続けるための合図です。

これで、賢く敏感なビジネス監視ツールを構築する探求を終えます。これらのコンセプトを実生活に持ち込む際の技術的な挑戦に焦点を当てた次回の内容をお楽しみに。

原文のリンク: https://mp.weixin.qq.com/s/qlvqPsz2fX0AyxMdXdVzxw

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
