# 生成AI向け情報

- AI agent が説明や実行を間違えないための固定情報
- conversion direction を明示
- release tag と artifact name を固定
- `--out` 必須
- heading level 1/2 slide rule
- image handling
- unsupported scope
- raw `--help` output
- runtime differences

AI agent の誤解防止:

| 情報 | 防ぐ誤解 |
| --- | --- |
| version | 実装混同 |
| direction | `md -> pptx` と `pptx -> md` の取り違え |
| `--out` | stdout にPPTXが出るという誤解 |
| image rules | remote image 自動取得の誤解 |
| path resolution | Node.js / Java の違い |
| Java parser caveat | full GFM parity の誤解 |

まとめ:

```text
明示する
  ↓
agent が invent しにくい
  ↓
安全に実行・説明できる
```
