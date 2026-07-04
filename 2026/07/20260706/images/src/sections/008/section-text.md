# 008. --help 出力の確認

## 主題

- CLI 契約を raw help として残す
- 人間にも AI agent にも参照しやすい

## help で見るもの

- Usage
- Purpose
- Options
- Output contract for agents
- Front matter fields
- Exit codes

## Node.js と Java の違い

| 共通 | Java 固有 |
| --- | --- |
| 単一 workbook 変換 | `--input-directory` |
| `--out`, `--zip` | `--output-directory` |
| mode / formatting / front matter | `--recursive`, `--verbose` |

## 重要ポイント

- raw help は契約文
- Java 固有オプションを Node.js に混ぜない

## 吹き出し案

「help は長いけれど、CLI の約束がまとまっています…」