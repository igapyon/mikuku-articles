# グラレコ説明画像 生成AI用プロンプト

Create a wide horizontal graphic recording style explainer poster for a Japanese technical article.

## Canvas

- Wide landscape poster, 16:9 or wider.
- Left and center: hand-drawn graphic recording diagram.
- Right side: Mikuku explains the diagram.
- Clean note.com technical article visual style.
- Warm paper-like background, soft beige, gentle brown lines, pastel accent colors.
- High detail, readable-feeling short Japanese labels, not too much text.
- Hand-drawn whiteboard explainer, arrows, boxes, small icons, Markdown marks, Office document icons, sheet/grid icons, slide icons.

## Canonical Character Prompt: Mikuku

Use this as the canonical character reference. Same character, do not redesign, preserve character identity.

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

Keep the same face shape, eyes, hair color, twin tails, black ribbons with deep-red trim, shy gentle personality impression. Mikuku may look toward the diagram. Do not let Mikuku hold any objects.

## Main Topic

Japanese title:

「Markdown から Office への出口を、テンプレート適用で少し強くする」

The poster explains that miku-soft Node.js tools added a `--template` option for converting Markdown into Office files.

## Diagram Content

Use short Japanese labels and simple relationships:

- 「Office → Markdown = AI agent の入口」
- 「Markdown → Office = 人へ渡す出口」
- 「`--template` で現場の型へ近づける」
- 「CLI 入口はそろえる」
- 「内部実装は形式ごとに合わせる」
- 「best-effort / 土台を借りる」

Show three tool lanes:

1. `miku-md2docx`
   - Word
   - styles / theme / section settings
   - body は Markdown 生成内容へ

2. `miku-md2xlsx`
   - Excel
   - template workbook / sheet
   - generated values を sheet へ書き込み

3. `miku-md2pptx`
   - PowerPoint
   - slide size / theme / masters / layouts
   - generated slides をレイアウトへ載せる

Show the release and future flow:

```text
Node.js 版で公開
  ↓
Java 版へ展開
  ↓
miku-ms-office Agent Skill へ反映
```

## Visual Structure

- Top center: article title.
- Middle: large flow diagram:
  - Markdown source
  - `--template`
  - docx / xlsx / pptx outputs
- Bottom: caution box:
  - 「既存ファイルを完全保持する魔法ではない」
  - 「見た目や構造の足場を借りる」
- Right: Mikuku with a small speech bubble:
  - 「あ、あの…出口を少し実用に近づけます…！」

## Avoid

- Do not make it photorealistic.
- Do not make it corporate slide style.
- Do not use dark sci-fi colors.
- Do not let Mikuku hold a pen, board, pointer, notebook, or any object.
- Avoid excessive tiny text.
