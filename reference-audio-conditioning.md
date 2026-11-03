---
id: "reference-audio-conditioning"
site: "ai"
cat: "B"
title: "参考音频条件"
title_en: "Reference Audio Conditioning"
summary: "先区分旋律条件、音频变换与风格参考，再核对输入范围和参数含义。"
summary_en: "Distinguish melody conditioning, audio transformation and style reference before choosing settings."
level: "standard"
tags: ["参考音频", "条件生成", "风格迁移", "控制"]
tags_en: ["reference audio", "conditioning", "style transfer", "control"]
alias: ["参考音频", "音频条件", "reference audio", "风格迁移"]
order: 7
links: ["[[glossary:timbre]]", "[[glossary:tempo]]", "[[glossary:stems]]"]
sources: ["https://kb.stability.ai/knowledge-base/tips-for-using-the-audio-to-audio-api", "https://kb.stability.ai/knowledge-base/stable-audio-3-prompt-guide"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
---

::: zh
## 参考音频不是一种统一功能

旋律条件可能主要提供音高或轮廓，audio-to-audio会以输入声音参与生成，风格参考则按产品自己的定义提供方向。这些接口不能仅凭“参考音频”四个字视为相同能力，也不能保证同时保留配器、旋律、节奏和混音。

## 输入前核对四项

| 项目 | 核对内容 |
|---|---|
| 功能 | 当前入口到底处理旋律、声音还是风格 |
| 文件 | 支持格式、长度和声道，按该版本文档填写 |
| 参数 | 强度的方向、范围与默认值，不跨产品照搬 |
| 使用范围 | 自己是否有权把这份录音用于该服务与任务 |

## 做一个可比较的小实验

以同一份有权使用的短素材和同一制作需求，保存默认设置的候选，再仅修改一个主要参数。用本地文件比较旋律、节拍、音色与结构分别保留了什么。素材时长按服务规定与任务需要确定；没有适用于所有模型的“三秒最好”规则。若工具没有声明相似度承诺，就把结果当作需要检查的候选。

将输入版本、完整参数与实际输出一同存档。普通MIDI回放不构成这个条件生成过程的证据。
:::

::: en
## Audio reference is not one universal feature

Melody conditioning may emphasize pitches or contour; audio-to-audio generation uses input sound in a different way; style reference follows the product's own definition. A shared label does not establish identical controls or guarantee preservation of instrumentation, melody, rhythm and mix together.

## Check before supplying a file

| Item | Verify |
|---|---|
| Feature | Melody, sound transformation or style reference |
| File | Supported format, length and channels |
| Parameter | Meaning, direction, range and default for this version |
| Permission | Whether this recording may be used for this service and task |

## Run a small comparison

Keep the same authorized input and brief. Save a candidate at the initial settings, then change one main control. Compare downloaded files for melody, timing, texture and form separately. Choose input duration from the service's limits and the task; there is no universal best three-second input. Treat an unspecified similarity claim as something to test, not a guarantee.

Archive input version, full settings and actual output together. Playback of an unrelated MIDI file cannot document this generation process.
:::
