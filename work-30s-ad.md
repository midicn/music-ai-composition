---
id: work-30s-ad
site: ai
cat: K
title: 三十秒广告
title_en: A Thirty-Second Ad
summary: 广告音乐要在两秒内抓住人，还要能剪成十五秒和六秒
summary_en: Ad music must hook in two seconds and survive cuts to fifteen and six.
level: standard
tags: [广告, 品牌, 剪辑, 交付]
tags_en: [advertising, brand, editing, delivery]
alias: [30秒广告, 广告配乐, TVC 音乐, 30s ad]
order: 1
tool_kind: guide
tool_vendor: 本站
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [广告配乐, 品牌传播, 剪辑适配]
tool_verified: 2026-10-30
links:
  - "[[glossary:sync-license]]"
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:cue]]"
instances:
  - pdmx-001170 | 主题不加铺垫直接出现，广告开头要的就是这种进入方式（C1）
  - giantmidi-007791 | 两秒内建立动机，钩子的长度可作参照（C1）
  - pdmx-000120 | 铜管长音与定音鼓收尾，logo 段落的收法（C1）
sources:
  - 广告音频的时长与响度交付口径（广播与流媒体公开规范）。
  - 广告音乐授权范围（媒介、地区、期限）的确认项，参考行业惯例。
updated: 2026-10-30
---

::: zh
## 需求长什么样

客户给一条三十秒片子，要求音乐贴画面、记住品牌、结尾落在 logo 上，同时交十五秒和六秒版本。投放渠道分电视、贴片与信息流，媒介、地区与期限决定授权范围。音乐要和旁白共存，句尾不能盖字。片子通常先有粗剪，音乐要随剪辑变化调整结构。交付不止一条立体声，还有分轨、无旁白版和三个时长版本。

## 工具组合

方向阶段用 Suno 或 Udio 快速出两三个三十秒草案，需要人声钩子时用 ACE Studio 唱。贴画面与剪版本在 Ableton Live、Logic Pro 或 Pro Tools 里完成。Demucs 用来分离参考素材或补分轨，iZotope RX 修噪声与口水音，Ozone 管响度与真峰值。生成负责方向，DAW 负责与画面同步，两件事分开做。

## 步骤

先写简报：三个时长、投放平台、旁白位置、品牌要的三个形容词。每个方向只做十五秒草图，同起点、同电平。选中后把音乐铺到画面，按剪辑点对齐重音，再定三十秒结构。十五秒与六秒版本从母版重剪，不重新生成。混音给旁白让出中频，母带按投放平台分别做。

## 验收标准

三个版本分别为三十秒、十五秒、六秒整，误差不超过一帧。钩子在前两秒出现，品牌落点与最后一帧对齐。电视版 -23 LUFS，网络版 -16 LUFS，真峰值不高于 -1 dBTP，三个版本的响度差不超过 0.5 LU。授权覆盖投放媒介、地区与期限。母版、分轨、无旁白版、提示词与生成记录齐全。

## 常见返工原因

前奏占了四小节，钩子迟到。音乐在 1 到 4 kHz 压住旁白。十五秒版重新生成，和三十秒版不是同一首。按网络响度做完直接送电视。授权只写网络，客户追加贴片。改时长时没锁速度，剪辑点整体错位。

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C4","E4","G4","C5","G4","E4"],"label":"三秒内说完的品牌动机","label_en":"A brand motif that lands in three seconds","hint":"听最后一个音能不能停住，品牌落点靠它","hint_en":"Hear whether the last note can hold; the logo lands on it"}
```
:::

::: en
## What the brief looks like

A client hands over a thirty-second film and asks for music that follows the picture, plants the brand and lands on the logo, plus fifteen- and six-second versions. Placement may be television, pre-roll or a social feed, and the medium, territory and term set the licence. The music has to share space with narration without covering the last word. The film usually exists as a rough cut first, so the score changes with it. Delivery is not one stereo file but stems, a no-voice version and three durations.

## Tool combination

Use Suno or Udio to sketch two or three thirty-second directions, and ACE Studio when the hook needs a sung voice. Cut picture and versions in Ableton Live, Logic Pro or Pro Tools. Demucs separates a reference or fills in missing stems, iZotope RX repairs noise and mouth clicks, Ozone handles loudness and true peak. Generation settles direction; the DAW settles sync.

## Steps

Write the brief first: three durations, placement, narration position and three adjectives the brand wants. Make each direction a fifteen-second sketch, same start, same level. Once chosen, lay the music against picture, align accents to cuts, then build the thirty-second structure. Cut the fifteen and six from the master rather than regenerating. Mix to leave the midrange for narration, and master separately per platform.

## Acceptance criteria

The three versions run exactly thirty, fifteen and six seconds, within one frame. The hook arrives in the first two seconds and the brand lands on the final frame. Television is mixed to -23 LUFS, online to -16 LUFS, true peak no higher than -1 dBTP, and the versions sit within 0.5 LU of each other. The licence covers medium, territory and term. Master, stems, no-voice version, prompts and generation records are all present.

## Common rework causes

A four-bar intro delays the hook. The music masks narration between 1 and 4 kHz. The fifteen is regenerated and no longer matches the thirty. A mix made for online goes straight to television. The licence names online only and the client adds pre-roll. Changing duration without locking tempo moves every cut.

```audiolab
{"type":"instrument","gm":"Brass Section","synth":"brass","phrase":["C4","E4","G4","C5","G4","E4"],"label":"A brand motif that lands in three seconds","label_en":"A brand motif that lands in three seconds","hint":"Hear whether the last note can hold; the logo lands on it","hint_en":"Hear whether the last note can hold; the logo lands on it"}
```
:::
