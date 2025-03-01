# クラウドネットワークトラフィック収集分析白書（2022）

**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Cloud-Network-Traffic-Collection-and-Analysis-White-Paper-ru.md)

IDCの調査によれば、今後2年間で、ほとんどの企業はハイブリッドクラウドやマルチクラウドを組み合わせて、クラウドネイティブプラットフォームを構築する方針を選択する見込みです。企業のクラウドアプリケーションが拡大するにつれ、予想以上にクラウド内の東西方向のデータトラフィックが増加しており、これを正確に収集・管理することが共通の課題となっています。これに対して、Gartnerは「IT意思決定者はトラフィック収集・分析方法を見直し、ハイブリッドクラウド環境で必要とされる可視性を提供することで、将来のパフォーマンス監視と管理を実現すべきだ」と勧告しています。

Netisでは、クラウドネットワークトラフィックの可観測性分析をクラウドネイティブ及びハイブリッドクラウド環境のパフォーマンス監視と管理を改善する有効な手法の一つと考えています。高性能で、あらゆるシナリオをカバーし、アプリケーションを侵害しないトラフィック収集及び処理技術を利用して、多様な環境とアーキテクチャ下でクラウドネットワークトラフィックを可視化し、最終的にクラウドネットワークの全面的な可視性を実現することが可能です。企業がこれらの問題を解決する手助けとして、Netisは《クラウドネットワークトラフィック収集分析白書（2022）》を発表しました。この白書は、クラウド時代の挑戦、クラウドネットワークトラフィックの可観測性の価値、クラウドネットワークトラフィック収集及び可観測性分析のアーキテクチャと技術、導入ソリューション、典型的な使用例及び業界ベストプラクティスなど、6つの章から構成されており、各業界のユーザーがクラウドへの移行をスムーズに進めるための最適な解決策を提供します。

白書の主要な観点は以下の通りです：

**1. 主要な機能**

- 多様な環境対応：

  様々な環境へのサポート：主要なオペレーティングシステム、主流のチップセット、そして主要な仮想化やコンテナ化環境をサポートしています。

  マイクロサービス対応：マイクロサービスアーキテクチャのもとでの様々なデプロイメント形態や、多種多様なコンテナランタイムに対応しています。

- 広範な機能：

  データパケットの処理：データパケットの収集、フィルタリング、配信、トリミング、重複排除など、主要な機能を提供しています。

  FlowとTelemetry機能：クラウドネットワークトラフィックを可視化するためには、収集された生データパケットを前処理し、Flowログを生成し、Telemetryのサポートが必要です。

  データパケット染色：収集された生データパケットに対して、ビジネス、ネットワーク、セキュリティの各シナリオに関連した情報を注入する染色機能をサポートしています。

  TCPによるデータ転送：収集したデータパケットの信頼性の高い転送を保証するために、TCPプロトコルを用いた転送をサポートしています。

- ビジネスへの影響なし：ビジネス運用に一切の変更を加えることなく、影響を与えずに機能します。

- 自己管理機能：管理ダッシュボードの統合、収集器の稼働状態のモニタリング、自動監視、自動回復、可視化などを含む、自己管理機能を備えています。

- スケーラビリティ：需要に応じて動的に拡張・縮小することが可能です。

**2. 主要技術**

- 収集技術について：

  対応シナリオ：アプリケーションの視点からは、公共クラウドとプライベートクラウドの2つの主要なシナリオに分類されます。技術的な視点からは、VM（仮想マシン）とContainer（コンテナ）の2つの主要な技術に分けられます。

  対応能力：トラフィック収集は、様々なシナリオに対応し、それぞれの状況に応じた適切な収集手段を取るべきです。また、混在環境での層別トラフィック収集後には、一元化された管理プラットフォームが求められます。

- 多層処理/vTAP：Netisは、「クラウド内発生、クラウド内処理」のアプローチに基づき、層別収集、層別処理、層別加工、層別管理を実行し、膨大な管理対象と大量のトラフィックに対応しながら、より詳細で包括的な可観測性の構築を提唱しています。

- 基盤となる収集技術：クラウドの基盤環境は多岐に渡り複雑であるため、最大限の収集性能と効率を実現するには、異なる環境に適した収集技術を選択する必要があります。

- 独立環境への対応：クラウドネットワークのトラフィック収集と可観測性分析では、ARMアーキテクチャのCPUやカスタマイズされたオペレーティングシステムなど、自主化されたサーバー環境をサポートする必要があります。

- Flowサポート：消費シナリオに基づく細かいFlowの流れの統計能力は、ネットワーク、アプリケーション、セキュリティなどの関連するアプリケーションシナリオに適用され、クラウドネットワークコストとのバランスを取りながら、価値の問題を効果的に解決します。

- Telemetry能力：Open Telemetryを活用することで、クラウドネットワークのトラフィック消費を大幅に削減しつつ、可観測性の能力を高めることが可能です。

**3. デプロイメントの計画**

主に以下の5つのタイプがあります：全体的な収集器のデプロイメント、ホストマシンのトラフィック収集、仮想マシンのトラフィック収集、コンテナ環境でのトラフィック収集、そしてvTAPを用いたトラフィックの分流。これらの各デプロイメント方式については、白書で詳しく説明されています。

**4. 典型的な適用シナリオ**

- セキュリティシナリオ：信頼できるクラウドネットワークのトラフィック収集システムにより、クラウド内のビジネスサーバーのトラフィックを正確かつ動的に抽出することが可能になります。

  状況感知：クラウド化された作業負荷により、ビジネスの内部セキュリティ状況についての深い理解が必要とされ、これはクラウドトラフィックの正確な分析に基づくセキュリティプローブやエンジンに依存します。

  レベル保護2.0：信頼性の高いクラウドネットワークトラフィック収集を通じて、クラウド内のビジネスサーバーのトラフィックを正確かつ動的に抽出することで、クラウド上でのレベル保護2.0の基準を満たすことができます。

- BPM/APM：Netisは、BPMがネットワークトラフィックを通じて迅速にユーザー体験の問題を発見し特定でき、APMのアプリケーションコード分析能力と組み合わせることで、問題の根本原因を解析し、クラウドでの観測可能性を提供する新しいアプローチを提供しています。

- NPMD：従来の環境と異なり、クラウド上でのネットワーク監視では、AZ、VPC、サービスなどの情報を取り入れ、クラウド上でのトポロジー分析と多層的なセッションレベルの追跡能力を強化する必要があります。

  クラウド上のトポロジー分析：クラウドネットワークのトポロジーを常に把握するために、クラウドトラフィックの可視化収集とその染色技術が必要であり、これによってクラウドのダイナミックな変更に適応できます。また、トラフィックの圧縮と流量混雑の回避のために、可視化収集による流量データの出力が必要です。

  多層的セッションレベル追跡：クラウド上でのネットワーク分析では、セッションレベルの追跡能力が必要とされ、これはクラウドトラフィックの可視化収集とその染色技術による多層的追跡によって実現されます。

- データベースの運用とセキュリティ：分散データベースアーキテクチャの登場により、クラウド上のデータベースは従来の監視方法に新たな要求を提示しています。データノードとアクセスノード間の頻繁な相互訪問により、問題が発生しやすくなっています。クラウドトラフィックの可視化収集を通じて、クラウド上の分散データベースの監視を構築することは、より適切な選択です。

[**こちらからダウンロード**](https://open.netis.com/datacenter/white-papers/天旦云网流量采集分析白皮书（2022）)
***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: Marketing@netis.com
