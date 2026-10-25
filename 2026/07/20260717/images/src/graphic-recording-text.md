# テキストを束ねて、渡し方を選ぶ：miku-text-bundle v1.5.1

## 主題

- 複数のテキストファイルを、ファイル境界を保った分割Markdownへ整理
- `v0.8.1`から`v1.5.1`へ、受け渡し契約と運用性を強化
- 出力先に応じて、`handoff`と`knowledge-source`を選択
- 中心の役割は「次の相手へ渡す直前まで整える」こと

## 図解キーワード

- 入力を収集
- 除外と文字コード
- `--dry-run`
- Part分割
- compact出力
- handoff
- Knowledge source
- 管理用index
- `--max-chars`は近似上限

## 関係・流れ・対比

### 全体の主図

```text
README / TODO / 設計資料 / ソースコード
                  ↓
        収集・除外・文字コード指定
                  ↓
       miku-text-bundle v1.5.1
          ┌───────┴────────┐
          ↓                ↓
       handoff       knowledge-source
          ↓                ↓
 text-bundle-001.md   knowledge-001.md
 prompt + 最終index   knowledge-002.md
          ↓           ＋ knowledge-index.md
     生成AIとの会話          ↓
                    Knowledge source用素材
```

### 2つの出力モード

| 観点 | handoff | knowledge-source |
| --- | --- | --- |
| 渡す先 | 生成AIとの会話 | Knowledge source |
| 会話用指示 | あり | なし |
| 診断情報 | 最終Part | 管理用index |
| 追跡 | ファイル単位中心 | 行範囲・文字オフセット |

### 約2か月の強化

```text
順番と終端を固定
  ↓
prefix・help contract・YAML front matter
  ↓
promptとindexをPartへ同梱
  ↓
dry-run・分割方針を改善
  ↓
Knowledge sourceモードを追加
```

## 役割分担・判断軸

| 要素 | 役割 |
| --- | --- |
| 入力収集 | 通常ファイルを広く候補化 |
| ignored | 最初から収集候補にしない |
| skipped | 候補に入ったが読み込めない |
| `--dry-run` | 書き込む前に規模を確認 |
| `--max-chars` | ソース本文量の近似上限 |
| handoff Part | 読み込み・応答契約を同梱 |
| Knowledgeファイル | 会話用指示なしの登録候補 |
| `knowledge-index.md` | 設定・対応・警告を管理 |

### 注意点

- `--max-chars`は生成Markdown全体の厳密な上限ではない
- Knowledge sourceへの変換・アップロードは呼び出し元の担当
- `knowledge-index.md`は登録対象ではない
- staleな番号付きファイルは削除せず警告する

## グラレコ構図案

- 左: README、TODO、設計資料、ソースコードの紙・ファイルアイコンと「収集」「除外」「文字コード」「dry-run」
- 中央: 大きな箱「miku-text-bundle v1.5.1」。入力が入り、下で2方向に分岐
- 右上: `handoff`カード。`text-bundle-001.md`、prompt、最終index、会話吹き出しへ矢印
- 右下: `knowledge-source`カード。番号付きMarkdownと別置きの`knowledge-index.md`、Knowledge source棚へ矢印
- 下部: 小さな成長タイムライン「順番と終端 → compact → dry-run・分割 → Knowledge source」
- 最も大きく見せる主図: 中央のツールから2つの出力モードへ分岐するフロー
- みくくの位置: 画面右端。手には何も持たず、身体と視線を左の分岐図へ向ける
- みくくの表情・視線: やさしい少し困り顔。中央の`miku-text-bundle`から2方向へ分かれる矢印を見る
- 吹き出し: 「あ、あの…渡す先に合わせて、包み方を選びます…！」

## 正確性メモ

- 対象は記事に明記されたNode.js版`v1.5.1`
- Java版は`v1.5.0`、Agent Skill版にも両runtimeを同梱
- Knowledge sourceの番号付きファイルには元パスと本文、分割時にはchunk番号と行範囲を記録
- UTF-16文字オフセットは管理用`knowledge-index.md`に記録
- 記事本文に明記された事実だけを使う
- 記事にないモデル名、数値、評価、生成環境を補わない
