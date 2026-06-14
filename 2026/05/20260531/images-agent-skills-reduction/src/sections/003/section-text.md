# 003 Agent Skills では何がトークンになるのか

## 主題

Skill が発火すると、`SKILL.md` を入口に、必要に応じて参照ファイルやテンプレート、例文が文脈へ入る。

## 重要キーワード

- `SKILL.md`
- `references/`
- `templates/`
- `examples/`
- `assets/`
- `scripts/`
- CLI
- MCP server
- 入口情報
- 参照範囲

## 階層

```text
1. 不要な Skill を発火させない
2. 必要な Skill だけ発火
3. SKILL.md を軽くする
4. 必要な参照だけ読む
5. 蒸留された入口から読む
```

## 役割分担

| 要素 | 役割 |
| --- | --- |
| `SKILL.md` | 入口 |
| `references/` | 詳細知識 |
| `templates/` | 出力の型 |
| `examples/` | 書きぶり |
| `assets/` | 出力用素材 |
| `scripts` / CLI / MCP | 実行処理 |

## 吹き出し案

「まず、何が文脈に入るのかを見るのです…」
