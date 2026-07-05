# 表現対応表

- Markdown 表現が PowerPoint でどう出るか
- Node.js v0.2.2 と Java v0.2.3 を分けて説明
- Java parser は intentionally small
- full `remark-gfm` AST behavior とはまだ同一ではない

主要対応:

| Markdown | PowerPoint |
| --- | --- |
| `#` / `##` | new slide |
| paragraph | editable slide text |
| list | bullet paragraph |
| pipe table | native PowerPoint table |
| `[text](url)` | external hyperlink |
| local image | embedded image |
| speaker-notes comment | speaker notes |

注意:

- remote image は skipped with warning
- absolute image path も skipped
- inline image inside paragraph は ignored
- ordered list は bullet-style へ正規化される代表ケースあり
