# Classical Chinese Comic Memory Skill

`guwen-comic-memory` is a Codex skill for turning 古诗文 and 文言文 recitation passages into sentence-by-sentence comic memory chains.

Instead of asking an image model to “draw the mood,” the skill asks it to build visual indexes for exact recall:

- split the passage into small memorization units
- design a concrete visual hook for every sentence
- anchor rare and easy-to-forget words with visible objects or labels
- create image-generation prompts for panels or overview pages
- give the learner a review route for recitation

The method is especially useful for Chinese literature exams, 大学语文 recitation tasks, and anyone who remembers images faster than raw text.

## Install

Copy the skill folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R guwen-comic-memory ~/.codex/skills/
```

Then ask Codex:

```text
Use $guwen-comic-memory to turn 《兰亭集序》 into a sentence-by-sentence comic memorization plan.
```

## What it produces

For each sentence or semantic unit:

| 原文 | 关键词 | 视觉梗 | 画面必须出现 | 复习提示 |
|---|---|---|---|---|
| 举世皆浊我独清 | 浊 / 独清 | 整个世界都是泥，只有屈原发光干净 | 泥世界、清白人物、强对比 | 看到“泥 vs 清”回忆原句 |

For image generation, it creates structured prompts for ink-wash manhua panels and story-chain overview pages.

## Why this works

The core idea is simple: make the image carry the wording. A panel should not merely represent the “feeling” of a passage; it should contain enough concrete hooks that the learner can reconstruct the sentence from the picture.

Good mnemonic panels are often literal, exaggerated, and a bit silly:

- clouds measure a tower with a ruler for “上与浮云齐”
- snoring becomes thunder for “鼻息已雷鸣”
- a muddy world contrasts with one clean person for “举世皆浊我独清”

## Repository structure

```text
guwen-comic-memory/
  SKILL.md
  agents/openai.yaml
  references/method.md
```

## Notes

AI image models may distort small Chinese characters. For exam-ready materials, generate the comic as a visual base, then overlay the exact original text with a real font.
