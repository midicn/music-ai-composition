---
id: "cue-sheet-template"
site: "ai"
cat: "F"
level: "standard"
order: 206
tags: ["制作流程", "工作表"]
tags_en: ["production", "worksheet"]
alias: ["配乐时间表：把画面事件写成音乐任务", "A Music Spotting Sheet"]
title: "配乐时间表：把画面事件写成音乐任务"
title_en: "A Music Spotting Sheet"
summary: "按时间码记录对白、转场与音乐进入退出，区分音乐需求表和版权cue sheet。"
summary_en: "Log dialogue, transitions and music entries; distinguish a production spotting sheet from a rights cue sheet."
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
sources: ["https://help.ableton.com/hc/en-us/articles/209773125-Using-Video", "https://help.ableton.com/hc/en-us/articles/360010120320-SMPTE-Timecode-FAQ"]
---

::: zh
## 先统一画面与时间基准

本页的表是制作时使用的配乐时间表，记录音乐何时进入、变化与退出；不是向版权组织申报作品的版权cue sheet。开始前固定画面版本、帧率和时间码起点。00:00:10:12是时、分、秒、帧写法，其中最后一项须结合帧率解释，不能当作百分之一秒。

| 时间段 | 画面或对白 | 音乐任务 | 检查与交付 |
|---|---|---|---|
| 00:00–00:04 | 标题出现 | 简短进入，建立主题 | 起点与画面标记一致 |
| 00:04–00:24 | 口播主体 | 减少旋律活动，保留推进 | 叠入口播检查清晰度 |
| 00:24–00:30 | 片尾标识 | 收束主题并保留尾音 | 结束点可编辑，无硬截断 |

这是30秒虚拟教学例子，表中为便于阅读使用分秒；正式项目按接收方的时间码约定填写。每个段落再附“必须同步”或“允许浮动”，避免把所有画面动作都机械写成强拍。

## 从表格到制作

把需求压缩成短提示或分段任务。生成后导入带有同一版画面的DAW，检查实际起止与变化，不以提示中的“30秒”作为输出已经合格的证据。工具不支持精确段落时，可先制作适合剪接的较长素材，再按时间表编辑；需要固定击点的复杂配乐则要预留人工编配或重录。

画面更新时另存版本，标出剪辑变化和受影响段落。交付说明中写清楚配的是哪一版画面。音乐文件与时间表一起保存，接收方才能判断是素材错误还是画面版本错位。
:::

::: en
## Agree picture and timing first

This production spotting sheet records music entries, changes and exits. It is not a copyright cue sheet submitted for rights reporting. Fix picture version, frame rate and timecode origin first. In 00:00:10:12, the last field represents frames, whose meaning depends on frame rate; it is not hundredths of a second.

| Range | Picture or dialogue | Music task | Check |
|---|---|---|---|
| 00:00–00:04 | Title | Establish a short theme | Align with picture marker |
| 00:04–00:24 | Narration | Reduce melodic activity, retain motion | Audition with narration |
| 00:24–00:30 | Closing identity | Resolve the theme and retain the tail | Editable ending, no abrupt cut |

This is a fictional thirty-second example using minutes and seconds for readability. Use the agreed timecode format in a production. Mark each event as a strict sync point or a flexible transition; not every picture action needs a musical accent.

## Turn the sheet into production tasks

Derive concise prompts or section requests, then import results beside the same picture version. Verify actual timing rather than assuming a “thirty seconds” prompt guarantees compliance. When precise sections are unavailable, a longer editable cue may provide useful material. Complex fixed hits may require manual arranging or replaying parts.

When picture changes, save another version and mark affected sections. State which picture version accompanies the delivery. Keep music and the spotting sheet together so the recipient can distinguish a timing error from a picture-version mismatch.
:::
