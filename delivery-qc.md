---
id: delivery-qc
site: ai
cat: H
title: 交付前检查
title_en: Delivery QC
summary: 交付前的错都能量出来，别靠再听一遍
summary_en: Delivery errors are measurable; another listen will not catch them
level: standard
tags: [交付, 质检, 真峰值, 响度]
tags_en: [delivery, QC, true peak, loudness]
alias: [交付检查, 交付质检, delivery QC]
order: 170
links:
  - "[[glossary:true-peak]]"
  - "[[glossary:lufs]]"
  - "[[glossary:stems]]"
instances:
  - pdmx-000153 | 二十六分钟的长文件，结尾淡出与分段在交付时最易漏（C1）
  - groove-000000 | 三十七秒鼓循环，循环点的咔哒一测就出（C1）
  - mutopia-000497 | 贝多芬第五的齐奏，密度会掩盖削波与真峰值超限（C1）
  - cyberhymnal-000000 | 管风琴赞美诗，持续低音在单声道检查里最见相位（C1）
sources:
  - ITU-R BS.1770 响度与真峰值测量方法，由国际电信联盟发布。
  - EBU R128 节目响度规范，由欧洲广播联盟发布。
  - 流媒体与母带交付规范，来自平台与行业组织公开文件。
updated: 2026-10-31
---

::: zh
## 返工往往不是因为音乐

交付前从头听一遍，注意力都在音乐上，漏掉的恰好是听不出来的东西：结尾多两秒静音，真峰值超零点几 dB，分轨相加不等于混音，文件名带空格。客户不会因为这些否掉作品，但会因此退回重交。

## 勾选表

- [ ] 头尾：开头无多余静音，结尾淡出完整，不截断尾音
- [ ] 峰值：真峰值低于目标上限，至少留 1 dB 余量
- [ ] 响度：整体与短时响度贴近平台目标，段落之间不忽大忽小
- [ ] 单声道：低频与主唱不塌，相位检查通过
- [ ] 剪切点：逐段扫，无咔哒、爆音、直流偏移
- [ ] 分轨：所有分轨相加能还原混音，增益补偿写在说明里
- [ ] 规格：采样率与位深跟工程一致，不把 44.1 kHz 升到 96 kHz 充高清
- [ ] 命名：项目_曲名_版本_分轨_速度_日期，ASCII，版本补零
- [ ] 元数据：曲名、作者、ISRC、版权行、工具与版本齐全
- [ ] 附件：交付清单、授权文件、联系人与日期

## 三个数必须用表测

真峰值、整体响度、短时响度范围。测量口径按 ITU-R BS.1770 与 EBU R128，目标值按平台或客户规范，不凭耳朵猜。真峰值留余量，是因为转码会改变采样间峰值；短时响度看的是段落之间有没有突然变响，不是单看一个总数。测完把数值写进交付说明，客户复核时不用再问。

## 清单管不到的地方

清单证明你查过，不证明作品好。编曲、音色、客户口味不在表里；权利文件是否齐全要另做一次清权；插件兼容要在对方机器上开一次。源文件本身有伪影，检查只能发现，不能修复。把清单和听辨分开做，先测后听，避免耳朵被音乐带走。
```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5"],"label":"交付前最后一遍","label_en":"The last pass before delivery","hint":"响度与峰值先过，再谈音色","hint_en":"Loudness and peaks before tone"}
```

:::

::: en
## Rework rarely starts with the music

On a final listen your attention sits on the music, so the things you miss are exactly the ones you cannot hear: two extra seconds of silence at the end, a true peak a fraction over, stems that do not sum to the mix, a filename with a space in it. None of these makes a client reject the track artistically, but each one sends it back.

## The checklist

- [ ] Head and tail: no stray silence at the start, the fade ends cleanly, no tail is cut off
- [ ] Peaks: true peak below the target ceiling, with at least 1 dB of margin
- [ ] Loudness: integrated and short-term values close to the platform target, no sudden jumps between sections
- [ ] Mono: low end and lead vocal hold up, phase check passes
- [ ] Edits: scan every cut for clicks, pops and DC offset
- [ ] Stems: all stems sum back to the mix, with gain offsets documented
- [ ] Specs: sample rate and bit depth match the session; never upsample 44.1 kHz to 96 kHz and call it high resolution
- [ ] Naming: project_title_version_stem_tempo_date, ASCII, zero-padded versions
- [ ] Metadata: title, author, ISRC, copyright line, tool and version
- [ ] Attachments: delivery note, licence files, contact and date

## Three numbers to measure

True peak, integrated loudness and the short-term range. Measure with ITU-R BS.1770 and EBU R128, and take the target from the platform or the client spec rather than from your ear. Peak margin matters because transcoding changes inter-sample peaks. Short-term loudness shows whether a section suddenly gets louder; a single integrated number hides that. Write the measured values into the delivery note so the client does not have to ask.

## What the checklist cannot cover

The checklist proves you looked, not that the work is good. Arrangement, timbre and taste are not on it. Rights completeness needs a separate clearance pass. Plug-in compatibility has to be tested on the recipient's machine. If the source already contains artefacts, inspection finds them but cannot repair them. Test first and listen second, or the music will carry your ear away.
:::
