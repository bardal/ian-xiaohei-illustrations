# Ian Xiaohei Illustrations

> Turn the judgments, flows, states, and metaphors inside articles into clean, hand-drawn, absurd-but-fresh 16:9 article illustrations.
>
> 16:9 horizontal | Xiaohei IP | pure-white hand-drawn | sparse red/orange/blue annotations | Codex Skill

---

## What this repository is

Ian Xiaohei Illustrations is a Codex Skill that guides an AI Agent to generate article illustrations for blog posts, social posts, Notion documents, and methodology content.

It is not a generic illustration prompt, and it is not a PPT infographic template. The core goal is: first understand the cognitive anchors in the article, then turn one judgment, flow, structure, state, or metaphor into a memorable 16:9 hand-drawn explanation image.

The default visual IP is "Xiaohei" (小黑): a solid-black creature with white dot eyes, thin legs, and a blank expression. Xiaohei is not a mascot, not a sticker, and not a corner decoration — Xiaohei is an absurd worker seriously participating in how a system operates.

In one sentence: **let the AI not just "add an image," but actually draw out one key cognitive action from the article.**

---

## Who this is for

Ideal for:

- People writing articles who need in-body illustrations and blog images
- People creating knowledge-type content, methodology content, or AI workflow content
- People who want to turn abstract judgments into concrete metaphors
- People who want a visual style that is lighter, stranger, and more personally distinctive than PPT infographics
- People using Codex for content production who want a stable, reusable visual language

Not ideal for:

- People who want commercial illustration, brand key visuals, or polished flat-design illustrations
- People who want traditional PPT infographics, complex architecture diagrams, or flowcharts
- People who want children's cartoons, cute IPs, or meme-style imagery
- People who want to pack large amounts of body text, long explanations, or a full course into a single image
- People who need strictly editable vector source files

---

## What it produces

Default output:

- 16:9 horizontal article illustrations
- A shot list of 4–8 images for one article
- For each image: theme, core meaning, structure type, Xiaohei's action, and suggested annotation labels
- Final PNG files saved to `assets/<article-slug>-illustrations/` in the workspace

Does not produce:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable graphics
- Commercial posters or cover key visuals
- Dense text-heavy infographics

---

## Visual style

This skill defaults to Ian's "Xiaohei absurd article illustration" style:

- Pure white background — no paper texture, off-white, shadows, or gradients
- Black hand-drawn line art, thin lines, slight wobble
- Lots of white space; main subject covers roughly 40%–60% of the canvas
- Sparse red, orange, and blue handwritten annotations
- One image expresses only one core action, structure, state, or metaphor
- Xiaohei must participate in the core action and cannot be merely decorative
- Absurd, creative, clean — but not childish or cute

---

## Example output

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sort by Purpose

![Sort by Purpose](examples/images/02-sort-by-purpose.png)

### One Fish Many Uses

![One Fish Many Uses](examples/images/03-one-fish-many-uses.png)

### Handoff Path

![Handoff Path](examples/images/04-handoff-path.png)

### Information Well

![Information Well](examples/images/05-information-well.png)

### Idea Press

![Idea Press](examples/images/06-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/07-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/08-trust-bridge.png)

These images are style calibration examples, not composition templates. When using the skill, invent fresh metaphors from the current article — do not copy the objects or compositions from these examples.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/helloianneo/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

### Codex

Copy the skill to your Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

After installation, use it in Codex:

```text
Use $ian-xiaohei-illustrations to design and generate 5 Xiaohei absurd article illustrations for this article.
```

### Claude Code / skills.sh

Install as a Claude skill:

```bash
npx skills add helloianneo/ian-xiaohei-illustrations@ian-xiaohei-illustrations
```

---

## How to use

### Shot list only

```text
Use $ian-xiaohei-illustrations — do not generate images yet.
Analyze the article below and identify where illustrations would add value. Output a shot list of about 5 images.
For each image specify: which paragraph it follows, theme, core meaning, structure type, what Xiaohei is doing, and suggested annotation labels.

<paste article here>
```

### Generate article illustrations directly

