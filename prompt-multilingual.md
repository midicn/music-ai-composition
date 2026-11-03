---
id: "prompt-multilingual"
site: "ai"
cat: "B"
title: "多语言提示"
title_en: "Prompting Across Languages"
summary: "换语言不只是换字幕，声调、重音与音节数都会改变结果。"
summary_en: "Changing language changes tone, stress and syllable count, not just the words on the screen."
level: "standard"
tags: ["多语言", "提示词", "声调", "重音"]
tags_en: ["multilingual", "prompting", "tone", "stress"]
alias: ["多语言提示", "中英提示", "multilingual prompting"]
order: 131
links: ["[[glossary:phrase]]", "[[glossary:word-painting]]", "[[instrument:voice]]"]
instances: []
sources: ["https://dreamtonics.com/svstudio-resources/", "https://www.w3.org/TR/speech-synthesis/", "https://help.udio.com/en/articles/10716221-create-a-song-with-your-own-lyrics"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "多语言提示与歌词需分别核对语言支持、音素和发音控制；普通器乐播放不包含语言辨识证据，更不能证明声调、重音或连读正确。"
---

::: zh
## 换语言，唱出来的不是同一句

同一段旋律填中文词和英文词，重音落点、字数和换气位置全变。把中文提示逐词翻成英文，模型得到的不是同一个要求。语言影响的是音节结构、声调走向，以及提示词在训练数据里的权重。

## 三种情况

| 情况 | 写法要点 | 常见偏差 | 检查点 |
|---|---|---|---|
| 中文提示、中文演唱 | 标声调与句读，控制每句字数 | 倒字、吞韵母、句尾上扬 | 逐字对照歌词听声调 |
| 英文提示、英文演唱 | 标重音与连读，拆开长从句 | 功能词被重读、辅音簇糊 | 关键词是否落在强拍 |
| 混合语言 | 指定主语言与切换位置 | 主语言吞掉第二语言、口音漂移 | 切换处是否换气、音色一致 |

## 中文：声调先于音色

普通话的四个声调常与旋律走向打架。一句词的字数、句读和押韵位置要写清楚，否则模型会为旋律改声调，听起来像另一个词。多音字与轻声单独标注，副歌叠唱处最容易糊。歌词按句断开，比整段粘贴更容易让模型保住句尾。

## 英文：重音决定可懂度

英文的关键在词重音与句重音。提示里给出重读词、避免连续三四个辅音、把长句拆短，比堆“clear vocal”有效。连读与弱读带来母语感，却会在快速段落牺牲清晰度，按用途取舍。人名与地名要标读音，否则默认重音可能落在错误音节。

## 混合语言的偏差

中英混写时，模型常把提示的主语言当作演唱主语言，第二语言只分到很短片段，或带上主语言的口音。把两种语言的歌词分段写，标出切换行，再补一句“第二段为英文”，比一行混排更稳。地区口音也要单独说明，不然默认腔调可能与角色设定不符。遇到一句里同时出现两种语言、歌词需要严格押韵，或交付要过母语审听，混写的不确定性通常超过收益。拆成两个单语版本，各自生成，再在后期拼接，反而更快。语言标签不是装饰，写错会让整段的发音策略偏离。
:::

::: en
## A new language is a new performance

The same melody with Mandarin and English lyrics changes stress placement, syllable count and breathing points. Translating a Chinese prompt word for word does not give the model the same request. Language changes syllable structure, tone movement and how strongly prompt words weigh in training data.

## Three cases

| Case | Writing focus | Typical drift | Check |
|---|---|---|---|
| Chinese prompt, Chinese vocal | Mark tones and phrasing, cap syllables per line | Wrong tone, swallowed finals, rising line ends | Compare tone word by word against the lyric |
| English prompt, English vocal | Mark stress and liaison, split long clauses | Function words stressed, consonant clusters blur | Do keywords land on strong beats |
| Mixed language | Name the lead language and switch points | Lead language swallows the second, accent drifts | Breath and timbre at the switch |

## Chinese: tone before timbre

The four Mandarin tones often fight the melodic line. State syllables per line, phrase breaks and rhyme positions, or the model will bend tones to the tune and the word will sound like another. Mark polyphonic characters and neutral tones separately; stacked chorus vocals blur first. Line-by-line lyrics hold their endings better than one pasted block.

## English: stress carries intelligibility

English hinges on word and sentence stress. Name the stressed words, avoid three or four consonants in a row, and shorten long clauses; that does more than piling on "clear vocal". Liaison and weak forms sound native but cost clarity in fast passages, so trade by use. Mark pronunciation for names, or the default stress may land on the wrong syllable.

## Drift in mixed-language prompts

When Chinese and English are mixed, the model often treats the prompt's main language as the sung language, gives the second language a short window, or carries the first language's accent. Write each language as its own block, mark the switch line and add "second verse in English"; that beats interleaving inside one line. State regional accent separately, or the default may not fit the character. When one line carries two languages, the rhyme must be strict, or delivery needs a native-speaker review, mixing is usually riskier than useful. Split into two monolingual versions, generate each, and join them later. Language tags are not decoration; the wrong one shifts pronunciation strategy for the whole section.
:::

