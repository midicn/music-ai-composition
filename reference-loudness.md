---
id: "reference-loudness"
site: "ai"
cat: "D"
title: "参考响度对齐"
title_en: "Matching Reference Loudness"
summary: "先把参考降到同一响度，再谈音色，否则比的是音量"
summary_en: "Bring the reference down to the same loudness first, or the ear is only comparing volume."
level: "standard"
tags: ["参考曲", "响度", "电平匹配", "比较"]
tags_en: ["reference", "loudness", "level matching", "comparison"]
alias: ["响度对齐", "参考对齐", "reference loudness"]
order: 142
links: ["[[glossary:reference-track]]", "[[glossary:lufs]]", "[[glossary:loudness-normalization]]"]
instances: ["atepp-001114", "groove-000000", "openscore-000270", "atepp-001283"]
sources: ["ITU-R BS.1770 与 EBU R128 关于整合响度、真峰值与平台归一化的定义。", "电平对齐后的参考比较方法，依据听感训练与混音实践。"]
updated: "2026-11-03"
---

::: zh
## 先把参考降下来

把参考曲和自己的版本直接 A/B，十次里有九次会选参考，因为它只是更响。响度差三 dB，耳朵就会觉得低频更足、人声更前、细节更多。比较音色之前，先把两者放到同一响度，这一步不做，后面的判断都不可靠。

## 对齐的是整合响度

用整曲的整合响度对齐，误差控制在 0.1 dB 以内。参考若是 -9 LUFS，先降到 -14 再比；自己的版本若在 -16，就升到 -14。短时响度用来比较段落，尤其是副歌有多满。真峰值单独看，别为了让响度对齐而顶破 -1 dBTP。对齐只改监听音量，不改文件，也不要在总线上加限制器去追参考。

## 对齐后的比较表

| 维度 | 对齐后听什么 | 不要据此判断 |
|---|---|---|
| 低频 | 100 Hz 以下谁更厚，是否发糊 | 更厚不等于更好 |
| 中频 | 人声与主奏的前后关系 | 编配不同，位置自然不同 |
| 高频 | 8 kHz 以上的空气感 | 亮不等于清晰 |
| 瞬态 | 鼓的字头与贝斯起音 | 响度对齐后仍差，才是真差距 |
| 宽度 | 单声道与立体声的差别 | 风格选择，不是对错 |
| 动态 | 主歌与副歌的落差 | 参考可能已经被压平 |

每次只比一个维度，每段听十秒，回到同一句。觉得参考更好时，写下具体是低频厚度、人声位置还是瞬态，再回混音改，而不是把总线推响。

## 对齐救不了什么

参考曲的编配、演奏、录音空间都与你的素材不同，对齐响度只能排除音量偏见，不能把不同编制变成同一把尺。参考被压得很平时，它的动态不能当目标；参考是现场录音时，它的空间感也不该被复制。还有一种常见错误是拿参考的母带去反推混音的电平，顺序反了，只会越做越紧。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","B4","G4","E4","C4"],"label":"音色与短句练习","label_en":"Timbre and phrase exercise","hint":"浏览器合成示意；不是模型输出或处理前后对比。","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

::: en
## Bring the reference down first

Play the reference against your own version and nine times out of ten the reference wins, because it is simply louder. Three dB of level is enough to make the low end seem fuller, the vocal closer and the detail richer. Match the two before comparing tone; skip that step and every later judgement is unreliable.

## Match integrated loudness

Match on integrated loudness over the whole track, within 0.1 dB. If the reference sits at -9 LUFS, bring it down to -14 before listening; if your version sits at -16, bring it up to -14. Use short-term loudness to compare sections, especially how full the chorus really is. Watch true peak separately and do not break -1 dBTP just to make the loudness match. The match changes monitoring level only: not the file, and not a limiter on the bus chasing the reference.

## A comparison table once levels agree

| Dimension | What to hear | What not to conclude |
|---|---|---|
| Low end | Which is fuller below 100 Hz, and whether it muddies | Fuller is not better |
| Midrange | How vocal and lead sit front to back | Different arrangements place them differently |
| High end | Air above 8 kHz | Bright is not clear |
| Transients | Drum attacks and bass onsets | A remaining gap after matching is real |
| Width | Difference between mono and stereo | A style choice, not a right answer |
| Dynamics | The drop between verse and chorus | The reference may already be squashed |

Compare one dimension at a time, ten seconds per excerpt, returning to the same phrase. When the reference still seems better, write down whether it is low-end weight, vocal position or transients, then go back to the mix rather than pushing the bus louder.

## What level matching cannot fix

The reference differs in arrangement, performance and recording space, so matching loudness only removes the volume bias; it cannot turn different forces into one ruler. A heavily compressed reference cannot set your dynamic target, and a live recording cannot dictate your sense of space. Another common error is reading the reference master backwards to set mix levels, which reverses the order of work and only makes the result tighter.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","B4","G4","E4","C4"],"label":"Timbre and phrase exercise","label_en":"Timbre and phrase exercise","hint":"A browser-synthesized exercise, not model output or a processing comparison.","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

