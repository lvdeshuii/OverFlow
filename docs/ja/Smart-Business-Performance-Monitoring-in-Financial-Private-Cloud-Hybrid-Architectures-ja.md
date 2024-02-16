# ユーザーケース：金融プライベートクラウドハイブリッドアーキテクチャにおけるインテリジェントビジネスパフォーマンスモニタリング


**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Smart-Business-Performance-Monitoring-in-Financial-Private-Cloud-Hybrid-Architectures-pt.md)



情報システム運用の核心基盤として、金融機関のITインフラはデジタル変革と技術独立の二重の挑戦に直面しています。これに対応するため、金融プライベートクラウドは金融機関にとって魅力的な選択肢となっています。最近、ある都市銀行は、金融テクノロジーを活用したビジネスモデルとしてプライベートクラウドの開発に注力しており、金融クラウド基盤設備・サービス、シナリオベースの金融イノベーション、クラウドネイティブビジネスシステム開発などの分野で先進クラウドプロバイダーと共に研究・技術開発を進めています。これにより、重要なビジネスシステムを継続的に金融プライベートクラウドに配置または移行させることができました。この取り組みは、ビジネスの迅速な対応能力、リソースコストの最適化、セキュリティ性能の向上など、多くの利点をもたらしました。しかし、運用管理にも新たな挑戦をもたらしています。

1. クラウドサーバー／コンテナクラウドを含むハイブリッドクラウドアーキテクチャを越えて、トラフィックを統一的に収集・管理する方法は？
2. ハイブリッドアーキテクチャ下ではビジネスのアクセス関係が複雑になり、モニタリングの盲点が出現しやすい。
3. クラウド環境では、障害がより隠れがちで、特定が難しくなります。
4. ハイブリッドクラウドアーキテクチャ下で、運用管理を統一し、効率を高める方法は？

これらの挑戦に直面し、Netisと当該都市銀行は協力して「金融プライベートクラウドハイブリッドアーキテクチャインテリジェントビジネスパフォーマンスモニタリングソリューション」を共同開発しました。この取り組みは、困難に立ち向かい、問題を解決するための一歩を踏み出しています。

**挑戦1：ハイブリッドクラウドのトラフィック収集の難しさ**

都市銀行が金融プライベートクラウドを展開するにつれて、クラウドサーバーやコンテナクラウドへのビジネスシステムの配置や移行が増えています。ハイブリッドクラウドのトラフィックを安全かつ効率的に収集し、クラウド外の伝統的な環境と統合して、一元管理することは、直面する最初の大きな課題です。Netisはユーザーの実際の使用シナリオに応じて、さまざまな探知器の配置（バイパス探知器とホスト探知器の組み合わせ）を提案し、ハイブリッドクラウドのトラフィック収集を効果的に実現しました。さらに、インテリジェントなトラフィック収集プラットフォーム（Cloud Probe Manager）を通じて収集器を一元管理し、クラウド外とハイブリッドクラウドから収集したトラフィックをNetisのビジネスパフォーマンス管理（BPC）へと統合しています。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eicSYpc2jHwmXaszCfF6HXqPXXba4nFMFro0zT1qjp3Vzjz9b6vuojuw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*図1：モニタリングソリューション配置図*

**挑戦2：ハイブリッドクラウド構成でのビジネスフロー整理の難点**

クラウドシステムが充実してくるにつれ、従来の環境とクラウド環境が共存する中で、ビジネスフローの整理がますます重要になっています。BPC（ビジネスパフォーマンスコントローラー）が解析する相互接続データを基に、自動的にビジネスプロセスを探索し、すべてのビジネスシステムのサービスパスをリアルタイムで視覚化することが可能になります。これにより、同じノード上のアプリケーションを賢く統合し、該当する都市銀行のクライアントがビジネスシステム内の各アクティビティのサービスノードとビジネスアプリケーションを明確に理解し、全ビジネスパスを検証し、システム内の盲点を解消し、技術部門がビジネスシステムを深く理解するのに役立ちます。 
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eOnrHmIC2n9WcbibYwPFRPQPZ96KHdQiahRjibd6tGibHPuYzUFLbjV6thQ/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*図2：SPVDによるビジネスフローの自動整理*

**挑戦3：混在クラウド構成での障害対応の複雑さ**

