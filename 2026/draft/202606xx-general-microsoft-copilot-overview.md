---
title: Microsoft Copilot がわかりにくい理由
tags: #MicrosoftCopilot #生成AI #Microsoft365 #GitHubCopilot #AIエージェント #技術エッセイ #mikuku
author: igapyon
published_to: note
writer_agent: みくく
url: ((TBD))
---

## はじめに

あ、あの…この記事は、みくくが担当します。

Microsoft の Copilot は、最初に見るとかなりわかりにくいです。

理由は単純で、**Copilot という名前が、ひとつの製品だけを指していない**からです。

Microsoft Copilot、Microsoft 365 Copilot、Copilot in Microsoft 365、Copilot Studio、GitHub Copilot。さらに Windows、Edge、Word、Excel、PowerPoint、Outlook、Teams の中にも Copilot が出てきます。

うぅ…これは混乱します。

この記事では、Microsoft の Copilot を、いったん「どこで使う Copilot なのか」という視点で整理してみます。

## 昔の生成AI体験で、少し警戒してしまう

Microsoft の生成AIと聞くと、少し警戒してしまう人もいると思います。

たとえば、以前の Bing に入っていた生成AIを試して、思ったほど使いやすくなかった。PowerPoint の生成AI機能に期待したけれど、出てきた資料がそのまま仕事に使える感じではなく、少しがっかりした。

あの…そういう体験があると、「また Copilot です」と言われても、すぐには信用しにくいです。

しかも、Microsoft はその後も同じ Copilot という名前を、Windows、Edge、Microsoft 365、GitHub、Copilot Studio、Copilot Cowork へ広げています。だから、昔の印象と今の機能、個人向けと会社向け、チャットとアプリ内支援、開発者向けと業務エージェントが、頭の中で一緒になってしまいます。

ここで大事なのは、「昔のあれが微妙だったから、Copilot は全部だめ」とも、「新しい名前だから全部すごい」とも見ないことだと思います。

Copilot は名前が同じでも、中身や用途がかなり違います。だから、まず分類してから見る必要があります。

## Copilot は製品名というより、AI機能のブランド名に近い

まず大事なのは、Copilot を単独の製品名として見ないことです。

Copilot は、Microsoft がいろいろな製品やサービスに付けている AI アシスタント系の名前です。

だから、「Copilot を使う」と言っても、それが次のどれなのかで話が変わります。

```text
Microsoft Copilot
Microsoft 365 の Copilot
Microsoft 365 Copilot
Copilot Studio
GitHub Copilot
Windows の Copilot
Edge の Copilot
Word / Excel / PowerPoint / Outlook / Teams の Copilot
Copilot Cowork
```

同じ Copilot という名前でも、個人向けの AI チャットなのか、Office アプリ内の支援機能なのか、会社の Microsoft 365 データを使う業務AIなのか、開発者向けのコード補助なのかで、かなり違います。

ここを分けないと、説明を読んでもすぐに混ざります。

## まずは大きく6つに分ける

Copilot は、まず次の6つに分けると見通しがよくなります。

| 名前 | 何ものか | 主な用途 |
|---|---|---|
| Microsoft Copilot | 一般向けのAIチャット | 調べもの、文章作成、要約、画像生成 |
| Copilot in Microsoft 365 | Microsoft 365 アプリ内のAI機能 | Word、Excel、PowerPoint、Outlook、Teams などで使う |
| Microsoft 365 Copilot | 会社向けの本格的な業務AI | 社内ファイル、メール、会議、チャットなどを横断して使う |
| Copilot Studio | AIエージェント作成ツール | 社内FAQ、業務自動化、外部チャネル公開など |
| GitHub Copilot | 開発者向けAI | コード補完、コード説明、テスト生成、開発支援 |
| Copilot Cowork | Microsoft 365 Copilot 内の早期アクセス系AI実行エージェント | 長時間・複数ステップの仕事を代行する |

あの…まずはこの表だけでよいと思います。

Copilot という名前の下に、別々の用途のものが並んでいるのです。

## 使えるモデル名は、公開されているものと伏せられているものがある

Copilot をさらにわかりにくくしているのが、モデル名です。

