---
id: mono-check-ai
site: ai
cat: D
title: AI 混音的单声道兼容
title_en: Mono Compatibility for AI Mixes
summary: 生成的宽度多数靠相位差撑着，单声道求和就现原形
summary_en: Most generated width leans on phase difference, and the mono sum exposes it.
level: standard
tags: [单声道, 相位, 声场, 兼容]
tags_en: [mono, phase, stereo field, compatibility]
alias: [单声道检查, 相位兼容, mono check]
order: 141
links:
  - "[[glossary:phase-check]]"
  - "[[glossary:stereo-technique]]"
  - "[[glossary:comb-filtering]]"
instances:
  - groove-000005 | 87 BPM 嘻哈鼓组，底鼓与军鼓居中，求和后低频不能少一块（C1）
  - musicnet-000248 | 坎比尼第一木管五重奏，五件管乐挤在中频，单声道下最考验声部分离（C1）
  - mutopia-001412 | 萨蒂《裸体歌舞》第二首，织体稀疏，单声道下听混响尾巴是否还在（C1）
  - groove-000000 | 138 BPM 放克鼓组，踩镲与打击乐铺得很宽，适合检查高频抵消（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer’s Handbook 与 Bartlett, Practical Recording Techniques 中关于单声道求和与相位的章节。
  - 生成式立体声的宽度来源，依据公开工具文档与听辨实践。
updated: 2026-10-31
---

::: zh
## 单声道一按，宽的东西先消失

把总线切到单声道，生成的宽铺底立刻退到后面，人声还在，底鼓却薄了一半。这不是播放设备的问题，是左右声道求和时相位相反的部分互相抵消。生成的立体声越宽，这种抵消越明显。

## 塌陷从哪里来

宽度可以由电平差、时间差或相位差造成，只有前两种在单声道下基本保留，相位差会被求和吃掉。生成模型常用相位差做宽度，混响与延迟返回尤其如此；分离出来的分轨之间也没有相位保证。低频最敏感，因为波长长，几毫秒的延迟就能让低频互相抵消。梳状滤波在单声道下最容易被听成空洞或金属声。

## 检查清单

- 单声道监听整曲，记下变薄或消失的轨
- 底鼓与贝斯单独求和，低频应基本不变
- 左右声道分别听，找只出现在一侧的元素
- 把宽度插件与立体声混响的返回量减半再听
- 单声道下人声不能被伴奏盖住
- 看相关性表，长期为负的段落要处理
- 用手机外放再听一次，确认关键元素还在

## 修不回来的部分

低频转单声道、宽度收窄、延迟时间改短，能救回大部分问题。但如果生成素材本身在某段是反相的，怎么调都救不回来，换一版生成比在相位上硬掰更快。另一方面，单声道兼容不是唯一标准：有些氛围音乐靠宽声场成立，强行收窄会失去空间。判断顺序是先保关键元素，再保宽度，最后才谈空气感。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D4","F4","A4","D5","A4","F4","D4","A3"],"label":"一条会被求和检验的弦乐","label_en":"A string line the mono sum will test","hint":"先听这条线的清晰度，再想把左右各延迟几毫秒后哪些泛音会抵消","hint_en":"Hear how clear the line is, then imagine which overtones cancel once one side is delayed a few milliseconds"}
```
:::

::: en
## Switch to mono and the wide parts leave first

Sum the bus to mono and the generated wide pad drops back at once, the vocal survives, and the kick loses half its body. This is not a playback fault: where the two channels are out of phase, the sum cancels them. The wider the generated stereo image, the more obvious the cancellation.

## Where the collapse comes from

Width can come from level difference, time difference or phase difference; only the first two survive the mono sum, while phase difference is eaten by it. Generative models often buy width with phase, especially in reverb and delay returns, and separated stems carry no guarantee of phase relationship. Low frequencies suffer most because their wavelengths are long, so a few milliseconds of delay is enough to cancel them. Comb filtering is what the mono sum turns into a hollow or metallic colour.

## Checklist

- Listen to the whole track in mono and note which parts thin out or vanish
- Sum kick and bass alone; the low end should barely change
- Listen to left and right separately to find one-sided elements
- Halve the width plugin and the stereo reverb return, then listen again
- The vocal must not be covered by the backing in mono
- Read the correlation meter and treat sections that stay negative
- Check once more on a phone speaker to confirm the key elements remain

## What cannot be repaired

Mono-ing the low end, narrowing the width and shortening delays recover most problems. But if the generated material is genuinely out of phase in a section, no adjustment brings it back, and a fresh generation is faster than fighting the phase. Mono compatibility is also not the only standard: some ambient music exists because of a wide field, and forcing it narrow costs the space. Judge in this order: keep the key elements first, the width second, and the air last.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D4","F4","A4","D5","A4","F4","D4","A3"],"label":"A string line the mono sum will test","label_en":"A string line the mono sum will test","hint":"Hear how clear the line is, then imagine which overtones cancel once one side is delayed a few milliseconds","hint_en":"Hear how clear the line is, then imagine which overtones cancel once one side is delayed a few milliseconds"}
```
:::
