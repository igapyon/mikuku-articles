# グラレコ制作用整理テキスト: interface 設計の順序が変わりつつある

## 1. 主題

- 中心は core logic。
- AI agent、CLI、MCP adapter、Web UI から同じ core logic を呼べる構造が扱いやすい。

## 2. 画像内キーワード候補

- 従来: Web UI → REST → CLI → AI
- これから: AI agent / tool → core logic
- AI 対応は後付けではない

## 3. 図解構成

```text
interface 設計の順序が変わりつつある
  ↓
重要な設計観点
  ↓
AI agent が扱いやすい tool へ
```

## 4. みくく吹き出し

```text
interface の順序が、少し変わってきています…！
```

## 5. 描画方針

- 横長ポスター構図
- 左から中央にグラレコ図解
- 右側にみくく
- 短い日本語ラベル中心
- 長文は入れすぎない
- 手描きホワイトボード風