クラウドアーキテクチャの柔軟な連携やアプリケーションノードの動的な変更などにより、クラウド環境では障害が表面化しにくく、原因の特定がより困難になります。このため、従来のシステムに比べて、クラウド上でのビジネスシステムの障害対応は一層難易度が高くなります。適切なツールがない場合、障害の警告が遅れたり、原因の特定が不正確になったり、分析が不正確になったりして、ビジネスシステムの運用に深刻な影響を及ぼし、最終的には顧客へのサービスにも影響を与えかねません。 安定したクラウドサービスを提供するため、Netisは、頻繁に発生する代表的な障害に対応するための監視アラームプリセットを設定し、重要な金融取引の障害を監視しています。自動障害特定機能と原因分析機能を併用し、障害の影響度を正確に評価します。これにより、障害の根本原因となるノードと異常な指標を迅速に特定し、クラウドサービスのメンテナンス反応速度を従来の環境に匹敵するレベルに維持しています。 
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8eZ07v3TGgWRswlTmhibicHKBdZia0OPxTMQxwHORfmGqvnMiahsTTYYJUuQ/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8ePCCCibQxF2DIvaTDHkIeTTBOTJs7MPO6BooPryicOAkZSsEcEYhXd1rw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*図 3：インテリジェントアラームシナリオとアラームのトリガー*

**挑戦4：混在クラウド構成における運営管理の複雑さ**

この都市型商業銀行がクラウドサービスプロバイダーとの連携を深めた結果、金融専用クラウドは新たなフェーズに突入しました。これにより、混在クラウドアーキテクチャを基盤とする運営管理作業が、技術運用部門の中核的な課題に浮上しています。これに対応するため、統合型インテリジェント監視プラットフォームの開発は必須となりました。Netisのビジネスパフォーマンス管理（BPC）は、混在クラウドおよび従来型環境を一つの監視インターフェースに統合し、盲点なしで端末間、プロセス全体を通じた監視を実現します。これにより、銀行の運営管理要件を満たし、運営効率を大幅に向上させました。 
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e7XjvzyrIL4l0ibJ9MQfBgGpdOMHve9iclMQvEicNURHvY5vx8kC9agXDg/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*図 4：サービス全体のパス-クラウド内外での一体型監視*

Netisビジネスパフォーマンス管理（BPC）のマルチレイヤートラッキング機能は、顧客にとって大きなメリットを提供します。この機能により、ビジネスのシリアルナンバーを使って、クラウド内外で異なるシステム間のトラッキングが容易になり、顧客はビジネスプロセスを端から端まで一貫してモニタリングできるようになります。 
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e2FTsia5XDYUnrfSlSbyrjmAibyuG1Dxa3Fp29w1nJXbcNoh5MAVTVVyw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e9mAK5j45wGqhT1bMceXP5BV6pcDiaKHv5fa0LRTib5O3VCtW49mSfMWQ/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*図5：マルチレイヤートラッキングを使用した一貫したトランザクションモニタリング*

さらに、Netis BPCの進化したアプリケーションパフォーマンスメトリクスコンポーネントは、ビジネスシステム全体の状況をリアルタイムで把握することを可能にします。視覚的なインターフェースを通じて、運用チームが重視するさまざまな指標を効果的に表示し、パフォーマンスの監視を直感的に理解できるようにします。アプリケーションパフォーマンスの「5つの重要指標」と多様なビジネス視点を曲線図、円グラフ、棒グラフでリアルタイムに示し、アプリケーションレイヤーのビューやスナップショット、多次元の統計分析、取引の追跡などを含む豊富な機能を提供します。 
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq3aiabrR0ibCBLmsV6iae9IV8e7mMSVibHAvuc6M4icWmYcK574PkxXfXL2ibric5mkAcF1AibM1RwWLV3HdA/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)
*図 6：Netis BPCによるビジネスとパフォーマンスの洞察*
***
At Netis, we're at the forefront of analyzing business(APM) and network performance(NPM), ensuring that over thirty billion transactions run smoothly every day. Our commitment to system and data security is paramount, and we pride ourselves on our ability to conduct real-time analysis through network traffic mirroring. This means we can get the job done without the need for any agents or disruptions to your existing operations. Based in Shanghai, China, Netis is a global software company known for its high-performance products and cost-effective solutions. Interested in what we offer? Don't hesitate to get in touch. We're excited about the possibility of working together and welcoming new partners.  
Discover more at: www.netis.com/en/  
Or drop me a line directly: dennis.li@netis.com
