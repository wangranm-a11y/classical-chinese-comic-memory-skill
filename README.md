# Classical Chinese Comic Memory Skill

> 中文名：古文漫画记忆  
> Turn classical Chinese recitation into sentence-by-sentence comic memory chains.

`guwen-comic-memory` is a Codex skill for memorizing 古诗文 / 文言文 with visual mnemonics.  
It helps an AI agent split a passage into small recall units, design a concrete comic panel for each sentence, and create an overview “story chain” that lets learners recite from images.

Instead of making pretty atmosphere art, this skill asks one sharper question:

> Can this picture help me reconstruct the exact original sentence?

---

## 中文介绍

背古文最痛苦的地方，常常不是“看不懂”，而是：

> 明明懂了，合上书就断片。

这个 skill 的思路是把每一句古文变成一个漫画格子。每格都要有一个足够具体、夸张、好记的视觉钩子，让学习者看到画面就能倒推出原句。

例如：

| 原文 | 不推荐 | 推荐的视觉钩子 |
|---|---|---|
| 上与浮云齐 | 画一座很高的楼 | 云拿着尺子认真量楼高 |
| 鼻息已雷鸣 | 画一个人在睡觉 | 鼾声变成雷暴和大喇叭 |
| 举世皆浊我独清 | 画屈原很孤独 | 整个世界都是泥，只有屈原干净发光 |

### 它适合什么？

- 古诗词全文背诵
- 文言文 / 古文散文段落背诵
- 大学语文、语文考试、默写复习
- 把 AI 生图从“画意境”改成“做记忆工具”

### 它会产出什么？

1. 逐句拆分后的记忆单元
2. 每一句的关键词与易错点
3. 每一句对应的漫画视觉梗
4. 可直接用于生图的 prompt
5. 一张串联整篇的总览图设计
6. 看图背诵的复习路线

示例输出：

| # | 原文 | 关键词 | 视觉梗 | 复习提示 |
|---|---|---|---|---|
| 1 | 举世皆浊我独清 | 浊 / 独清 | 世界变成泥浆，屈原独自发光干净 | 看到“泥世界 vs 清白人”回忆原句 |
| 2 | 众人皆醉我独醒 | 醉 / 独醒 | 众人倒在酒坛旁，屈原举着醒字灯笼 | 先背“皆醉”，再背“独醒” |

---

## English Introduction

This skill turns classical Chinese memorization into a visual recall workflow.

It is designed for passages where exact wording matters: poems, ci, fu, prose, dialogue passages, and exam recitation texts. The goal is not to illustrate the “vibe” of a text. The goal is to create visual indexes for exact recall.

### What makes it different?

Most image prompts for poetry ask for mood:

> “Draw a lonely poet by the river.”

This skill asks for memory hooks:

> “Show the whole world covered in mud while Qu Yuan alone remains clean and glowing, so the learner remembers 举世皆浊我独清.”

### What it generates

- sentence-by-sentence chunking
- visual mnemonic hooks
- keyword anchors for rare or easy-to-forget characters
- image-generation prompts for comic panels
- overview page prompts for the full story chain
- a review method for reciting from images

---

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

Or in Chinese:

```text
使用 $guwen-comic-memory，把《渔父》做成逐句背诵漫画脚本和生图提示词。
```

---

## Example Workflow

Input:

```text
Use $guwen-comic-memory to make a comic memorization plan for:
屈原曰：「举世皆浊我独清，众人皆醉我独醒，是以见放。」
```

Expected style of output:

| Text | Visual hook | Must show |
|---|---|---|
| 举世皆浊我独清 | A muddy gray world; Qu Yuan alone is clean and bright | mud world, clean figure, strong contrast |
| 众人皆醉我独醒 | Everyone is drunk around giant wine jars; Qu Yuan holds a glowing “醒” lantern | drunk crowd, awake Qu Yuan, lantern |
| 是以见放 | A banishment seal lands beside Qu Yuan as he walks toward the river | exile seal, river road |

---

## Prompt Pattern

The skill guides Codex to produce prompts like this:

```text
Use case: illustration-story
Asset type: sentence-by-sentence classical Chinese memorization comic
Primary request: Create a comic panel for 《渔父》.
Text to encode: "举世皆浊我独清"
Visual hook: The whole world is covered in dark mud, while Qu Yuan alone stands clean and glowing.
Key visual anchors: mud world, clean white robe, isolated Qu Yuan, contrast between 浊 and 清.
Style: Chinese ink-brush manhua, parchment background, readable caption ribbon.
Constraints: prioritize memorization over decorative scenery.
```

---

## Repository Structure

```text
.
├── README.md
├── LAUNCH_PLAN.md
└── guwen-comic-memory/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    └── references/
        └── method.md
```

---

## Important Note on Chinese Text in Images

AI image models may distort small Chinese characters. For exam-ready materials:

1. Generate the comic as a visual mnemonic base.
2. Inspect the image.
3. Overlay the exact original text with a real font.

The image should help memory; the final caption should preserve textual accuracy.

---

## Launch / 宣发一句话

中文：

> 我做了一个 AI skill，把古诗文背诵变成逐句漫画记忆：不是画“意境”，而是让每个画面都能倒推出原句。

English:

> I built a Codex skill that turns classical Chinese recitation into comic memory chains: every panel is designed to help you recover the exact line.

---

## License

No license has been added yet. If you plan to share this widely, add an open-source license such as MIT.
