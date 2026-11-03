---
id: "model-google-musicfx"
site: "ai"
cat: "I"
title: "Google MusicFX / Lyria 系"
title_en: "Google MusicFX / Lyria"
summary: "按具体入口与 Lyria 版本核对人声、时长和导出。"
summary_en: "Distinguish early MusicFX from current Lyria versions when checking vocals, length and controls."
level: "standard"
tags: ["模型档案", "音乐生成", "Lyria", "版本选型"]
tags_en: ["model profile", "music generation", "Lyria", "version selection"]
alias: ["MusicFX", "Lyria", "Google 音乐生成"]
order: 6
model_vendor: "Google"
model_form: "网页或接口（依具体产品）"
model_input: ["文本（其他输入依入口核对）"]
model_output: ["音频"]
model_licence: "商用与再分发范围随产品与云服务条款变化，需逐项核对"
model_verified: "2026-11-03"
links: ["[[glossary:timbre]]", "[[instrument:violin]]", "[[period:contemporary]]"]
instances: []
sources: ["https://deepmind.google/models/lyria/", "https://deepmind.google/models/model-cards/lyria-3/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页介绍Google音乐生成研究与服务，应区分历史MusicFX和不同Lyria版本的能力；普通MIDI不是相关模型输出，不能证明当前人声、长度或控制功能。"
---

::: zh
## MusicFX 与 Lyria 分开看

早期 MusicFX 入口与现行 Lyria 模型不能共用一组规格。Google 当前官方页面介绍 Lyria 3.5，并列出人声、音乐表现与可变歌曲长度；Lyria 3 另有独立模型卡。这些说明属于相应版本，不能据此认定旧 MusicFX 界面已获得全部新功能。

查资料和记录测试时，写全产品入口、模型版本及日期。仅写“Google 音乐生成”不足以复现一次测试，也无法说明他人账号能否使用同一功能。

## 按任务核对能力

| 需要完成的任务 | 在实际入口检查 |
|---|---|
| 带人声的歌曲 | 是否支持歌词输入、目标语种及逐句修改；试听实际咬字与段落 |
| 器乐与画面铺底 | 可选长度、结尾与循环方式；是否能按当前画面调整 |
| 接回 DAW | 导出格式、实际起点、尾音、是否提供分轨或其他可编辑文件 |
| 自动化调用 | 对应模型的接口、账号与地区可用范围、配额和返回方式 |

不要把风格描述当成对速度、调性或和声的精确控制。若入口提供专门参数，记录实际值；若只接受文字，把要求写进需求单，再测量生成结果是否满足。

## 一次可比较的试用

为同一个虚拟项目写一份固定需求，保存多个候选的原文件与标识。比较结构、人声、画面节点和可修改范围，记录具体时间点。更换产品入口或模型版本时单独建一轮记录，避免把版本差异当成提示词效果。

在脱离生成页面的位置重新打开导出文件。若目标是交给剪辑师或混音师，先确认对方收到的文件能完成后续工作，再判断这个入口是否适合项目。商用、发布与再分发按所用产品条款核对，不从另一个 Google 产品推定。
:::

::: en
## Separate MusicFX from Lyria versions

Early MusicFX and current Lyria models should not share one undifferentiated specification. Google's current official page presents Lyria 3.5 with vocals, musicality and variable song lengths; Lyria 3 also has its own model card. These descriptions belong to the respective versions and do not establish that an older MusicFX interface has every newer feature.

Record the product entry, model version and date when reading documentation or testing. “Google music generation” alone cannot reproduce a test or establish which features another account can access.

## Check capabilities against the task

| Task | Check in the actual entry |
|---|---|
| Songs with vocals | Lyric input, target language and line editing; audition real diction and sections |
| Instrumental beds for picture | Duration choices, endings, looping and adjustment to the current edit |
| DAW handoff | Export format, actual start and tails, stems or other editable files if available |
| Automated calls | The relevant model endpoint, account and region availability, quotas and responses |

A style description is not precise tempo, key or harmony control. Record dedicated parameter values where available. When the entry only accepts text, put the requirement in the brief and measure whether the output meets it.

## Run a comparable trial

Write one fixed brief for a fictional project and retain original files and identifiers for several candidates. Compare structure, vocals, picture events and editing scope, noting specific time positions. Start a separate test round when changing the product entry or model version so version differences are not mistaken for prompt effects.

Reopen exports outside the generation page. If an editor or mixer will receive them, confirm that the delivered files support their next task before selecting the entry for the project. Check commercial use, publication and redistribution under the selected product terms rather than inferring them from another Google product.
:::
