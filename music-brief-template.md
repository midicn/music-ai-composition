---
id: "music-brief-template"
site: "ai"
cat: "B"
level: "standard"
order: 200
tags: ["制作流程", "工作表"]
tags_en: ["production", "worksheet"]
alias: ["项目需求单：先把交付写清楚", "A Project Brief: Define the Deliverable"]
title: "项目需求单：先把交付写清楚"
title_en: "A Project Brief: Define the Deliverable"
summary: "把用途、段落、输入素材与验收条件写成一份可复制的制作说明。"
summary_en: "Turn use, sections, inputs and acceptance criteria into a reusable production brief."
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
sources: ["https://kb.stability.ai/knowledge-base/stable-audio-3-prompt-guide", "https://help.suno.com/en/articles/6141505"]
---

::: zh
## 一张需求单解决什么

先分开硬条件与偏好。30秒、没有人声、可在对白下使用，是可以检查的要求；“温暖”“有电影感”只是方向，需要用可讨论的配器、密度和段落进一步说明。写进提示词不等于工具一定执行，严格时长和收尾可能仍需在制作软件中编辑。

## 可填写的字段

| 字段 | 写法 | 怎样验收 |
|---|---|---|
| 项目、用途与听众 | 片头、广告或游戏状态；使用渠道 | 与接收方确认范围 |
| 时长与段落 | 进入、主体、收尾；是否循环 | 对照时间线逐段播放 |
| 声音方向 | 主要乐器、节奏密度、速度方向 | 听实际文件，不只看提示 |
| 必须保留或避免 | 对白段减少旋律、不加入歌声 | 对照指定时间点检查 |
| 输入素材 | 文件名、来源、可用范围 | 上传前确认素材记录 |
| 交付 | 混音、分轨或MIDI；规格由接收方确认 | 逐个打开下载文件 |
| 修改与验收 | 谁确认、何时交付、允许几轮 | 留一份书面修改记录 |

## 虚拟案例：30秒读书播客片头

0–4秒建立主题，4–24秒降低旋律密度以容纳口播，24–30秒完整收尾。声音方向是木吉他和轻打击乐，约90 BPM；这里的数字是教学选择，并非平台标准。先交立体声混音，分轨仅在所选工具实际提供且项目需要时列入。把口播叠回时间线，检查文字是否清楚、收尾是否被截断。

[AI 分站首页的“制作项目需求单”](../#brief)可整理这些字段并导出文本。需求确认后，再写一条短提示用于试作；不要把完整合同、私人录音或无关文件直接塞进生成接口。

## 何时换路线

若必须逐音改旋律，而工具只能返回整首音频，应先安排转写、重新演奏或其他编辑方案。若接收方要求工程轨而服务只有分离分轨，应在生成前确认是否接受。无法满足的硬条件要改变制作路线，反复增加形容词不能替代缺失功能。
:::

::: en
## Separate requirements from preferences

Thirty seconds, no vocals and room for narration are testable requirements. “Warm” is a preference that needs discussion of instruments, density and form. A written prompt is a request, not proof of compliance; strict duration or an ending may still require editing in a DAW.

## Brief fields

| Field | Record | Acceptance check |
|---|---|---|
| Project and use | Audience, scene and distribution context | Confirm with the recipient |
| Duration and form | Entry, main section, ending and loop needs | Check the timeline |
| Sound direction | Instruments, density and intended tempo | Audition the actual file |
| Keep or avoid | Narration space, required motifs, no vocals | Inspect named time ranges |
| Inputs | File names, sources and permitted use | Review before uploading |
| Deliverables | Mix, available stems or MIDI; agreed formats | Open every exported file |
| Revisions | Approver, deadline and revision rounds | Keep a written change log |

## Fictional example: a podcast opening

For a thirty-second reading podcast intro, establish the theme during 0–4 seconds, reduce melodic activity during narration at 4–24 seconds, and leave a complete ending during 24–30 seconds. Acoustic guitar, light percussion and around 90 BPM are choices for this teaching example, not platform standards. Deliver a stereo mix first. Include stems only when the chosen service actually offers them and the project needs them. Place the narration over the result and check intelligibility and the ending.

Use the [AI home-page brief builder](../#brief) to export these fields as text. Then derive a short production prompt. Keep unrelated personal files and full contracts out of the generation request.

## Change the route when needed

If individual note editing is essential but the tool returns only mixed audio, plan transcription, replaying or another editing route. A separated stem is not necessarily an original project track. Resolve mismatches between the required deliverable and the service before generating more candidates.
:::
