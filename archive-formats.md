---
id: archive-formats
site: ai
cat: H
title: 归档格式
title_en: Archiving Formats
summary: 归档选格式看的是十年后还能不能打开
summary_en: Choose archive formats by whether they still open in ten years
level: standard
tags: [归档, 无损, 工程文件, 生成记录]
tags_en: [archiving, lossless, session files, generation logs]
alias: [归档格式, 长期保存, archive formats]
order: 180
links:
  - "[[glossary:bit-depth]]"
  - "[[glossary:sample-rate]]"
  - "[[glossary:master-rights]]"
instances:
  - pdmx-000153 | 二十六分钟托卡塔，长母带的分段与体积要一起归档（C1）
  - mutopia-000178 | 巴赫 d 小调托卡塔与赋格，多声部工程缺一层就无法重混（C1）
  - groove-000000 | 短循环也要存提示词与参数，否则无法再生成（C1）
  - mutopia-000497 | 贝多芬第五，大型工程要留冻结分轨与插件清单（C1）
sources:
  - Library of Congress, Sustainability of Digital Formats 与 IASA TC-04 关于长期保存格式的建议。
  - 母带与分轨交付的位深与采样率实务，参考行业公开资料。
  - 校验值与异地备份实践，来自公开档案标准。
updated: 2026-10-31
---

::: zh
## 归档不是备份

三年后要重混，工程能打开，插件却找不到；母带还在，生成记录没了。备份防的是硬盘坏，归档防的是格式、插件与上下文消失。两件事都做，才算留住。

## 四类文件，四种格式

| 类别 | 首选 | 可接受 | 不要单独存 | 附带 |
|---|---|---|---|---|
| 工程 | DAW 工程加冻结分轨 | 导出的轨道 | 只有工程文件 | 插件清单、版本、授权 |
| 分轨 | 24 位 WAV，工程采样率 | FLAC | MP3 当唯一副本 | 增益、起点、命名表 |
| 母带 | 24 位 WAV 加 DDP | FLAC | 流媒体转码版 | 响度、ISRC、校验值 |
| 生成记录 | 纯文本或 CSV | PDF 截图 | 只留网页历史 | 工具版本、提示词、条款快照 |

格式的选择标准不是“专业”，是十年后还有没有软件能打开。WAV 与 FLAC 的解码器到处都有，工程文件依赖 DAW 版本，插件更脆弱。所以工程包必须带冻结分轨，哪怕它让体积翻倍。

## 校验、拷贝与迁移

每个文件算 SHA-256，清单放在包的第一层；两份拷贝，不同介质，一份异地；每年抽读一次，确认还能打开，读取记录也留下，否则明年不知道上次查过什么。三到五年或系统、DAW、插件停止支持时做迁移，优先转到开放格式，原格式保留。不要把有损文件转成无损就叫保存，那只是变大。

## 无损也救不了的情况

插件厂商消失，冻结音频是唯一退路；云账号关闭，本地没有副本就全丢；权利证据缺失，音质再好也说不清能不能用；创建时元数据就写错，归档只会把错误一起保存。归档的目标不是文件齐全，是十年后还能回答这是什么、怎么做的、能不能用。
```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G4","D4","G3"],"label":"归档前听一遍格式痕迹","label_en":"Hear the format before archiving","hint":"转换是否留下痕迹，耳朵先知道","hint_en":"The ear notices conversion artefacts first"}
```

:::

::: en
## Archiving is not backup

Three years later the session opens but a plug-in is gone. The master survives but the generation log does not. Backup guards against a failed drive; archiving guards against the loss of formats, plug-ins and context. You need both.

## Four file types, four formats

| Category | Preferred | Acceptable | Never the only copy | Keep with it |
|---|---|---|---|---|
| Session | DAW project plus frozen stems | Exported tracks | The project file alone | Plug-in list, version, licences |
| Stems | 24-bit WAV at the session rate | FLAC | An MP3 as the only copy | Gain, start point, naming map |
| Master | 24-bit WAV plus DDP | FLAC | A streaming transcode | Loudness, ISRC, checksums |
| Generation log | Plain text or CSV | PDF screenshots | Browser history alone | Tool version, prompts, terms snapshot |

Choose a format by whether software will still open it in ten years, not by whether it sounds professional. WAV and FLAC decoders are everywhere; session files depend on a DAW version, and plug-ins are more fragile still. That is why a session package must include frozen stems, even when it doubles the size.

## Checksums, copies and migration

Hash every file with SHA-256 and put the manifest at the top level. Keep two copies on different media, one offsite, and read a sample once a year to confirm it still opens. Migrate every three to five years, or when the OS, DAW or a plug-in loses support, preferring open formats while keeping the originals. Converting a lossy file to a lossless format is not preservation; it only makes it bigger.

## When lossless is not enough

If the plug-in maker disappears, frozen audio is the only way back. If a cloud account closes and no local copy exists, everything is gone. If rights evidence is missing, perfect audio still cannot answer whether the work may be used. If metadata was wrong at creation, the archive preserves the error. The goal is not a complete folder; it is being able to answer what this is, how it was made and whether it can be used, ten years from now.
:::
