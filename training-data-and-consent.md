---
id: training-data-and-consent
site: ai
cat: G
title: 训练数据与同意
title_en: Training Data and Consent
summary: 模型学过什么，决定你能拿它做什么，也决定谁本该被问过
summary_en: What a model learned shapes what you can do with it, and who should have been asked
level: standard
tags: [训练数据, 同意, 数据来源, 采购]
tags_en: [training data, consent, provenance, procurement]
alias: [训练数据, 数据来源, training data]
order: 1
links:
  - "[[glossary:public-domain]]"
  - "[[glossary:music-copyright]]"
  - "[[glossary:sample-clearance]]"
instances:
  - mutopia-001411 | 萨蒂《裸体歌舞》第一首的谱面文件，只有音符没有触键，看训练数据停在哪一层（C1）
  - atepp-001283 | 肖邦夜曲作品37之2的录音，同一份谱被演奏成什么样，录音层与谱面层要分开问（C1）
  - wikifonia-000434 | 采集者署名的爱尔兰角笛舞曲，来源链上有一个具体的人名（C1）
  - abcmisc-001404 | 只标"传统"的单声部克莱兹默曲调，找不到可询问的授权主体（C1）
sources:
  - 训练数据的层次划分，依公开模型文档与数据说明核对，未抄原文
  - 版权与人格利益对同意的要求，依公开法律评论归纳，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

"这个模型是用什么训练的"，多数产品页答不完整，只给"数百万首曲目""授权与公开数据"。对使用者来说，这不是八卦，而是两件实际的事。输出能不能商用，你上传的素材会不会进入下一轮训练。两件事都取决于数据从哪来、有没有人同意过。

## 原理

训练数据至少分三层。谱面与 MIDI 是符号层，只有音高、时值、力度。录音是音频层，带演奏者的触键、气息与房间。歌词与元数据是文本层。三层的权利不同，需要征求同意的对象也不同。符号层的民调常标着"传统"，但"传统"不是授权，只表示没有已知权利人，采集者、编曲者、译配者都可能是具体的人。音频层还叠着表演者与录音制作者。模型把三层混在一起学，输出里分辨不出来源，你也就无法从结果反推它学了谁。

## 做法

向供应商要四样东西，并且落到纸面。训练数据的类别与时间范围，不接受"公开可得"这类笼统说法。有没有过滤与退出机制，权利人能否要求移除。你的输入是否用于训练，能否关闭，关闭后功能是否受损。商用授权的范围，是否覆盖你所在地区与发行渠道。自己这边也留档，采购日期、条款快照、对方答复邮件，都放进项目文件夹。条款会改，存的是当时那一版。跨境项目还要注意，不同法域对数据与人格利益的规则不一样，具体边界向律师核实。

## 听什么

在《裸体歌舞》第一首的谱面里听只有音符时缺了什么，触键与踏板都不在文件里；在肖邦夜曲作品37之2的录音里听同一份谱被演奏成什么样，那是另一层数据；在采集者署名的角笛舞曲里听一条旋律背后的具体来源，再对比只标"传统"的克莱兹默曲调，后者连该问谁都不清楚。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","B4","G4","E4","C4","G3"],"label":"谱面能给出的东西","label_en":"What a score can give","hint":"音符、时值与力度都有，触键与踏板没有","hint_en":"Pitch, duration and velocity are here; touch and pedal are not"}
```
:::

::: en
## The problem

Ask what a model was trained on and most product pages trail off into "millions of tracks" and "licensed and public data". For a user this is not gossip. Two practical questions hang on it. Can the output be used commercially, and will what you upload feed the next training round. Both depend on where the data came from and whether anyone agreed.

## How it works

Training data comes in layers. Scores and MIDI are symbolic, holding pitch, duration and velocity. Recordings are audio, carrying touch, breath and room. Lyrics and metadata are text. The three carry different rights and require consent from different people. A folk tune in symbolic form is often labelled traditional, but traditional is not a licence, it only means no known rights holder, while a collector, an arranger or a translator may each be a specific person. Audio adds performers and record producers on top. A model learns all of it together, so the output cannot tell you whose playing it absorbed, and you cannot work the provenance back from a result.

## Practice

Ask a vendor for four things in writing. The categories and date range of training data, not "publicly available". Whether there is filtering and an opt-out route for rights holders. Whether your inputs are used for training, whether that can be switched off, and what breaks if it is. The scope of the commercial licence, including your territory and distribution channels. Keep your own record too, purchase date, a snapshot of the terms, the reply email, all in the project folder. Terms change, so store the version you agreed to. Rules on data and personality interests differ by jurisdiction, so confirm the specifics with a lawyer.

## What to listen for

In the Gymnopedie score, what is missing when only notes remain, touch and pedal are not in the file. In the Chopin nocturne recording, what one score becomes under a pair of hands, which is another layer of data. In the hornpipe credited to a named collector, the specific source behind a tune, and then in the Klezmer tune labelled only traditional, a case where nobody is named to ask.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","B4","G4","E4","C4","G3"],"label":"What a score can give","label_en":"What a score can give","hint":"Pitch, duration and velocity are here; touch and pedal are not","hint_en":"Pitch, duration and velocity are here; touch and pedal are not"}
```
:::
