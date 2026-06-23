# Method: sentence-to-comic memory for 古诗文

This method is distilled from practical examples of turning classical Chinese recitation passages into comic memory chains.

## Principle

Human recall is often stronger for concrete images than for abstract text. The goal is to transform each sentence into a specific, exaggerated, story-like picture so the picture becomes an index back to the original wording.

The output should help the user think: “I see this panel, therefore I remember this sentence.”

## Chunking

Chunk the source by recall units:

- One poem line, ci phrase, or couplet when the lines are parallel.
- One prose semantic unit.
- One dialogue move: question, answer, challenge, rebuttal, or closing action.
- One difficult rhetorical chain when the meaning depends on a sequence.

Avoid making one panel carry too many characters. A useful target is under about 14 Chinese characters of essential recall load per panel. Long captions can be placed under the image, but the visual hook should focus on the hardest words.

## Visual hook rules

### Direct-literal first

Prefer drawing what the words say. If the text says “举世皆浊我独清,” show a whole world full of mud while one person stands clean. Do not replace this with a vague “noble loneliness” scene.

### Keyword anchoring

Every fragile word should get a visual anchor:

- confusing words: turn them into distinct objects or actions
- rare words: enlarge them as labels or plaques
- numbers: make the number countable in the image
- names and allusions: show a mini-icon of the allusion
- contrasts: split the panel into two visible halves

### Useful absurdity

Exaggeration improves recall when it is tied to the exact phrase:

- “上与浮云齐”: clouds hold a ruler and measure the tower.
- “鼻息已雷鸣”: snoring becomes thunder from a giant trumpet.
- “回眸一笑百媚生”: surrounding beauties turn gray to show “无颜色.”

### Emotion alignment

Keep emotional tone faithful:

- exile, mourning, separation: sparse, gray, cold, much empty space
- freedom, awakening, transcendence: wide water, wind, light, motion
- argument or debate: opposing diagonals, facing figures, speech ribbons
- political satire: sharp contrast, broken symbols, tilted banners

## Prompt pattern

Use this pattern for single panels:

```text
Chinese ink-brush comic panel in manhua style, clean and expressive.
[Concrete scene that directly encodes the sentence.]
The scene visually encodes the classical Chinese text: "[original text]"
Key visual elements: [2-5 visual anchors]
Mood: [emotion]
Text annotation in the corner or caption ribbon: "[original text]"
Avoid: generic scenery, unrelated symbols, modern objects, illegible tiny text.
```

Use this pattern for overview pages:

```text
Portrait study-sheet comic page for memorizing [title] by [author].
Arrange [N] numbered panels connected by arrows.
Each panel encodes one sentence or semantic unit.
Top title: [title].
Include a bottom memory chain: [short structure].
Style: Chinese ink-brush manhua, parchment background, readable captions.
```

## Text accuracy warning

Image models often hallucinate or distort Chinese characters. For exam or recitation use:

1. Generate the image for visual hooks.
2. Inspect the text.
3. Overlay exact captions with a deterministic editor, real font, or document layout tool.

Do not treat model-rendered small Chinese captions as authoritative.

## Example: dialogue passage

For 《渔父》:

- “颜色憔悴，形容枯槁”: draw Qu Yuan gaunt at the riverbank.
- “子非三闾大夫与？何故至于斯？”: fisherman points to an official hat and a question mark.
- “举世皆浊我独清”: world is muddy gray; Qu Yuan alone is clear and bright.
- “淈其泥而扬其波”: fisherman stirs mud and raises waves.
- “新沐者必弹冠，新浴者必振衣”: clean bath scene with crown and robe being flicked clean.
- “沧浪之水清兮，可以濯吾缨；沧浪之水浊兮，可以濯吾足”: split clear-water/dirty-water panel, washing hat strings vs feet.

## Example: long argumentative prose

For 《与元九书》, turn the logic into a visual route:

1. 文与三才: heaven/sun-moon-stars, earth/five materials, human/six classics.
2. 诗感人心: poetry enters hearts from sages to ordinary people, animals, spirits.
3. 六义五音: words become six vertical threads; sound becomes five horizontal musical threads.
4. 周衰秦兴: song-collecting official’s gate is locked; political mirror ignored.
5. 丽而无讽: beautiful clouds, rivers, flowers, and snow surround a hollow center labeled “无讽.”
6. 李杜评议: Li Bai as brilliant strange talent; Du Fu as huge archive, then a small basket of socially corrective poems.

## Review route

Teach the user to review in three passes:

1. Structure pass: recite only the overview chain.
2. Picture pass: cover captions, name the original sentence from each image.
3. Repair pass: revisit only the panels that fail, strengthen their visual hook or enlarge the easy-wrong word.
