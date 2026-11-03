---
id: "tool-ai-audiobook"
site: "ai"
cat: "J"
title: "有声书工具"
title_en: "Audiobook Tools"
summary: "有声书的难点不在音色，而在几十万字的读音一致与章节交付。"
summary_en: "The hard part of an audiobook is not the voice but consistent pronunciation and clean chapter delivery."
level: "standard"
tags: ["有声书", "旁白", "发音", "交付"]
tags_en: ["audiobook", "narration", "pronunciation", "delivery"]
alias: ["语音合成", "有声书制作", "长文本朗读"]
order: 259
links: ["[[glossary:loudness-normalization]]", "[[glossary:lufs]]", "[[glossary:music-copyright]]", "[[glossary:public-domain]]"]
tool_kind: "service"
tool_vendor: "ElevenLabs、Microsoft Azure AI Speech"
tool_form: "服务"
tool_platforms: ["浏览器", "macOS", "Windows"]
tool_price: "按量 + 订阅"
tool_jobs: ["有声书", "旁白", "本地化"]
tool_verified: "2026-10-31"
instances: []
sources: ["https://www.w3.org/TR/speech-synthesis/", "https://help.acx.com/s/article/what-are-the-acx-audio-submission-requirements"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "有声书工具涉及发音标记、分章和平台准入，ACX 对未经授权的合成朗读另有限制；普通音频播放不能证明全文发音合格或具备投稿资格。"
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
- 首尾留白按接收平台要求设置，避免截断首尾字；ACX 建议保留 1–5 秒 room tone，不能直接套用半秒静音。
- 全书响度一致，连播时检查相邻章节的音量变化。
- 采样率与位深统一，交付格式跟平台要求。
- 章节标题、作者、朗读者在元数据里写全。
- 试听每章前三句与最后一句，专有名词逐个核对。
- 留一份未处理的干声，改稿时不用重生成整章。

## 哪些内容别交给合成语音

诗歌、方言对白、回忆录里的哭腔、法律免责声明，合成语音很难处理得体；需要角色表演的童书，也要人先定语气。克隆声音必须拿到本人书面同意，公开发布要按平台要求披露合成语音。训练素材与参考录音的授权范围，决定了成品能不能商用。

## 从一章开始

先确认目标平台是否接受合成朗读，再做样章。ACX 当前要求真人朗读，除非另获授权；达到其 RMS、峰值和底噪指标并不等于获准提交 AI 朗读。确认准入后，用一章样带确定词典、停顿和响度，再批量制作。
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
- Follow the receiving platform’s head-and-tail spacing requirements without clipping words. ACX recommends 1–5 seconds of room tone; half a second of silence is not a universal specification.
- Keep loudness consistent and check adjacent chapters in continuous playback.
- Use consistent sample rate and bit depth, in the format the platform asks for.
- Complete the title, author and narrator metadata.
- Audition the opening and closing sentences of every chapter and check proper nouns.
- Keep an untreated dry master for revisions.

## What not to hand to a synthetic voice

Poetry, dialect dialogue, a sob in a memoir, legal disclaimers: synthetic speech struggles to carry them, and a children's book that needs character acting still needs a human to set the tone. Voice cloning requires written consent from the person, and public release must disclose synthetic speech where the platform requires it. The licence covering training and reference audio decides whether the result can be sold.

## Start with one chapter

Confirm whether the receiving platform accepts synthetic narration before producing a sample chapter. ACX currently requires human narration unless otherwise authorized; meeting its RMS, peak and noise-floor limits does not establish permission to submit AI narration. Once eligibility is confirmed, use a sample chapter to settle pronunciation, pauses and loudness before batch production.
:::

