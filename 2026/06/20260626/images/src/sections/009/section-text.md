# AI agent との接点

- AI agent が Web 画面を操作するには、ブラウザ操作基盤が必要
- クリック、入力、スクリーンショット、DOM、アクセシビリティ、ネットワーク確認
- E2E テストで必要だった能力と近い

用途別の入口:

| 入口 | 向く用途 |
| --- | --- |
| Playwright MCP | AI agent にブラウザ操作を渡す |
| @playwright/cli | coding agent に軽く操作させる |
| @playwright/test | 保守する正式テスト |
| playwright | 一回限りの自動化スクリプト |

注意:

- 認証情報
- 操作範囲
- 実行環境
- 外部サービスへの影響
