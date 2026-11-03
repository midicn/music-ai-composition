---
id: "structure-control"
site: "ai"
cat: "C"
title: "段落结构控制"
title_en: "Controlling Song Structure"
summary: "段落要写小节数和进出方式，只写主歌副歌等于没写"
summary_en: "Sections need bar counts and entry points; naming verse and chorus alone specifies nothing."
level: "standard"
tags: ["段落", "主副歌", "桥段", "转场"]
tags_en: ["sections", "verse and chorus", "bridge", "transitions"]
alias: ["结构控制", "段落控制", "song structure"]
order: 131
links: ["[[glossary:ternary-form]]", "[[glossary:strophic-form]]", "[[glossary:cadence]]"]
instances: ["thesession-015842", "atepp-007103", "mutopia-000498", "cyberhymnal-001486"]
sources: ["Walter Piston, Harmony 与 William Caplin, Classical Form（Oxford）中关于段落划分与终止式的判断。", "文本提示里的段落标记与结构控制，依据公开模型文档与制作实践。"]
updated: "2026-11-03"
---

::: zh
## 段落名不等于段落

只写主歌、副歌、桥段，模型交回来的常是一段四分钟不换气的循环。段落名对它只是标签，除非绑上小节数、能量和乐器进出。真正的结构信息是：这一段多长，谁先进，谁退出，最后落在哪个和弦。

## 把段落写成一张表

| 段落 | 小节 | 进入方式 | 退出方式 | 听辨点 |
|---|---|---|---|---|
| 前奏 | 8 | 钢琴单声部 | 鼓填四拍 | 主题是否提前露头 |
| 主歌 | 16 | 贝斯与鼓同时进 | 人声句尾留空 | 每四小节是否有变化 |
| 副歌 | 16 | 全体进，镲打开 | 最后一拍全体停 | 能量是否真的抬起来 |
| 桥段 | 8 | 鼓撤，和声换色 | 上行过门接回副歌 | 有没有带来新信息 |
| 尾奏 | 8 | 主奏重复主题 | 渐弱或干净收 | 结束是否落在主和弦 |

表里最容易被忽略的是退出方式。进入写得再清楚，退出含糊，段落就会黏在一起。副歌最后一拍全体停，比任何形容词都更能把下一段推开。

## 转场要写谁先动

转场不是自然过渡，而是一个具体动作：鼓的过门、贝斯先落半小节、和声换到小下属、全体休止一拍。写“副歌前两小节加军鼓十六分过门，最后一拍停”比写“情绪推上去”可执行得多。段落之间若用同一动机连接，听感最顺；换调或换拍则要在边界前留出准备。

## 时长与段落数会互相挤压

三分钟要装五段，每段平均只有三十六秒，桥段剩四小节，发展不起来。与其硬塞，不如减少段落，或者把桥段写成四小节的间奏。生成后再裁切通常比一次写对更可靠，但裁切会切掉尾音与混响，接缝处要做短交叉淡化，并确认拍点没有半拍偏移。段落数超过六个而总长不足四分钟时，先怀疑结构本身，而不是继续加提示词。

```audiolab
{"type":"progression","key":"C4","degrees":["I","V","vi","IV"],"beat":0.9,"label":"合成和弦进行","label_en":"Synthesized chord sequence","hint":"浏览器合成示意；不是模型输出或处理前后对比。","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

::: en
## A section name is not a section

Write verse, chorus, bridge and the model often returns four minutes of one loop that never exhales. A section name is only a label until it is tied to a bar count, an energy level and instruments entering or leaving. Real structural information is: how long this part runs, who enters first, who drops out, and which chord it lands on.

## Write the sections as a table

| Section | Bars | Entry | Exit | What to hear |
|---|---|---|---|---|
| Intro | 8 | Solo piano | Four-beat drum fill | Does the theme appear early |
| Verse | 16 | Bass and drums together | Vocal leaves space at phrase ends | Any change every four bars |
| Chorus | 16 | Full band, open hi-hat | Everything stops on the last beat | Does the energy actually lift |
| Bridge | 8 | Drums out, harmony shifts colour | Rising fill back to the chorus | Does it add new information |
| Outro | 8 | Lead restates the theme | Fade or clean stop | Does it end on the tonic |

The exit is the column people skip. A clear entry with a vague exit glues two sections together. One beat of silence at the end of a chorus pushes the next part away better than any adjective.

## Say who moves first at the transition

A transition is not a natural flow but a specific action: a drum fill, the bass landing half a bar early, the harmony shifting to the minor subdominant, everyone resting for a beat. “A sixteenth-note snare fill in the two bars before the chorus, then a beat of silence” is executable; “build the emotion” is not. Connecting sections with one motive sounds smoothest, while a key or metre change needs preparation before the seam.

## Duration and section count pull against each other

Five sections in three minutes leaves thirty-six seconds each, and the bridge gets four bars, too short to develop. Cut a section or make the bridge a four-bar interlude instead of forcing everything in. Editing after generation is usually safer than getting it right in one pass, but cutting removes tails and reverb, so crossfade briefly at the seam and confirm the downbeat has not slipped half a beat. When a piece has more than six sections and runs under four minutes, question the structure before adding more prompt text.

```audiolab
{"type":"progression","key":"C4","degrees":["I","V","vi","IV"],"beat":0.9,"label":"Synthesized chord sequence","label_en":"Synthesized chord sequence","hint":"A browser-synthesized exercise, not model output or a processing comparison.","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

