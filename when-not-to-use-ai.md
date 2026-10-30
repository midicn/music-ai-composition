---
id: when-not-to-use-ai
site: ai
cat: H
title: 何时不该用 AI
title_en: When Not to Use AI
summary: 有些活用真人更快、更好，或者根本不能生成
summary_en: Some jobs are faster, better or only legal with a human.
level: standard
tags: [判断, 录音, 版权, 伦理]
tags_en: [judgement, recording, copyright, ethics]
alias: [不该用 AI, 工具边界, limits of AI]
order: 11
links:
  - "[[glossary:music-copyright]]"
  - "[[glossary:public-domain]]"
  - "[[glossary:master-rights]]"
instances:
  - thesession-006629 | 爱尔兰传统曲调《提琴手》，装饰音属于传统内部知识（C1）
  - atepp-001115 | 肖邦第一叙事曲，大结构的自由速度需要演奏者决定（C1）
  - musicnet-000067 | 贝多芬第十五弦乐四重奏，合奏音准与融合无法生成（C1）
  - cyberhymnal-000000 | 管风琴赞美诗，礼仪场合需要真实空间与乐器（C1）
sources:
  - 生成与录音的取舍，依制作实务通识归纳，未抄原文
  - 声音权利与同意的基本要求，依公开法律资料与平台条款核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

AI 在初稿上很便宜，在最后百分之十很贵。有些活看起来适合生成，实际用真人更快、更好，或者根本不能这么做。判断标准不是 AI 能不能做，而是这条路径是否更快、更合法、更值得。

## 该录的

一段三十秒的独奏、一个具体的音色、一次有明确档期的录音，找乐手弹一遍通常比调一小时提示词更快，也更可控。乐手会给你没想过的处理，生成器只会给你概率上安全的选择。需要精确到帧的同步、需要给真人演奏的乐谱、需要能弹出来的吉他 riff，也该走录音或写作。录音有档期与预算的成本，但一次到位的演奏省下的返工往往更多。

## 该写与该停的

权利不允许时不要绕，现有版权歌曲、在世艺人的声音、客户合同禁止 AI 的项目，生成一个像的版本不是解决方案。伦理上同样如此，逝者的声音、仪式音乐、特定文化的装饰音，没有授权就不要碰。还有一种情况是手艺，编曲能力靠写出来，不靠挑选；以真人演奏为卖点的现场专辑、比赛、考试，不能外包。生成之前先问三个问题，乐手能不能在更短时间内做到，客户或平台是否禁止，披露之后作品是否还成立。生成适合做变体、临时轨、音效、繁琐剪辑，以及给人听的参考小样，之后由人来替换。

## 听什么

在《提琴手》这样的传统曲调里听装饰音与律动，那是传统内部的知识，不是随机采样能给的。在肖邦第一叙事曲里听大结构的自由速度，需要演奏者做整体决定。在贝多芬第十五弦乐四重奏里听合奏的音准与融合。在管风琴赞美诗里听礼仪场合需要的真实空间与乐器。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5","B4","A4","G4"],"label":"一句需要真人运弓的旋律","label_en":"A line that needs a real bow","hint":"换弓、揉弦与呼吸，生成器给不了","hint_en":"Bow changes, vibrato and breath are not on the menu"}
```
:::

::: en
## The problem

AI is cheap for a first draft and expensive for the last ten percent. Some jobs look suitable for generation but are faster, better or only legal with a human. The test is not whether AI can do it, but whether that path is faster, lawful and worth it.

## Record it

For a thirty-second solo, one specific sound, or a session with a fixed date, hiring a player is usually faster than an hour of prompt tuning, and more controllable. A player offers a phrasing you did not imagine; a generator offers the probabilistically safe choice. Frame-accurate sync, a score for real players, a guitar riff that must be playable, all belong to recording or writing. Recording carries scheduling and budget costs, but one good take usually saves more rework than it costs.

## Write it, or stop

When rights forbid it, do not route around them. An existing copyrighted song, a living artist's voice, a contract that bans AI, generating a soundalike is not a solution. The same applies ethically to dead artists' voices, ritual music and culturally specific ornamentation without permission. Then there is craft. Arranging is learned by writing, not by selecting, and a live album, a competition or an exam whose value is human performance cannot be outsourced. Ask three questions before generating, could a player do it sooner, do the client or platform forbid it, and would disclosure damage the work. Generation suits variants, temp tracks, sound design, tedious editing and reference mockups that a human later replaces.

## What to listen for

In a traditional tune such as The Fiddler, ornaments and swing that belong to knowledge inside the tradition, not to random sampling. In Chopin's First Ballade, large-scale rubato that needs a performer's overall decision. In Beethoven's String Quartet No. 15, ensemble intonation and blend. In the organ hymn, the real space and instrument that a liturgical occasion requires.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["G4", "A4", "B4", "D5", "B4", "A4", "G4"], "label": "A line that needs a real bow", "label_en": "A line that needs a real bow", "hint": "换弓、揉弦与呼吸，生成器给不了", "hint_en": "Bow changes, vibrato and breath are not on the menu"}
```
:::
