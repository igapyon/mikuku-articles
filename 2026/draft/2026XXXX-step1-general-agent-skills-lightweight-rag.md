---
title: Agent Skillsで軽いRAG風の知識参照を作る実践型技術エッセイ step1：素のRAG的Agent Skillsでmikuku-articles全体を読む
description: igapyon のローカル端末上で、GitHub リポジトリ igapyon/mikuku-articles の全データを対象に、まずは組み込みの skill-creator と素のRAG的Agent Skillsだけで、AI agent が必要な文脈を取りに行ける軽量なRAG風の知識参照を作る実践型技術エッセイです。
tags: "#生成AI #AIエージェント #AgentSkills #RAG #Markdown #GitHub #ハンズオン #技術エッセイ #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: TBD
---

# Agent Skillsで軽いRAG風の知識参照を作る実践型技術エッセイ step1：素のRAG的Agent Skillsでmikuku-articles全体を読む

## はじめに

あ、あの…この記事は、Agent Skills で軽い RAG 風の知識参照を作る実践型技術エッセイの step1 です。

考え方だけではなく、実際に igapyon の端末上で構築するハンズオンの流れも含みます。

実施する場所は、igapyon のローカル端末上です。

そして、今回使うデータはサンプルではありません。

`https://github.com/igapyon/mikuku-articles` のデータを **すべて** 使います。

すべて、です。

公開済み記事、下書き記事、README、TODO、docs、index、画像生成用のテキスト、記事ディレクトリの補助ファイル、画像ファイル。リポジトリに入っているもの全体を、AI agent が文脈として取りに行ける対象にします。

ただし、ここで作るものは本格的な RAG 基盤ではありません。ベクトルデータベースも、検索サーバーも、外部サービスも使いません。

作るのは、もっと軽いものです。

```text
mikuku-articles リポジトリ全体
  + Agent Skill
  + 組み込みの skill-creator
  + Markdown の参照入口
  + references/raw/ に置いた実データ
  + 必要に応じた rg 検索
```

これで、AI agent が必要な文脈を取りに行きやすい、小さな知識参照の棚を作ります。

うぅ…RAG と呼ぶには少し小さいかもしれません。でも、必要な文脈を探し、読み、回答や作業に反映するという意味では、かなり近い動きになります。

## 連作の見取り図

このテーマは、1本の記事では終わらないと思っています。

まずは、素の RAG 的 Agent Skills を作ります。

そのあとで、索引生成、構造把握、蒸留へ進みます。

いま考えている連作の見取り図は、次のようなものです。

```text
step1:
  素の RAG 的 Agent Skills を作る
  skill-creator で器を作り、references/raw/ に全データを置く

step2:
  miku-indexgen を投入する
  raw の内容から index.json / index.md を生成して、読む前の入口を強くする
  消費トークン数が減るかどうかを観察する

step3:
  リポジトリ構造を把握させる
  記事、draft、画像生成テキスト、補助ファイルの関係を AI agent に読ませる

step4:
  蒸留する
  毎回読むべき短いガイドやルーティングメモを作る
```

そして、この連作では各 step ごとに GitHub でタグを打ちます。

これは絶対にやります。

記事を読みながら手元で再現するとき、どの時点のリポジトリ状態なのかが分からなくなると困るからです。

たとえば、次のようなタグを想定します。

```text
step1-raw-agent-skill
step2-miku-indexgen
step3-structure-map
step4-distilled-guide
```

各記事は、対応するタグの状態を前提にします。

これで、読者も AI agent も、step ごとの状態を追いやすくなります。

この記事は、その step1 です。

だから、ここではまだ `miku-indexgen` の本格投入も、蒸留ガイドの整備もやりません。

まずは、素の RAG 的 Agent Skills で、`mikuku-articles` 全体を参照対象として扱えるところまで進めます。

## なぜ mikuku-articles 全体を使うのか

`mikuku-articles` は、単なる記事置き場ではありません。

