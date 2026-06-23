---
name: guwen-comic-memory
description: Transform classical Chinese poems, prose, fu, and dialogue passages into sentence-by-sentence comic memorization plans. Use when the user wants to memorize 古诗文/文言文/大学语文背诵篇目 with visual mnemonics, generate comic panel scripts, image-generation prompts, overview story-chain pages, or review routes that map each original sentence to concrete visual hooks.
---

# Guwen Comic Memory

Use this skill to turn a classical Chinese passage into a visual memorization system: chunk the text, design one concrete comic panel per sentence or semantic unit, then produce prompts and a review route that let the user recover the original text from images.

Read `references/method.md` when you need the detailed principles, especially for long prose, dialogue, rare characters, or avoiding generic “atmosphere art.”

## Core rule

Prioritize recall over beauty. The comic should be a memory index for the exact words, not a decorative illustration of the general mood.

For each panel:

1. Make the visual hook direct and literal before poetic.
2. Anchor error-prone words with visible objects, labels, gestures, or exaggerated symbols.
3. Keep each panel to one sentence, paired line, question/answer, or compact semantic unit.
4. Include the original phrase as a caption or reserve a clean caption area for later text overlay.
5. Use a story-chain overview after the sentence panels.

## Workflow

### 1. Prepare the source text

Ask for or extract the exact version the user must recite. If multiple editions exist, do not silently mix them.

For long works, first list the selected recitation range and divide it into pages. A practical density is:

- poem or ci: 4–10 panels per overview page
- prose or fu: 6–9 panels per overview page
- dialogue: one question, answer, or rhetorical turn per panel

### 2. Chunk the passage

Chunk by memorization load, not by paragraph formatting.

- Poetry: usually one line per panel, or two parallel lines in one panel.
- Prose: one complete semantic unit per panel.
- Parallel prose/fu: one rhythmic pair or image cluster per panel.
- Dialogue: one speaker turn or question-answer move per panel.

When a unit exceeds about 14 Chinese characters, either split it or make the panel carry only the hardest keywords and leave exact text to the caption.

### 3. Design the visual hook

For every chunk, output:

- original text
- recall keywords
- visual hook
- must-show details
- mood
- text/caption instruction

Use absurdity when useful. “Clouds measuring a tower with a ruler” is often better for memory than a tasteful tower landscape.

### 4. Generate image prompts

When generating images, use a structured prompt:

```text
Use case: illustration-story
Asset type: sentence-by-sentence classical Chinese memorization comic
Primary request: Create [page/panel] for [work title].
Style/medium: Chinese ink-brush manhua, parchment study sheet, clear panel borders.
Composition/framing: [numbered panels, arrows, caption ribbons].
Text to encode: "[exact original text]"
Visual hook: [direct scene].
Key visual anchors: [2-5 anchors].
Mood: [emotion].
Constraints: prioritize memorization, keep captions readable, avoid generic landscape-only art.
```

For AI image models that render Chinese unreliably, treat in-image text as a guide only. If the result will be used for serious recitation, recommend a final pass that overlays exact text with a real font.

### 5. Build the overview chain

After panels are planned or generated, create an overview page with:

- title and author
- numbered panels in reading order
- arrows or a path through the page
- a one-line structure summary, such as “楼 → 声 → 人 → 心”
- a final “closed-eye recall route”

### 6. Review with the user

Give the user a short recitation routine:

1. Look at the overview and recite the structure.
2. Cover the captions and recall each sentence from the picture.
3. Open the captions and mark stuck panels.
4. Rehearse only the stuck panels, then recite the whole passage.

## Output format

For planning-only requests, use a table:

| # | 原文 | 关键词 | 视觉梗 | 画面必须出现 | 复习提示 |
|---|---|---|---|---|---|

For image-generation requests, provide one prompt per panel/page and then generate or save the images if an image tool is available.

For long passages, first produce page-level plans, then images page by page. Do not start a huge batch if the user is waiting interactively.

## Quality checks

Before finalizing, verify:

- Every sentence or required semantic unit has a visual anchor.
- Rare or easy-to-misremember words are visible, enlarged, or labeled.
- The sequence can be recited as a story, not as disconnected pictures.
- Captions match the user’s original text exactly, or text inaccuracies are clearly flagged.
- The emotional tone supports the passage: bright for freedom, gray for exile, tense for debate, sparse for mourning.
