---
id: harmony-control
site: ai
cat: C
title: 和声控制
title_en: Controlling Harmony
summary: 把和弦走向写出来，再用低音与转位核对生成结果
summary_en: Write the progression out, then check the result against its bass line and inversions.
level: standard
tags: [和声, 和弦进行, 离调, 转调]
tags_en: [harmony, chord progression, borrowed chord, modulation]
alias: [和声控制, 和弦走向, harmony control]
order: 9
links:
  - "[[glossary:borrowed-chord]]"
  - "[[glossary:modulation]]"
  - "[[glossary:pivot-chord]]"
instances:
  - pdmx-000575 | 维塔利《恰空》，固定低音上反复变奏，框架清楚（C1）
  - giantmidi-000504 | 斯卡拉蒂《福利亚》，小调固定进行，便于逐小节核对（C1）
  - pdmx-002370 | 《特里斯坦》钢琴改编，听解决被推迟后调性游移（C1）
  - giantmidi-004867 | 亨德尔《G 大调恰空》，大调固定低音，与福利亚对照（C1）
sources:
  - 和声进行的标注方式；和声学惯例是主要依据。
  - 音频与符号两类生成路径的差异——依据来自公开工具说明。
updated: 2026-10-30
---

::: zh
## 为什么会用到

"悲伤一点的和声"只会得到模糊的小调色彩。和声是最容易被模型平均掉的维度，结果常常通顺却不对，走向和你想要的不一样，该抬的地方没抬起来。

## 背后的原理

和声的可控性取决于路径。符号类工具直接编辑音符，和弦、转位、低音都能写死。音频类工具只能靠提示、参考音频或事后分轨，模型倾向于回到常见的功能进行。两条路共通的判断依据是低音，因为转位与经过音都写在低音里，低音对了，骨架就对了。功能和声之外，模型很少主动处理半音经过、挂留与低音线条，写出来它才会照做。

## 具体做法

先写四到八小节的和弦表，用级数或和弦名都行，标明每小节几个和弦。需要借用和弦时写清借自哪个调，比如 C 大调里用 Fm；需要转调时写清在第几小节、通过哪个和弦过去。走 MIDI 路径就直接改音符；走音频路径就把和弦表写进提示，再用低音与长音当参照。生成后逐小节比对，先看低音是否落在预期根音，再看三音与七音，最后才听色彩。对不上就分段重生成，别整首重来。和弦表存成纯文本，和音频放在同一目录，下次改一版有据可查。

## 耳朵要抓的点

在维塔利《恰空》里听同一低音上如何换和声，在《福利亚》里逐小节核对固定进行，在《特里斯坦》里听解决被推迟后调性怎样游移，在亨德尔《恰空》里听大调版本与前者对照。低音对上了，和声基本就对了，色彩才有意义；对不上时先怀疑分段边界，而不是模型听不懂和声。

```audiolab
{"type":"progression","key":"C","chords":["C","Am","F","Fm","C"],"label":"借用小下属的进行","label_en":"A progression borrowing the minor subdominant","hint":"第四个和弦借自小调，色彩一变就听得出","hint_en":"The fourth chord is borrowed from the minor; the shift is audible"}
```
:::

::: en
## Why you reach for it

Ask for a sadder harmony and you get a vague minor colour. Harmony is the dimension models average away most readily. The result often sounds correct yet wrong, moving somewhere other than the brief, and the lift you wanted never arrives.

## The principle

Control depends on the path. Symbolic tools edit notes directly, so chords, inversions and bass can be fixed. Audio tools work through prompts, references or later separation, and the model drifts back toward common functional progressions. What both paths share is the bass as evidence, since inversions and passing motion are written there. Beyond functional harmony the model has little sense of chromatic passing notes, suspensions or a moving bass line, so state them or they will not appear. Get the bass right and the skeleton is right.

## In practice

Write a chord chart of four to eight bars, in roman numerals or chord names, stating how many chords fall in each bar. Name the key a borrowed chord comes from, for instance F minor inside C major, and for a modulation state the bar and the chord that carries you there. On the MIDI path, edit the notes. On the audio path, put the chart into the prompt and use the bass and sustained notes as references. Then compare bar by bar, checking first whether the bass lands on the expected root, then the third and seventh, and only then the colour. Regenerate in sections where it fails rather than starting the whole piece again. Keep the chart as plain text beside the audio so the next revision has something to check against.

## What the ear catches

In Vitali's Chaconne, how the harmony changes over one repeating bass; in the Folia, the fixed progression checked bar by bar; in Tristan, how the delayed resolution lets the key drift; in Handel's Chaconne, the major-key ground set against the former. When the bass agrees, the harmony is mostly right; when it fails, suspect a section boundary before suspecting the model.

```audiolab
{"type":"progression","key":"C","chords":["C","Am","F","Fm","C"],"label":"A progression borrowing the minor subdominant","label_en":"A progression borrowing the minor subdominant","hint":"The fourth chord is borrowed from the minor; the shift is audible","hint_en":"The fourth chord is borrowed from the minor; the shift is audible"}
```
:::
