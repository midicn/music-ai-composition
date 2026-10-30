---
id: work-cover
site: ai
cat: K
title: 翻唱
title_en: A Cover Version
summary: 词曲许可与录音许可分开算，改歌词就变成另一件事
summary_en: Composition and master licences are separate; changing lyrics makes it a different job.
level: standard
tags: [翻唱, 授权, 人声, 编曲]
tags_en: [cover, licensing, vocals, arrangement]
alias: [翻唱, cover, 翻唱授权, 二次演唱]
order: 6
tool_kind: guide
tool_vendor: 本站
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [翻唱制作, 人声合成, 授权确认]
tool_verified: 2026-10-30
links:
  - "[[glossary:melody]]"
  - "[[glossary:key]]"
  - "[[glossary:timbre]]"
instances:
  - thesession-015842 | 传统曲调的演唱版本，咬字与呼吸是合成人声的弱点（C1）
  - openscore-000014 | 英语艺术歌曲，辅音起音决定词的边界（C1）
  - mutopia-001093 | 乔普林《枫叶拉格》，切分与左手跳进是可指认的创作选择（C1）
sources:
  - 翻唱涉及的词曲与录音两类权利，依发行与平台公开规则核对，未抄原文
  - 翻唱的署名与改编边界，依行业通识归纳
updated: 2026-10-30
---

::: zh
## 需求长什么样

客户想要一首已有歌曲的翻唱，可以换歌手、换编曲或换语言。先分清两件事：词曲版权与原始录音的版权。只用自己的伴奏与演唱，仍然要为词曲取得机械许可。平台各有翻唱规则，商用与非商用不同。翻唱不等于免版权，越接近原版，越容易被识别。交付通常是母版、伴奏与清唱三条。

## 工具组合

伴奏用 Suno 或 Udio 生成，或按原曲重编。人声用 ACE Studio 或 Synthesizer V 合成，真人录唱同样可行。音准与节奏在 Melodyne 里修。工程放在 Ableton Live、Logic Pro 或 REAPER。Demucs 只用于分析原曲结构，分离出的伴奏不能直接发行。iZotope RX 修噪声。

## 步骤

先确认词曲授权与平台规则，写下原曲作者与出版方。定调与速度，必要时整体升降。做一版新伴奏，保留原曲的和声骨架。录或合成主唱，修音准但不改咬字。叠和声与双轨。混音给人声留出中频。母带后分别导出伴奏、清唱与成品。

## 验收标准

歌词与旋律与原曲一致，改词就按改编重新授权。成品时长与原曲相差不超过五秒，编曲明确改结构时另算。调性与速度写进元数据。伴奏里不能残留原曲录音的片段。整体 -14 LUFS，真峰值不高于 -1 dBTP。词曲许可与录音许可分别存档。署名包含原曲作者。

## 常见返工原因

用了原曲伴奏，却没拿录音许可。歌词改了几个字，性质变成改编。合成人声咬字含糊，副歌听不清。升调后高音挤，修音痕迹明显。平台识别出原曲，视频被静音。署名漏了作者，发行被退回。清唱与伴奏电平不匹配，混起来人声发飘。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["G4","A4","B4","D5","B4","A4","G4","E4"],"label":"翻唱要保留的旋律骨架","label_en":"The melodic skeleton a cover must keep","hint":"换编曲可以，骨架一散就不是翻唱","hint_en":"Rearrange freely, but once the skeleton dissolves it is no longer a cover"}
```
:::

::: en
## What the brief looks like

A client wants a cover of an existing song, perhaps with another singer, another arrangement or another language. Two rights have to be separated first: the composition and the original recording. Even with your own backing track and your own voice, the composition still needs a mechanical licence. Platforms have their own cover rules, and commercial use differs from personal use. A cover is not copyright-free, and the closer it sits to the original the more likely it is to be recognised. Delivery is usually a master, a backing track and an a cappella.

## Tool combination

Generate the backing with Suno or Udio, or re-arrange from the original. Synthesize the vocal with ACE Studio or Synthesizer V, or record a real singer. Fix pitch and timing in Melodyne. Work in Ableton Live, Logic Pro or REAPER. Demucs is for studying the original's structure; a separated backing cannot be released as your own. iZotope RX repairs noise.

## Steps

Confirm the composition licence and platform rules, and note the writers and publisher. Settle key and tempo, transposing the whole song if needed. Build a new backing that keeps the harmonic frame. Record or synthesize the lead, correcting pitch without changing diction. Add harmonies and doubles. Mix with room for the voice in the midrange. Master, then export backing, a cappella and full mix separately.

## Acceptance criteria

Lyrics and melody match the original; changed lyrics require a derivative licence. The finished track is within five seconds of the original length unless the brief restructures it. Key and tempo are in the metadata. The backing carries no fragments of the original recording. The master sits at -14 LUFS with true peak no higher than -1 dBTP. Composition and master licences are filed separately. Credits name the original writers.

## Common rework causes

The original backing is used without a master licence. A few words are changed and the work becomes a derivative. Synthesized diction is mushy and the chorus is unintelligible. A key lift makes the top notes tight and the tuning audible. The platform recognises the song and mutes the video. A writer is missing from the credits and distribution is rejected. The a cappella and backing are not level-matched, so the voice floats when they are combined.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["G4","A4","B4","D5","B4","A4","G4","E4"],"label":"The melodic skeleton a cover must keep","label_en":"The melodic skeleton a cover must keep","hint":"Rearrange freely, but once the skeleton dissolves it is no longer a cover","hint_en":"Rearrange freely, but once the skeleton dissolves it is no longer a cover"}
```
:::
