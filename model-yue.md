---
id: "model-yue"
site: "ai"
cat: "I"
title: "YuE"
title_en: "YuE"
summary: "先区分 YuE-v1 与 YuE2，再核对部署、文件与权重许可。"
summary_en: "Separate YuE-v1 from YuE2 before checking deployment, files and weight licensing."
level: "standard"
tags: ["模型档案", "开源权重", "歌词生歌", "本地部署"]
tags_en: ["model profile", "open weights", "lyrics to song", "local deployment"]
alias: ["YuE", "乐", "歌词生歌"]
order: 200
model_vendor: "YuE 项目（M-A-P / 中国香港科技大学）"
model_form: "本地模型 / 项目在线入口"
model_input: ["歌词", "文本"]
model_output: ["音频"]
model_licence: "代码与模型权重分别授权；原始 YuE、YuE2 及公司商用按对应版本许可核对"
model_verified: "2026-11-03"
links: ["[[glossary:strophic-form]]", "[[glossary:timbre]]", "[[glossary:stems]]"]
instances: []
sources: ["https://github.com/multimodal-art-projection/YuE", "https://github.com/multimodal-art-projection/YuE/blob/main/MODEL_LICENSE"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页介绍YuE系列，需要区分原始YuE与YuE2代码、权重及许可版本；普通MIDI不是这些模型的生成结果，不能证明实际显存、运行速度、长曲质量或权重授权。"
---

::: zh
## 先选择版本

当前官方主分支介绍 YuE2，原始 YuE 的代码、文档与许可保存在 YuE-v1 分支。两代的输入流程、脚本和运行要求不能混用。阅读安装教程前，先记录仓库分支、提交或发布版本，以及所用模型文件。

本地部署与项目列出的在线入口也应分别测试。在线能运行，不代表同一配置能在自己的显卡上运行；某个社区量化方案能启动，也不代表它保留官方版本的全部行为。

## 做一次完整的小样测试

选择一段有权使用的歌词和明确的制作需求，先按所选版本文档完成短样。保留输入、实际参数和原始文件，记录显存占用、运行时间、失败日志及输出长度。硬件是否够用，应依据这组实测与版本要求判断，不能用一个固定显存数字概括整个系列。

| 检查对象 | 要记录的结果 |
|---|---|
| 人声与歌词 | 漏字、重复、音节位置和目标语种的发音；逐句标时间点 |
| 结构 | 段落是否完整，转接与收尾是否满足项目需求 |
| 音频与分轨 | 实际导出了什么；文件起点、尾音与可编辑范围 |
| 工程交接 | 离开推理环境能否打开文件，DAW 导入是否需要拉伸或补齐 |

如果某版本提供符号文件或分轨，按实际文件验收，不据另一版本的介绍推定。生成完成不代表已经达到混音或发行交付标准。

## 分清代码和模型许可

项目分别列出代码 LICENSE 与模型 MODEL_LICENSE。当前 YuE2 说明区分个人或内容创作者的变现、学术非商用及公司商用许可；原始 YuE 应回到对应分支检查。保存实际使用的许可文件、模型版本和素材来源，不只保存一个仓库首页链接。

选型时把部署成本、发音检查与可修改文件一起比较。若项目只需一次小样，可先评估在线入口；若需要本地批量流程，再以所选版本的资源和许可要求作决定。
:::

::: en
## Select a version first

The current official main branch documents YuE2, while original YuE code, documentation and licensing remain on the YuE-v1 branch. Do not mix generations of input workflows, scripts and runtime requirements. Record the branch, commit or release and model files before following an installation guide.

Test local deployment separately from online entries listed by the project. An online run does not establish that the same configuration fits your GPU, and a community quantization setup starting successfully does not establish full equivalence with the official version.

## Complete one small production test

Choose lyrics you have permission to use and a clear brief, then make a short sample using the selected version's instructions. Keep inputs, actual parameters and original files, recording VRAM use, runtime, failure logs and output length. Judge hardware suitability from these measurements and the version requirements rather than one memory figure for the entire family.

| Object | Record |
|---|---|
| Vocals and lyrics | Missing or repeated words, syllable placement and target-language pronunciation at specific times |
| Structure | Complete sections, transitions and ending against the brief |
| Audio and stems | Files actually exported, their start and tails, and editing scope |
| Handoff | Files reopening outside inference, and any stretching or alignment required in the DAW |

If a version provides symbolic files or stems, inspect the actual exports rather than inferring them from another version's description. A completed generation does not establish mix or release readiness.

## Separate code from model licensing

The project lists a code LICENSE separately from MODEL_LICENSE. Current YuE2 guidance distinguishes individual or content-creator monetization, academic noncommercial use and company commercial licensing. Check original YuE on its corresponding branch. Save the applicable licence files, model version and material sources rather than only a repository homepage link.

Compare deployment cost, pronunciation checks and editable files together. For a one-off demo, assess the online route first; for local batch work, decide from the chosen version's resource and licensing requirements.
:::
