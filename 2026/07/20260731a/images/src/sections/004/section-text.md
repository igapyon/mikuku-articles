# Agent Skill は薄く、文字コード処理は CLI へ

## 主題

- Skill は「いつ・どの操作・どの範囲」を判断する薄い入口
- 文字コードや revision、atomic mutation などの繊細な処理は CLI runtime が担当
- 制御用 request は UTF-8 JSON、対象ファイルの表現だけを CLI に任せる

## 図解キーワード

- Agent Skill
- CLI runtime
- 役割分担
- UTF-8 JSON
- 対象ファイル
- 繊細な境界

## 関係・流れ・対比

| Agent Skill | CLI runtime |
| --- | --- |
| 発火・操作・範囲 | encoding・rule・revision |
| 読む範囲 | patch・atomic mutation |
| 固定 launcher | diagnostics |

## グラレコ構図案

- 左: AI agent の依頼
- 中央: 薄い Agent Skill と厚い CLI runtime の二層
- 右: Windows-31J の対象ファイル
- みくくの表情・視線: 二層の境界をやさしく見る
- 吹き出し: 「繊細な処理は CLI に任せるのです…」

## 正確性メモ

- 制御経路は UTF-8 JSON
- Skill 自身へ文字コード処理を実装していない
