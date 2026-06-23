# Launch plan

## Positioning

一句话：把古诗文背诵从“硬背文字”变成“看漫画回忆原句”的 Codex skill。

Core audience:

- Chinese literature students preparing recitation or默写
- 大学语文 / 高中语文 learners
- AI educators interested in memory workflows
- Codex / Claude / AI-agent users who collect practical skills

## Launch angle

Lead with the pain:

> 古文最难的不是理解，是“明明懂了但背不出来”。这个 skill 把每一句变成一个漫画格子：看到画面，就能倒推出原句。

Then show the mechanism:

1. 拆句：一句或一个语义单元一格
2. 视觉钩子：直译、夸张、关键词锚定
3. 总览图：把整篇变成一条故事链
4. 复习：遮住字幕，看图回忆原文

## Demo content

Best first demos:

- 《渔父》：对话体强，价值观冲突明显，适合展示“举世皆浊我独清”等视觉梗
- 《临江仙·夜归临皋》：短，传播快，4 格就能看懂
- 《与元九书》：展示它不只会诗词，也能处理论说类长文逻辑

## Suggested posts

### 小红书 / 即刻 / 朋友圈

标题：

> 我做了个 AI skill：把古文背诵变成漫画记忆

正文：

> 背古文最痛苦的是：每个字都认识，但合上书就断片。  
> 我试了一种方法：把每一句拆成漫画格子，每格必须有一个“能倒推出原句”的视觉梗。  
> 比如“举世皆浊我独清”不是画一个忧郁诗人，而是画整个世界都变成泥浆，只有屈原一个人干净发光。  
> 这个 Codex skill 会自动完成：拆句 → 设计视觉梗 → 写生图 prompt → 做复习路线。  
> 适合古诗文背诵、大学语文、文言文默写。  
> GitHub: [repo link]

配图建议：

1. 一张总览漫画
2. 一张“原句 → 视觉梗 → 画面”的对照图
3. 一张 README 截图

### Twitter / X

> I made a Codex skill that turns classical Chinese recitation into comic memory chains.  
> It chunks each sentence, designs literal + exaggerated visual hooks, and generates prompts for mnemonic comic panels.  
> The goal: see the image, recall the exact line.  
> GitHub: [repo link]

### Product Hunt / Hacker News style

Frame it as “AI as a memory-system designer,” not just image generation.

> This is a tiny skill for using AI to build visual mnemonics for classical text memorization. It focuses on text recall rather than pretty illustrations: every panel must encode one sentence with explicit visual anchors.

## Short demo script

1. Paste a passage, e.g. 《渔父》.
2. Ask: “Use $guwen-comic-memory to create a sentence-by-sentence comic memorization plan.”
3. Show the table of panels.
4. Generate one overview page.
5. Cover captions and recite from images.

## Next improvements

- Add sample outputs for 3 public-domain passages.
- Add a deterministic caption-overlay script for exact Chinese text.
- Add templates for overview pages: 4-panel, 8-panel, and long-prose layouts.
- Package examples as a small gallery.
