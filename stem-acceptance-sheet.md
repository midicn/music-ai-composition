---
id: "stem-acceptance-sheet"
site: "ai"
cat: "H"
level: "standard"
order: 204
tags: ["制作流程", "工作表"]
tags_en: ["production", "worksheet"]
alias: ["分轨验收表：先确认拿到的是什么", "Stem Acceptance Sheet"]
title: "分轨验收表：先确认拿到的是什么"
title_en: "Stem Acceptance Sheet"
summary: "核对分轨来源、共同起点、尾音、串音和可编辑范围，记录与原混音的差异。"
summary_en: "Check stem origin, alignment, tails, leakage and editability against a saved reference mix."
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
sources: ["https://docs.acestudio.ai/project/file-management/export-files", "https://help.ableton.com/hc/en-us/articles/22998838817820-Committing-Audio-in-Live"]
---

::: zh
## 先区分三种“分轨”

原工程导出的单轨、按乐器组汇总的stem，以及从混音分离得到的文件，能改动的程度不同。文件名写着“人声”并不能证明它是原始干声。索取或保存导出说明：由什么过程生成、是否带效果、是否包含母线处理。

| 检查 | 填写或操作 | 怎样判定 |
|---|---|---|
| 来源类型 | 原轨、编组导出或混音分离 | 与提供方说明核对 |
| 起点与长度 | 共同起点，开头静音与结尾范围 | 同时导入后播放 |
| 内容 | 每个文件实际含什么 | 独听再合听，标出串音 |
| 电平 | 保存原始增益关系 | 避免每轨单独归一化 |
| 伪影 | 金属音、抽吸、残留人声 | 标明时间点与影响 |
| 合成比较 | 与保存的原混音A/B | 记录差异，不预设能精确相消 |

## 虚拟案例：鼓轨里仍有歌声

将残留标为“00:10–00:14，人声可辨；单独做器乐版本时不接受”，而不是一概判定整个分轨不可用。如果只把鼓轨轻叠回原曲，影响可能不同；如果用途是公开器乐伴奏，标准又不同。验收须对应实际用途。

带非线性总线处理的原始轨道重新相加，也可能与处理后的混音不一致；混音分离更不等于找回原工程。把可编辑范围与已知缺陷写入交接说明。若关键声部缺失，优先重新导出或更换制作路线，而不是用音量放大来掩盖内容问题。
:::

::: en
## Identify the type of stem

Original project tracks, grouped exports and files separated from a finished mix offer different editing possibilities. A file named “vocal” is not automatically an original dry recording. Keep an export description: how it was produced, which effects remain and whether bus processing is included.

| Check | Record or action | Acceptance method |
|---|---|---|
| Origin | Original track, grouped export or separation | Confirm the process |
| Alignment | Common origin, leading silence and tails | Import together and play |
| Contents | Actual audible material per file | Solo, then combine; note leakage |
| Level | Original relative gains | Avoid normalizing each file separately |
| Artefacts | Metallic texture, pumping, residual vocals | Record time ranges and impact |
| Sum | Compare against the saved reference mix | Log differences without assuming an exact null |

## Fictional example: vocals in a drum stem

An actionable note is “intelligible vocal residue at 00:10–00:14; unsuitable for the requested instrumental version.” Its impact may differ when the drum stem is only layered quietly into the original mix. Acceptance follows the intended use.

Tracks feeding nonlinear mix-bus processing may not sum to the processed reference when exported separately. Separation also does not recover the original project. Document editable scope and known defects. If an essential part is missing, request another export or change the production route rather than simply increasing level.
:::