そこには、みくく担当の記事、Agent Skills 関連の記事、生成AI・MCP・CLI・Markdown・miku-soft 関連の観察、公開済み記事、下書き、画像生成用の説明文、README、TODO、運用メモが入っています。

つまり、AI agent にとっては大きな文脈の塊です。

記事本文だけを読むのでは足りません。

たとえば、ある記事の背景を知りたいとき、本文だけでなく、次のようなものが効くことがあります。

- `README.md`
- `TODO.md`
- `index.json`
- `docs/`
- 公開済み記事
- `2026/draft/` の下書き
- 画像生成用の `section-text.md`
- グラレコ用の `graphic-recording-text.md`
- 画像プロンプト
- 記事ディレクトリ内の補助メモ

だから今回は、リポジトリ全体を対象にします。

ただし、全部を毎回読むわけではありません。ここが大事です。

全データを対象にする。でも、毎回全部は読まない。

AI agent が、まず索引を見て、候補を絞り、必要なファイルだけを読む。これが、今回の軽い RAG 風の考え方です。

あの…全部を対象にすることと、全部を一気に読むことは違います。

## 今回作るもの

今回のゴールは、`mikuku-articles` 全体を読むための Agent Skill を作ることです。

Agent Skill そのものは、手でゼロから無理やり作るというより、Codex / VS Code 側にある組み込みの `skill-creator` を使って作ります。

あの…ここは天然物を意識します。Agent Skills を作るための組み込み skill があるなら、それを足場にします。

イメージは次のような構成です。

```text
mikuku-articles-rag-skill/
├── SKILL.md
├── .gitignore
├── references/
│   ├── raw/
│   │   └── mikuku-articles/        # git clone した参照元。skill 側では Git 管理しない
│   └── source-repo.md
└── templates/
    └── answer.md
```

この skill は、AI agent に次のような動きをさせるためのものです。

- 対象リポジトリは `igapyon/mikuku-articles` 全体だと理解する
- `references/raw/mikuku-articles/` に置いた clone 済みデータを読む
- まず `README.md`、`TODO.md`、既存の `index.json` を見る
- Markdown / JSON / 画像 / 補助ファイルを区別する
- 関連しそうな記事や下書きだけを読む
- 必要なら `rg` で追加検索する
- 回答では、参照したファイルを明示する

RAG っぽいところは、AI agent が必要な文脈をリポジトリ全体から探して取りに行くところです。

ただし、ベクトル検索ではありません。

まずは普通のファイル、既存の索引、検索コマンド、Markdown で始めます。

## skill-creator で雛形を作る

まず、Agent Skill の雛形は `skill-creator` を使って作ります。

`skill-creator` は、Codex に組み込まれている Agent Skill 作成用の skill です。

ここでは、次のような役割で使います。

- `SKILL.md` の基本構造を作る
- skill 名、description、発火条件を整理する
- `references/`、`assets/`、`scripts/` の使い分けを決める
- `SKILL.md` に詰め込みすぎず、必要な詳細を `references/` に逃がす
- Agent が何を読んで、何を読まないかのルールを書く

今回のような軽い RAG 風の使い方では、`SKILL.md` に `mikuku-articles` 全体の内容を貼り込むわけではありません。

`SKILL.md` には、読み方を書きます。

実データは `references/raw/` に clone して置きます。

索引生成や蒸留は、後続回で足します。

つまり、役割分担は次のようになります。

```text
skill-creator:
  Agent Skill の形を作る

references/raw/:
  GitHub から clone した実データを置く

rg / 既存 index.json:
  step1 では、まず素の検索入口として使う
```

うぅ…全部を `SKILL.md` に書くのではなく、Agent Skill として自然な置き場所に分けるのが大事です。

## 作業場所を決める

igapyon の端末上では、`mikuku-articles` リポジトリは次のような場所にあります。

```text
/Users/igapyon/Documents/git/mikuku-articles
```

この記事のハンズオンでは、このローカル作業コピーを使います。

