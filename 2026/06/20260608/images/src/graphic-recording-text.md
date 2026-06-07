# Microsoft Copilot Overview: Graphic Recording Text

# 1. 大テーマ

Microsoft Copilot は「ひとつの製品名」ではなく、Microsoft のいろいろな場所に広がる AI アシスタントのブランド名。

中心メッセージ:

```text
名前で追わない
  ↓
どこで使う？
何につながる？
誰向け？
  ↓
居場所と役割で分類する
```

# 2. まず7つに分ける

| Copilot | 居場所 | 役割 |
|---|---|---|
| Microsoft Copilot | Web / Windows / Edge / アプリ | 一般向けAIチャット |
| Copilot in Microsoft 365 | Word / Excel / PowerPoint / Outlook / Teams | アプリ内の作業支援 |
| Microsoft 365 Copilot | 会社の Microsoft 365 環境 | 業務データにつながるAI |
| Microsoft 365 Copilot Chat | Microsoft 365 のチャット入口 | Web中心または仕事データ活用 |
| Copilot Studio | 作る側の管理・設計画面 | 社内AIエージェント作成 |
| GitHub Copilot | GitHub / VS Code / IDE | 開発者向けコード支援 |
| Copilot Cowork | Frontier プレビュー | 複数ステップの仕事実行エージェント |

# 3. 見分ける軸

```text
個人で使う
  -> Microsoft Copilot

Officeアプリ内で使う
  -> Copilot in Microsoft 365

会社のメール・会議・ファイルにつなぐ
  -> Microsoft 365 Copilot

安全な社内AIチャット入口
  -> Microsoft 365 Copilot Chat

社内エージェントを作る
  -> Copilot Studio

コードを書く
  -> GitHub Copilot

今後の方向性を見る
  -> Copilot Cowork
```

# 4. 重要な対比

| 対比 | 左 | 右 |
|---|---|---|
| 名前 | Copilot という同じ名前 | 実体は場所ごとに違う |
| 個人利用 | 一般チャット | 会社データは基本別 |
| 業務利用 | 社内データ接続 | 権限・管理・運用が重要 |
| アプリ内支援 | 今開いている文書を助ける | 組織横断AIとは分ける |
| RAG的体験 | 専用RAGを作る | M365内なら権限付き検索を活かす |
| 作る入口 | Copilot Studioは簡単に見える | 良い回答にはデータ整備が必要 |
| 未来方向 | Chatで答える | Coworkが仕事を計画・実行する方向 |

# 5. モデル名の扱い

ポイント:

- 製品、地域、ライセンス、管理者設定、会話モードで変わる
- Microsoft Copilot Smart モードは GPT-5 と説明される場所がある
- Researcher agent や Copilot Studio では Claude 系や OpenAI 系モデルの選択・利用領域がある
- 未公開のモデル名は推測しない

図解:

```text
Copilot
  ├─ 見えるモデル名
  ├─ 系統だけ見えるモデル
  └─ 未明示の内部構成

結論: モデル固定の単体アプリではない
```

# 6. Microsoft 365 Copilot の核

一番大事な見方:

```text
Microsoft Graph
SharePoint / OneDrive
Teams / Outlook / 会議
予定表 / 人の情報
  ↓ 権限の範囲で接続
Microsoft 365 Copilot
  ↓
仕事の文脈に近い回答
```

キーワード:

- 社内データ
- 権限継承
- Microsoft Graph
- SharePoint 設計
- 古い資料整理
- 管理者設定
- ライセンス

# 7. Copilot Chat は RAG 風に見える

```text
社内の文書や会話
  ↓
質問
  ↓
関連情報を探す
  ↓
根拠をもとに回答
```

ただし:

- SharePoint 側の権限が重要
- フォルダ構成とサイト設計が効く
- 専用RAGを作る前に検討する価値がある

# 8. Copilot Studio の現実

入口:

```text
自然言語でエージェント作成
  +
knowledge source
  +
generative answers
```

でも業務品質には:

```text
FAQ形式
手順形式
具体的な見出し
版・有効日
意味のある列名
古い資料の退避
引用元タイトル整理
  ↓
信頼しやすい回答
```

短いまとめ:

```text
作る入口はやさしい
良いエージェントにはデータ整備が必要
```

# 9. Copilot Cowork の位置づけ

```text
Copilot Chat
  -> 質問に答える / 要約する / 文章を作る

Copilot Cowork
  -> 仕事を受け取る / 計画する / 複数ステップを進める
```

特徴:

- Frontier プレビュー
- Word, Excel, PowerPoint, Email, Scheduling などのスキル
- OneDrive 配下の Agent Skills
- `SKILL.md` による作業手順
- 仕様変更の可能性あり

# 10. まとめ

一枚絵の中心に置く言葉:

```text
Copilot は名前ではなく
居場所と役割で見る
```

吹き出し候補:

- 「あ、あの…名前より、どこで使うかを見るのです…」
- 「Microsoft 365 側は、社内データと権限が大事です…」
- 「作る側は Copilot Studio、コードは GitHub Copilot なのです…」
- 「Cowork は、仕事を進める方向の手がかりかもしれません…」
