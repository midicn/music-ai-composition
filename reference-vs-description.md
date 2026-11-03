---
id: "reference-vs-description"
site: "ai"
cat: "B"
title: "参考音频与文字的分工"
title_en: "Reference Audio vs Description"
summary: "把文字与参考音频分别映射到当前工具的实际输入，不预设万能控制。"
summary_en: "Map text and reference audio to the actual controls of the chosen tool."
level: "standard"
tags: ["参考音频", "提示词", "音色", "结构"]
tags_en: ["reference audio", "prompting", "timbre", "structure"]
alias: ["参考与描述", "音频条件", "reference vs text"]
order: 133
links: ["[[glossary:reference-track]]", "[[glossary:timbre]]", "[[glossary:texture]]"]
sources: ["https://kb.stability.ai/knowledge-base/tips-for-using-the-audio-to-audio-api", "https://docs.acestudio.ai/ai-vocal-synth/creating-ai-vocals/vocal-parameters", "https://docs.acestudio.ai/project/file-management/export-files"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
---

::: zh
## 先看工具提供了什么

文字、参考音频、旋律条件和局部选区是不同的输入路径。文字通常用于表达意图，但工具能否精确执行，需要检查；音频参考也不等于锁定全部节奏、音色与混音。不同入口对长度、格式与可编辑范围的规定可能不同。

## 选择输入的方法

| 当前需要 | 先核对 |
|---|---|
| 描述用途与声音方向 | 文本提示与可用参数 |
| 保留一段旋律或节奏线索 | 是否有对应的条件输入，以及保留范围 |
| 修改已生成的一小段 | 是否支持选区替换或需接回DAW |
| 使用特定录音作参考 | 输入许可、上传规则、文件限制 |

## 做对照而非猜机制

固定同一需求，分别记录仅文字与加入参考后的实际参数和文件。逐项听旋律、节拍、结构及音色，不把“更像”当成一个没有定义的总分。想去掉某个参考影响时，核对工具的参数或移除该输入；不能保证在文字里写一句否定就能消除条件音频的作用。

如结果仍不可控，把硬条件交给可编辑的制作步骤。保存输入与输出版本，结论限定在自己测试的工具、版本和任务上。
:::

::: en
## Inspect the available inputs

Text, reference audio, melody conditioning and region selection are different input paths. Text expresses intent but does not prove precise execution. An audio reference does not automatically lock rhythm, texture and mix together. Length, format and editable scope can vary by feature.

## Choose an input route

| Need | Verify first |
|---|---|
| State use and sound direction | Text prompting and supported parameters |
| Retain melody or rhythmic cues | Relevant conditioning and its scope |
| Revise a short existing section | Region editing or a DAW route |
| Supply a recording | Permission, upload rules and file limits |

## Compare instead of guessing the mechanism

Use the same brief and record actual settings and files for text-only and reference-assisted candidates. Assess melody, timing, form and texture separately rather than using an undefined similarity score. To remove a reference's influence, inspect controls or remove that input; a negative sentence is not guaranteed to cancel audio conditioning.

If control is insufficient, move strict requirements to an editable production stage. Preserve versions and limit conclusions to the tool, version and task actually tested.
:::