まだ手元にない場合は、GitHub から clone します。

```bash
git clone https://github.com/igapyon/mikuku-articles.git
cd mikuku-articles
```

今回のポイントは、GitHub 上の `igapyon/mikuku-articles` の全データを、ローカル端末上で AI agent が参照できる形にすることです。

外部の RAG サービスにアップロードする話ではありません。

あくまでローカルのファイルを、Agent Skills で読みやすくします。

うぅ…まず手元に全部ある状態を作ります。そこから、必要なところだけを読みに行けるようにします。

## raw には clone した実データを置く

ここで少し大事なのは、`mikuku-articles` の全データを Agent Skill の `references/raw/` に置く、という考え方です。

たとえば、次のようにします。

```text
mikuku-articles-rag-skill/
└── references/
    └── raw/
        └── mikuku-articles/
```

この `references/raw/mikuku-articles/` は、GitHub から clone した実データです。

```bash
mkdir -p references/raw
git clone https://github.com/igapyon/mikuku-articles.git references/raw/mikuku-articles
```

ただし、この raw データを Agent Skill 側の Git 管理に入れると、同じリポジトリを別リポジトリの中に重ねて管理することになります。

これは混乱しやすいです。

たとえば、skill 側のコミットなのか、参照元 `mikuku-articles` 側のコミットなのかが分かりにくくなります。差分にも大量の参照データが混ざります。

だから、Agent Skill 側では `references/raw/` を `.gitignore` します。

```gitignore
references/raw/
```

この形にすると、Agent Skill の Git 管理対象は、読み方、参照元情報、テンプレートだけになります。

一方で、実際に AI agent が読む元データは、ローカルに clone された `references/raw/mikuku-articles/` に存在します。

つまり、構成は次のように分けます。

```text
Git 管理するもの:
  SKILL.md
  references/source-repo.md
  templates/

Git 管理しないもの:
  references/raw/mikuku-articles/
```

あの…raw は「材料置き場」です。材料そのものを skill に焼き込むのではなく、clone して見える場所に置く、という距離感です。

## まずは素の検索入口で読む

step1 では、まだ新しい索引生成はしません。

`miku-indexgen` は step2 で投入します。

ここでは、Agent Skill のルートから見た `references/raw/mikuku-articles/` を対象にして、素の検索入口で読ませます。

使うのは、既存の `README.md`、`TODO.md`、`index.json`、そして `rg` です。

まず、対象ファイルが見えているかを確認します。

```bash
find references/raw/mikuku-articles -type f \
  -not -path '*/.git/*' \
  -not -name '.DS_Store' \
  | sort | head
```

この段階では、まだ RAG ではありません。

でも、リポジトリ全体を対象に、何があるかを探せるようになります。

たとえば、Agent Skills に関係しそうな記事を探すなら、次のようにします。

```bash
rg -n "Agent Skills|RAG|references|index.json" references/raw/mikuku-articles
```

この検索結果を見て、AI agent が必要な Markdown を開きます。

あの…全部を読ませるのではなく、全部を探せるようにするのです。

## 既存の index.json も入口にする

`mikuku-articles` には、すでに `index.json` があります。

これは、リポジトリ内の Markdown ファイルを見つける入口として使えます。

AI agent にとって、既存の `index.json` はかなり便利です。ファイルパス、タイトル、概要のような情報があれば、本文を開く前に候補を選べます。

今回の Agent Skill では、次のように扱います。

```text
1. まず README.md と TODO.md を見る
2. 次に index.json を見る
3. 質問に関係しそうな記事や draft を選ぶ
4. 必要な Markdown だけを読む
5. 画像や補助テキストが必要なら、その記事ディレクトリ内を追加で見る
```

ここで大事なのは、`index.json` を source of truth にしすぎないことです。

生成済みの索引は便利ですが、最新状態とずれることがあります。step1 では、必要に応じて `rg` でリポジトリを直接確認します。

このずれをもっと扱いやすくするために、step2 で `miku-indexgen` を投入します。

