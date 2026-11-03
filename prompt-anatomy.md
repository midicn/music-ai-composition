---
id: "prompt-anatomy"
site: "ai"
cat: "B"
title: "提示词结构"
title_en: "The Anatomy of a Prompt"
summary: "把风格、配器与段落写成可检验的制作说明，再用实际输出检查是否满足。"
summary_en: "Describe testable musical requirements, then check the actual output."
level: "standard"
tags: ["提示词", "结构", "生成", "工作流"]
tags_en: ["prompt", "structure", "generation", "workflow"]
alias: ["提示词", "prompt", "提示结构"]
order: 1
links: ["[[glossary:tempo]]", "[[glossary:timbre]]", "[[glossary:daw]]"]
sources: ["https://kb.stability.ai/knowledge-base/stable-audio-3-prompt-guide", "https://www.ableton.com/en/live-manual/12/audio-clips-tempo-and-warping/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
---

::: zh
## 先写关键要求

一条提示可以包括用途、风格、主要乐器、速度方向和段落变化，但并非每个任务都需要填满相同字段。先列必须满足的两三项，再补偏好。工具若另有时长、歌词或参考音频控件，应按其说明设置，而不是全部挤在文字里。

## 虚拟提示与验收

示例：“30秒器乐片头，木吉他与轻打击乐，约90 BPM，4秒后减少旋律活动以容纳口播，结尾完整收束。”这是教学需求，未代表任何一次模型生成。

| 请求 | 实际核验 |
|---|---|
| 约90 BPM | 导入时间线检查拍点与漂移 |
| 4秒后给口播留空间 | 叠入口播，听遮蔽与音乐密度 |
| 30秒并完整收束 | 检查真实时长和结尾，必要时编辑 |

## 修改一项，记录结果

保存完整提示、工具及版本和实际参数，再改变一个主要要求。若多次生成仍无法满足硬条件，检查工具能力或改用DAW编辑。写了速度并不能保证整段不漂移；写了某个和弦或禁止元素，也不能代替听音和结构检查。记录表见“候选试听记录表”，完整需求可先在首页整理。
:::

::: en
## Start with the important requirements

A prompt may describe use, style, instruments, tempo direction and section changes, but not every task needs the same fields. State the essential requirements before preferences. Use separate duration, lyric or audio controls when the product provides them.

## A fictional prompt and its checks

“Thirty-second instrumental intro, acoustic guitar and light percussion, around 90 BPM; reduce melodic activity after four seconds for narration; finish with a complete ending.” This is a teaching brief, not a model result.

| Request | Verify in the output |
|---|---|
| Around 90 BPM | Inspect beats and drift on a timeline |
| Narration space after four seconds | Audition with the narration |
| Thirty seconds and a complete ending | Measure duration and inspect the tail |

## Revise and record

Save the prompt, tool version and actual settings, then change one major requirement. If repeated candidates fail an essential constraint, check capability or use DAW editing. Naming a tempo does not guarantee stable timing; naming a chord or forbidden element does not replace listening and structural checks. Use the candidate log to connect each change to a result.
:::
