# Nulab 公式の Backlog MCP Server

## 主題

- Nulab が 2025 年 5 月に公開した MIT ライセンスの MCP Server
- 多様な Backlog 情報を自然言語から扱える
- 公式公開でも保証・公式サポートはなく、権限確認と自己責任が必要

## 図解キーワード

- Backlog MCP Server
- GitHub 公開
- MIT
- stdio
- Streamable HTTP
- toolset／fields
- 読み取り／変更
- 自己責任

## 関係・流れ・対比

```text
AI agent → MCP Server → Backlog
                  ├ 読み取り
                  └ 作成・更新・削除
```

- 便利さ: project、issue、Wiki、document、Git、通知など
- 注意: 保証なし／公式サポートなし／内容と権限を確認

## グラレコ構図案

- 左: AI agent と Backlog をつなぐ MCP Server
- 中央: Docker／npx／Node.js、stdio／Streamable HTTP の入口カード
- 右: 読み取りと変更操作の分岐、注意ボックス、みくく
- みくくの表情・視線: 安心しすぎない慎重な表情で注意ボックスを見る
- 吹き出し: 「公式でも、権限の確認は大切です…」

## 正確性メモ

- 「公式」を保証や公式サポートがあるという意味にしない
- Docker 以外の起動方法も描く
- 対応対象をすべて長文で列挙せず、代表アイコンで示す