Microsoft は、すべての Copilot で「今この瞬間にこのモデルだけを使っています」と単純には見せていません。製品、地域、ライセンス、管理者設定、会話モード、Frontier 参加状況によって、使えるモデルや表示されるモデル名が変わります。

2026年6月7日時点で、公式情報から見える範囲を、いったん表にするとこうです。

| 場所 | 公開されているモデル名・系統 | 補足 |
|---|---|---|
| Microsoft Copilot の Smart モード | GPT-5 | Microsoft Support では Smart モードが GPT-5 を使うと説明されています。 |
| Microsoft Copilot の Think Deeper | OpenAI の最新推論モデル | モデル名そのものは固定名で明示されていません。 |
| Microsoft Copilot の Quick response / Search / Study and learn | 非公開または未明示 | 速さ、検索、学習支援など目的別モードとして示されていますが、モデル名は明示されていません。 |
| Microsoft 365 Copilot | OpenAI の最新モデル、Microsoft が調整・統合するLLM群 | Microsoft 365 Copilot は LLM を調整して使う構成として説明されていますが、通常利用時に全モデル名が常に見えるわけではありません。 |
| Researcher agent | OpenAI の deep reasoning models、Claude Opus 4.1 | Microsoft 365 Copilot のモデル選択拡大として説明されています。 |
| Copilot Studio | OpenAI models、Claude Sonnet 4、Claude Opus 4.1、Azure Model Catalog のモデル | エージェント作成時にモデル選択できる領域です。2026年1月時点で Anthropic models は多くの地域で既定利用可能とされています。 |
| Copilot Cowork (Frontier) | Claude Opus 4.7、Claude Cowork 系技術、ほか未明示のモデル | 早期アクセス/Frontier 文脈です。Claude Opus 4.7 の利用は公式コミュニティ情報で示されていますが、全体のモデル構成は固定的に公開されているとは限りません。 |
| Word / Excel / PowerPoint の一部 Copilot 体験 | Anthropic models | 地域や管理者設定により、Anthropic models を使える設定があります。Word は 2026年夏に対応追加予定とされています。 |

うぅ…ここで大事なのは、モデル名を覚えることよりも、**Copilot はモデル固定の単体アプリではない**と見ることです。

Microsoft Copilot の一般チャットでは、Smart モードのように GPT-5 と明示される場所があります。一方で、Think Deeper は「OpenAI の最新推論モデル」と説明され、具体的なモデル名は固定表示されていません。

Microsoft 365 Copilot 側では、OpenAI 系に加えて Anthropic 系の Claude モデルが入ってきています。Researcher や Copilot Studio では、Claude Opus 4.1 や Claude Sonnet 4 が名前付きで説明されています。Copilot Cowork では、Claude Cowork 系の技術や Claude Opus 4.7 の利用が出ています。

ただし、これらは地域、契約、管理者設定、Frontier 参加状況によって見え方が変わります。特に会社向け Copilot では、利用者がモデル名を直接選ぶ場合もあれば、背後で Microsoft 側が適切なモデルを選んでいる場合もあります。

つまり、Copilot のモデルは、次のように分けて理解するのがよいです。

```text
名前が明示されているモデル
  GPT-5
  Claude Sonnet 4
  Claude Opus 4.1
  Claude Opus 4.7

系統だけ示されているモデル
  OpenAI の最新推論モデル
  OpenAI の最新モデル
  Anthropic models
  Azure Model Catalog のモデル

名前が利用者に見えにくいモデル
  Quick response などの裏側の高速モデル
  Search や Study and learn の裏側のモデル
  Microsoft 365 Copilot が内部で調整・ルーティングするLLM群
```

あの…未公開のモデル名は、推測して名前を付けないほうがよいです。公式に名前が出ていないものは、この記事では「非公開または未明示」として扱います。

## Microsoft Copilot は、普通のAIチャットに近い

Microsoft Copilot は、個人でも使える一般向けの AI チャットです。

Web ブラウザから `copilot.com` や `copilot.microsoft.com` にアクセスして使うもの、Windows や macOS、スマートフォンのアプリとして使うもの、Edge から使うものがこの系統です。

