---
id: "work-audiobook"
site: "ai"
cat: "K"
title: "做一集有声书"
title_en: "Produce an Audiobook Episode"
summary: "长文本先分章，角色与气口决定听众能不能跟下去"
summary_en: "Chapter the text first; casting and breath decide whether a listener stays."
level: "standard"
tags: ["有声书", "长文本", "角色", "质检"]
tags_en: ["audiobook", "long-form", "characters", "QC"]
alias: ["有声书", "有声书制作", "audiobook", "长文本朗读"]
order: 260
tool_kind: "guide"
tool_vendor: "—"
tool_form: "案例"
tool_platforms: ["通用"]
tool_price: "不适用"
tool_jobs: ["有声书", "长文本朗读", "章节交付"]
tool_verified: "2026-10-31"
links: ["[[glossary:loudness-normalization]]", "[[glossary:stems]]", "[[instrument:voice]]"]
instances: []
sources: ["https://help.acx.com/s/article/what-are-the-acx-audio-submission-requirements", "https://help.acx.com/s/article/upload-audio-files"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "有声书交付需按章测量编码、峰值、底噪和实际投稿准入；ACX 未经授权禁止合成朗读，普通音乐播放不能证明这些条件得到满足。"
---

::: zh
## 交付的不是一条音频

先按接收方要求确认分章方式、文件格式和交付清单；整集母版、章节表、发音表与质检记录可另作项目归档。以 ACX 为例，音频要求为 -23 至 -18 dB RMS，峰值不高于 -3 dB，底噪不高于 -60 dB RMS；每个文件只包含一章或一个章节单元。ACX 建议首尾保留 1–5 秒 room tone。其他平台的口径可能不同，不应把这些数值当作统一标准。ACX 同时要求真人朗读，除非另获授权。

## 先分词，再出声，最后分章

第一步通读全文，按场景切章，把生僻词、人名、外来语列成发音表，标出每个角色的音区与语速。第二步录旁白，旁白保持稳定，角色只做轻微音色差别，不要在一个人身上演三个腔调。第三步按章导出，统一响度，逐章试听，修齿音、口水音与句尾塌下去的气口。生成工具只用来做章节之间的过渡垫乐，不参与正文朗读。

## 工具分工

朗读在 Audacity、Adobe Audition 或 Descript 里录和剪，Descript 的文本编辑适合改口误，发音词典用来锁人名。iZotope RX 处理齿音、房间反射与底噪，Auphonic 或 Ozone 统一每章响度。过渡垫乐用 Suno 或 Udio 生成无人声片段，长度控制在五到八秒。章节表与发音表放在同一个交付目录，文件名带章节号。

## 哪里会坏

角色演得过满，听众先注意表演再听内容。齿音修得太狠，声音发闷。每章单独压限，连播时一章比一章响。过渡垫乐带人声哼唱，和旁白打架。发音表没锁，同一人名三种读法。授权只写了背景音乐，没有覆盖有声书的商业发行与试听片段。
:::

::: en
## What leaves the studio

Confirm chapter structure, file format and delivery items with the receiving platform. A full-program master, chapter list, pronunciation sheet and QC log can be kept as project records. For ACX, audio must measure between -23 and -18 dB RMS, with peaks no higher than -3 dB and a noise floor no higher than -60 dB RMS; each file contains one chapter or section. ACX recommends 1–5 seconds of room tone at the head and tail. These are platform-specific requirements, not a universal standard. ACX also requires human narration unless otherwise authorized.

## Read, record, chapter

Read the whole text first and cut chapters at scene changes. Build a pronunciation sheet for names, dialect words and foreign terms, and note the register and pace of each character. Record the narration straight; characters get a light change of timbre, not three accents from one throat. Export chapter by chapter, set loudness once, and audition each file for sibilance, mouth noise and sagging phrase endings. Generation is only for five-to-eight-second transitions between chapters, never for the body of the read.

## Where the tools sit

Record and edit in Audacity, Adobe Audition or Descript; Descript's text editing is good for fixing fluffs, and its pronunciation lexicon locks names. iZotope RX handles sibilance, room reflection and noise floor, while Auphonic or Ozone matches chapter loudness. Make transition beds with Suno or Udio, instrumental and short. Keep the chapter list and pronunciation sheet in the delivery folder, and put the chapter number in every file name.

## Three listening passes

| Check | Pass line | What the ear hears |
|---|---|---|
| Noise floor | Below -60 dB | No hum or room tone in silence |
| Loudness | -23 to -18 dB RMS | No jump between consecutive chapters |
| Peaks | No higher than -3 dB | Emphatic lines do not clip |
| Chapters | Even head and tail silence | Playback does not lurch |
| Characters | Audibly different timbre | You can tell who speaks with eyes closed |
| Pronunciation | Matches the sheet | Names need no re-read |

## Where it breaks

A character is overplayed and performance outranks content. Sibilance is over-repaired and the voice turns dull. Each chapter is limited on its own, so the book gets louder chapter by chapter. A transition bed carries a hummed vocal that fights the narrator. The pronunciation sheet is not enforced and one name gets three readings. The licence covers background music only, not commercial audiobook release and sample clips.
:::

