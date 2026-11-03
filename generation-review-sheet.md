---
id: "generation-review-sheet"
site: "ai"
cat: "H"
level: "standard"
order: 201
tags: ["制作流程", "工作表"]
tags_en: ["production", "worksheet"]
alias: ["候选试听记录表：从多版里选定一版", "A Listening Log for Generation Candidates"]
title: "候选试听记录表：从多版里选定一版"
title_en: "A Listening Log for Generation Candidates"
summary: "用文件标识、具体时间点和修改动作记录候选，减少只凭第一印象选曲。"
summary_en: "Log candidate files, timestamps and actionable revisions rather than selecting by first impression."
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
sources: ["https://huggingface.co/docs/diffusers/en/using-diffusers/reusing_seeds", "https://tech.ebu.ch/publications/r128"]
---

::: zh
## 先筛硬条件，再听偏好

先检查是否缺段、时长明显不符、出现不需要的人声或无法导出。对仍可使用的候选，在相近的主观试听响度下比较；较响的文件不应自动得高分。保留原文件，试听增益只用于比较，不要逐轨覆盖原始电平。

## 可复制记录表

| 候选 | 工具与版本、实际参数 | 发现的问题与时间段 | 决定与下一步 |
|---|---|---|---|
| A：本地文件路径 | 完整提示、生成日期；种子仅在支持时记录 | 例如00:12–00:15有口播遮蔽 | 保留结构，降低该段密度 |
| B：本地文件路径 | 同一需求的另一候选 | 例如结尾在00:28突然截断 | 尝试补尾或换候选 |
| C：本地文件路径 | 记录生成次数和实际费用 | 例如旋律好但无可用分轨 | 先核对能否满足交付 |

这三行是虚拟教学案例，不是对任何模型的测试成绩。评价可分为结构、演奏或歌唱、音频伪影、修改难度与交付条件。每个“不满意”都补一个时间点和一个动作；“不高级”无法直接成为返修任务。

## 复听与停止

先整段听一次，再循环问题片段；隔一段时间或请另一位听者复核。比较时只改变一个主要需求有利于记录，但一次成功仍可能来自随机差异，不能据此宣称某个提示词必然有效。达到硬条件且剩余问题可在预算内修复时，就进入编辑；核心结构失败而无法局部改动时，再换候选。候选轮数由项目预算和期限决定。
:::

::: en
## Screen requirements before preferences

First reject missing sections, incompatible duration, unwanted vocals or unusable exports. Compare the remaining files at similar perceived playback loudness. Louder should not automatically score better. Preserve the originals and use listening gain for comparison rather than overwriting source levels.

## Reusable candidate log

| Candidate | Tool, version and actual settings | Problem and time range | Decision and next action |
|---|---|---|---|
| A: local file | Prompt, date; seed only if supported | Narration is masked at 00:12–00:15 | Keep the structure, reduce density |
| B: local file | Another candidate for the same brief | Abrupt ending at 00:28 | Extend, edit the tail or replace |
| C: local file | Attempts and actual cost | Good melody, but missing required stems | Resolve the delivery constraint |

These are fictional teaching rows, not measurements of a model. Assess form, performance or vocals, audible artefacts, editability and deliverables separately. Pair each criticism with a timestamp and a feasible action. “Not professional enough” does not define an edit.

## Recheck and stop deliberately

Listen to the whole piece, then loop problem sections. Revisit after a break or involve another listener. Changing one main requirement helps record keeping, but a single successful candidate may still be random variation. Do not treat it as proof that a phrase always works. Proceed to editing when requirements are met and remaining repairs fit the budget. Regenerate when essential structure fails and local revision is unavailable. Set candidate limits from the project's budget and deadline.
:::
