# グラレコ制作用整理テキスト

## 1. 大テーマ

- Markdown から Office へ戻す「出口」
- Node.js 版 miku-soft に `--template` を追加
- 変換だけでなく、現場の見た目や型へ近づける
- Word / Excel / PowerPoint は同じ Office でも文書モデルが違う
- CLI の入口はそろえる、内部実装は形式ごとに合わせる

```text
Office → Markdown = AI agent の入口
Markdown → Office = 人へ渡す出口
```

## 2. きっかけ

- `miku-md2xlsx` の記事に予想より反応
- Excel には現場感がある
- 表、一覧、台帳、チェックリスト、WBS、比較表
- AI agent が作った Markdown を Office として渡したい場面がある

## 3. なぜテンプレート適用が必要？

- 単純変換だけでは現場ファイルの型に届きにくい
- Word: 見出しスタイル、余白、フォント、セクション
- Excel: 列幅、行高、罫線、シート設定
- PowerPoint: テーマ、マスター、レイアウト、プレースホルダー

```text
Markdown の内容
  ↓
Office 生成
  ↓
テンプレートの土台を借りる
  ↓
現場に置きやすいファイル
```

## 4. 3ツールの役割

| tool | 出力 | テンプレートの借り方 |
| --- | --- | --- |
| `miku-md2docx` | Word | styles / theme / section settings を引き継ぎ、本文は生成内容へ |
| `miku-md2xlsx` | Excel | template workbook / sheet に生成値を書き込み |
| `miku-md2pptx` | PowerPoint | slide size / theme / masters / layouts / placeholders を利用 |

## 5. 大事な対比

```text
同じ `--template`
  ├─ CLI 入口: そろえる
  └─ 内部実装: そろえすぎない
```

```text
テンプレート適用
  = 既存ファイルを完全保持する魔法ではない
  = 見た目や構造の足場を借りる best-effort
```

## 6. 公開状況と次の流れ

- Node.js 版で先行公開
- `miku-md2docx` v0.9.5
- `miku-md2xlsx` v0.7.0
- `miku-md2pptx` v0.5.0
- Java 版はこれから
- その後 `miku-ms-office` Agent Skill へ反映

```text
Node.js 版で試す
  ↓
Java 版へ展開
  ↓
Agent Skill に判断ルールを追加
  ↓
AI agent が迷わず使える
```

## 7. まとめ

- Markdown から Office へ戻す出口にはニーズがありそう
- テンプレート適用で実用に少し近づく
- Word / Excel / PowerPoint はそれぞれ自然な単位が違う
- 共通 API に見せつつ、内部は形式ごとに無理をしない
- 機能だけでなく Agent Skill の説明層も大切
