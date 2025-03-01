
# Netis NPMが顧客のIPv6移行を支援


**Other Languages**

+ [Chinese / 中文](https://github.com/lvdeshuii/OverFlow/blob/main/docs/zh/Netis-NPM-Empowers-Customers-IPv6-Upgrade-zh.md)
+ [English](https://github.com/lvdeshuii/OverFlow/blob/main/docs/en/Netis-NPM-Empowers-Customers-IPv6-Upgrade-en.md)
+ [Spanish / español / castellano](https://github.com/lvdeshuii/OverFlow/blob/main/docs/es/Netis-NPM-Empowers-Customers-IPv6-Upgrade-es.md)
+ [Japanese / 日本語](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ja/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ja.md)
+ [German / Deutsch](https://github.com/lvdeshuii/OverFlow/blob/main/docs/de/Netis-NPM-Empowers-Customers-IPv6-Upgrade-de.md)
+ [French / français](https://github.com/lvdeshuii/OverFlow/blob/main/docs/fr/Netis-NPM-Empowers-Customers-IPv6-Upgrade-fr.md)
+ [Arabic / al arabiya / العربية](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ar/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ar.md)
+ [Portuguese (Portugal)](https://github.com/lvdeshuii/OverFlow/blob/main/docs/pt/Netis-NPM-Empowers-Customers-IPv6-Upgrade-pt.md)
+ [Russian / Русский язык](https://github.com/lvdeshuii/OverFlow/blob/main/docs/ru/Netis-NPM-Empowers-Customers-IPv6-Upgrade-ru.md)


**背景**

2021年7月、中国の中央ネット情報弁公室、国家発展改革委員会、および工業情報化部は、インターネットプロトコル第6版（IPv6）の大規模な展開と応用を加速するためのガイドラインを共同で発表しました。このガイドラインでは、**金融機関のIPv6への移行を推し進め、一般公衆に対する金融サービスのインターネットアプリケーションのIPv6サポートを継続的に強化し、IPv6の監視と運用体系を整備すること**を、IPv6の展開と応用の主要な任務として強調しています。

**事例紹介**

ある銀行は、この呼びかけに積極的に応答し、IPv6への移行作業に全力を尽くしました。2022年初頭までに、インターネットに接続されたネットワークセグメントでは、IPv4とIPv6のデュアルスタック輸送ネットワークが確立され、ウェブサイト、オンラインバンキング、モバイルバンキング、WeChatバンキングなどの一般公衆向けサービスのアプリケーションはIPv6サポートを強化しました。IPv4とIPv6のデュアルスタックネットワークの運用能力を向上させ、運用体系を整備するために、この銀行は従来のネットワーク運用の基盤に、業界をリードする全トラフィックネットワーク分析システム（Netis NPM）を導入し、インターネット関連のアプリケーションおよび重要なネットワークセグメントのトラフィックをリアルタイムで監視しました。

**価値提案**
- ネットワークトラフィックの視覚化：ネットワークの構造と内容を迅速に直感的に把握し、ネットワーク内の商業価値を深掘りするための基礎を築きます。
- サービスパスの業務視点図：従来のネットワークとアプリケーション運用の間の壁を取り払います；
- インターネットアプリケーションのIPv4とIPv6比較：IPv4とIPv6のアクセス数やパフォーマンス指標をリアルタイムで確認し、ネットワークリソースを動的に調整してアプリケーションのニーズに迅速に対応します；
- ネットワーク異常の迅速な特定と警告：障害対応時間を短縮し、ネットワークサービス品質を向上させます。

**1. Netis NPM、一体型ネットワークトラフィック管理プラットフォーム**

全トラフィックを分析するこのシステムは、成熟したネットワークミラーリング技術を使用してネットワークトラフィックをリアルタイムでネットワーク分流器（TAP）へコピーし、TAPがトラフィックを集約、タグ付け、そして異なるバックエンドプローブデバイスに配信することで、指定トラフィックを効率的に管理します。これらのプローブデバイスはネットワークトラフィックを分析し、その結果を一元化された管理プラットフォームで統合して表示します。
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdmOY8s0Zx1QLXLJAwZPCTCVweXBzFohlQVec4ZWSD75iafRL0nuxPedQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*図 1：Netis NPMの論理的配置アーキテクチャ*
インターネットの専用線出口やセキュリティ機器の前後にあるスイッチを対象に行わ

れる全トラフィック分析を通じて、IPv4とIPv6それぞれの状態をリアルタイムで把握できる独立した可視化ビューが構築されます。これにより、運用担当者はネットワークの日々の状態を迅速かつ正確に理解することが可能になります。
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdzV9UeJb7j2j2MdKqialiaWyAg8aaWdNAnxxkH5ibOpcL3mykCg1G68bPA/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*図 2：特定のIPv4専用線出口のリンクビュー-アプリケーションのパフォーマンス指標*
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdLebyqoTAYIJEwomHz2EAtVUYrickXjJ57I8POcGUIXDL3wg7TzyibD6w/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*図 3：特定のIPv4専用線出口のリンクビュー-ネットワーク負荷*
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdNd5IJZE9kThvyGBOKXnLbicb8h9yHh7gQZXriboIntLgvIXEjXSFLUrQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*図 4：特定のIPv6専用線出口のリンクビュー-ネットワーク負荷*

**2. サービスパスビジュアライゼーション（SPV）、アプリケーション視点でネットワークを見る新しい視点**

日々の運用ではネットワークとアプリケーションが別々のチームによって管理されており、問題が発生すると、それぞれが独立して対応することが故障特定と解決の速度を遅らせています。Netis NPMはこの問題に対して一石を投じ、サービスパスビジュアライゼーション（SPV）という独自の技術で、ビジネス視点からエンドツーエンドの監視体系を構築し、アプリケーションの視点からネットワークを評価します。SPVは、負荷、ネットワークパフォーマンス、アプリケーションパフォーマンス、アプリケーション可用性の四つの側面からアプリケーションのネットワーク状態を描き出し、問題が発生した際には運用担当者が迅速に原因を突き止め、障害を解消するための支援を提供します。
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrd7ibZGpAdR6x5s4JPYOrSQqgibTXTVoK53cRxPSawqYnplztwXVAiaNIFQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*図 5：Netis NPMによるビジネス視点でのサービスパスの可視化*

**3. 一画面で把握：IPv4とIPv6のネットワーク指標の対比**

インターネットの出口で、特定の銀行はNetis NPMの高度なディスプレイを利用して、IPv4とIPv6の出口専用線のネットワーク指標を比較するカスタムディスプレイを作成しました。これにより、インターネット出口の状況をリアルタイムで管理し、ユーザーエクスペリエンスを大幅に向上させています。
![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrd0icN9vsmAf2Tp1gks2V2Z3nx266D6ia02XqbTP9Jvu1srs0ve7xFa2Dw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)
*図 6：Netis NPMのディスプレイ画面*

公衆に提供される重要なビジネスシステム向けに、日次、週次、月次レポートをカスタマイズし、必要に応じて監督機関への報告を行います。

![图片](https://mmbiz.qpic.cn/mmbiz_png/o672k3fsicq3hHmITGktAGic9O31RicFkrdIngXzdI72uJ9mrwpx0LHnmpWslsam5qu2s1R5ADQDcTos941Xz4vXg/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

*図 7：重要ビジネスのための週次レポート*

Netis製品はIPv6ビジネス分析を包括的にサポートし、顧客のIPv6ビジネスが安定して運用されることを効果的に保証します。
***
At Netis, we're at the forefront of analyzing business(APM) and network performance(NPM), ensuring that over thirty billion transactions run smoothly every day. Our commitment to system and data security is paramount, and we pride ourselves on our ability to conduct real-time analysis through network traffic mirroring. This means we can get the job done without the need for any agents or disruptions to your existing operations. Based in Shanghai, China, Netis is a global software company known for its high-performance products and cost-effective solutions. Interested in what we offer? Don't hesitate to get in touch. We're excited about the possibility of working together and welcoming new partners.  
Discover more at: www.netis.com/en/  
Or drop me a line directly: Marketing@netis.com
