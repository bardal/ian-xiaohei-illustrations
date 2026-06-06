---
name: ian-xiaohei-illustrations
description: Generate Ian-style article illustrations. Use when the user asks to generate "absurd", "Xiaohei", "hand-drawn", "article illustration", "blog illustration", "illustration suggestions", "shot list", or "remove title / edit image" tasks for articles, posts, blogs, Notion documents, workflows, methodologies, processes, structures, states, metaphors, or viewpoints; defaults to the Xiaohei IP, pure-white hand-drawn style, sparse red/orange/blue annotations, clean and imaginative visual language.
---

# Ian Xiaohei Absurd Article Illustrations

## Core purpose

Design and generate 16:9 horizontal article illustrations. The goal is not commercial illustration, PPT infographics, or cute cartoons — it is to take a key judgment, process, structure, state, or metaphor from an article and turn it into a clean, absurd, creative, readable-but-not-instructional hand-drawn explanation.

The default visual IP is "Xiaohei" (小黑): solid black, white dot eyes, thin legs, blank expression — seriously doing something slightly absurd. Xiaohei must participate in the core action of the image and must not simply stand to the side as decoration.

## Read these references first

Load on demand; do not flood the context all at once:

- `references/style-dna.md`: Style DNA, colors, text, prohibitions.
- `references/xiaohei-ip.md`: Xiaohei's appearance, personality, action pool, and prohibitions.
- `references/composition-patterns.md`: Structure types, original metaphor method, and no-copy rules.
- `references/prompt-template.md`: Single-image generation prompt template.
- `references/qa-checklist.md`: Post-generation QA and iteration rules.
- `assets/examples/`: For infrequent visual calibration only; not part of the default generation path. Do not copy compositions, objects, or labels from these examples.

## Workflow

### 1. Digest the article

Read the article, link, Notion page, Markdown file, or screenshot content the user provides. Extract:

- What the core argument is
- Which paragraphs carry the key cognitive shift
- Which content is worth illustrating
- Which parts are better left as text, without an image

Do not illustrate every paragraph. Prioritize "cognitive anchors": core judgments, two-point breakdowns, input-output loops, branching paths, before/after contrasts, one-source-many-uses, handoff paths, common pitfalls, role state changes.

### 2. Output a shot list first

If the user says only "analyze what needs illustrating / think about where to add images," provide a shot list first. For each image, specify:

- Which paragraph it follows
- The image theme
- The core meaning
- The structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested short annotation labels

Default: 4–8 images. For short articles: 1–3. Do not go above 9 even for long articles. Enough is enough; avoid turning the article into a picture book.

### 3. Generate individual images

If the user explicitly says "generate / output / make image / create for me," do not pause to ask for confirmation; use the built-in `image_gen` to generate each image separately. Do not combine multiple images into one.

Each image communicates only one core structure. The prompt must include:

- 16:9 horizontal article illustration
- Pure white background
- Black hand-drawn line art
- Sparse red/orange/blue handwritten annotations
- Lots of white space
- Xiaohei as the core action subject
- No PPT, no commercial illustration, no childish cute style, no complex architecture, no type label in the top-left corner

Do not copy previous examples. Examples provide only style density and Xiaohei participation quality — do not reuse known compositions such as "conveyor belt breakpoints / Xiaohei pulling a lever / material fish / stamp toolbox / common-pitfalls path" unless the user explicitly requests a remake. Always invent a fresh, strange-but-plausible metaphor from the current article.

### 4. QA and iteration

After generating, check `references/qa-checklist.md`. If any of the following appear, prefer regeneration or local editing:

- Xiaohei is only decoration
- The canvas is too crowded
- Looks like a flowchart or PPT
- Too many annotations or severe text errors
- Top-left corner shows a type label ("Common Pitfalls / Workflow / System Architecture")
- Art style is too cute, childish, or rigid
- Background is not clean white

### 5. Save and deliver

If the user is working in a workspace, copy the final images to:

```text
assets/<article-slug>-illustrations/
```

Name them in sequence:

```text
01-topic-name.png
02-topic-name.png
```

Keep the original generated files; do not overwrite existing assets unless the user explicitly asks.

## Output format

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- The purpose of each image
- The save path
- Which images are most solid and which are optional

Do not write lengthy explanations of style theory; let the images speak for themselves.
