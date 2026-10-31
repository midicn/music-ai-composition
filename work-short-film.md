---
id: work-short-film
site: ai
cat: K
title: 短片配乐
title_en: Scoring a Short Film
summary: 先有 cue 表再写音乐，留白与对白位置决定成败
summary_en: A cue sheet comes before the music; silence and dialogue placement decide the result.
level: standard
tags: [短片, 配乐, 对白, 时间码]
tags_en: [short film, scoring, dialogue, timecode]
alias: [短片配乐, 电影配乐, short film score]
order: 5
tool_kind: guide
tool_vendor: 本站
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [影视配乐, 对白混音, 母带交付]
tool_verified: 2026-10-30
links:
  - "[[glossary:cue]]"
  - "[[glossary:sync-license]]"
  - "[[glossary:dynamics]]"
instances:
  - pdmx-000160 | 固定音型加独奏小提琴写场面，临时音轨常用的方向（C1）
  - pdmx-000580 | 大编制在空间里铺开，听爆发前的留白（C1）
  - mutopia-000497 | 贝多芬第五第一乐章，长、密、多声部，生成与迭代都更贵（C1）
sources:
  - 影视响度与交付口径（广播与发行公开规范）。
  - cue 表与 spotting 的做法，参考影视配乐惯例。
updated: 2026-10-30
---

::: zh
## 需求长什么样

一部五到二十分钟的剧情短片需要一张 cue 表，标明每段的情绪、起止时间码与是否压对白。导演先给粗剪，音乐跟着画面改。片子既送电影节也上网络，两套响度要求不同。交付包含母版、分轨、cue 表与授权说明，片名与版本号写进每份文件，缺一样都过不了后期。

## 工具组合

用 Suno 或 Udio 做每段初稿，Udio 便于同一主题做变奏。真实乐器质感用 Spitfire 或 Kontakt 的音色补，人声吟唱用 ACE Studio。贴画面与混音在 Pro Tools、Logic Pro 或 Ableton Live 里做。iZotope RX 修对白，Ozone 做母带。生成负责素材，时间码上的取舍由人决定。

## 步骤

先和导演做 spotting，把每段的入点、出点与情绪写进 cue 表，用临时音轨试长度。逐段生成，保留同一动机的连续性。把音乐贴到画面，按动作与台词调整重音。对白段让出 1 到 4 kHz，必要时做自动化。混音分对白、音乐、音效三组。母带按电影节与网络各做一版。

## 验收标准

每段 cue 的起止与时间码误差不超过一帧。对白段音乐比对白低 6 dB 以上，字头清楚，单声道下相位不抵消。全片动态保留，最响与最轻段差不少于 12 dB。电影节版 -23 LUFS，网络版 -14 LUFS，真峰值不高于 -1 dBTP。分轨、cue 表与授权文件齐全。授权覆盖电影节报名、展映与线上发行。

## 常见返工原因

临时音轨太合适，导演要一模一样。音乐铺满全片，没有留白。动作点没对上，打斗像配乐练习。对白被压，台词听不清。母带压得太狠，安静段落没有空间。授权只写展映，报名电影节时被拒。分轨与母带不是同一版，客户听到两个结果。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","C4","E4","D4","C4","G3","C3"],"label":"一段留白里的大提琴","label_en":"A cello line with room around it","hint":"听句子之间空出来的地方，那里也属于配乐","hint_en":"Hear the gaps between phrases; they are part of the score too"}
```
:::

::: en
## What the brief looks like

A five-to-twenty-minute narrative short needs a cue sheet listing each cue's mood, start and end timecode, and whether it sits under dialogue. The director supplies a rough cut and the music follows it. The film goes to festivals and online, which means two loudness targets. Delivery includes the master, stems, the cue sheet and a licence note, with the film title and version in every file name; miss one and post stalls.

## Tool combination

Sketch each cue with Suno or Udio, and use Udio when one theme needs variations. Spitfire or Kontakt supplies acoustic texture and ACE Studio covers sung lines. Lay cues against picture and mix in Pro Tools, Logic Pro or Ableton Live. iZotope RX repairs dialogue, Ozone handles the master. Generation supplies material; decisions at timecode stay human.

## Steps

Do a spotting pass with the director and write each cue's in point, out point and mood into the sheet, testing length against a temp track. Generate cue by cue and keep one motif recurring. Place music against picture and move accents to action and lines. Under dialogue, clear 1 to 4 kHz with automation where needed. Mix in three groups: dialogue, music, effects. Master once for festivals and once for online.

## Acceptance criteria

Every cue starts and ends within one frame of its timecode. Under dialogue the music sits at least 6 dB below speech and consonants stay clear without phase cancellation in mono. The film keeps its dynamics, with at least 12 dB between the loudest and quietest passages. The festival version is -23 LUFS, the online version -14 LUFS, true peak no higher than -1 dBTP. Stems, cue sheet and licence documents are complete. The licence covers festival submission, screenings and online release.

## Common rework causes

The temp track is too good and the director wants it matched. Music runs wall to wall with no silence. Action points are missed and a fight sounds like a scoring exercise. Dialogue is buried and lines are lost. The master is crushed and quiet scenes have no air. The licence covers screenings only and a festival submission is rejected. Stems and master come from different versions, so the client hears two results.

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","C4","E4","D4","C4","G3","C3"],"label":"A cello line with room around it","label_en":"A cello line with room around it","hint":"Hear the gaps between phrases; they are part of the score too","hint_en":"Hear the gaps between phrases; they are part of the score too"}
```
:::
