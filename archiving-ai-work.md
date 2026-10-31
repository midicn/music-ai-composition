---
id: archiving-ai-work
site: ai
cat: H
title: 存档
title_en: Archiving the Work
summary: 存档要保证三年后还能重剪、授权与举证
summary_en: Archive so a re-edit, a licence or a claim is still possible years later.
level: standard
tags: [存档, 无损, 权利, 保留期]
tags_en: [archiving, lossless, rights, retention]
alias: [存档, 长期保存, cold archive]
order: 10
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:master-rights]]"
  - "[[glossary:public-domain]]"
instances:
  - pdmx-000153 | 二十六分钟托卡塔，长母带的体积与分段都要留（C1）
  - mutopia-000178 | 巴赫 d 小调托卡塔与赋格，多声部工程要留层（C1）
  - groove-000000 | 短循环也要留来源与参数，否则无法再生成（C1）
  - mutopia-000497 | 贝多芬第五，大型工程缺一层就无法重混（C1）
sources:
  - 数字音频长期保存的格式选择；档案与图书馆惯例是主要依据。
  - 权利证据与保留期的做法——依据来自合同与公开保存指南。
updated: 2026-10-30
---

::: zh
## 问题

项目结束时，最常见的做法是把一个 MP3 留在笔记本上，工程、分轨、提示词、模型条款、授权文件全部散落。三年后要重剪、要授权、要应对版权主张，才发现原始文件找不到了。存档不是把文件堆起来，而是保证未来某个具体用途还能用得上。

## 存什么

母带用二十四位 WAV，保留工程采样率，不做有损压缩。分轨、MIDI、工程文件、提示词与种子记录、模型条款的截图或 PDF、样本与人声授权、客户简报与验收记录、最终交付文件，全部收进同一个项目包。每个文件算校验值，清单也存进去。项目包用作品名加年份命名，清单放在包的第一层。两份拷贝，不同介质，一份异地，每半年到一年抽读一次，确认还能打开。

## 格式与保留期

冷存档用无损，WAV 或 FLAC，不用 MP3 与 AAC 当唯一副本。不要为了高清把四十四点一升到九十六，那只是变大。记录打开工程需要的 DAW 与插件版本，纯文本与 PDF 优先于专有格式。保留期按合同与法律走，客户项目与制作音乐常按财务记录的要求保存数年，权利证据要覆盖作品的使用周期，模型条款会变，所以交付当时就要留档。权利证据包括当时的工具条款、输入授权、人声同意与披露文本。

## 听什么

在二十六分钟的托卡塔里体会长母带的体积与分段，存档要考虑的正是这些。在巴赫 d 小调托卡塔与赋格的多声部版本里看多轨工程需要保留多少层。在放克循环里看短素材也需要保留来源与参数，不然无法再生成。在贝多芬第五交响曲里看大型工程的分轨与工程文件，缺一层就无法重混。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4"],"label":"十年后还能打开吗","label_en":"Will it open in ten years","hint":"无损、开放、带元数据，才经得起时间","hint_en":"Lossless, open and documented is what survives time"}
```
:::

::: en
## The problem

Projects usually end with an MP3 on a laptop while sessions, stems, prompts, model terms and licences scatter. Three years later a re-edit, a licence or a claim arrives and the originals cannot be found. Archiving is not piling up files; it is making sure a specific future use is still possible.

## What to keep

A 24-bit WAV master at the project sample rate, with no lossy compression. Stems, MIDI, session files, prompt and seed records, snapshots of the model terms, sample and voice licences, the client brief and sign-off, and the delivered files, all in one project package. Hash every file and store the list with them. Name the package with the work and year, and put the manifest at the top level. Keep two copies on different media, one off-site, and read a sample every six to twelve months to confirm it still opens.

## Formats and retention

Cold storage should be lossless, WAV or FLAC, never MP3 or AAC as the only copy. Do not upsample 44.1 kHz to 96 kHz to look high resolution; it only gets bigger. Record the DAW and plug-in versions needed to open the session, and prefer plain text and PDF over proprietary-only formats. Retention follows contract and law; client and production music work is often kept for years as financial records, while rights evidence must cover the life of the work. Model terms change, so snapshot them at delivery. Rights evidence includes the terms in force, input licences, voice consent and the disclosure text.

## What to listen for

In the twenty-six minute Toccata, the size and segmentation of a long master, exactly what archiving must plan for. In the Bach Toccata and Fugue for ensemble, how many layers a multi-part session needs. In the funk loop, why even short material needs its source and settings, or it cannot be regenerated. In the Beethoven Fifth, a large session where one missing stem blocks any remix.

```audiolab
{"type": "instrument", "gm": "Church Organ", "synth": "blown", "phrase": ["C3", "G3", "C4", "E4"], "label": "Will it open in ten years", "label_en": "Will it open in ten years", "hint": "无损、开放、带元数据，才经得起时间", "hint_en": "Lossless, open and documented is what survives time"}
```
:::
