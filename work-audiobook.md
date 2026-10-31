---
id: work-audiobook
site: ai
cat: K
title: 做一集有声书
title_en: Produce an Audiobook Episode
summary: 长文本先分章，角色与气口决定听众能不能跟下去
summary_en: Chapter the text first; casting and breath decide whether a listener stays.
level: standard
tags: [有声书, 长文本, 角色, 质检]
tags_en: [audiobook, long-form, characters, QC]
alias: [有声书, 有声书制作, audiobook, 长文本朗读]
order: 260
tool_kind: guide
tool_vendor: —
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [有声书, 长文本朗读, 章节交付]
tool_verified: 2026-10-31
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:stems]]"
  - "[[instrument:voice]]"
instances:
  - pdmx-000153 | 二十六分钟不间断的长文件，章节切分与长段电平都要在这里过关（C1）
  - mutopia-001411 | 三分钟钢琴小品，句短、留白多，垫在朗读下不抢字（C1）
  - thesession-015842 | 四十六秒的短旋律，句短、换气清楚，旁白的断句可参照（C1）
  - pdmx-000789 | 独唱与合唱交替，角色声线的区分可借这种层次（C1）
sources:
  - ACX 公开的音频提交要求，涉及底噪、RMS 与峰值。
  - 有声书朗读与章节交付的制作惯例。
updated: 2026-10-31
---

::: zh
## 交付的不是一条音频

一集三十分钟的有声书，中文大约八千到一万字。交给平台的是每章一个文件加一条整集母版，另附章节表、发音表与质检记录。平台对底噪、响度和峰值有硬口径：底噪低于 -60 dB，RMS 在 -23 到 -18 dB 之间，峰值不超过 -3 dB。开头结尾各留零点五到一秒静音，章与章之间不能忽长忽短。听众每天听半小时，一处齿音或喷麦会在通勤路上被放大。

## 先分词，再出声，最后分章

第一步通读全文，按场景切章，把生僻词、人名、外来语列成发音表，标出每个角色的音区与语速。第二步录旁白，旁白保持稳定，角色只做轻微音色差别，不要在一个人身上演三个腔调。第三步按章导出，统一响度，逐章试听，修齿音、口水音与句尾塌下去的气口。生成工具只用来做章节之间的过渡垫乐，不参与正文朗读。

## 工具分工

朗读在 Audacity、Adobe Audition 或 Descript 里录和剪，Descript 的文本编辑适合改口误，发音词典用来锁人名。iZotope RX 处理齿音、房间反射与底噪，Auphonic 或 Ozone 统一每章响度。过渡垫乐用 Suno 或 Udio 生成无人声片段，长度控制在五到八秒。章节表与发音表放在同一个交付目录，文件名带章节号。

## 试听三遍的判据

| 检查项 | 通过线 | 听感判据 |
|---|---|---|
| 底噪 | 低于 -60 dB | 静音处没有电流声与房间嗡声 |
| 响度 | -23 到 -18 dB RMS | 相邻两章接续播放不跳音量 |
| 峰值 | 不高于 -3 dB | 强调句不破 |
| 章节 | 头尾静音一致 | 连播时节奏不忽快忽慢 |
| 角色 | 音色有差别 | 不看文本能分出谁在说 |
| 发音 | 与发音表一致 | 人名与术语不需回读 |

## 哪里会坏

角色演得过满，听众先注意表演再听内容。齿音修得太狠，声音发闷。每章单独压限，连播时一章比一章响。过渡垫乐带人声哼唱，和旁白打架。发音表没锁，同一人名三种读法。授权只写了背景音乐，没有覆盖有声书的商业发行与试听片段。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G4","E4","C5","G4","E4","D4","C4"],"label":"朗读下面的钢琴，句子之间留空","label_en":"Piano under narration, with gaps between phrases","hint":"听句子之间有没有留出换气的位置","hint_en":"Hear whether each phrase leaves room to breathe"}
```
:::

::: en
## What leaves the studio

A thirty-minute episode runs to eight or ten thousand Chinese characters. The platform receives one file per chapter plus a full-episode master, a chapter list, a pronunciation sheet and a QC log. The technical limits are fixed: noise floor below -60 dB, RMS between -23 and -18 dB, peaks no higher than -3 dB. Leave half a second to a second of silence at the head and tail, and keep that gap consistent between chapters. Listeners hear half an hour a day, so one sibilant or plosive gets magnified on a commute.

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

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G4","E4","C5","G4","E4","D4","C4"],"label":"Piano under narration, with gaps between phrases","label_en":"Piano under narration, with gaps between phrases","hint":"Hear whether each phrase leaves room to breathe","hint_en":"Hear whether each phrase leaves room to breathe"}
```
:::
