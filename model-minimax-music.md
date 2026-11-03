---
id: "model-minimax-music"
site: "ai"
cat: "I"
title: "MiniMax Music"
title_en: "MiniMax Music"
summary: "按账户权限选择服务或开放权重路线，核对版本与导出。"
summary_en: "Check access separately for existing API accounts, MiniMax Audio and open-weight Music 3."
level: "standard"
tags: ["模型档案", "中文歌曲", "API", "整曲生成"]
tags_en: ["model profile", "Chinese songs", "API", "full-song generation"]
alias: ["MiniMax Music", "MiniMax 音乐", "海螺音乐"]
order: 206
model_vendor: "MiniMax"
model_form: "服务 / 开放权重"
model_input: ["歌词", "文本（其他输入依入口核对）"]
model_output: ["音频"]
model_licence: "在线服务、代码和模型权重分别适用对应条款，使用前核对所选版本"
model_verified: "2026-11-03"
links: ["[[glossary:stems]]", "[[glossary:tempo]]", "[[instrument:polysynth]]"]
instances: []
sources: ["https://platform.minimax.io/docs/guides/models-intro", "https://www.minimax.io/blog/minimax-music-3-0-next-generation-open-weights-production-ready-versatile-music-model"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页介绍MiniMax音乐服务，需要核对模型版本、API账户开放范围与部署路线；普通MIDI不是服务输出，也不能证明当前接口可向新用户开放或实际生成规格。"
---

::: zh
## 先确认能用哪条路线

官方模型页注明：自 2026 年 8 月 20 日起，音乐和歌词的付费 API 不再向新用户开放；已有付费用户可继续使用，所列免费音乐 API 停用。新用户应先核对 MiniMax Audio 或开源 Music 3 路线，不能把 API 当作默认可用入口。

| 路线 | 开始前核对 |
|---|---|
| 存量付费 API | 当前账号是否仍有访问权限、端点和模型标识、计费与返回文件 |
| MiniMax Audio | 实际界面的生成与编辑功能、账号可用范围、导出和服务条款 |
| Music 3 开放权重 | 模型卡、代码与权重许可、部署说明和运行资源 |

三个入口不共用一张功能表。某个接口接受参考音频，不代表另一个入口也接受；网页能导出的文件，也不能直接推定为 API 返回内容。

## 用一个小项目验收

准备有权使用的歌词和一份项目需求单，写明用途、时长、段落及交付。先做短样，保存实际模型标识、歌词、描述和生成时间。逐句核对人声，标出段落进入、漏字和尾音的问题，再决定继续生成还是接回 DAW 修改。

拿到文件后检查格式、实际时长、采样率、尾音和可编辑范围。若交付要求包括分轨或 MIDI，必须确认当前入口确实支持并逐个打开检查，不能把立体声成品当成分轨工程。

## 接口与归档记录

已有 API 权限的团队应按当前端点文档实现请求、错误处理和保存，不预设所有版本都同步返回或允许相同并发。重试前确认任务状态与计费规则，避免重复创建任务。把原始返回文件、请求参数和修改后的交付文件分开保存。

在线服务条款与开放权重许可分别核对；账号能生成，不等于所有输入素材和输出用途都已获得许可。
:::

::: en
## Establish which route is available

The official models page states that from August 20, 2026, paid Music Generation and Lyrics Generation APIs are no longer offered to new users. Existing paying users can continue, while the listed free music APIs are discontinued. New users should check MiniMax Audio or the open-weight Music 3 route instead of assuming API access.

| Route | Check before starting |
|---|---|
| Existing paid API access | Account eligibility, current endpoint and model identifier, billing and returned files |
| MiniMax Audio | Actual generation and editing controls, account availability, exports and service terms |
| Music 3 open weights | Model card, code and weight licences, deployment instructions and resources |

Do not share one capability table across all three routes. An audio-reference input on one endpoint does not establish that another entry accepts it, and browser exports do not define API responses.

## Test one small project

Use lyrics you have permission to use and a project brief stating the purpose, duration, sections and deliverables. Generate a short sample first and save the actual model identifier, lyrics, description and date. Check the vocal line by line, noting section entries, missing words and tails before choosing between another generation and editing in a DAW.

Inspect the downloaded format, measured duration, sample rate, tails and editing scope. If delivery requires stems or MIDI, confirm that the selected entry supports them and open every file. A stereo mix is not a multitrack session.

## API and archive records

Teams with existing API access should implement requests, errors and saving from the current endpoint documentation. Do not assume every version is synchronous or has the same concurrency allowance. Check task state and billing before retrying to avoid duplicate jobs. Keep original responses, request parameters and edited delivery files separately.

Check online service terms separately from open-weight licences. Account access alone does not clear input material or every intended use of the output.
:::
