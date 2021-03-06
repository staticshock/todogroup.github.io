---
title: 'オープンソース コードの使用'
---

オープンソース プログラム オフィスの最も重要な責務の 1 つは、オープンソース コードを商用製品のプロプライエタリなソース コードやサードパーティ ソース コードと統合する際に、組織が確実に法的義務を果たすようにすることです。

開発者がオープンソース コードをどのように使用できるかのガイドライン、およびオープンソース コードの出所がどこで、どのようにライセンスされ、最終的にどう使用されるかを追跡する詳細なプロセスを確立する必要があります。このガイドでは、オープンソース コードを使用、リリース、配布するためのベースライン コンプライアンス プログラムについて説明します。

**内容**

1. [コードの追跡とレビューの必要性](#コードの追跡とレビューの必要性)
2. [コンプライアンスにおける役割と責任](#コンプライアンスにおける役割と責任)
3. [オープンソース コード利用のためのシンプルなポリシー](#オープンソース-コード利用のためのシンプルなポリシー)
4. [5 段階のコード レビュー プロセス](#5-段階のコード-レビュー-プロセス)
5. [バージョン 1.0 後のプロセス](#バージョン-1.0-後のプロセス)
6. [オープンソース利用申請フォーム サンプル](#オープンソース利用申請フォーム-サンプル)
7. [結論](#結論)
8. [アーキテクチャ概略図テンプレート](#アーキテクチャ概略図テンプレート)

[ガイド一覧 »](https://www.linuxfoundation.jp/resources/open-source-guides/)
[GitHub上で貢献する »](https://github.com/todogroup/guides)

#### このガイドの貢献者

**Ibrahim Haddad**
Samsung Research America社
R&amp;D 担当 VP 兼オープンソース グループ長

セクション 1

## コードの追跡とレビューの必要性

単純な話として、開発者がオープンソース コードをどこでどのように使用しているかを把握してない企業は、適用されるオープンソース ライセンスに違反する恐れがあります。これは、弁護士費用の点でも、失敗の修正に費やされるエンジニアリング時間の点でもコストがかかる結果になる可能性があります。また、オープンソースの法的義務を無視することは、オープンソース コミュニティ内で企業の評判を損なうことにもなります。

オープンソース プログラム オフィスは、オープンソースの使用、配布、リリースに関わるポリシーおよび意思決定の一元化を支援し、コードの出所と使用を追跡して、組織がコンプライアンス義務に違反しないようにします。

オープンソース プログラムは包括的なコンプライアンス プログラムを含み、法務専門家の協力を得て開発されていることが理想的です。このガイドでは、コンプライアンス プログラムの重要な側面、つまりオープンソース コードを使用、リリース、配布するためのポリシーとプロセスについて説明します。

> **「うまく設計されたオープンソース コンプライアンス プロセスは、オープンソース ライセンス条項の遵守を確実にすると同時に、企業が自身の知的財産およびサードパーティ サプライヤの知的財産を意図しない漏洩やその他の結果から保護するのにも役立ちます。」**
>
> **[Ibrahim Haddad](https://twitter.com/ibrahimatlinux) – Samsung Research America 社 R&amp;D 担当バイスプレジテント 兼
オープンソース グループ長**

オープンソース コンプライアンス プログラムを維持することにより、企業は次のようなメリットを得ることができます。

- **技術的優位性の確保** 。なぜなら、オープンソース ライセンスに準拠したソフトウェア ポートフォリオは容易に提供、テスト、アップグレード、維持できるからです。
- **重要なオープンソース コードの特定** 。複数の製品や組織の部署にまたがって使用されているコードや、オープンソース戦略にとって特に重要で有益なコードを把握できます。
- **オープンソース コンポーネントの使用に関するコストとリスクの実証** 。コードのレビューを複数回にわたって行うことによって、容易に把握できます。
- **コミュニティの信頼の構築** 。コンプライアンスに関する問題が生じた場合、このようなプログラムにより、継続して誠意をもって行動する姿勢を示すことができます。
- **起こりうる買収、売却、あるいは新製品/サービスのリリースなどへの備え** 。これは、あまり一般的ではないメリットですが、このような取引を完了させるうえで、コンプライアンス保証は必須です。
- **サプライ チェーン内の信頼関係の構築** 。OEM や下流ベンダーとのやり取りを通じて、ソフトウェア サプライ チェーン全体のコンプライアンスを強化できます。

セクション 2

## コンプライアンスにおける役割と責任

オープンソース プログラムでは、オープンソース コンプライアンスの確保を目的とする専任のオープンソース コンプライアンス チームを作る必要があります。

この中核チームは、監査チームまたはオープンソース レビュー ボード (OSRB: Open Source Review Board) とも呼ばれ、エンジニアリングと製品チームの代表者、1 人以上の法務専門家、およびコンプライアンス オフィサー (通常、オープンソース プログラム マネージャー) で構成されます。

ドキュメント製作、サプライ チェーン、経営企画、IT、ローカライゼーション、オープンソース戦略全体を監督するオープンソース執行委員会 (OSEC: Open Source Executive Committee) など、他のさまざまな部門の人々も、拡張チームのメンバーとしてオープンソース コンプライアンスの取り組みに継続的に貢献します。ただし、中核チームと異なり、拡張チームのメンバーは、OSRB から依頼された作業に基づいてパートタイム ベースでコンプライアンスに取り組むだけです。

OSRB は、オープンソース コンプライアンス戦略を策定し、企業が日常的に規則をどのように実施するかを決定する一連のプロセスを作成する責任を担っています。この戦略は、コンプライアンス確保のために何をすべきかを決定し、従業員がオープンソース ソフトウェアとどのように向き合えばよいかについて一連の統治原則を提供します。これには、オープンソースの承認、取得、使用のための正式なプロセス、およびオープンソースを含むソフトウェアまたはオープンソース ライセンスの元で許可されたたソフトウェアのリリース方法が含まれます。

セクション 3

## オープンソース コードを利用するためのシンプルなポリシー

利用ポリシーは、オープン コンプライアンス プログラムの中で不可欠なコンポーネントです。利用ポリシーに含まれる一連の規則は、オープンソース戦略文書 (既にお持ちでは？) に含まれ、誰でも入手して簡単に参照できるようになっています。

利用ポリシーは、製品を支えるすべてのソフトウェア (プロプライエタリ、サードパーティ製、オープンソースを問わず) の監査、レビュー、承認が完了することを推進するものです。また、さまざまなソフトウェア コンポーネントを使用することで生じたライセンス義務を履行するための活動を製品が顧客の元に届く前に完了するようにします。

この利用ポリシーは長い文書や複雑な文書である必要はありません。良く出来たオープンソース利用ポリシーには、次の 6 つのシンプルな規則が含まれます。

- 技術者は、オープンソース コードを製品に統合する前に OSRB から承認を得る必要があります。
- サードパーティから受け取ったソフトウェアは、監査を受けて、含まれているオープンソース コードを特定する必要があります。これにより、製品出荷前にライセンス義務を確実に履行することができます。
- すべてのソフトウェアは、すべてのプロプライエタリ ソフトウェア コンポーネントも含めて、監査およびレビューを受ける必要があります。
- 製品は、顧客が受け取る前にオープンソース ライセンス義務を履行する必要があります。
- ある製品で特定のオープンソース コンポーネントの使用が承認されても、その同じオープンソース コンポーネントを別の方面で使用することが承認されたことにはなりません。
- 変更されたコンポーネントはすべて承認プロセスを経る必要があります。

セクション 4

## 5 段階のコード レビュー プロセス

利用ポリシーを策定したら、そのポリシーを容易に適用できるプロセスを作成する必要があります。さらに、開発者がオープンソースの利用とオープンソース プロジェクトへの貢献を円滑に行えるようにする必要があります。

> **「コードのレビュー プロセスがあまりに面倒なものだと、イノベーションのスピードが落ちたり、開発者にプロセス全体を回避する格好の口実を与えることになります。」**
>
> **[Ibrahim Haddad](https://twitter.com/ibrahimatlinux) – Samsung Research America 社 R&amp;D 担当バイスプレジテント 兼
オープンソース グループ長**

プロセスではまず、対象となっているソフトウェア パッケージのソース コードをスキャンします。次に、発見された問題を特定および解決し、法的レビューとアーキテクチャ レビューを行ったのち、利用承認に関する決定を行います。

下の図は、コンプライアンス利用プロセスを単純化して図示したものです。実際には、プロセスはその性質上、かなり反復的です。以下の各段階は説明することを目的としており、企業特有の必要性やオープンソース プログラムの構成に応じて変更が必要なことに注意してください。

 ![](https://www.linuxfoundation.jp/wp-content/uploads/2017/09/OpenSourceGuideGraphics_V2_G1.png)

プロセスの各段階を順を追って説明しましょう。

### 第 1 段階：ソース コードのスキャン

ソース コードのスキャン段階では、専門のソフトウェア ツールを使用して、すべてのソース コードがスキャンされます (このようなツールは、いくつかのオープンソース ツールの他に、数多くの商用ベンダーから提供されています)。

この段階は、通常、技術者がオンラインの利用フォームを提出することで開始されます (以下のサンプルの利用フォームと利用規則を参照)。このフォームには、対象となっているオープンソース コンポーネントに関するすべての情報を含め、ソース コード リポジトリ システム内のソース コードの場所を指定します。

フォームを提出すると、JIRA、Bugzilla などのシステムにコンプライアンス チケットが自動的に作成され、決められた監査スタッフにソース コード スキャン要求が送られます。

対応する利用フォームの提出なしにオープンソース ソフトウェア コンポーネントがプラットフォームに統合されることがないようにするため、プラットフォームの定期的なフル スキャンも数週間ごとに行う必要があります。

何らかの問題が見つかった場合は、JIRA チケットが自動的に発行され、監査スタッフに割り当てられます

ソース コードのスキャンが開始される要因には、次のようなものがあります。

- 利用フォーム (通常はエンジニアリング スタッフが入力) の受信。
- 定期的にスケジュールされているプラットフォーム全体のスキャン。
このようなスキャンは、利用フォームが提出されないままソフトウェア プラットフォームに密かに入り込んだオープンソース コードを発見するのに非常に役立ちます。
- 以前に承認されたソフトウェア コンポーネントの変更。
多くの場合、技術者はまず、OSS コンポーネントの特定のバージョンを評価およびテストし、その後、新しいバージョンが利用可能になると、それを採用します。
- サードパーティ ソフトウェア プロバイダからのソース コードの入手。プロバイダがオープンソースを公開しているかどうかは問いません。
- 作成者やライセンスが不明なソース コードの Web からのダウンロード。ソース コードにオープンソース コードが組み込まれているかどうかは問いません。
- 新しいプロプライエタリ ソフトウェア コンポーネントのビルド システムへの組み込み。エンジニアリング担当者がオープンソース コードを借用し、それをプロプライエタリ ソフトウェア コンポーネントで使用したかどうかは問いません。

コードのスキャンが終了すると、スキャン ツールは、以下の情報を提供するレポートを生成します。

- 使用されている既知のソフトウェア コンポーネント。ソフトウェア部品表 (Bill Of Material: BOM) とも呼ばれます。
- 有効なライセンス、ライセンス テキスト、義務の概要
- 法務専門家による確認が必要なライセンスとの矛盾点
- ファイル目録
- ライセンスが識別されたファイル
- 依存関係
- コードの一致
- ライセンスの識別が保留されたファイル
- ライセンスの識別が保留されたファイル中のマッチしたソース コード

### ダウンロードしたオープンソース パッケージに関する注意

Web からダウンロードしたオープンソース パッケージは、元の形のまま保管しておくことが重要です。
このパッケージは、後の段階 （出荷の前）で元のパッケージと変更後のパッケージの間の差分を調べることにより、ソース コードに加えられた変更を検証し、追跡するために使用します。

サードパーティ ソフトウェア プロバイダがオープンソースを使用している場合、そのコードを製品に統合する製品チームは、使用されているオープンソースについて記述したオープンソース利用申請フォームを提出する必要があります。
サードパーティ ソフトウェア プロバイダがソース コードを提供せず、バイナリしか提供しない場合は、製品チーム、またはサードパーティ ソフトウェア プロバイダとの関係を管理するソフトウェア サプライヤ マネージャーは、提供されたソフトウェアにオープンソースが含まれていないという確証 (たとえば、スキャン レポート) を得る必要があります。

### 第 2 段階: 特定および解決

特定および解決段階では、監査チームが、スキャン ツールによってフラグが付けられたファイルまたはスニペットを検査し、解決します。

たとえば、スキャン ツールのレポートは、矛盾するライセンスや互換性のないライセンスなどの問題にフラグを付けます。問題がない場合、コンプライアンス オフィサーはコンプライアンス チケットを法的レビュー段階へ進めます。

解決すべき問題がある場合、コンプライアンス オフィサーはコンプライアンス チケット内にサブタスクを作成して、適切なエンジニアリング担当者に割り当てて解決させます。コードを修正する場合も、確認だけで済む場合もあります。サブタスクには、問題の説明、エンジニアリング担当者が実施すべき解決策の提案、完了までのタイムラインを含める必要があります。

すべての問題が解決したら、コンプライアンス オフィサーはサブタスクを閉じ、チケットを法的レビューに渡すことができます。あるいは、まずソース コードの再スキャンを指示し、新しいスキャン レポートを生成してから、以前の問題がなくなったことを確認するという方法もあります。すべての問題が解決されたと納得できたら、コンプライアンス オフィサーは、レビューと承認のためにコンプライアンス チケットを法務部門の担当者に送ります。

法的レビューに向けた準備として、オープンソース ソフトウェアに関連するすべてのライセンス情報 (COPYING、README、LICENSE ファイルなど) をコンプライアンス チケットに添付する必要があります。

### 第 3 段階: 法的レビュー

法的レビュー段階では、法務専門家 (通常、オープンソース レビュー ボード (OSRB) のメンバー) がスキャン ツールによって生成されたレポート、ソフトウェア コンポーネントのライセンス情報、エンジニアリング担当者や監査チームのメンバーがコンプライアンス チケットに残したコメントなどのレビューを行います。

法的レビュー段階に到達したコンプライアンス チケットには、既に以下が含まれています。

- ソース コード スキャン レポート、およびスキャン段階で特定されたすべての問題が解決済みであることの確認。
- チケットに添付されたライセンス情報のコピー。通常、コンプライアンス オフィサーは、ソース コード パッケージで入手できる README、COPYING、および AUTHORS ファイルをコンプライアンス チケットに添付します。ライセンス情報 (OSS コンポーネントでは、通常、COPYING ファイルまたは LICENSE ファイルで確認できます) の他に、著作権や帰属告知についても取得する必要があります。この情報は、製品ドキュメントに適切な属性の情報を提供します。
- コンプライアンス チケットに関するコンプライアンス オフィサーからのフィードバック (懸念事項、新たな疑問点など)。
- 監査チームに対するエンジニアリング担当者からのフィードバック、またはこのパッケージを内部で追跡/維持する技術者 (パッケージ所有者) からのフィードバック。

この段階の目標は、コンプライアンスに関する法務専門家の見解をまとめ、対象となっているソフトウェア コンポーネントでの使用ライセンスと公開ライセンスについて決定することです。ソフトウェア コンポーネントには複数のライセンスの下で利用できるソース コードが含まれている場合があるため、使用ライセンスと公開ライセンスは、複数ある場合があります。この段階では、次の 3 つの結果が得られる可能性があります。

**問題なし**

ライセンスに関して問題がない場合、法務専門家は、ソフトウェア コンポーネントの使用ライセンスと公開ライセンスを決定し、コンプライアンス チケットのプロセスをコンプライアンスのアーキテクチャ段階へと一歩進めます。

使用ライセンスは、受け取ったソフトウェア パッケージに対するライセンスです。公開ライセンスは、自身がライセンスしているソフトウェアパッケージを公開するライセンスです。場合によっては、使用ライセンスが再ライセンス (BSD など) を許可するパーミッシブライセンスであることがあり、その場合、企業は、自身のプロプライエタリ ライセンスの下でソフトウェアを再ライセンスする場合があります。さらに複雑な例として、ソフトウェア コンポーネントにプロプライエタリ ソース コード、ライセンス A でライセンスされたソース コード、ライセンス B の下で利用できるソース コード、ライセンス C の下で利用できるソース コードが含まれる場合を考えます。

> 法的レビュー時、法務専門家は、使用ライセンスと公開ライセンスを次のように決定する必要があります。
>
> 使用ライセンス = プロプライエタリ ライセンス + ライセンス A + ライセンス B + ライセンス C
> 公開ライセンス = ?


**問題あり**

互換性のないライセンスを持つソース コードの混在など、ライセンスに関する問題が見つかった場合、法務専門家は、それらの問題にフラグを付け、JIRA のコンプライアンス チケットを再度エンジニアリング担当者に割り当てて、コードを修正させます。

たとえば、法的レビューにより、非公開の知的財産がオープンソース コード パッケージと組み合わされていることが明らかになったとします。法務専門家は、これにフラグを付け、コンプライアンス チケットを再度エンジニアリング担当者に割り当てて、オープンソース コンポーネントからプロプライエタリ ソース コードを削除させます。エンジニアリング担当者がオープンソース コンポーネントにプロプライエタリ ソースコードを保持することを主張する場合、オープンソース執行委員会 (OSEC) は、オープンソース ライセンスの下でプロプライエタリ ソース コードを提供する必要があります。

**不明**

ライセンス情報が不明確だったり、利用できない場合は、法務専門家またはエンジニアリング スタッフ メンバーがプロジェクト管理者またはオープンソース開発者に問い合わせて、曖昧さを解決し、その特定のソフトウェア コンポーネントがどのライセンスの下にライセンスされているかを確認します。

### 第 4 段階：アーキテクチャ レビュー

アーキテクチャ レビューでは、監査チームまたはオープンソース レビュー ボードのコンプライアンス オフィサーとエンジニアリング担当者が、オープンソース、プロプライエタリ、およびサードパーティのコード間の相互関係を分析します。これは、以下に示すアーキテクチャ概略図 (以下の例を参照) を調べることで実施されます。

- オープンソース コンポーネント (そのまま使用、または変更)
- プロプライエタリ コンポーネント
- サードパーティ ソフトウェア プロバイダ起源のコンポーネント
- コンポーネントの依存関係
- 通信プロトコル
- 特に、特定のソフトウェア コンポーネントが別のオープンソース ライセンスによって管理されている場合、そのコンポーネントがやり取りするまたは依存する、その他のオープンソース パッケージ。

アーキテクチャ レビューの結果として、ライセンス義務に関する分析が得られます。ライセンス義務は、オープンソースからプロプライエタリまたはサードパーティ ソフトウェア コンポーネントに及ぶ場合があり、また、複数のオープンソース コンポーネントにまたがって及ぶ場合もあります。

コンプライアンス オフィサーが問題 (たとえば、GPL ライセンスされたコンポーネントにリンクしているプロプライエタリ ソフトウェア コンポーネント) を発見した場合、コンプライアンス オフィサーは解決のためにコンプライアンス チケットをエンジニアリング担当者に送ります。問題がない場合は、コンプライアンス オフィサーはチケットを承認プロセスの最終段階へ送ります。

### 第 5 段階：最終レビュー

最終レビューは、通常、監査チームまたはオープンソース レビュー ボード (OSRB) の対面での会議で行われ、この会議で、チームはソフトウェア コンポーネントの使用を承認または却下します。

チームの決定は、ソフトウェア コンポーネントの完全なコンプライアンス レコードに基づいて行われますが、これには以下が含まれます。

- スキャン ツールによって生成されたソース コード スキャン レポート。
- 発見された問題のリスト、どのように解決されたかの情報、および誰がこれらの問題が適切に解決されたことを検証したか。
- アーキテクチャ概略図、および対象ソフトウェア コンポーネントが他のソフトウェアコンポーネントとどのように関係するかの情報。
- コンプライアンスに関する法務専門家の意見、および使用ライセンスと公開ライセンスに関する決定。
- 組み込み環境 (C/C++) の場合、動的および静的リンケージ分析。

ほとんどの場合、最終レビューに到達したソフトウェア コンポーネントは、何らかの条件が見つからない限り (ソフトウェア コンポーネントが使用されなくなった場合など)、承認されます。承認されると、コンプライアンス オフィサーは、承認されたソフトウェア コンポーネントのライセンス義務のリストを作成して適切な部門に渡し、義務を履行させます。これには、以下が含まれます。

- 特定の OSS ソフトウェア コンポーネントのバージョン x を製品 y のバージョン z で使用することが承認されたことを反映するように、ソフトウェア目録を更新します。
- 製品またはサービスでオープンソースが使用されていることを反映するように製品ドキュメントのエンド ユーザー向け通知を更新するために、チケットをドキュメント製作チームに発行します。
- 製品出荷前に配布プロセスを開始します。

 ![](https://www.linuxfoundation.jp/wp-content/uploads/2017/09/OpenSourceGuideGraphics_V2_G3.png)
OSRB 承認後に実施される手順


コンプライアンス オフィサーは、すべてのオープンなチケットを追跡し、製品出荷時またはサービス開始時までに完了するようにします。

詳細な利用プロセスと想定されるシナリオについては、電子書籍「[企業におけるオープンソース コンプライアンス](https://www.linuxfoundation.org/open-source-management/2016/11/open-source-compliance-enterprise/)」を参照してください。

セクション 5

## バージョン 1.0 後で実行すべきこと

初期のコンプライアンス (ベースライン コンプライアンスとも呼ばれる) は、開発が開始された時点で発生し、製品の最初のバージョンのリリースまで継続します。コンプライアンス チームは、ベースライン ソフトウェアに含まれるすべてのオープンソース コードを特定し、すべてのソース コンポーネントに対して上述の 5 段階の承認プロセスを完了させます。

> **「オープンソース コンプライアンスはバージョン 1.0 で終了ではないことをしっかりと覚えておいてください。」**
>
> **[Ibrahim Haddad](https://twitter.com/ibrahimatlinux) – Samsung Research America 社 R&amp;D 担当バイスプレジテント 兼 オープンソース グループ長**

製品出荷後は、ソース コードをチェックするインクリメンタル コンプライアンス プロセスを開発する必要があります。このプロセスは、追加機能やバグ修正などを含む新しいブランチに関する開発が始まったときに開始されます。

インクリメンタル コンプライアンスは、ベースライン バージョン 1.0 に製品の機能が追加されたときにコンプライアンスを維持するためのプロセスです。

 ![](https://www.linuxfoundation.jp/wp-content/uploads/2017/09/OpenSourceGuideGraphics_V2_G4.png)
_Incremental Compliance_

インクリメンタル コンプライアンス

インクリメンタル コンプライアンスは、ベースライン コンプライアンスの確立に必要な労力と比べると、比較的手間がかかりません。
しかし、いくつかの問題が生じる可能性があります。
バージョン 1.0 とバージョン 1.1 の間で変更されたソース コードを正確に特定し、リリース間の次のような差分についてコンプライアンスを検証する必要があります。

- 新しいソフトウェア コンポーネントが導入されている可能性があります。
- 既存のソフトウェア コンポーネントの使用が中止されている可能性があります。
- 既存のソフトウェア コンポーネントが新しいバージョンにアップグレードされている可能性があります。
- ソフトウェア コンポーネントのライセンスがバージョン間で変更されている可能性があります。
- 既存のソフトウェア コンポーネントで、バグ修正や機能/アーキテクチャの変更に伴うコード変更が行われている可能性があります。

当然の疑問として、このような変更のすべてを追跡し続けるにはどうすればいいでしょうか？答えは簡単です。部品表比較ツール (BOM 比較ツール) の利用です。バージョン 1.1 の製品の BOM とバージョン 1.0 の製品の BOM がある場合、ツールを使用すると、差分を比較して以下を出力できます。

バージョン 1.1 で追加された新しいソフトウェア コンポーネントの名前

- 更新されたソフトウェア コンポーネントの名前
- 使用が中止されたソフトウェア コンポーネントの名前

この情報を入手できれば、インクリメンタル コンプライアンスの実現は比較的容易な作業になります。

- 新しいソフトウェア コンポーネントを 5 段階の利用承認プロセスに投入します。
- 変更されたソフトウェア コンポーネントのソース コードの差分を 1 行ごとに比較し、ソース コードを再度スキャンするか、以前のスキャンを信頼するかを決定します。
- 使用されなくなったソフトウェア コンポーネントを削除して、ソフトウェア レジストリを更新します。

下の図に、インクリメンタル コンプライアンス プロセスの概要を示します。各製品リリースの BOM ファイルはビルド サーバーに保存されます。BOM 比較ツールは、それぞれが異なる製品リリースに対応する 2 つの BOM ファイルを入力として使用して、差分を比較し、前述の変更リストを作成します。

この段階でコンプライアンス オフィサーは、当該リリースのすべての新しいソフトウェア コンポーネントに対して新しいコンプライアンス チケットを作成し、変更されたソース コードについてはコンプライアンス チケットを更新し、場合によってはプロセスを再度通過させ、最後に、ソフトウェア レジストリを更新することにより、使用が中止されたソフトウェア コンポーネントを承認リストから削除します。

 ![](https://www.linuxfoundation.jp/wp-content/uploads/2017/09/OpenSourceGuideGraphics_V2_G5.png)
インクリメンタル コンプライアンス プロセスの例

### オープンソース利用申請フォーム

オープンソース利用申請フォームの記入は、開発者がオープンソース ソフトウェアを企業に持ち込む際の重要なステップで、慎重に行う必要があります。

開発者は、特定のオープンソース コンポーネントを使用する承認を求めるオンライン フォームに入力します。

このフォームはいくつかの質問で構成されており、監査チームまたはオープンソース レビュー ボードは、これらの質問から得られる情報により、提案されたオープンソース コンポーネントの使用を承認するかどうかを決定することができます。

次の表に、オープンソース利用申請フォームで入力を求められる情報を示します。

通常、これらの値はプルダウン メニューから選択できるため、データを効率よく入力できます。

OSRB 利用フォームに関しては、次のようないくつかの規則があります。例えば：

- フォームは、特定の製品および特定のコンテキストでのオープンソースの利用に限定して適用されます。これはすべての製品のすべてのユースケースについて、オープンソース コンポーネントの一般的な承認を申請するためのものではありません。
- フォームは監査活動の基礎です。レビュー チームは、実装がフォームで示されている利用計画や監査およびアーキテクチャ レビューの結果と一致しているかどうかを検証するために、フォームによって提供される情報を必要とします。
- 当該オープンソース コンポーネントの利用計画が変更された場合は必ず、フォームを更新して再提出する必要があります。
- エンジニアリング担当者がオープンソースを製品ビルドに統合する前に、監査チームまたはレビュー ボードがフォームを承認する必要があります。
- オープンソース執行委員会は、ライセンス条項が特許ライセンスの付与または特許の非係争を要求しているすべてのオープンソース パッケージについて、使用を承認する必要があります。

セクション 6

## オープンソース利用申請フォーム サンプル

![](https://www.linuxfoundation.jp/wp-content/uploads/2017/09/Screen-Shot-2017-09-07-at-10.35.29-PM-768x591.png)
オープンソース利用申請フォーム サンプルのPDFは[こちら](https://github.com/todogroup/policies/blob/master/linuxfoundation/lf_compliance_approval.pdf "オープンソース利用申請フォーム サンプル")


セクション 7

## 結論

オープンソース コンプライアンスは、ソフトウェアの開発プロセスに不可欠のものです。製品でオープンソース ソフトウェアを使用しているにも関わらず、確立されたコンプライアンス プログラムがない場合は、ぜひこのガイドをきっかけとして行動を起こしてください。

本質的に、オープンソース コンプライアンスは、商品で使用されるオープンソースの取り込みと配布を管理する一連の活動で構成されます。コンプライアンスのデュー デリジェンス (適正評価) の結果、製品で使用されるすべてのオープンソース (コンポーネントおよびスニペット) が特定され、ライセンス義務の履行計画が策定されます。オープンソース コンプライアンスに関する詳細なガイドについては、無料の電子書籍「[企業におけるオープンソース コンプライアンス](https://www.linuxfoundation.org/open-source-management/2016/11/open-source-compliance-enterprise/)」(Ibrahim Haddad 著) をダウンロードしてください。

セクション 8

## アーキテクチャ概略図テンプレート

オープンソース レビュー プロセスのアーキテクチャ レビュー段階で使用されるアーキテクチャ概略図に、プラットフォーム内のさまざまなソフトウェア コンポーネント間の相互作用を示します。
以下のアーキテクチャ概略図サンプルでは、次のものが示されています。

- モジュールの依存関係
- プロプライエタリ コンポーネント
- オープンソース コンポーネント (変更されたものと元のままのもの)
- 動的リンクと静的リンク
- カーネル空間とユーザー空間
- 共有ヘッダー ファイル
- 通信プロトコル
- 特に、対象となっているソフトウェア コンポーネントが別のオープンソース ライセンスによって管理されている場合、そのコンポーネントがやりとりまたは依存するその他のオープンソース コンポーネント

 ![](https://www.linuxfoundation.jp/wp-content/uploads/2017/09/OpenSourceGuideGraphics_V2_G6.png)

このアーキテクチャ概略図のテンプレートは、C または C++ に依存する組み込み環境に適用されます。
