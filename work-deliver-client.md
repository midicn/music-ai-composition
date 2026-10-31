---
id: work-deliver-client
site: ai
cat: K
title: 给客户交付
title_en: Delivering to a Client
summary: 交付是一份可核对的清单，不是一条 mp3
summary_en: Delivery is a checkable list of files, not a single mp3.
level: standard
tags: [交付, 分轨, 命名, 授权]
tags_en: [delivery, stems, naming, licensing]
alias: [给客户交付, 交付清单, delivery, 文件交付]
order: 12
tool_kind: guide
tool_vendor: —
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [交付, 文件管理, 母带检查]
tool_verified: 2026-10-30
links:
  - "[[glossary:stems]]"
  - "[[glossary:true-peak]]"
  - "[[glossary:lufs]]"
instances:
  - mutopia-000497 | 贝多芬第五，多组总线与大量分轨的交付样本（C1）
  - pdmx-000153 | 二十六分钟长文件，分段与体积在交付时最容易被忽略（C1）
  - groove-000001 | 105 BPM 放克鼓组，导出的分轨在任何工具里都能继续用（C1）
sources:
  - 分轨与母带的交付口径，参考制作与发行惯例。
  - 文件命名与元数据的做法；交付实践是主要依据。
updated: 2026-10-30
---

::: zh
## 需求长什么样

一首曲子做完，客户要的是一整套文件，不是一条 mp3。清单通常包括母版、伴奏、清唱、分轨、不同时长与不同响度的版本。每个文件要有命名规则、采样率与位深。合同里写了修改轮次与交付日期。清单越具体，后面的争议越少。交付后还要留档，方便半年后回来要同一版。

## 工具组合

导出在 Ableton Live、Logic Pro 或 Pro Tools 里做，母带用 Ozone，并检查真峰值。分轨要从工程内部按总线导出，而不是用 Demucs 再分一次。iZotope RX 做最后的噪声检查。响度报告用测量工具生成。文件清单与授权说明写进一份 readme。

## 步骤

先把合同里的交付物抄成清单，逐项确认。导出母版与各分轨，统一采样率与位深。核对分轨相加是否等于母版。检查响度、真峰值与单声道。补上伴奏、清唱与短版。填元数据与 credit。写 readme，包含授权、修改轮次与联系信息。打包上传并记录校验值。

## 验收标准

文件数量与命名与清单完全一致。采样率 48 kHz、位深 24 bit，或按合同约定。分轨相加与母版差不超过 0.1 dB。响度与真峰值符合目标，单声道不塌。元数据与 credit 完整。授权文件与 readme 同包。压缩包解压后目录结构清楚。校验值可复核。交付日期不晚于合同。

## 常见返工原因

分轨少了和声层，客户混不出来。分轨相加与母版不一致。命名混乱，客户分不清版本。响度按流媒体做，客户拿去广播。授权文件没附，法务卡住。修改轮次没写清，第七轮还在改。交付后没有留档，客户回头要旧版时找不到。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"各版本从同一工程导出","label_en":"Every version from one session","hint":"听两份文件是不是同一场演奏，不要靠文件名判断","hint_en":"Hear whether two files are the same performance; do not trust the file name"}
```
:::

::: en
## What the brief looks like

When a track is finished, the client wants a set of files, not an mp3. The list usually includes the master, a backing, an a cappella, stems, and versions in different lengths and loudness targets. Every file needs a naming rule, a sample rate and a bit depth. The contract sets revision rounds and a delivery date. The more specific the list, the fewer disputes later. Archive the package too, because a request for the same version will come back months later.

## Tool combination

Export from Ableton Live, Logic Pro or Pro Tools, master with Ozone and check true peak. Stems come from buses inside the session, not from running Demucs a second time. iZotope RX does a last noise check. A meter produces the loudness report. File list and licence notes live in a readme.

## Steps

Copy the contracted deliverables into a checklist and confirm each line. Export the master and stems at one sample rate and bit depth. Check that stems sum to the master. Measure loudness, true peak and mono compatibility. Add backing, a cappella and shorter cuts. Fill metadata and credits. Write the readme with licence, revision rounds and contact details. Package, upload and record a checksum.

## Acceptance criteria

File count and naming match the list exactly. Sample rate is 48 kHz and bit depth 24 bit, or as contracted. Stems sum to the master within 0.1 dB. Loudness and true peak meet the target and mono does not collapse. Metadata and credits are complete. Licence documents and readme sit in the same package, and the folder structure is clear once unzipped. Checksums can be verified. Delivery lands on or before the contracted date.

## Common rework causes

A harmony layer is missing and the client cannot mix. Stems do not sum to the master. Naming is chaotic and versions are indistinguishable. The loudness is set for streaming and the client takes it to broadcast. No licence document is attached and legal blocks release. Revision rounds are undefined and the seventh pass is still in progress. Nothing is archived, so an old version cannot be found when the client asks.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"Every version from one session","label_en":"Every version from one session","hint":"Hear whether two files are the same performance; do not trust the file name","hint_en":"Hear whether two files are the same performance; do not trust the file name"}
```
:::
