# 画像生成AI用プロンプト

Create a wide horizontal Japanese graphic recording explainer poster for a technical article.

## Canonical character prompt for Mikuku

Use the following as the canonical character reference. Same character, do not redesign, preserve character identity, preserve face shape, warm chestnut-brown eyes, caramel-chestnut twin-tails, black ribbons with deep-red trim, shy uneasy expression, soft Japanese anime technical explainer style.

```text
masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.
```

Do not let Mikuku hold any objects.

## Overall poster concept

Mikuku gently explains `miku-md2xlsx`, a small local tool that converts Markdown `.md` into Excel `.xlsx` workbooks.

The poster should feel like a warm hand-drawn graphic recording note for a Japanese technical article on note.com:

- cozy beige paper background
- soft brown and pastel accent lines
- hand-drawn boxes, arrows, small icons, sticky notes
- readable-looking short Japanese labels
- not a corporate slide
- not photorealistic
- not dark
- not sci-fi

## Layout

Wide 16:9 poster.

Left to center: the graphic recording content.
Right side: Mikuku, same character, looking toward the diagram and explaining with a small speech bubble.

Speech bubble text:

```text
あ、あの…Markdown の構造を
Excel に戻す出口なのです…！
```

## Content to visualize

Main title in Japanese:

```text
Markdown を Excel に戻す小さな出口
```

Show the core flow:

```text
Markdown
  → miku-md2xlsx
  → Excel workbook
  → 人間が確認・共有・編集
```

Include these short labels as hand-drawn notes:

- Markdown 正本
- 見出し / 段落 / 表
- link / image / merge marker
- `--out output.xlsx`
- single / heading
- Node.js v0.6.6
- Java v0.6.5
- 完全帳票ではない
- 編集できる土台
- local-first

Show a clear contrast:

```text
できること
- Markdown 表を Excel 化
- AI agent の調査表を共有
- miku-xlsx2md 由来 Markdown を戻す

しないこと
- pixel-perfect layout
- native formula / chart / shape
- 完全 round-trip
```

Show a small sheet-mode note:

```text
single: 1 worksheet
heading: 見出しごとに sheet 分割
```

Show merge marker note:

```text
[←M←] / [↑M↑] → merge range
```

## Text constraints

Use short Japanese labels only. Do not put long paragraphs inside the image.
The labels should be readable-looking, but exact OCR-perfect text is not required.

## Quality constraints

- high resolution
- cute Japanese anime technical explainer
- graphic recording illustration
- warm hand-drawn infographic poster
- Mikuku appears on the right side
- Mikuku has no pen, marker, pointer, notebook, board, or other held object
- hands should be simple and natural
- preserve Mikuku identity from the canonical character prompt