```text
Use $ian-xiaohei-illustrations to generate 4 Xiaohei absurd article illustrations for the article below.
Requirements: 16:9 horizontal, pure white background, black hand-drawn line art, sparse red/orange/blue handwritten annotations.

<paste article here>
```

### Generate one image for a single concept

```text
Use $ian-xiaohei-illustrations to generate one article illustration for: "Trust is not proclaimed — it is laid down one piece of evidence at a time."
The image should be absurd but clean. Xiaohei must perform the core action.
```

### Remove a title or unwanted text from an image

```text
Use $ian-xiaohei-illustrations to edit this image and remove the "flowchart" title in the top-left corner. Keep everything else unchanged.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

The skill's workflow is:

1. Read the article, Markdown content, Notion page, screenshot, or user-provided theme
2. Extract core arguments, cognitive turning points, structural flows, and illustratable paragraphs
3. Output a shot list: each image captures only one cognitive anchor
4. Choose a structure type for each image: Workflow, System slice, Before/after contrast, Role state, Conceptual metaphor, Method layers, Map route, or Mini comic strip
5. Invent a fresh low-tech, absurd-but-plausible physical metaphor
6. Give Xiaohei the core action
7. Generate each image separately using the image model
8. Check against the QA checklist: white background, white space, Xiaohei's action, annotations, not-PPT feel, not a copy of old examples
9. Save the final PNGs and report their purpose and path

---

## Directory structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
├── ian-xiaohei-illustrations/
│   ├── SKILL.md
│   ├── agents/
│   │   └── openai.yaml
│   ├── assets/
│   │   └── examples/
│   └── references/
│       ├── style-dna.md
│       ├── xiaohei-ip.md
│       ├── composition-patterns.md
│       ├── prompt-template.md
│       └── qa-checklist.md
└── skills/
    └── ian-xiaohei-illustrations/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        ├── assets/
        │   └── examples/
        └── references/
            ├── style-dna.md
            ├── xiaohei-ip.md
            ├── composition-patterns.md
            ├── prompt-template.md
            └── qa-checklist.md
```

The Codex skill directory is:

```text
ian-xiaohei-illustrations/
```

The Claude skill directory (for skills.sh packaging) is:

```text
skills/ian-xiaohei-illustrations/
```

The root-level README, LICENSE, NOTICE, and examples folder are GitHub documentation only.

---

## Notes

- Shorter annotation text in images produces more stable results.
- Each image communicates only one core structure; do not turn an article into an instruction manual.
- Xiaohei must perform the core action; if removing Xiaohei leaves the image completely intact, Xiaohei is too decorative.
- Example images are for calibrating line density, white space, color restraint, and Xiaohei's involvement — do not copy their compositions.
- AI image models may produce garbled text, hallucinated labels, style drift, or unwanted titles; always review generated images.
- If text errors are severe, reduce the number of annotation labels and regenerate.

---

## Related projects

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — Hand-drawn technical PPT-style page generation Skill
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — Curated collection of Claude Code Skills / Agents / Plugins
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — Obsidian + Claude AI personal knowledge base guide

---

## About the author

**Ian** — Product Designer / Solo-business practitioner / AI Builder

Building a one-person company with an AI team.

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Website: [www.ianneo.xyz](https://www.ianneo.xyz)
- WeChat: `ianneoxyz`
- Email: hello.neoc@gmail.com

---

## Keep exploring

This Xiaohei illustration Skill is just one small tool in the personal production system I'm building with AI.

If you're also using AI for content, knowledge bases, workflows, or product building, visit my website: [www.ianneo.xyz](https://www.ianneo.xyz).

If you'd like to observe first, follow me on [X/Twitter](https://x.com/ianneo_ai).

To learn about the Indie Builders Club, add me on WeChat: `ianneoxyz` with the note "OPC".

<p>
  <img src="assets/ian-wechat-qr.jpg" alt="Ian WeChat QR code" width="120">
</p>

Can't scan? Search WeChat for: `ianneoxyz`.

---

## License

MIT License. See [LICENSE](LICENSE).