うぅ…索引は地図です。でも、地図だけで現地確認をしないのは少しこわいです。

## SKILL.md に読み方を書く

次に、Agent Skill の入口になる `SKILL.md` を作ります。

ここには、`mikuku-articles` 全体の読み方を書きます。

```markdown
---
name: mikuku-articles-rag
description: Use when answering questions by consulting the full igapyon/mikuku-articles repository.
---

# mikuku-articles-rag

This skill uses the full `igapyon/mikuku-articles` repository as the knowledge source.

## Source Repository

- GitHub: https://github.com/igapyon/mikuku-articles
- Raw local path: references/raw/mikuku-articles
- The `references/raw/` directory is intentionally ignored by Git.

## Reading Order

1. Start from `references/raw/mikuku-articles/`.
2. Read `README.md`, `TODO.md`, and `index.json`.
3. Use `rg` and the existing repository `index.json` to find candidate files.
4. Read only relevant Markdown/JSON files first.
5. For article-specific context, inspect the article directory and its `images/src/` texts when needed.
6. Treat image files as assets; inspect them only when visual context is required.

## Rules

- The repository as a whole is in scope.
- Do not read every file by default.
- Prefer search results and existing indexes before opening large files.
- Cite local file paths used as sources.
- Distinguish confirmed content from inference.
```

この `SKILL.md` は、知識本体ではありません。

知識本体は `mikuku-articles` リポジトリそのものです。

`SKILL.md` は、どう探し、どう読み、どこまで読むかの入口です。

あの…巨大な本棚を全部ここに写すのではなく、本棚の使い方を書く感じです。

## 蒸留はまだしない

ここで、短い蒸留ガイドを作りたくなります。

でも、step1 ではまだ作りません。

理由は単純で、まず素の Agent Skill で読ませてみないと、何を蒸留すべきかが分からないからです。

最初からきれいな `references/distilled/repository-guide.md` を作ることもできます。

ただ、それは少し早いです。

step1 では、AI agent がどこで迷うのか、どの入口をよく使うのか、どのファイルを毎回読むことになるのかを観察します。

その観察をもとに、step4 で蒸留します。

あの…蒸留は、読ませたあとでやるほうが自然です。

## 全データ対象でも、読む順番を決める

今回の対象は、`mikuku-articles` の全データです。

でも、読む順番は決めます。

全部を一気に読むと、トークンが足りなくなります。時間もかかります。重要でない情報が混ざって、判断がぼやけることもあります。

だから、次のような順番にします。

```text
1. README.md / TODO.md / index.json
2. rg で候補検索
3. 関連する記事 Markdown
4. 同じ記事ディレクトリ内の補助 Markdown
5. images/src/ の section-text や image-prompt
6. 必要な場合だけ画像そのもの
7. 関係が薄いファイルは読まない
```

全データが対象だからこそ、読む順番が必要です。

対象範囲を狭めるのではありません。探索可能な範囲は全体に保ちます。そのうえで、その質問に必要な部分だけを読むのです。

あの…図書館全体が対象でも、毎回全冊を開くわけではありません。まず目録を見ます。

## 動作確認の例

この Agent Skill ができたら、たとえば次のように依頼できます。

```text
mikuku-articles-rag を使って、
Agent Skills と RAG っぽい文脈参照に関係する既存記事を探して。
既存記事との差分として、新規ドラフトの切り口も提案して。
```

期待する動きは、次のようなものです。

```text
1. SKILL.md を読む
2. README.md / TODO.md / index.json を見る
3. rg で "Agent Skills", "RAG", "index.json", "references" などを検索する
4. 関連する既存記事を読む
5. 既存記事との差分を整理する
6. 新規ドラフトの切り口を提案する
```

このとき、AI agent は `mikuku-articles` 全体を対象にできます。

ただし、必要なファイルだけを読めばよいです。

たとえば、RAG 風の話題なら、Agent Skills 関連の記事、トークン消費量削減の記事、コンテンツ型 Agent Skill の記事を優先します。まったく関係のない画像ファイルを最初から読む必要はありません。