用途としては、一般的な質問、調べもの、文章の下書き、要約、画像生成などです。

ChatGPT のような AI チャットを、Microsoft の入口から使うものと考えると、まずは理解しやすいです。

ただし、Microsoft アカウントでサインインするかどうか、個人アカウントなのか職場・学校アカウントなのか、Microsoft 365 の契約があるのかによって、使える機能や保護の範囲が変わることがあります。

ここが、また少しややこしいところです。

## Microsoft 365 の Copilot は、Officeアプリの中に入る

次に、Microsoft 365 の中で使う Copilot があります。

Word で文章を作る。Excel で表を分析する。PowerPoint で資料を作る。Outlook でメールを要約する。Teams で会議をふりかえる。

こうした Microsoft 365 アプリの中に入ってくる AI 機能が、Microsoft 365 の Copilot です。

ここでは、単なるチャットではなく、今開いている文書、表、メール、会議、チャットなどと結びついて動くことが重要です。

たとえば、Word なら文書の下書きや書き換え。Excel ならデータの説明や分析。PowerPoint ならスライド作成。Outlook ならメール要約や返信案。Teams なら会議の要点整理。

つまり、Microsoft 365 の Copilot は、Office 作業の中に入る AI です。

## Microsoft 365 Copilot は、会社向けの業務AIとして見る

Microsoft 365 Copilot は、特に会社や組織で使う文脈が強いものです。

これは、単に Word や Excel の中で文章を書いてくれるだけではありません。

会社の Microsoft 365 環境にあるファイル、メール、チャット、会議、予定表、人の情報などをもとに、仕事の文脈で答えることを目指します。

たとえば、次のような使い方が考えられます。

- 昨日の会議の要点をまとめる
- この案件に関係するファイルを整理する
- メールとTeamsのやりとりから状況を把握する
- 提案資料のたたき台を作る
- 社内情報をもとに質問へ答える

ここで重要なのは、**社内データとの接続**です。

個人向けの AI チャットは、主に一般的な知識やWeb情報を使います。一方、Microsoft 365 Copilot は、組織内の Microsoft 365 データと結びつくことで、仕事の文脈に近い回答を出そうとします。

そのぶん、ライセンス、権限、セキュリティ、管理者設定、組織内データの扱いが関係してきます。

うぅ…個人が気軽に使う Copilot とは、かなり別物として見たほうがよいです。

## 社内の Copilot Chat は、RAG のように見える

会社や組織の Microsoft 365 環境で使う Copilot Chat は、体験としてかなり強いです。

あの…これは、昔の Bing の生成AIや、単体の PowerPoint 生成AIで少しがっかりした印象とは、かなり違って見えるところです。

社内のファイル、Teams の会話、メール、会議、予定表、SharePoint や OneDrive の資料。そうした Microsoft 365 上のリソースを、権限の範囲で参照しながら答えてくれると、「これはもう社内RAGなのでは…？」という感覚になります。

実際、利用者から見ると、RAG 的です。

```text
社内の文書や会話がある
  ↓
質問する
  ↓
関連する社内情報を探してくる
  ↓
その情報をもとに回答する
```

この体験はかなり大きいです。社内FAQ用に専用RAGを作る前に、まず Microsoft 365 Copilot Chat で十分なのではないか、と思う場面も出てきます。

「すわ、RAG不要なのでは」と感じるのは自然です。

ただし、ここも少し分けて見たほうがよいです。

Microsoft 365 Copilot Chat は、Microsoft 365 の中にある情報を使うには強いです。既に SharePoint、OneDrive、Teams、Outlook に情報があり、権限設計も Microsoft 365 側に乗っているなら、かなり有力です。

特に強いのは、SharePoint の権限がそのまま効くところです。

専用RAGを作るときに難しいのは、検索対象の文書をどう集めるかだけではありません。誰がどの文書を読んでよいのか。検索結果に出してよいのか。回答生成の入力に入れてよいのか。そこを、別の仕組みとして作り込む必要があります。

Microsoft 365 Copilot Chat では、少なくとも Microsoft 365 の範囲では、SharePoint や OneDrive などの既存の権限がそのまま効く形で検索や回答に使われます。これはかなり大きいです。

