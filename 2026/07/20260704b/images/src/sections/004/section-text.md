# 対応範囲外または限定対応

- Word 固有の細かなレイアウトは対象外
- template input は対象外
- header / footer / page number は対象外
- table alignment / merged cells は対象外または非保持
- raw HTML は限定対応

| 対応しないもの | 理由 |
| --- | --- |
| 厳密な帳票設計 | Markdown 標準構造ではない |
| remote image | download しない |
| SVG 安全表示 | Word 側互換に依存 |
| round-trip 完全復元 | 元 DOCX 再現ではない |

