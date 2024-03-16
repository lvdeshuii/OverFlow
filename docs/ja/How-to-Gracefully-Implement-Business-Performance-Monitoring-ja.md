
# ビジネスパフォーマンスモニタリングを上品に実現する方法

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


現代では、多種多様なモニタリングツールが溢れています。しかし、どのようにしてこれらの複雑さを簡潔にし、ユーザーがビジネスパフォーマンスのモニタリングをスマートに実行できるようサポートするのでしょうか？

### **1. ビジネス中心のモニタリング視点**

モニタリング指標と目的の違いを考慮すると、アプリケーションパフォーマンスモニタリング製品の警告ロジックもさまざまです。これは大きく「下から上へ」のアラームと「上から下へ」のアラームの二つに分けられます。「下から上へ」のアプローチでは、データパケットのヘッダーなどの基底データにアラームポイントを設け、アプリケーションやサービスの利用状況を評価し、最終的にどのビジネスプロセスに問題があるのかを特定します（例：DNSエラーや応答遅延など）。一方、「上から下へ」のアプローチでは、ビジネスのアプリケーションノードやネットワークノードの一部を監視し、上層の集約データに基づく警告指標を設定し、トップレベルのビジネス問題から深掘りしていきます。底層データの誤報が多く、解析が困難なため、「下から上へ」のアプローチは時間も精度も要求されます。しかし、「上から下へ」のアプローチによる警告設定は、システムやサービスが障害を起こした瞬間に迅速に警告を発することができ、ビジネスを中心とした運用構造においては特に価値があります。
![002316seeudyfefdc8nldk.jpg](http://image.sciencenet.cn/album/201306/28/002316seeudyfefdc8nldk.jpg)

*図1：知識階層図*

Netis BPCは技術面で「上から下へ」のモニタリングアプローチを採用しています。エンドツーエンドのモニタリングを通じて、マクロレベルからミクロレベルまでの深い洞察力を実現し、ビジネスを中心とした視点で運用と運営の間の壁を取り除きます。これにより、モニタリングとビジネス視点が一体化され、警告指標の精度と可読性を高めることができます。

### **2. ユーザー中心のデザイン哲学**

ピアノの鍵盤を使って時間を表現し、四つのセクションでビジネスのキー指標を視覚化することは、Netis BPCのデザインの核心をなします。
![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyo1rZQMYRmK4Yfiambegqu7bWA3usmGboVBg1Ziav7DHAmztEEPeSWuh7Q/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*図2：Netis BPCにおける故障アラートと位置特定でのピアノの鍵盤と四つのセクションの活用*

**なぜピアノの鍵盤一つが1分を象徴するのでしょうか？**

ユーザーにビジネスの動きをリアルタイムで感じさせる一方で、反復的でストレスの多い作業をなるべくエレガントにリラックスして行えるように、Netisは時間を表すためにピアノの鍵盤を選びました。BPCは、異なる色でビジネス状況を示す1分間隔のタイムラインを通して時間を具体化します。利用者はピアノを弾くようにマウスで鍵盤上を動かし、情報とのインタラクションを楽しみます。特定の時間断片にマウスがフォーカスされると、該当の鍵盤は拡大表示されます。これらの細かなデザインは、ユーザーが情報を精確に取得できるよう配慮されています。

また、分単位のアラート設定は、アラートの即時性とコストのバランスを考慮して選択されました。金融クライアントの広範な実践に基づき、Netisはアラートの粒度が細かすぎると、大量で重複するアラートが増加することを発見しました。一方、粒度が粗すぎると、アラートがタイムリーでなく、遅延や見逃しが生じる可能性があります。そのため、Netisの製品専門家は、1分をアラートの粒度として採用し、これがピアノの鍵盤一つが1分を表す理由となりました。

分単位の粒度でのアラートはほとんどのシナリオに適していますが、特定の業界ではまだ要求を満たしていません。例えば、証券取引では、株取引の監視により高いリアルタイム性が求められます。ある特定の特徴が現れた瞬間をもって故障とみなす場合があり、例として、1秒以内に10回の特定イベントが連続して発生するか、1回の取引の長さが10ミリ秒を超えるなど、アラートのトリガー条件を定義できます。これにより、Netis BPCは秒単位でイベントの特徴に基づくアラートを発動する、第二のアラートモードを導入しました。

**黄金指標をどのように表示するか**

Netisの製品専門家は、取引量がアプリケーションサービスの負荷に正比例し、応答率がシステムの健全性に正比例し、成功率がビジネスの健全性に正比例し、取引応答時間が顧客体験に逆比例することを発見しました。金融業界の特徴に基づき、Four Golden Signals、RED、USE指標を横断的に比較分析した結果、取引量、応答率、応答時間、成功率をNetis BPCの四つの黄金指標として採用しました。

ユーザー中心の設計理念に立ち、ユーザーにこれらの黄金指標を明瞭かつ直感的に提示し、優れたユーザー体験を提供する方法を模索しました。その結果、製品専門家とユーザー体験デザイナーの広範な分析、仮設、実験、検証を経て、業界で初めての四つのセクションがあるグリッドデザインが誕生しました。

この四つのセクションデザインのインスピレーションは、Netisの共同創設者兼チーフプロダクトオフィサー、Wizardがニューヨークのモダンアートミュージアムを訪れた際に得られました。展示では、方形を使って当時のアメリカの地理や人口情報などを明瞭に示し、四つの方形を組み合わせたグリッドが、アプリケーションコンポーネントやネットワークの概念と見事に一致していました。これは、最重要情報の提示において、完全さよりも視聴者が重要な情報を正確に把握できるようにすることの大切さを教えてくれました。情報案内板、高速道路の案内板、交通標識など、日常生活の中で至る所に見られるこのアプローチを観察し、アラート情報を迅速に得たいというユーザーのニーズと現実のIT環境を組み合わせ、古典的なグリッドデザインを開発しました。
![图片](https://mmbiz.qpic.cn/mmbiz_jpg/o672k3fsicq0zib9UrUva92PkicX1HbHqyo8icuiaU00eVBRmcY23lm9lq2fzViaRNFP7DiaiccI3GpszkEpyQFMf4TEQw/640?wx_fmt=jpeg&wxfrom=5&wx_lazy=1&wx_co=1)

*図3：ニューヨークモダンアートミュージアムにおける古典的なグリッドデザイン：*

![图片](https://mmbiz.qpic.cn/mmbiz_gif/o672k3fsicq0zib9UrUva92PkicX1HbHqyoVNumuLZRlcb00S7bS3dP9oicnycxmmwSAGrvAukAunwnB6HePm1FFUg/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)

*図4：Netis BPCにおける古典的なグリッドデザイン：*

BPC製品は、ユーザーの要求を正確に理解し、製品を精緻にデザインするこ

とから生まれました。顧客の視点からアラートの必要性を見極め、機能デザインを通じてアラート指標を提示し、ユーザー体験の観点からピアノの鍵盤とグリッドをデザインしました。人間とサービスを中心としたこのアプローチは、Netisがソフトウェア製品を創造する過程で、ユーザーの課題を理解し、彼らが製品を使うことで、製品の機能価値とユーザー側の価値を統合するのに貢献しています。

***
Netis specializes in Business Performance Analysis (BPC) and Network Performance Monitoring (NPM). Each day, our transaction monitoring solutions ensure the smooth completion of over 30 billion transactions. We prioritize the security and autonomy of systems and data. Utilizing real-time analysis through network traffic mirroring, we ensure zero intrusion into business operations, without the need for any agent installations. Headquartered in Shanghai, China, Netis is a global software company renowned for its high-performance, cost-effective products. If you're interested in our offerings, please don't hesitate to reach out. We eagerly await your trial and partnership.  
For further details, visit: www.netis.com/en/  
Contact me via email at: dennis.li@netis.com