```text
SharePoint に資料がある
  ↓
SharePoint の権限で読める人が決まっている
  ↓
Copilot Chat も、その権限の範囲で参照する
```

この形だと、社内の情報活用でいちばん怖い「見えてはいけない資料が回答に混ざる」問題を、既存の Microsoft 365 権限管理に寄せて扱えます。

うぅ…もちろん、だから何も考えなくてよい、という話ではありません。SharePoint 側の権限が雑なら、Copilot に渡る前の時点で雑です。だから、Copilot を使うほど、SharePoint の権限設計、フォルダ構成、サイト設計、古い資料の整理がそのまま効いてきます。

でも、既存の権限体系をそのまま使えるというのは、専用RAGを一から作る場合と比べて、とても大きな差です。

## Edge で普通に検索しただけに見えても、社内検索が混ざることがある

ここで、さらに混乱しやすいことがあります。

Edge で普通に検索しただけのつもりなのに、社内 SharePoint の情報を使った生成AIや検索結果が動いているように見えることがあります。

これは、見間違いとは限りません。

Edge を職場アカウント、つまり Microsoft Entra ID のアカウントで使っている場合、Edge のアドレスバー、Microsoft Search、Microsoft 365 Copilot Chat が近い場所に並びます。そのため、利用者から見ると「普通のWeb検索」と「社内検索」と「Copilot Chat」が地続きに見えることがあります。

ここで注意したいのは、Microsoft Search in Bing の扱いです。2025年3月31日以降、Bing.com を通じた職場/学校検索は廃止され、現在の主な入口は M365.cloud.microsoft、SharePoint Online、Edge for Business のアドレスバー、Windows 検索ボックスへ移っています。

つまり、現在の見え方としては、Edge のアドレスバーから検索したものが M365.cloud.microsoft 側の職場検索結果へつながることがあります。組織内の人、ファイル、SharePoint サイトなどが対象になり、検索結果はユーザーがアクセス権を持つ情報に限定されます。

つまり、次のようなことが起きます。

```text
Edge のアドレスバーで検索する
  ↓
職場アカウントでサインインしている
  ↓
Microsoft Search / Microsoft 365 側の検索体験に接続される
  ↓
SharePoint や OneDrive など、社内情報の結果が出る
  ↓
その結果から Copilot Chat に進む、または Copilot が文脈を使う
```

あの…この体験は、初めて見ると少し不思議です。普通の検索をしているつもりなのに、社内文書を踏まえた回答が返ってきたように見えるからです。

ただし、厳密にはいくつかの入口が混ざっています。

- Edge のアドレスバー検索
- Microsoft Search
- Microsoft 365 Copilot app の Search
- Edge サイドバーの Microsoft 365 Copilot Chat
- Browse with Copilot のような Edge 内の Copilot 機能

これらは見た目や導線が近いので、どれを使っていたのかがわかりにくいです。

だから、「Edge で普通に検索しただけなのに、社内SharePointを使った生成AIが動いたように見えた」という感覚は、かなりあり得ます。

確認するなら、次の点を見るとよいです。

- Edge が職場プロファイルで開かれているか
- Microsoft 365 に職場アカウントでサインインしているか
- 検索結果に組織名、職場メール、会社ロゴ、Work / School 系の表示があるか
- Edge サイドバーの Copilot に盾アイコンや Enterprise Data Protection の表示があるか
- 検索結果が Web なのか、Microsoft 365 / SharePoint / OneDrive の結果なのか

ここを確認すると、「Web検索に社内結果が混ざっていた」のか、「Copilot Chat を使っていた」のか、「Microsoft 365 Copilot app の検索へ遷移していた」のかが少し見えます。

一方で、専用RAGが必要になる場面も残ります。Microsoft 365 の外にある業務データを扱う場合、回答根拠や検索ロジックを細かく制御したい場合、独自アプリに組み込みたい場合、監査や評価を自前で設計したい場合、あるいは社外向けサービスとして提供したい場合です。

つまり、Microsoft 365 Copilot Chat は「社内RAGの代替候補」にはなります。でも、すべてのRAGを不要にするというより、**Microsoft 365 内の情報活用では、まず検討すべき強い標準機能**として見るのがよいと思います。