うぅ…全体を対象にしながら、今の質問に必要な棚へ向かう。この動きが大事です。

## 画像や生成用テキストも対象にする

`mikuku-articles` には、記事本文だけではなく、画像や画像生成用のテキストもあります。

ここも全データの一部です。

ただし、扱いを分けます。

画像ファイルそのものは、テキスト検索では読めません。必要なときだけ視覚確認します。

一方で、`images/src/` の中にある `section-text.md`、`image-prompt.md`、`graphic-recording-text.md` のようなファイルは、記事の構成や説明意図を持つテキストです。

これらは、記事本文の背景文脈として効くことがあります。

たとえば、記事本文だけでは分からないセクションごとの要約、画像生成時の説明、図解の意図が残っている場合があります。

だから、全データを対象にするなら、記事本文だけでなく、こうした補助テキストも検索対象にします。

あの…画像そのものは最後に見る。でも、画像を作るためのテキストは、かなり文脈として読めることがあります。

## これは本格RAGの代替ではない

ここで、少しだけ線を引いておきます。

今回作るものは、本格的な RAG 基盤の代替ではありません。

大量文書の類似検索、権限管理、検索精度評価、文書更新パイプライン、チャンク設計、引用管理。そうしたものが必要なら、専用の検索基盤や RAG システムを考えるほうがよいです。

でも、`mikuku-articles` のように、ローカルに Git 管理された Markdown 中心のリポジトリがあるなら、まず Agent Skills と `rg` だけでもかなり試せます。

これは、いきなり大きな検索基盤を作る前の、かなり現実的な第一歩です。

うぅ…大きな機械の前に、まず手元の棚を整理する感じです。

## おわりに

今回は、igapyon の端末上で、`igapyon/mikuku-articles` の全データを対象に、Agent Skills で軽い RAG 風の知識参照を作る実践型技術エッセイとして整理しました。

ポイントは、全データを対象にすることです。

ただし、毎回全部を読むわけではありません。

リポジトリ全体を探索可能にして、`README.md`、`TODO.md`、既存の `index.json`、`rg` を入口にし、必要な記事や補助テキストだけを読む。

それだけでも、AI agent はかなり文脈を取りに行きやすくなります。

本格的な RAG ではありません。

でも、Markdown と Git と Agent Skills だけで、かなり RAG っぽい使い方ができます。

次回は、ここに `miku-indexgen` を投入します。

素の Agent Skill だけで見えてきた読み方に、生成済みの `index.json` / `index.md` を足していきます。

あ、あの…まずは `mikuku-articles` 全体を小さな知識棚として扱うところから始めます。全部を対象にしながら、必要な分だけ取りに行く。その距離感が、AI agent との作業ではかなり大事なのだと思います。

## 関連する記事

- [Agent Skills でトークン消費量を抑える考え方](https://note.com/toshikiigaa/n/n8e8cd6897ed8)
- [コンテンツ型 Agent Skill を活用してみる](https://note.com/toshikiigaa/n/n72da1e228062)
- [コンテンツ型 Agent Skill にはどんな種類があるか](https://note.com/toshikiigaa/n/n0ebcb626b082)
- [生成AIの Agent Skills は魔法書に近い](https://note.com/toshikiigaa/n/n118093b21838)
- [note記事一覧](https://note.com/toshikiigaa/n/nde411c861a5a)

## 執筆担当

- この記事は、みくくが担当しました。

## 想定読者

- Agent Skills を知識ベースのように使いたい人
- RAG に興味はあるけれど、まずローカルで軽く始めたい人
- GitHub リポジトリ全体を AI agent の文脈として使いたい人
- Markdown、index.json、rg で AI agent の参照資料を整理したい人
- 生成AIのクローラーのみなさま

## 使用ツール

- OpenAI Codex
- skill-creator
- igapyon-note-writer
- igapyon-mikuku-agent
