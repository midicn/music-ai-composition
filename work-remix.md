---
id: work-remix
site: ai
cat: K
title: 重混
title_en: A Remix
summary: 先拿到分轨与授权，再动人声的时间与音高
summary_en: Get the stems and the licence before touching the vocal's time and pitch.
level: standard
tags: [重混, 分轨, 授权, 舞曲]
tags_en: [remix, stems, licensing, dance]
alias: [重混, remix, 混音改编, bootleg]
order: 11
tool_kind: guide
tool_vendor: 本站
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [重混, 分轨处理, 舞曲制作]
tool_verified: 2026-10-30
links:
  - "[[glossary:stems]]"
  - "[[glossary:tempo]]"
  - "[[glossary:key]]"
instances:
  - mutopia-000497 | 贝多芬第五，大型工程缺一层就无法重混（C1）
  - groove-000002 | 86 BPM 灵魂乐鼓组，听军鼓落在拍后那一点（C1）
  - openscore-000269 | 马勒艺术歌曲，人声从低语到爆发，宏观动态清楚（C1）
sources:
  - 重混的分轨与授权流程（发行与制作惯例）。
  - 时间伸缩与移调对音色的影响，参考音频处理公开资料。
updated: 2026-10-30
---

::: zh
## 需求长什么样

把一首已有歌曲重混成舞曲或另一种风格，客户是版权方，或自己做一版 bootleg，用途决定能不能发行。官方重混会拿到分轨与授权，bootleg 只能靠分离，且不能发行。要保留原曲最可识别的部分，通常是主唱。重混不是换一套鼓，原曲的身份要留下来。速度、调性与结构与原曲的关系要写清楚。交付包含成品、分轨与 credit。

## 工具组合

分轨来自版权方。没有分轨时用 Demucs 分离，但要接受串音。变速与变调在 Ableton Live 或 Logic Pro 里做，Melodyne 修人声共振峰。新编曲用 Serum 与 Vital 做合成器层，鼓组用采样。Suno 或 Udio 可做风格草图。iZotope RX 清人声，Ozone 做母带。

## 步骤

先确认授权与 stem 清单，写下原曲版本。定新速度与调性，算出人声需要的时间伸缩比例。把主唱对齐到新网格，逐句听咬字。搭新鼓组与贝斯，再叠和声与效果。安排 breakdown 与 drop，保留原曲钩子。混音给人声留位置。母带分俱乐部版与流媒体版。

## 验收标准

人声与新网格误差不超过 10 毫秒，咬字不变形。调性关系写明，移调不超过三个半音。成品时长符合约定，钩子至少出现两次。俱乐部版 -8 到 -9 LUFS，流媒体版 -14 LUFS，真峰值不高于 -0.5 dBTP。授权覆盖发行与平台，credit 写明原曲作者与重混者。工程里保留原曲参考轨，写清原曲 BPM 并标注版本号。分轨与工程齐全。

## 常见返工原因

分离出的人声带串音，镲片跟着唱。拉伸比例太大，人声发金属味。鼓组太满，原曲钩子被埋。bootleg 直接上架，收到下架通知。credit 只写自己，原作者缺失。响度做到 -6 LUFS，平台压回来后动态全无。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q e e e e q q q q","bpm":128,"label":"人声对齐的新网格","label_en":"A new grid the vocal must sit on","hint":"听主唱落在拍上还是拍后，重混的松紧全在这里","hint_en":"Hear whether the vocal sits on or behind the beat; the feel lives there"}
```
:::

::: en
## What the brief looks like

An existing song is remixed into dance music or another style, and the client may be the rights holder or the producer's own bootleg. An official remix comes with stems and a licence; a bootleg relies on separation and cannot be released. The most recognisable part, usually the lead vocal, has to survive. A remix is not a new drum kit; the identity of the original stays. The relationship of tempo, key and structure to the original must be stated. Delivery includes the master, stems and credits.

## Tool combination

Stems come from the rights holder. Without them, Demucs separates a mix, bleed included. Change tempo and key in Ableton Live or Logic Pro, and repair vocal formants in Melodyne. Build new synth layers with Serum and Vital, and drums from samples. Suno or Udio can sketch a style. iZotope RX cleans the vocal, Ozone masters.

## Steps

Confirm the licence and the stem list, and note which version of the original is used. Choose the new tempo and key, then calculate the time-stretch ratio the vocal needs. Align the lead to the new grid and check diction line by line. Build new drums and bass, then add harmony and effects. Plan a breakdown and a drop while keeping the original hook. Mix with room for the vocal. Master a club version and a streaming version.

## Acceptance criteria

The vocal sits within 10 ms of the new grid without distorting diction. The key relationship is documented and transposition stays within three semitones. The length matches the brief and the hook appears at least twice. The club version is -8 to -9 LUFS, the streaming version -14 LUFS, true peak no higher than -0.5 dBTP. The licence covers release and platforms, and credits name the original writers and the remixer. The session keeps a reference track of the original with its tempo and version noted. Stems and the session are included.

## Common rework causes

A separated vocal carries bleed and the cymbals sing along. The stretch ratio is extreme and the voice turns metallic. Drums are so full that the original hook disappears. A bootleg goes live and draws a takedown. Credits name only the remixer and the original writers are missing. The mix hits -6 LUFS and the platform turns it down to nothing.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q e e e e q q q q","bpm":128,"label":"A new grid the vocal must sit on","label_en":"A new grid the vocal must sit on","hint":"Hear whether the vocal sits on or behind the beat; the feel lives there","hint_en":"Hear whether the vocal sits on or behind the beat; the feel lives there"}
```
:::