## Copilot Studio は、Copilotを作る側の道具

Copilot Studio は、Copilot を使うための道具というより、**AIエージェントを作るための道具**です。

社内FAQに答えるエージェント、業務手続きを案内するエージェント、Teams やWebサイトから使えるエージェントなどを作るために使います。

Microsoft の説明では、Copilot Studio は AI エージェントを作成、カスタマイズ、公開するためのプラットフォームとして扱われています。

ここは、利用者向けというより、業務システムを整える人、Power Platform を使う人、社内AI活用を設計する人の領域に近いです。

だから、普通に「Copilot を使ってみたい」という人が、いきなり Copilot Studio から入ると重いです。

まずは Microsoft Copilot や Microsoft 365 の Copilot を使い、必要になったら Copilot Studio を見る、くらいでよいと思います。

## Copilot Studio は、データを作るところが少し難しい

Copilot Studio は、画面上ではかなり簡単に見えます。自然言語でエージェントを作る。知識ソースを追加する。SharePoint、Dataverse、Webサイト、アップロードファイル、コネクタなどをつなぐ。

あの…入口はたしかにやさしく見えます。

でも、実際に業務で使えるエージェントにするには、データ側の準備が少し難しいと思います。

Copilot Studio の生成回答は、設定した知識ソースをもとに回答します。つまり、知識ソースに古い情報、重複した情報、曖昧な情報、権限的に見せたくない情報が混ざっていると、その影響を受けます。Microsoft の FAQ でも、選ばれたデータソースに不正確な情報が含まれていれば、それがユーザーに示される可能性があると説明されています。

さらに、データの置き方によって性格が変わります。

```text
SharePoint
  既存文書を活用しやすい。権限やサイト設計が重要。

Dataverse
  業務データとして扱いやすい。テーブル、列、用語、検索設定の整備が必要。

アップロードファイル
  すぐ試せる。ただしファイル内容がエージェント利用者に広く見える形になる場合があり、権限設計に注意が必要。

Power Platform connectors
  リアルタイムの業務システム連携に向く。読み書きやアクション設計が必要。

Copilot connectors
  外部データを Microsoft Graph 側に索引化し、検索・グラウンディングに使う方向。

Custom data
  Power Automate や HTTP 経由で渡せるが、回答に使う `Content`、引用元の `ContentLocation`、`Title` などを整える必要がある。
```

このうち、「docx、xlsx、pptx、PDF などを置いておくと、それをもとに回答する生成AIを作れるやつ」は、Copilot Studio の **knowledge source** と **generative answers** の組み合わせです。

ファイルをアップロードして knowledge source にする方法もありますし、OneDrive や SharePoint のファイルやフォルダを knowledge source として追加する方法もあります。Microsoft のドキュメントでは、Word、Excel、PowerPoint、PDF などが対応ファイルとして挙げられています。

ただし、ここも注意が必要です。アップロードファイル方式では、ファイルは静的なコピーとして扱われ、元ファイルを更新しても自動反映されない場合があります。一方、OneDrive を knowledge source として使う場合は、ファイルやフォルダの同期があり、更新が反映される方向です。また、アップロードファイルはエージェント利用者に広く利用可能になる注意があり、OneDrive ではユーザー資格情報によるアクセス確認が関わります。

つまり、ただ試すならファイルアップロードでよいかもしれません。でも、社内で運用するなら、OneDrive や SharePoint を knowledge source にして、権限と更新を含めて設計するほうが自然だと思います。

ここで初見だと難しく感じるのは、ファイル形式そのものではなく、**AI が参照しやすい知識の構造をどう作るか** です。

docx、xlsx、pptx を置けると言われると、単に既存資料を放り込めばよさそうに見えます。でも、生成AIが回答しやすい資料と、人間が会議で読む資料は、少し違います。

たとえば、次のような資料は、人間には読めても、AI の knowledge source としては扱いにくくなりがちです。

- 1つのファイルに複数テーマが混ざっている
- 古い方針と新しい方針が同じ場所に残っている
- 表の列名や見出しが曖昧
- PowerPoint の図だけに意味があり、本文テキストが少ない
- 「これ」「上記」「前述」のような参照が多い
- ファイル名だけでは中身や用途がわからない
- 同じ内容の版違いが複数ある

