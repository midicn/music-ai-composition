---
id: work-jingle
site: ai
cat: K
title: 品牌音效
title_en: A Brand Sonic Logo
summary: 三到五秒要能记住，还要在手机外放上站得住
summary_en: Three to five seconds must be memorable and still work on a phone speaker.
level: standard
tags: [品牌, 音效, 广告歌, 买断]
tags_en: [brand, sonic logo, jingle, buyout]
alias: [品牌音效, 声音标识, sonic logo, 广告歌]
order: 9
tool_kind: guide
tool_vendor: 本站
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [品牌声音, 广告歌, 音频标识]
tool_verified: 2026-10-30
links:
  - "[[glossary:timbre]]"
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:true-peak]]"
instances:
  - pdmx-000120 | 铜管长音与定音鼓，logo 段落的收法（C1）
  - oga-000053 | 两秒的 fanfare，方向阶段第一个短选项（C1）
  - oga-000054 | 同长度的第二个 fanfare，正好做 A/B 对照（C1）
sources:
  - 品牌声音标识的时长与买断范围，参考品牌与广告制作惯例。
  - 广播与网络响度口径；公开规范是主要依据。
updated: 2026-10-30
---

::: zh
## 需求长什么样

一条三到五秒的品牌声音标识，加十五秒与三十秒的广告歌版本，通常用于电视、广播、App 启动与客服等待音。品牌名必须听清，旋律要能哼出来。手机外放几乎没有低频，混音要按小喇叭检查。声音标识和广告歌是两件交付，可以分开验收。客户通常要买断，授权覆盖所有媒介与地区。

## 工具组合

方向阶段用 Suno 或 Udio 生成几条短动机，品牌名用 ACE Studio 唱，真人演唱同样可行。工程与剪辑放在 Ableton Live、Logic Pro 或 Pro Tools。iZotope RX 修人声，Ozone 统一响度与真峰值。需要器乐版时用 Demucs 分出人声，再补录替代声部。

## 步骤

先写品牌三个形容词与禁用词，定三到五个音的核心动机。做三个方向，每个五秒，同起点同电平。选中后扩展成十五秒与三十秒，结构是动机、展开、回到动机。品牌名放在重拍上，辅音要清楚。做无人声版与纯音乐版。手机、笔记本、电视各听一遍。最后按媒介分别母带。

## 验收标准

声音标识为三到五秒整，广告歌为十五秒与三十秒整。品牌名在首尾各出现一次，听写测试能复述。手机外放能听出旋律轮廓，300 Hz 到 3 kHz 有足够能量。网络版 -16 LUFS，广播版 -23 LUFS，真峰值不高于 -1 dBTP。授权为买断，覆盖全部媒介与地区。所有版本响度一致，从同一工程导出。三种时长与伴奏版齐全。

## 常见返工原因

动机太复杂，五秒记不住。品牌名被和声盖住，听不清。低频做太多，手机外放只剩噗噗声。三个版本像三首歌，品牌不统一。授权只覆盖电视，App 启动音要另签。棚里好听，客户手机上一团。

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C4","G4","A4","C5"],"label":"五秒品牌动机","label_en":"A five-second brand motif","hint":"只听一遍，看能不能哼回来","hint_en":"Listen once and see whether you can hum it back"}
```
:::

::: en
## What the brief looks like

A three-to-five-second sonic logo plus fifteen- and thirty-second jingle versions, used on television, radio, an app launch and a hold line. The brand name has to be intelligible and the melody hummable. A phone speaker has almost no low end, so the mix is checked on a small driver. The logo and the jingle are two deliverables and can be accepted separately. Clients usually want a buyout covering all media and territories.

## Tool combination

Sketch short motifs with Suno or Udio, and sing the brand name with ACE Studio or a real voice. Build and edit in Ableton Live, Logic Pro or Pro Tools. iZotope RX repairs the vocal, Ozone sets loudness and true peak. When an instrumental is needed, Demucs lifts the vocal and replacement parts are recorded.

## Steps

Write three brand adjectives and the words to avoid, then set a core motif of three to five notes. Make three directions of five seconds each, same start and level. Extend the chosen one to fifteen and thirty seconds with a shape of motif, development, return. Put the brand name on a strong beat and keep consonants clear. Produce a no-voice and an instrumental version. Listen on a phone, a laptop and a television. Master separately per medium.

## Acceptance criteria

The logo runs exactly three to five seconds and the jingles exactly fifteen and thirty. The brand name appears at the start and the end and survives a dictation test. The melody's outline is audible on a phone speaker, with enough energy between 300 Hz and 3 kHz. Online is -16 LUFS, broadcast -23 LUFS, true peak no higher than -1 dBTP. The licence is a buyout covering all media and territories, every version is matched in loudness, and all of them come out of one session. Three durations and the backing version are delivered.

## Common rework causes

The motif is too busy to remember in five seconds. Harmonies bury the brand name. Too much low end leaves only thumps on a phone. The three versions sound like three different songs and the brand stops being consistent. The licence covers television only and an app launch needs a new deal. It sounds good in the studio and turns to mush on the client's phone.

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C4","G4","A4","C5"],"label":"A five-second brand motif","label_en":"A five-second brand motif","hint":"Listen once and see whether you can hum it back","hint_en":"Listen once and see whether you can hum it back"}
```
:::
