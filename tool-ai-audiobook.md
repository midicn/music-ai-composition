---
id: tool-ai-audiobook
site: ai
cat: J
title: 有声书工具
title_en: Audiobook Tools
summary: 有声书的难点不在音色，而在几十万字的读音一致与章节交付。
summary_en: The hard part of an audiobook is not the voice but consistent pronunciation and clean chapter delivery.
level: standard
tags: [有声书, 旁白, 发音, 交付]
tags_en: [audiobook, narration, pronunciation, delivery]
alias: [语音合成, 有声书制作, 长文本朗读]
order: 259
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:lufs]]"
  - "[[glossary:music-copyright]]"
  - "[[glossary:public-domain]]"
tool_kind: service
tool_vendor: ElevenLabs、Microsoft Azure AI Speech
tool_form: 服务
tool_platforms: [浏览器, macOS, Windows]
tool_price: 按量 + 订阅
tool_jobs: [有声书, 旁白, 本地化]
tool_verified: 2026-10-31
instances:
  - openscore-000008 | 《魔王》四个角色在几分钟内切换，试多角色音色分配与旁白基准（C1）
  - aria-159860 | 十八分钟的长段，章节底乐要连续铺满而不露接缝（C1）
  - maestro-000799 | 九分半的即兴曲，单章长度的器乐垫乐，句尾要给人声让位（C1）
  - chinafolk-000750 | 粤语童谣，儿童书的轻语气与句读参照（C1）
sources:
  - ElevenLabs、Microsoft Azure AI Speech 与 Amazon Polly 官方文档中的长文本、SSML 与发音词典说明。
  - W3C Speech Synthesis Markup Language 规范中停顿、重音与发音标注。
  - Audible 与 Spotify 有声书投稿规范中的章节、响度与元数据要求。
  - 合成语音披露与声音克隆同意的平台政策。
updated: 2026-10-31
---

::: zh
## 长文本要按章切

一次贴进十万字，语音合成会截断、超时或从头重来。按章或按场景切成一到三千字的块，每块单独生成、单独试听、单独重录。段落之间用停顿标记而不是空行，数字、单位、日期先写成要读出来的形式。角色对白与旁白分轨生成，后面才好调音量与语气。

## 发音词典是成败点

- 人名、地名、品牌先列清单，按出现顺序建词条。
- 多音字按上下文写，别靠默认读音：行、重、长、乐、着。
- 数字与符号写成口语：二〇二六、三点五、百分之二十。
- 英文缩写是逐字母还是连读，逐条指定。
- 音标或近似拼写二选一，团队统一，不要混用。
- 词条区分大小写与词形变化，复数与所有格单独加。
- 每改一次词典，抽三处回听，确认没有连带改坏别处。

## 章节交付检查清单

- 每章一个文件，文件名带书号、章号与版本。
- 开头与结尾各留半秒静音，章间不吞字。
- 全书响度一致，不靠后期压缩去救。
- 采样率与位深统一，交付格式跟平台要求。
- 章节标题、作者、朗读者在元数据里写全。
- 试听每章前三句与最后一句，专有名词逐个核对。
- 留一份未处理的干声，改稿时不用重生成整章。

## 哪些内容别交给合成语音

诗歌、方言对白、回忆录里的哭腔、法律免责声明，合成语音很难处理得体；需要角色表演的童书，也要人先定语气。克隆声音必须拿到本人书面同意，公开发布要按平台要求披露合成语音。训练素材与参考录音的授权范围，决定了成品能不能商用。

## 从一章开始

先做一章十五分钟的样带，把词典、停顿与响度定下来，再批量生成。之后再看响度归一、合成语音披露与版权归属的条目。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","E4","G3"],"label":"章节垫乐","label_en":"Chapter bed","hint":"把音量压到能听清字，再听垫乐是否还在","hint_en":"Drop the bed until words are clear, then hear whether the music survives"}
```
:::

::: en
## Cut long text by chapter

Paste a hundred thousand words at once and the engine truncates, times out or starts over. Cut by chapter or scene into blocks of one to three thousand characters, each generated, auditioned and re-recorded on its own. Mark paragraph pauses instead of relying on blank lines, and spell out numbers, units and dates the way they should be read. Generate dialogue and narration as separate tracks so level and tone can be adjusted later.

## The pronunciation lexicon decides the result

- List names, places and brands first, and add entries in order of appearance.
- Write heteronyms by context instead of trusting the default reading.
- Spell numbers and symbols as speech: years, decimals, percentages.
- Specify whether an abbreviation is spelled out or read as a word.
- Choose IPA or respelling, and keep one convention across the team.
- Respect case and inflections; add plurals and possessives separately.
- After each lexicon change, spot-check three places for collateral damage.

## Chapter delivery checklist

- One file per chapter, named with book, chapter and version.
- Half a second of silence at each end; no clipped first or last word.
- Consistent loudness across the book, not rescued by compression later.
- One sample rate and bit depth, in the format the platform asks for.
- Title, author and narrator complete in the metadata.
- Audition the first and last sentences of every chapter; check proper nouns one by one.
- Keep an untreated dry master so a revision does not regenerate whole chapters.

## What not to hand to a synthetic voice

Poetry, dialect dialogue, a sob in a memoir, legal disclaimers: synthetic speech struggles to carry them, and a children's book that needs character acting still needs a human to set the tone. Voice cloning requires written consent from the person, and public release must disclose synthetic speech where the platform requires it. The licence covering training and reference audio decides whether the result can be sold.

## Start with one chapter

Make a fifteen-minute sample chapter, settle the lexicon, pauses and loudness, then generate in batches. After that, read loudness normalisation, synthetic-voice disclosure and copyright ownership.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","E4","G3"],"label":"Chapter bed","label_en":"Chapter bed","hint":"Drop the bed until words are clear, then hear whether the music survives","hint_en":"Drop the bed until words are clear, then hear whether the music survives"}
```
:::
