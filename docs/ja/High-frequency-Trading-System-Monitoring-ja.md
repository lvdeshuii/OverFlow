# 高頻度取引システムの監視

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/High-frequency-Trading-System-Monitoring-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/High-frequency-Trading-System-Monitoring-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/High-frequency-Trading-System-Monitoring-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/High-frequency-Trading-System-Monitoring-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/High-frequency-Trading-System-Monitoring-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/High-frequency-Trading-System-Monitoring-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/High-frequency-Trading-System-Monitoring-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/High-frequency-Trading-System-Monitoring-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/High-frequency-Trading-System-Monitoring-ru.md)

取引システムが進化する過程で、トレーダーは常に速さを追求してきました。量的取引が普及するにつれて、トレーダーからはさらに速いシステムへの要望が強まっています。

### 高頻度取引システムが直面する監視の課題

高頻度取引システムの登場により、アプリケーション運用管理の難易度が一層増し、運用監視ツールは監視の精度、製品性能、そして安定性に対して非常に高い要求に応える必要があります。

- **ナノ秒レベルの監視精度が求められる**：高頻度取引では、注文を迅速に処理し、市場情報を低遅延で反映する必要があり、通常、取引処理速度はマイクロ秒レベルで保たれています。しかし、従来の監視ツールでは、このようなマイクロ秒やナノ秒レベルの測定精度を実現することが難しく、高頻度取引システムの速度要求に応えることができません。
- **専門的なプロトコル解析の必要性**：従来の監視ツールでは、多岐にわたるビジネスシステムの解析能力に欠け、主要な高頻度取引システムを自動で解析することができません。
- **システム性能への影響を最小限に抑える**：ログやコード挿入などの従来型ツールは、システム性能を低下させ、安定性に悪影響を及ぼします。これらのツールでは、高頻度取引システムの精密な監視が難しいです。

このため、運用管理部門は、高い精度、性能、そして強力な解析能力を備えた監視ツールを使用することが求められます。これにより、障害対応の難しさ、原因特定の困難さ、分析の複雑さなど、運用上の課題を解決し、高頻度取引システムが最高速度で稼働できるよう保証します。

### BPC高頻度取引版の新時代へ

長年にわたる信頼と実績を誇るNetis BPCは、証券業界におけるビジネスの継続性を保証し続けています。バイパス配置によるネットワークトラフィックの収集から、四つの重要指標、インテリジェントアラート、取引の追跡、多角的な分析機能まで、Netis BPCは業界のニーズに応えてきました。今回、ナノ秒単位の監視能力を備えた「BPC高頻度取引版」をリリースし、高頻度取引システムへの全面的なサポートを強化します。

**先進のナノ秒タイムスタンプ技術**

高頻度取引では、マイクロ秒単位で測定される遅延時間が重要な役割を担います。これに対応するため、「BPC高頻度取引版」は、マイクロ秒レベルからナノ秒レベルへの大幅な精度向上を実現。この高精度なタイムスタンプにより、取引の各ステージの所要時間や全体の取引時間を素早く算出し、遅延が発生した際には迅速に警告を発します。さらに、遅延と処理能力のバランスを示し、問題の原因を特定する機能も備えています。

**ビジネスを中心とした監視の視点**

「BPC高頻度取引版」は、ビジネスプロセスに沿った監視を実現します。具体的には、サービスのフローチャートを用いてシステム間の繋がりを分析し、コアなミドルウェアや取引所のコンポーネントの状態をリアルタイムでチェックします。取引量や応答速度など、重要な指標を提供し、運用担当者が迅速に問題を解決できるよう支援します。

![%E6%99%BA%E8%83%BD%E6%95%85%E9%9A%9C%E5%91%8A%E8%AD%A6-scaled.jpg](https://www.netis.com/wp-content/uploads/2022/05/%E6%99%BA%E8%83%BD%E6%95%85%E9%9A%9C%E5%91%8A%E8%AD%A6-scaled.jpg)

*図 1：サービスパスの概観*

**多段取引追跡機能**

この多段取引追跡機能により、一つの注文を取引プロセス全体で、重要な各ステップにおけるデータと賢くリンクさせることができます。ボタン一つで、注文が各ステップでどれだけの時間を要しているかなど、具体的な情況を一目で分析することが可能になります。

「BPC高頻度取引版」は、高頻度の取引注文のリクエスト、注文の内部からの返答、取引所からの応答メッセージなどをすべて、迅速に解析します。高性能ネットワークカードによる高精度タイムスタンプを使用して、取引プロセス全体の所要時間（注文リクエストから取引所の応答まで）やミドルウェア処理時間（注文リクエストと注文の内部返答）などの指標を算出し、運用保守スタッフが詳細な分析を行えるよう支援します。さらに、実際の運用保守シーンに合わせて、証券の秒単位監視ビューを柔軟に構築できます。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq19VyEficPiaZ2k9iaJhBWWYicHSHVWKyCm89sMW99ER72MfE1GBUsmQob7o6hmpjQvUD3BrDsFV33zlQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

*図 2：多段取引追跡機能*

**主要な高頻度取引システムの全面サポートと迅速な監視の実現**

Netisのトップレベルのデコード技術を基盤に、「BPC高頻度取引版」は、恒生、華銳、頂点などの主要な高頻度取引システムに完全対応しており、上海証券取引所や深セン証券取引所のグループブロードキャスト、プライベートマーケットデータ配信システムなど、取引所の市場システムを幅広くサポートしています。BPCは、柔軟なカスタムデコードを提供し、サードパーティのプロトコルデコードの要件に迅速に対応することが可能です。

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