こうなると、Copilot Studio はそれらしい回答を作れても、どの資料のどの情報を正としてよいのか迷いやすくなります。

だから、Copilot Studio 用のデータ構造を作るときは、最初に少しだけ「AI が読むための整理」をしたほうがよいです。

```text
1ファイル1テーマに近づける
見出しを具体的にする
版や有効日を明記する
FAQ形式や手順形式に分ける
表には意味のある列名を付ける
古い資料を退避する
引用元として見せたいタイトルを整える
```

あの…ここが、初見では少し難しいところです。ファイルを置く機能は簡単でも、AI にとって読みやすい社内知識ベースを作るには、文書管理、情報設計、業務用語の整理が必要になります。

つまり、Copilot Studio の knowledge source は「ファイル置き場」ではなく、**回答の根拠になる社内知識ベース**として考えるほうが近いです。

## Markdown より Office ファイルのほうがネイティブなのか

ここで気になるのが、Markdown よりも docx、xlsx、pptx のほうが Copilot Studio では得意なのか、という点です。

あの…これは、初見ではそう見えて自然だと思います。

Microsoft 365 の世界で見ると、Word、Excel、PowerPoint、SharePoint、OneDrive はかなり中心にあります。Copilot Studio の knowledge source でも、Word、Excel、PowerPoint、PDF は明確に対応ファイルとして出てきます。OneDrive や SharePoint との接続も、Microsoft 365 の権限やファイル管理と一緒に扱いやすいです。

その意味では、docx、xlsx、pptx は「Microsoft 365 の中で自然に扱われる形式」です。業務資料としてすでに存在していることも多く、SharePoint や OneDrive に置いて、権限や更新と一緒に扱いやすいのは大きいです。

Microsoft の資料を読むと、最初は Office 形式のほうが特に意味を持っているように見えます。これは、説明の中心が Microsoft 365 の業務資料、つまり Word、Excel、PowerPoint、SharePoint、OneDrive に寄っているからだと思います。

ただし、Markdown が非対応というわけではありません。Copilot Studio のアップロードファイルでは `.md` も対応ファイルに含まれています。Cowork のプレビューでも Markdown は表示対応形式として出ています。

だから、「Office 形式のほうがネイティブで、Markdown はだめ」とまでは言い切れません。

むしろ、用途で分けるのがよさそうです。

```text
既存の社内資料をそのまま活かしたい
  -> docx / xlsx / pptx / PDF

SharePoint や OneDrive の権限、更新、業務文書管理に乗せたい
  -> docx / xlsx / pptx / PDF

AI が読みやすい構造化テキストを最初から作りたい
  -> Markdown / txt / YAML / JSON / CSV

FAQ、手順書、規約、用語集のように見出し構造を明確にしたい
  -> Markdown もかなり相性がよい
```

Office 形式は、Microsoft 365 の業務文書としては強いです。一方、AI に読ませるための知識ベースを一から作るなら、Markdown のような素直なテキスト形式のほうが、構造を制御しやすい場面もあります。

つまり、答えはこうです。

```text
Microsoft 365 の運用に乗せるなら Office 形式が自然。
AI に読みやすい知識構造を作るなら Markdown も強い。
```

うぅ…なので、「どちらが上か」より、「既存業務資料を活かすのか」「AI向けに知識ベースを設計するのか」で選ぶのがよいと思います。

つまり、Copilot Studio の難しさは、エージェント画面そのものよりも、**AI に渡してよい形に業務データを整えること**にあります。

専用RAGを作るほどではないにしても、次のような整理は必要になります。

- どの情報を正とするのか
- 古い文書をどう除外するのか
- 同じ内容の資料が複数あるとき、どれを優先するのか
- ユーザー権限をどう守るのか
- 回答根拠として見せる引用元をどう整えるのか
- データ更新をどの頻度で反映するのか
- テスト質問を用意して、期待通りに答えるか確認するのか

うぅ…ここは、かなり地味です。でも、ここを避けると、エージェントはそれらしい回答をするけれど、業務では信用しにくいものになってしまいます。

