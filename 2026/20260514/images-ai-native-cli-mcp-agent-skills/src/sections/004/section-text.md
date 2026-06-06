# グラレコ制作用整理テキスト: 実運用では MCP server は CLI adapter になりやすい

## 1. 主題

- MCP server が既存 CLI を呼ぶ構成は多い。
- 下にある CLI の入出力が安定しているほど、MCP adapter は薄くできる。

## 2. 画像内キーワード候補

- MCP server
- CLI wrapper
- rg / git / ffmpeg / docker
- machine-readable
- thin adapter

## 3. 図解構成

```text
実運用では MCP server は CLI adapter になりやすい
  ↓
重要な設計観点
  ↓
AI agent が扱いやすい tool へ
```

## 4. みくく吹き出し

```text
下の CLI が安定していると、MCP も作りやすいです…！
```

## 5. 描画方針

- 横長ポスター構図
- 左から中央にグラレコ図解
- 右側にみくく
- 短い日本語ラベル中心
- 長文は入れすぎない
- 手描きホワイトボード風
