---
id: metadata-and-credits
site: ai
cat: H
title: 元数据与署名
title_en: Metadata and Credits
summary: 元数据是录音的身份，署名与披露都要具体
summary_en: Metadata is the identity of a recording; credits and disclosure must be specific.
level: standard
tags: [元数据, ISRC, 署名, 披露]
tags_en: [metadata, ISRC, credits, disclosure]
alias: [元数据, 署名, credits and disclosure]
order: 5
links:
  - "[[glossary:isrc]]"
  - "[[glossary:music-copyright]]"
  - "[[glossary:public-domain]]"
instances:
  - mutopia-000178 | 巴赫 d 小调托卡塔与赋格，曲名与作者齐全但缺编号（C1）
  - thesession-000083 | 传统里尔舞曲，没有作曲家，字段该留空（C1）
  - atepp-000238 | 肖斯塔科维奇 Op.87 第 23 首，作品号加序号定位明确（C1）
  - atepp-001283 | 肖邦 Op.37 No.2，浪漫派作品的字段写法样本（C1）
sources:
  - ISRC 的十二位结构与登记方式，依 ISO 3901 与发行实务核对
  - 录音署名与披露的写法，依公开发行规范与平台条款归纳，未抄原文
updated: 2026-10-30
---

::: zh
## 问题

AI 生成的文件最容易变成孤儿，名字叫 output_final.wav，没有工具版本，没有作者，没有授权说明。三个月后要授权、要结算、要证明这条曲子怎么来的，全都找不到。元数据不是发行平台才需要的东西，它是这条录音的身份。

## 字段与层级

至少写清四层。作品层，曲名、作曲家、作品号、乐章。录音层，演奏者、制作人、录音日期、ISRC。文件层，采样率、位深、时长、版本。权利层，版权行、授权方式、样本来源、工具与版本。ISRC 是十二位，国家两位、登记方三位、年份两位、序号五位，它标识的是一次录音，不是一首作品，所以新混音、新剪辑要重新申请。不要自己编代码，通过发行方或登记机构取得。

## 署名与披露

人该记的记全，概念、编曲、剪辑、混音、母带分别是谁，写清楚。工具也要署，写名称、版本与角色，例如人声由某工具生成，编曲与混音由某人完成。披露要短而具体，不写本作品由 AI 辅助这种空话，写清哪一部分是生成的，哪一部分是人工的。不要声称百分之百人工，也不要隐瞒，平台和客户的政策不一样，交付前查一遍。传统曲调没有作曲家，就留空，不要填传统当作者。交付时把元数据随文件一起发，不要只写在邮件正文里。

## 听什么

在巴赫 d 小调托卡塔与赋格里听曲名、调性与作曲家都在，但编号缺失会让同一作品的不同版本混在一起。在里尔舞曲里听完整段旋律也找不到作者，作者一栏就该留空。在肖斯塔科维奇 Op.87 第 23 首里听作品号加序号如何精确定位。在肖邦 Op.37 第二首夜曲里听同一套字段在浪漫派曲目上的写法。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4"],"label":"没有标签的音频","label_en":"Audio without a label","hint":"声音本身不告诉你作者、版本与授权","hint_en":"The sound itself will not tell you the author, version or licence"}
```
:::

::: en
## The problem

AI files become orphans easily, named output_final.wav, with no tool version, no author and no licence note. Three months later, licensing, payment or a provenance question arrives and nothing can be found. Metadata is not only for distributors; it is the identity of the recording.

## Fields and layers

Write at least four layers. Work, meaning title, composer, catalogue number and movement. Recording, meaning performer, producer, date and ISRC. File, meaning sample rate, bit depth, duration and version. Rights, meaning copyright line, licence, sample sources, tool and version. An ISRC is twelve characters, two for country, three for registrant, two for year, five for designation. It identifies a recording, not a composition, so a new mix or edit needs a new code. Never invent codes; get them through a distributor or registrar.

## Credits and disclosure

Credit the people fully, concept, arrangement, editing, mix and master, each by name. Credit the tools too, with name, version and role, for example vocals generated with a named tool, arrangement and mix by a named person. Disclosure should be short and specific. Assisted by AI says nothing; state which part was generated and which was human. Do not claim one hundred percent human, and do not hide it either; platform and client policies differ, so check before delivery. A traditional tune has no composer, so leave the field empty rather than writing Traditional as the author. Send the metadata with the files, not only in the body of an email.

## What to listen for

In Bach's Toccata and Fugue in D minor, the title, key and composer are present but the catalogue number is missing, which lets versions of the same work merge. In the reel, the tune has no author, so the field should stay blank. In Shostakovich's Op. 87 No. 23, an opus plus number locates the movement precisely. In Chopin's Op. 37 No. 2, the same fields applied to a Romantic work.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C4", "D4", "E4", "G4"], "label": "Audio without a label", "label_en": "Audio without a label", "hint": "声音本身不告诉你作者、版本与授权", "hint_en": "The sound itself will not tell you the author, version or licence"}
```
:::
