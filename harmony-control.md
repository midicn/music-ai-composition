---
id: "harmony-control"
site: "ai"
cat: "C"
title: "和声控制"
title_en: "Controlling Harmony"
summary: "把和弦走向写出来，再用低音与转位核对生成结果"
summary_en: "Write the progression out, then check the result against its bass line and inversions."
level: "standard"
tags: ["和声", "和弦进行", "离调", "转调"]
tags_en: ["harmony", "chord progression", "borrowed chord", "modulation"]
alias: ["和声控制", "和弦走向", "harmony control"]
order: 9
links: ["[[glossary:borrowed-chord]]", "[[glossary:modulation]]", "[[glossary:pivot-chord]]"]
instances: []
sources: ["https://www.ableton.com/en/manual/editing-midi/", "https://help.suno.com/en/articles/6141505"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论和声要求在编辑和生成中的落实，需要检查实际音符、低音与工具可编辑范围；普通MIDI不代表AI已经遵守指定和弦或实现和声锁定。"
---

::: zh
## 为什么会用到

"悲伤一点的和声"只会得到模糊的小调色彩。和声是最容易被模型平均掉的维度，结果常常通顺却不对，走向和你想要的不一样，该抬的地方没抬起来。

## 背后的原理

和声的可控性取决于路径。符号类工具直接编辑音符，和弦、转位、低音都能写死。音频类工具只能靠提示、参考音频或事后分轨，模型倾向于回到常见的功能进行。两条路共通的判断依据是低音，因为转位与经过音都写在低音里，低音对了，骨架就对了。功能和声之外，模型很少主动处理半音经过、挂留与低音线条，写出来它才会照做。

## 具体做法

先写四到八小节的和弦表，用级数或和弦名都行，标明每小节几个和弦。需要借用和弦时写清借自哪个调，比如 C 大调里用 Fm；需要转调时写清在第几小节、通过哪个和弦过去。走 MIDI 路径就直接改音符；走音频路径就把和弦表写进提示，再用低音与长音当参照。生成后逐小节比对，先看低音是否落在预期根音，再看三音与七音，最后才听色彩。对不上就分段重生成，别整首重来。和弦表存成纯文本，和音频放在同一目录，下次改一版有据可查。
:::

::: en
## Why you reach for it

Ask for a sadder harmony and you get a vague minor colour. Harmony is the dimension models average away most readily. The result often sounds correct yet wrong, moving somewhere other than the brief, and the lift you wanted never arrives.

## The principle

Control depends on the path. Symbolic tools edit notes directly, so chords, inversions and bass can be fixed. Audio tools work through prompts, references or later separation, and the model drifts back toward common functional progressions. What both paths share is the bass as evidence, since inversions and passing motion are written there. Beyond functional harmony the model has little sense of chromatic passing notes, suspensions or a moving bass line, so state them or they will not appear. Get the bass right and the skeleton is right.

## In practice

Write a chord chart of four to eight bars, in roman numerals or chord names, stating how many chords fall in each bar. Name the key a borrowed chord comes from, for instance F minor inside C major, and for a modulation state the bar and the chord that carries you there. On the MIDI path, edit the notes. On the audio path, put the chart into the prompt and use the bass and sustained notes as references. Then compare bar by bar, checking first whether the bass lands on the expected root, then the third and seventh, and only then the colour. Regenerate in sections where it fails rather than starting the whole piece again. Keep the chart as plain text beside the audio so the next revision has something to check against.
:::

