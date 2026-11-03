---
id: "gain-staging-ai"
site: "ai"
cat: "D"
title: "AI 分轨的增益结构"
title_en: "Gain Staging AI Stems"
summary: "区分峰值、试听增益和内部动态；保留分轨之间的参考电平关系。"
summary_en: "Separate peaks, listening gain and internal dynamics, preserving relative stem levels."
level: "standard"
tags: ["增益结构", "分轨", "峰值", "响度"]
tags_en: ["gain staging", "stems", "peaks", "loudness"]
alias: ["分轨增益", "电平结构", "gain staging AI stems"]
order: 140
links: ["[[glossary:gain-staging]]", "[[glossary:headroom]]", "[[glossary:stems]]"]
sources: ["https://www.ableton.com/en/manual/managing-files-and-sets/", "https://www.itu.int/rec/R-REC-BS.1770-5-202311-I/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
---

::: zh
## 先区分三件事

静态增益把整段一起升高或降低，不会单独改变该段内部各时刻的相对动态；压缩和限制则可能改变动态或瞬态。响度归一化通常通过播放或文件增益调整来对齐目标，不能直接称为“把动态压扁”。峰值、真峰值与响度也不是同一个指标。

## 按处理链检查

| 场景 | 合适的检查 |
|---|---|
| 候选A/B试听 | 匹配试听响度，保存原文件 |
| 原始分轨接回 | 保留相对增益，避免每轨独立归一化后再求和 |
| 插件处理 | 按该插件的输入、输出和过载表现检查 |
| 最终导出 | 按接收用途检查响度、峰值与真实听感 |

没有适用于所有工程的“-6dBFS就正确”或“必须留6–10dB”规则。为后续处理留余量是工作方法，具体电平应结合素材、插件与接收方要求；较低峰值也不自动意味着声音更干净。

## 一个可复核的小比较

用同一份有权使用的音频做副本，一份仅改变固定增益，另一份按明确参数压缩。在相近试听响度下比较瞬态和段落对比，并把处理参数与输出一起保存。普通MIDI短句没有这两个实际处理结果，不能被当作AI母带前后的证据。
:::

::: en
## Separate three ideas

Static gain raises or lowers a segment together, preserving its internal level differences. Compression and limiting can change dynamics or transients. Loudness normalization commonly applies playback or file gain and should not simply be described as flattening dynamics. Peaks, true peaks and loudness are also different measurements.

## Check the actual chain

| Situation | Check |
|---|---|
| Candidate comparison | Match listening loudness and retain originals |
| Stem import | Preserve relative gain; avoid normalizing every stem separately |
| Plug-in processing | Inspect the processor's input, output and overload behaviour |
| Delivery | Check agreed loudness and peaks alongside listening |

There is no universal correct minus-six-dBFS peak or mandatory six-to-ten-decibel margin for every project. Headroom depends on material, processing and delivery requirements. A lower peak does not automatically mean cleaner sound.

## Make a documented comparison

Use copies of the same authorized audio. Apply only fixed gain to one and explicitly recorded compression settings to another. Compare transients and section contrast at similar listening loudness, keeping settings and outputs. An ordinary MIDI phrase without those processing results cannot document a before-and-after AI mastering test.
:::
