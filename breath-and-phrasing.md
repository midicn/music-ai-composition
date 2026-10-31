---
id: breath-and-phrasing
site: ai
cat: E
title: 换气与句读
title_en: Breath and Phrasing
summary: 气口决定句子怎么被听懂，合成人声默认不会替你呼吸
summary_en: Breath marks decide how a line is understood, and a synthetic voice will not breathe for you.
level: standard
tags: [换气, 句读, 连断, 句尾]
tags_en: [breath, phrasing, legato, line endings]
alias: [气口, 呼吸, breath marks]
order: 143
links:
  - "[[instrument:voice]]"
  - "[[glossary:legato]]"
  - "[[glossary:phrase]]"
instances:
  - openscore-000084 | 舒伯特《你是我的安宁》，长句在哪里换气，句子才不塌（C1）
  - openscore-000008 | 舒伯特《魔王》，一人三腔，气口和音色一起换角色（C1）
  - openscore-000538 | 霍尔梅斯《晨曲》，法语连诵与句尾收法，合成最容易硬切（C1）
  - openscore-000014 | 奎尔特《来吧，死亡》，英语宣叙靠辅音与停顿断句（C1）
sources:
  - Richard Miller, The Structure of Singing（Schirmer）与 James McKinney, The Diagnosis and Correction of Vocal Faults 中关于气口与分句的章节。
  - 合成歌声系统文档里对呼吸标记、音素时长与连奏参数的说明。
  - Vocal pedagogy texts on breath placement and phrasing, with reference to singing-voice system documentation.
updated: 2026-10-31
---

::: zh
## 气口就是标点

一句歌词没有逗号，歌手也会在某处换气，听者靠这个气口把句子切成意思。合成人声默认按音符切，不管语义，于是该连的地方断了，该断的地方一口气拖到底。判断一条人声自不自然，先不看音色，数一数它在哪几处呼吸。

## 五个能改的地方

气口位置、气口长度、字间连断、句尾收法，还有辅音起点。位置由歌词和旋律共同决定，通常落在语法边界，一句六到十个音节；长度给八十到二百毫秒，太短听不出换气，太长拍子就散。连断用很小的重叠或断开做，重叠多了字糊，断多了像念字。句尾最考验，长音要提前收力，短句要留一点余气，硬切会露馅。

## 参数表

| 参数 | 作用 | 常见做法 | 过头会怎样 |
|---|---|---|---|
| 气口位置 | 决定分句与语义 | 落在语法边界，每六到十音节一处 | 太密像喘，太疏像念经 |
| 气口长度 | 做出换气感 | 八十到二百毫秒 | 超过半拍，节奏就散 |
| 字间重叠 | 控制连断 | 二十到六十毫秒 | 多了糊字，少了像蹦字 |
| 句尾衰减 | 收住一句 | 在最后一拍内收完 | 拖长显假，切早显硬 |
| 辅音起点 | 咬字落在拍前 | 提前十到三十毫秒 | 多了像抢拍 |

## 句尾和辅音

气口做对，句子仍然可能假，问题常在句尾。合成人声习惯把最后一个音唱满时值再突然停，真人会提前半拍收，留一点气息。辅音也要提前一点，让字头落在拍前一点点，听起来才是说出来的。把这些做成模板，下一句直接套，比逐字调整省事。

## 哪里会坏

气口加太密，听起来像喘不上气；为了自然乱加呼吸声，反而暴露是贴上去的。快歌里气口要短，慢歌里可以长，但都不要压掉拍点。合唱和声部不需要每句都换气，几条线一起呼吸会整齐得可疑。念白、旁白和歌唱的气口规则不同，别把唱歌的模板套到口播上。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["E4","E4","G4","G4","A4","G4","E4","D4"],"label":"一口气唱完的一句","label_en":"A phrase taken in one breath","hint":"听句尾怎么收，气口迟一拍，整句就塌","hint_en":"Hear how the ending closes; breathe one beat late and the line sags"}
```
:::

::: en
## A breath is punctuation

A line of lyrics has no comma printed on it, yet a singer breathes somewhere and the listener uses that break to parse the sentence. A synthetic voice cuts on notes rather than meaning, so it joins what should break and holds what should close. To judge whether a take sounds human, count the breaths before judging the tone.

## Five things to change

Where the breath falls, how long it lasts, how much adjacent notes overlap, how the line ends, and where the consonants land. Position follows both lyrics and melody and usually sits on a syntactic boundary, one breath every six to ten syllables. Length runs from about eighty to two hundred milliseconds: shorter and the breath disappears, longer and the pulse sags. Overlap or separation controls the joins; too much smears the words, too little turns singing into recitation. Endings are the hardest part, because a long note has to release early and a short one has to keep a little air.

## Settings

| Parameter | What it does | Common practice | When pushed too far |
|---|---|---|---|
| Breath position | Parses the phrase | On a syntactic boundary, every six to ten syllables | Too frequent reads as gasping, too rare as chanting |
| Breath length | Creates the intake | Eighty to two hundred milliseconds | Past half a beat, the pulse falls apart |
| Note overlap | Controls joins | Twenty to sixty milliseconds | More smears words, less makes them jump |
| Ending decay | Closes the phrase | Finish inside the last beat | Drawn out sounds fake, cut early sounds stiff |
| Consonant onset | Places the attack | Ten to thirty milliseconds ahead of the beat | Too far ahead sounds like rushing |

## Endings and consonants

Even with breaths in the right places a line can still fail, and the fault is usually at the end. Synthesis tends to fill the last note for its full value and stop dead, while a singer releases half a beat early and leaves a little air behind. Consonants also need to arrive slightly before the beat so the word feels spoken rather than switched on. Turn these choices into a template and the next line costs almost nothing.

## Where it breaks

Breaths packed too closely sound like panic, and breath noise added for realism often sounds pasted on. Fast songs need short breaths and slow ones can afford long breaths, but neither should cover the beat. Backing parts do not need a breath at every phrase, and several lines breathing together sound suspiciously tidy. Spoken narration and singing follow different rules, so do not carry a vocal template into a voice-over.

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["E4","E4","G4","G4","A4","G4","E4","D4"],"label":"A phrase taken in one breath","label_en":"A phrase taken in one breath","hint":"Hear how the ending closes; breathe one beat late and the line sags","hint_en":"Hear how the ending closes; breathe one beat late and the line sags"}
```
:::
