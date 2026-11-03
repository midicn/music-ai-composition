---
id: "extending-and-continuing"
site: "ai"
cat: "C"
title: "续写与接续"
title_en: "Extending and Continuing"
summary: "续写的难点不在第一个音，而在八小节之后往哪里去"
summary_en: "Continuation rarely fails at the first note; it fails where the form has to decide what comes next."
level: "standard"
tags: ["续写", "接续", "曲式", "动机"]
tags_en: ["continuation", "extension", "form", "motif"]
alias: ["继续生成", "往后接", "continuation"]
order: 3
links: ["[[glossary:thematic-transformation]]", "[[glossary:sonata-form]]", "[[glossary:tempo]]"]
instances: []
sources: ["https://help.suno.com/en/articles/6141505", "https://kb.stability.ai/knowledge-base/tips-for-using-the-audio-to-audio-api"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论续写输入、上下文与接续编辑，需要以具体工具功能及真实续写文件核验；普通曲名和固定MIDI不能证明已有续写结果或接缝成功。"
---

::: zh
## 常见卡点

续写看起来最省事，给一段已有的音频或 MIDI，让它往后接。失败很少发生在第一个音，而是从第八小节开始。动机原地打转，段落没有目标，该换段的地方还在重复，结尾草草收住。听的人说不出哪里错，只觉得这不像同一首曲子。这类问题在纯音乐配乐里最明显，因为没有歌词替你撑住结构。

## 它怎么运转

续写的条件只有前面那一段。模型擅长延续表面特征，速度、调性、音色、织体密度都能对上，但它不替你决定曲式。所以往哪去必须写进条件，总长度、是否转调、第几小节换段、结尾怎么收。调性与拍号是底线，给动机一个下一步的变形，比给一堆形容词有用。

## 怎么调整

截取八到十六小节做起点，最好停在乐句的开放处，停在终止上，续写往往只再补一个终止。把速度、调性、拍号写进提示或工程，生成后重新对齐一次。一次要两个版本，一个只延续，一个做发展，变奏或转调，比较哪个更像同一首曲子。接上后先改结尾两小节，让收束落在你安排的段落位置上。接上的部分先单独听一遍，站得住再往下写。
:::

::: en
## Common snags

Continuing looks like the easy job: hand over an existing audio file or MIDI part and ask for more. Failure seldom happens on the first note. It starts around bar eight, where the motif circles, the section has no destination, the place that should change keeps repeating, and the ending stops abruptly. Listeners cannot name the fault, they just feel it is no longer the same piece. It shows most in instrumental cues, where no lyric holds the structure up.

## How it runs

The only condition a continuation model gets is the passage before it. It is good at carrying surface features, tempo, key, timbre, texture density, but it will not decide the form for you. So the destination belongs in the conditions: total length, whether to modulate, which bar changes section, how to close. Key and meter are the floor; a suggested next transformation of the motif is worth more than a pile of adjectives.

## How to adjust

Cut eight to sixteen bars as the start, ideally ending on an open phrase, since a continuation after a cadence usually just adds another cadence. Put tempo, key and meter into the prompt or the session, and realign after generating. Ask for two versions, one that merely continues and one that develops, by variation or modulation, and compare which sounds like the same piece. Then rewrite the last two bars so the close lands where your form needs it, and let the joined passage stand alone before extending again.
:::