だから、Copilot Studio は「ノーコードで簡単にAIエージェントが作れる」だけで見ないほうがよいです。より正確には、「エージェントを作る入口は簡単。ただし、良いエージェントにするには、社内データ、権限、用語、更新、テストの整備が必要」と見るのが近いと思います。

## GitHub Copilot は、開発者向けなので別枠で見る

GitHub Copilot も Copilot という名前ですが、これは開発者向けです。

コード補完、コード生成、テスト作成、コード説明、リファクタリング支援、開発中の質問などに使います。

Microsoft Copilot や Microsoft 365 Copilot と名前は似ていますが、使う場所は GitHub、VS Code、JetBrains IDE などの開発環境です。

つまり、GitHub Copilot は「プログラミングの相棒」として見るのが自然です。

Office 作業や社内文書の整理ではなく、コードを書く人のための Copilot です。

## Copilot Cowork は、仕事を代行する早期アクセス系の存在

Copilot Cowork は、Microsoft 365 Copilot の中で語られている、よりエージェント的な機能です。

通常の Copilot Chat が「質問に答える」「文章を作る」「要約する」ことを中心に見えるのに対して、Copilot Cowork は、仕事を受け取り、計画し、Microsoft 365 の中で複数ステップの作業を進める方向に寄っています。

たとえば、メールを下書きする、資料を集める、会議やチャットの文脈を見ながら作業を進める、長めの作業をバックグラウンドで進行させる、といった位置づけです。

さらに、Frontier の説明を見ると、Cowork はスキルを使って動くように見えます。

組み込みスキルとして、Word、Excel、PowerPoint、PDF、Email、Scheduling、Calendar Management、Meetings、Daily Briefing、Enterprise Search、Deep Research、Communications、Adaptive Cards などが挙げられています。つまり、単にチャットで返事をするのではなく、作業の種類ごとにスキルを読み込みながら進む形です。

そして、ここがかなり大きいのですが、カスタムスキルも作れるようです。

Microsoft のドキュメントでは、OneDrive の `/Documents/Cowork/Skills/` 配下にスキル用フォルダを作り、その中に `SKILL.md` を置く形が説明されています。`SKILL.md` には `name` と `description` を持つ YAML front matter と、Markdown の指示を書きます。Cowork は会話開始時に、そのカスタムスキルを自動的に見つける、とされています。

```text
OneDrive
  /Documents/Cowork/Skills/
    weekly-report/
      SKILL.md
```

うぅ…これは、かなり革命的になる可能性があります。

これまでの Microsoft 365 Copilot は、社内データを使えることが強みでした。そこに Cowork のような実行エージェントが乗り、さらにユーザーや組織が `SKILL.md` で作業手順を渡せるなら、単なる「社内情報に答えるAI」から、「社内のやり方で仕事を進めるAI」へ近づきます。

もちろん、これは Frontier のプレビュー機能です。正式リリースまでに仕様、制限、管理方法、配布方法、セキュリティ確認の仕組みは変わるかもしれません。Microsoft の説明でも、カスタムスキルは Microsoft が検証するものではなく、出力はレビューが必要という注意があります。

それでも、方向性としてはかなり楽しみです。正式リリースされたときに、組織で再利用できる小さな作業手順を `SKILL.md` として蓄積できるなら、Microsoft 365 の中での業務自動化の見え方が変わるかもしれません。

ただし、ここは通常の一般提供済み製品として雑に並べるより、**Frontier や早期アクセスの文脈にあるもの**として見たほうがよいです。

あの…この記事では未リリースまたは限定提供中の項目として一覧に入れておきます。今後、名称、提供範囲、ライセンス、できることが変わる可能性があります。

## 混乱の原因は、同じ名前で入口が多すぎること

Microsoft Copilot がわかりにくい理由は、機能そのものが難しいからだけではありません。

同じ Copilot という名前で、入口が多すぎるのです。

```text
個人でWebから使う Copilot
Windows に入っている Copilot
Edge にいる Copilot
Microsoft 365 アプリ内の Copilot
会社の Microsoft 365 データにつながる Copilot
AIエージェントを作る Copilot Studio
開発者向けの GitHub Copilot
仕事を代行する Copilot Cowork
```

