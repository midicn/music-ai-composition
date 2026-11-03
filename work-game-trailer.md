---
id: "work-game-trailer"
site: "ai"
cat: "K"
title: "做游戏预告片"
title_en: "Cut a Game Trailer"
summary: "先标 hit point 再写音乐，版本与授权一起交"
summary_en: "Mark the hit points before writing, and ship versions with the licence."
level: "standard"
tags: ["游戏预告片", "落点", "版本", "授权"]
tags_en: ["game trailer", "hit points", "versions", "licensing"]
alias: ["游戏预告片", "预告片配乐", "game trailer", "trailer cut"]
order: 263
tool_kind: "guide"
tool_vendor: "—"
tool_form: "案例"
tool_platforms: ["通用"]
tool_price: "不适用"
tool_jobs: ["预告片配乐", "版本裁切", "授权确认"]
tool_verified: "2026-10-31"
links: ["[[glossary:cue]]", "[[glossary:sync-license]]", "[[glossary:true-peak]]"]
instances: []
sources: ["https://helpx.adobe.com/premiere/desktop/add-audio-effects/apply-audio-effects/remix-in-premiere.html", "https://tech.ebu.ch/docs/r/r128s1.pdf"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "游戏预告片需要把音乐切点与实际镜头和多长度版本逐一对齐，再按发布规范验收；脱离画面播放音乐不能证明剪辑命中或广告版响度合格。"
---

::: zh
## 一支片子的交付清单

九十秒主版，加六十、三十、十五秒裁切，竖版一条。每条配 48 kHz、24 bit 的混音与分轨，hit point 表写清时间码，另交一版不带 logo 音效的干净版。平台投放通常按 -14 LUFS 做，真峰值 -1 dBTP；送展会或电视另做 -23 LUFS。授权要写明预告片、游戏本体、DLC、地区与投放期限，只写宣传片通常不够。

## 落点、铺底、收尾

第一步和剪辑师过一遍画面，把 logo、角色亮相、发售日三个点标成 hit point，同时标出必须静音的位置。第二步按三段生成素材：建立段只留一个动机与环境声，累积段加层不加旋律，爆发段让主题完整出现一次。第三步在 DAW 里对时间码，把 riser 的终点压到 hit 前一两帧，收尾留两秒混响，再按版本裁切。

## 在时间线上用的工具

素材用 Suno 或 Udio 生成，Udio 适合同一动机做强弱两版。对画面与混音在 Pro Tools、Logic Pro 或 Ableton Live 里做，Premiere 或 Resolve 只用来核对画面。iZotope RX 清掉生成素材自带的前奏与尾巴，Ozone 统一各版本响度。分轨按低、中、高与打击拆，方便平台做前贴或竖版重混。

## 版本表与验收线

| 版本 | 时长 | 必须保留 | 可以删掉 |
|---|---|---|---|
| 主版 | 90 秒 | 三个 hit 与主题完整出现 | 建立段的一半 |
| 中版 | 60 秒 | logo hit 与主题 | 第一次累积 |
| 短版 | 30 秒 | 爆发与收尾 | 建立段全部 |
| 竖版 | 15 秒 | logo hit | 其余全部 |

所有版本的 hit 与画面误差不超过一帧，速度与调性一致。静音处真的是静音，不是压低的音乐。爆发段的响度不比前段高过 6 dB，否则平台归一后 hit 反而变弱。

## 预告片最容易假的地方

整段都在响，logo 出现时已经没有余量。riser 每次都是四小节上行，第二遍就能预测。生成素材尾巴拖进下一个镜头，剪辑点露馅。四个版本各自生成，速度差半拍，平台换版时听得出来。授权写的是预告片使用，游戏发售与后续 DLC 又要重新谈。
:::

::: en
## What ships with the cut

A ninety-second master, cuts at sixty, thirty and fifteen seconds, and one vertical version. Each comes with a 48 kHz, 24-bit mix and stems, a hit point sheet with timecodes, and a clean version without the logo sound. Online placement is usually mastered to -14 LUFS with true peak at -1 dBTP; a festival or broadcast copy goes to -23 LUFS. The licence must name the trailer, the game, DLC, territory and term. "Promo use" on its own rarely covers a launch.

## Hits, bed, tail

Sit with the editor and mark the logo, the character reveal and the release date as hit points, plus every place that must go silent. Generate in three blocks: the setup keeps one motif and some ambience, the build adds layers rather than melody, the release states the theme in full once. Align to timecode in the DAW, end the riser one or two frames before the hit, leave two seconds of reverb on the tail, then cut the versions.

## Tools on the timeline

Make material in Suno or Udio; Udio is useful for loud and quiet takes on one motif. Place and mix in Pro Tools, Logic Pro or Ableton Live, and use Premiere or Resolve only to check picture. iZotope RX removes the intro and tail that generation leaves attached, Ozone matches loudness across versions. Split stems into low, mid, high and percussion so a platform can re-cut for pre-roll or vertical.

## Four checks

| Version | Length | Must keep | Can lose |
|---|---|---|---|
| Master | 90 s | Three hits and the full theme | Half the setup |
| Medium | 60 s | Logo hit and theme | First build |
| Short | 30 s | Release and tail | All of the setup |
| Vertical | 15 s | Logo hit | Everything else |

Every hit lands within one frame of picture, at the same tempo and key across versions. Silence is real silence, not ducked music. The release sits no more than 6 dB above the section before it; push harder and platform normalisation makes the hit weaker.

## Where trailers start to lie

The whole cut is loud, so the logo arrives with nothing left. The riser climbs four bars every time and is predictable on a second viewing. Generated tails drag into the next shot and expose the edit. Each version is generated separately and drifts half a beat, which shows when a platform swaps them. The licence says trailer only, and the launch and DLC need a new negotiation.
:::

