# たくさんの資料を AI アシスタントへ渡す、その少し手前

## 主題

- `miku-ai-assistant-builder-skills v0.8.0`
- 多数の資料ファイルを、AI アシスタントへ登録しやすい件数と形式へ整える
- AI アシスタント自体を作るのではなく、配備前の準備を担当する小さな Agent Skill
- 自動でまとめる資料と、人が丁寧に準備した資料を両立する

## 図解キーワード

- 多数のファイル
- 登録件数の上限
- `miku-text-bundle`
- 少数の Knowledge
- Markdown → DOCX
- `manual-input/`
- `upload/`
- Agent Builder
- Gem Classic
- 人が最終確認

## 関係・流れ・対比

### 主流れ

```text
Markdown・ソースコード・メモ
          ↓
    miku-text-bundle
          ↓
少数の Knowledge 向け Markdown
          ↓
Agent Builder: miku-md2docx → DOCX
Gem Classic: Markdown または DOCX
          ↓
       upload/
          ↓
  人が確認してサービスへ登録
```

### 人が準備した資料との合流

```text
人が丁寧に準備した資料
Markdown・Word・Excel・PowerPoint
          ↓
     manual-input/
          ↓
自動でまとめた Knowledge と合流
```

### 二段階

```text
第 1 段階
配備先と入力範囲を確認
自動処理対象を決定
manual-input/ を用意
いったん停止
          ↓ 人が資料を追加、または「追加なし」を確認
第 2 段階
件数を確認
バンドル・形式変換
upload/ と設定用 Markdown を作成
```

## 役割分担・判断軸

| 要素 | 役割 |
|---|---|
| `miku-text-bundle` | 多数のテキストを少数の Knowledge 向け Markdown へまとめる |
| `miku-md2docx` | Agent Builder 向けに Markdown を DOCX へ橋渡しする |
| `manual-input/` | 人が準備した Markdown や Office 文書を受け取る |
| `upload/` | 最終的な登録候補をまとめる |
| 人 | 内容を確認し、サービスへアップロード・設定する |

### 配備先の違い

- Microsoft 365 Copilot Agent Builder
  - 端末から直接アップロードする Knowledge は最大 20 件
  - 対応形式に Markdown が含まれない
  - Knowledge 用 Markdown を DOCX へ変換
- Google Gemini Gem Classic
  - Markdown のまま使うか DOCX へ変換するかを選ぶ
  - 実際の件数はアカウント、プラン、管理者設定、画面で確認

### 大事な注意

- 登録できたことと、全内容が毎回参照されることは同じではない
- ファイル添付を利用できるライセンスや利用環境が必要
- 自動アップロードや共有は行わない
- 元のフォルダと、人が追加した原本は変更しない
- スキル全体はベータ版

## グラレコ構図案

- 左: 小さなファイルカードが多数並ぶ。「Markdown」「Code」「Memo」と、人が準備した「Word」「Excel」「PowerPoint」
- 中央: 最も大きい主図。二本の入力が合流する配備準備パイプライン
  - 上段: 多数ファイル → `miku-text-bundle` → 少数の Knowledge
  - 下段: 人が準備 → `manual-input/`
  - 合流後: Markdown → DOCX、`upload/`
- 右: 「Agent Builder」と「Gem Classic」の二つの到着先。直前に人の確認を表すチェックマーク
- 最も大きく見せる主図: 「多数のファイルを減らし、形式を橋渡しする」中央の流れ
- みくくの表情・視線: 右下。少し心配そうだが優しい表情で、左上の中央パイプラインを見る。物は持たない
- 吹き出し: 「あ、あの…資料が入口で迷子にならないように、少し手前を整えます」

## 正確性メモ

- 記事本文に明記された事実だけを使う
- Agent Builder の 20 件は端末から直接アップロードする埋め込みファイルの件数
- Microsoft のファイルサイズ値は公式文書間に差があるため、画像では強調しない
- Gem Classic の固定登録件数を画像内で断定しない
- Knowledge の内部検索方式を断定しない
- 記事にない機能、モデル名、価格、評価を足さない
