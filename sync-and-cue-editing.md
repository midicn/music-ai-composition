---
id: "sync-and-cue-editing"
site: "ai"
cat: "F"
title: "同步与 cue 剪辑"
title_en: "Sync and Cue Editing"
summary: "切点要落在乐句收尾，不要切在重音和混响里"
summary_en: "Cut at the end of a phrase, never on an accent or inside a reverb tail"
level: "standard"
tags: ["同步", "剪辑", "乐句", "速度映射"]
tags_en: ["sync", "cue editing", "phrasing", "tempo map"]
alias: ["对画面", "cue 剪辑", "sync editing"]
order: 5
links: ["[[glossary:tempo]]", "[[glossary:cue]]"]
instances: []
sources: ["https://support.apple.com/en-ie/guide/logicpro/lgcpfff75e20/mac", "https://helpx.adobe.com/premiere/desktop/add-audio-effects/apply-audio-effects/remix-in-premiere.html"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "同步与 cue 剪辑依赖画面帧率、时间码、标记及实际切点；离开视频只播放音乐，不能验证命中点、时长或改版后的同步关系。"
---

::: zh
## 阻碍在哪

把生成音乐贴到画面上，最容易犯的错是按画面长度硬切，切在乐句中间、重音上或者混响尾巴里。观众说不清哪里不对，只觉得廉价。改一版再切一次，问题往往挪到别处，因为素材本身没有给切点留位置。

## 背后的机制

音乐有句法，四小节、八小节为一个单位，重音落在强拍，收尾落在终止。切点如果落在句尾最后一拍之后，听感是"说完"；落在句中，听感是被打断。速度稳定的素材可以直接对网格，带 rubato 的演奏必须先做 tempo map，否则越到后面偏得越多。生成的素材常常没有明确终止，段落之间是渐变的，这就是难切的原因。

## 怎么调整

先数清素材的乐句，标出所有可能的落点，再回头改画面或改音乐。优先伸缩音乐，其次才是裁画面。需要缩短时，删掉一个完整乐句比截掉两秒好。需要延长时，复制一段并做配器变化，不要拉长最后一个音。切点避开镲、定音鼓和混响长的音符，宁可早半拍收在干声上。给每条素材做 tempo map，把重音对齐到画面上，再检查整段有没有漂移。对白盖住的段落可以粗切，音乐露出来的地方才值得精切。
:::

::: en
## Where it blocks

The commonest mistake when fitting generated music to picture is cutting to the exact length of the shot, which puts the cut inside a phrase, on an accent, or in a reverb tail. Viewers cannot name the problem, they just find it cheap. Re-cut a new version and the fault moves somewhere else, because the material never left room for a cut.

## The mechanism

Music has syntax, in units of four or eight bars, with accents on strong beats and endings on cadences. A cut placed after the last beat of a phrase feels finished; a cut inside the phrase feels interrupted. Material at a steady tempo can be cut against the grid, while a performance with rubato needs a tempo map first, or the drift grows with every bar. Generated cues often lack a clear cadence and change gradually between sections, which is exactly why they are hard to cut.

## How to adjust

Count the phrases and mark every possible landing before changing picture or music. Stretch the music first and trim the picture second. To shorten, remove a whole phrase rather than chop two seconds. To lengthen, repeat a section with a change of orchestration instead of stretching the last note. Keep cuts away from cymbals, timpani and long reverb, and prefer ending half a beat early on dry sound. Map the tempo of every cue, land the accents on picture, then check the whole sequence for drift. Cuts only matter where the music is exposed; under dialogue they can be rough.
:::

