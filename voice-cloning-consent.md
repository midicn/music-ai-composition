---
id: voice-cloning-consent
site: ai
cat: E
title: 声音克隆的同意
title_en: Consent for Voice Cloning
summary: 克隆声音之前，先把用途、期限、撤回和标注写成可查的记录
summary_en: Before cloning a voice, put purpose, term, withdrawal and labelling into a record you can show.
level: standard
tags: [声音克隆, 同意, 标注, 留证]
tags_en: [voice cloning, consent, labelling, record keeping]
alias: [声音授权, 克隆同意, voice consent]
order: 2
links:
  - "[[instrument:voice]]"
  - "[[instrument:popular-voice]]"
  - "[[glossary:sample-clearance]]"
instances:
  - openscore-000105 | 舒曼宣叙性歌曲，咬字习惯构成声音身份，授权要覆盖（C1）
  - cyberhymnal-008179 | 德文摇篮曲，气声与近距离是样本里最敏感的部分（C1）
  - openscore-000324 | 德彪西法语歌曲，鼻化元音与口音同样属于可识别特征（C1）
sources:
  - 声音人格利益与录音授权的区分，对照公开法律评论整理。
  - , with reference to Consent practice for synthetic voice.
updated: 2026-10-30
---

::: zh
## 难在哪

克隆一个声音只要几十秒素材，但要用在发行、广告或平台上，先得有一份拿得出来的同意。口头答应在分成、下架、继承或平台申诉时都撑不住。同意不是一句“可以”，而是一份写清边界的文件，谁签、签了什么、什么时候失效，都要能查到。同意的对象是人，不是文件，人换了、用途变了，就要重新确认。

## 内部发生了什么

声音的可识别性来自音色、口音、咬字习惯和呼吸方式，这些恰好也是克隆模型学走的东西。所以授权范围要覆盖“像谁”，而不只是“用哪段录音”。录音版权和声音人格利益是两件事，前者管母带，后者管别人能不能模仿你。只买下录音，不等于买到模仿的权利。训练数据里如果混进了别人的录音，同意书也补不上这个洞。

## 从哪开始

同意书至少写四件事。用途，哪首歌、哪个平台、是否用于广告或政治内容。范围，语言、音域、时长、可否再授权给第三方。期限，起止日期以及到期后成品怎么处理。撤回，怎么提出、几天内下架、已经发出的物料怎么办。未成年人加监护人签字。另外保存原始干声、模型版本、生成日期和操作人。同意书用双方都看得懂的语言写，不要只留一份英文模板。发布时在简介、元数据和字幕里标注合成人声，不要只在角落写一行小字。

## 耳朵要抓的点

在 Ich grolle nicht 里听宣叙性的咬字怎么带出性格，在 Schlaf, Kindlein, schlaf 里听气声与近距离，在 Spleen 里听法语鼻化元音。咬字、气息、口音这三样，正是同意书要覆盖的范围，也是克隆最容易抹平、最容易被听出来的部分。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["G3","A3","B3","D4","B3","A3"],"label":"一段可被克隆的样本","label_en":"A short sample that could be cloned","hint":"样本越短，越要写清用途、期限与撤回方式","hint_en":"The shorter the sample, the more precisely the use, term and withdrawal must be written"}
```
:::

::: en
## Where it gets hard

Cloning a voice takes seconds of audio, but using that clone on a release, in an advertisement or on a platform requires consent you can produce. A verbal yes will not survive a royalty dispute, a takedown, an estate or an appeal. Consent is not a single word of permission. It is a document that states its boundaries, who signed it, what it covers and when it expires.

## What happens inside

A voice is recognisable through timbre, accent, diction habits and breathing, and those are exactly what a clone learns. Consent therefore has to cover likeness, not merely the recording it was trained on. Recording copyright and voice personality rights are separate things. The first governs the master, the second governs whether someone may imitate you. Buying the recording is not buying the imitation. If the training set contains another person's recording, a consent form cannot repair the hole.

## Where to start

Write at least four things into the agreement. Use: which song, which platform, whether advertising or political content is included. Scope: languages, range, duration, and whether sublicensing is allowed. Term: start and end dates, plus what happens to finished work at expiry. Withdrawal: how it is requested, how many days until takedown, and what happens to material already distributed. A minor needs a guardian's signature. Write it in a language both sides actually read rather than leaving an English template in the folder. Keep the raw dry recording, the model version, generation dates and the operator's name. Keep refusals on file as well; they record what was never approved. Label synthetic output in the credits, metadata and captions, not in a footnote.

## What the ear catches

In Ich grolle nicht, listen to how declamatory diction carries character. In Schlaf, Kindlein, schlaf, listen to breath and closeness. In Spleen, listen to the French nasal vowels. Diction, breath and accent are what consent must cover, and what a clone flattens most easily and reveals most quickly.

```audiolab
{"type": "instrument", "gm": "Voice Oohs", "synth": "vocal", "phrase": ["G3", "A3", "B3", "D4", "B3", "A3"], "label": "A short sample that could be cloned", "label_en": "A short sample that could be cloned", "hint": "样本越短，越要写清用途、期限与撤回方式", "hint_en": "The shorter the sample, the more precisely the use, term and withdrawal must be written"}
```
:::