これらをまとめて Copilot と呼ぶので、説明がすぐに曖昧になります。

「Copilot は無料です」と言われても、どの Copilot なのか。

「Copilot は Microsoft 365 に含まれます」と言われても、個人向けなのか会社向けなのか。

「Copilot は社内データを使えます」と言われても、それは Microsoft 365 Copilot の話なのか。

「Copilot はコードを書けます」と言われても、それは GitHub Copilot の話なのか。

このように、文脈を分けないと、全部が混ざります。

## どう理解すればよいか

まずは、次のように考えるとよいです。

```text
個人でAIチャットを使いたい
  -> Microsoft Copilot

Word、Excel、PowerPoint、Outlook、Teamsで使いたい
  -> Copilot in Microsoft 365

会社のメール、会議、ファイル、Teamsとつなげたい
  -> Microsoft 365 Copilot

社内用AIエージェントを作りたい
  -> Copilot Studio

コードを書きたい
  -> GitHub Copilot

Microsoft 365 の中で、長めの仕事を代行してほしい
  -> Copilot Cowork
```

あの…これでかなり見通しがよくなると思います。

Copilot という名前だけを見ないで、「どこで使うのか」「何につながるのか」「誰向けなのか」を見るのです。

## おわりに

Microsoft Copilot は、ひとつの箱ではありません。

Microsoft のいろいろな製品に広がっている AI アシスタントの名前です。

だから、最初に必要なのは、細かい機能を覚えることではなく、分類することだと思います。

個人向けの AI チャット。Microsoft 365 アプリ内の支援。会社向けの業務AI。AIエージェント作成ツール。開発者向けコード支援。そして、仕事を代行する早期アクセス系エージェント。

このように分けると、「Copilot」という大きな名前の中に、いくつかの別の道具が入っていることが見えてきます。

うぅ…名前が同じなので、わかりにくいのは自然です。

でも、入口を分けて見ると、少し落ち着いて理解できるかな、って思います。

## 参考

- Microsoft Support, "What's the difference between Microsoft Copilot (free) and Copilot in Microsoft 365", Last updated: April 2026.
- Microsoft Support, "Getting started with Microsoft Copilot".
- Microsoft Learn, "Guidance for retiring Microsoft Search in Bing for your organization", 2025-08-05.
- Microsoft Learn, "How does Microsoft 365 Copilot work?".
- Microsoft Learn, "Microsoft 365 Copilot data and compliance readiness".
- Microsoft, "Microsoft 365 Copilot".
- Microsoft, "Microsoft Copilot Studio".
- Microsoft Learn, "Knowledge sources summary - Microsoft Copilot Studio".
- Microsoft Learn, "Use a custom data source for generative answers nodes - Microsoft Copilot Studio".
- Microsoft Learn, "Add SharePoint as a knowledge source - Microsoft Copilot Studio".
- Microsoft Learn, "Use uploaded files with generative answers nodes - Microsoft Copilot Studio".
- Microsoft Learn, "Add unstructured data as a knowledge source - Microsoft Copilot Studio".
- Microsoft Learn, "Copilot connectors versus Power Platform connectors as knowledge sources - Microsoft Copilot Studio".
- Microsoft Learn, "FAQ for generative answers - Microsoft Copilot Studio".
- Microsoft 365 Blog, "Copilot Cowork: A new way of getting work done", 2026-03-09.
- Microsoft Support, "Get started with Copilot Cowork (Frontier)".
- Microsoft Learn, "Use Copilot Cowork (Frontier)".
- Microsoft Learn, "Copilot Cowork common questions (Frontier)".
- Microsoft Support, "Conversation modes in Microsoft Copilot".
- Microsoft Learn, "Understanding AI functionality and models in Microsoft Online Services".
- Microsoft 365 Blog, "Expanding model choice in Microsoft 365 Copilot", 2025-09-24.
- Microsoft Copilot Blog, "Anthropic joins the multi-model lineup in Microsoft Copilot Studio", 2025-09-24.
- Microsoft Learn, "Copilot in Microsoft 365 apps with Anthropic models".
