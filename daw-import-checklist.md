---
id: "daw-import-checklist"
site: "ai"
cat: "C"
level: "standard"
order: 202
tags: ["制作流程", "工作表"]
tags_en: ["production", "worksheet"]
alias: ["DAW导入检查单：让素材回到工程", "DAW Import Checklist"]
title: "DAW导入检查单：让素材回到工程"
title_en: "DAW Import Checklist"
summary: "区分混音、分轨、MIDI与工程文件，检查时间起点、速度处理和尾音。"
summary_en: "Distinguish mixes, stems, MIDI and projects, then check timing, tempo treatment and tails."
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
sources: ["https://www.ableton.com/en/manual/managing-files-and-sets/", "https://www.ableton.com/en/live-manual/12/audio-clips-tempo-and-warping/"]
---

::: zh
## 文件类型决定能改什么

立体声混音可以剪接、调整增益或处理频谱，但不能直接当成完整的独立音符和乐器轨。分轨能提供较粗的层次控制；MIDI主要保存事件，需要音源重新发声；工程文件是否能打开，还取决于软件版本、插件和引用的素材。先记录实际得到的文件，再决定编辑方式。

## 导入前与导入后

| 项目 | 操作 | 失败时的处理 |
|---|---|---|
| 保留原件 | 原文件放只读的源素材目录，工作副本另存 | 重新下载或取回备份 |
| 起点 | 所有轨从约定位置导入，保留开头静音 | 查清是否被独立裁切 |
| 速度与拉伸 | 先听未处理版本，再决定是否启用自动拉伸 | 撤销不必要的Warp或拉伸 |
| 音高 | 对照参考音或乐谱，记录是否转调 | 分清工程转调和原文件音高 |
| 尾音 | 播放完整结尾，检查混响和延迟尾部 | 扩大导出范围或补尾 |
| 收集工程 | 将依赖的外部文件纳入项目 | 在另一位置重开检查缺失项 |

## 虚拟案例：片头比画面慢了半秒

先比对文件起点与画面标记，不要立刻把整段加速。若只是导入位置偏移，移动音频即可；若速度在中途漂移，设置少量有意义的节拍锚点，再听瞬态、音高和音色是否被处理破坏。若模型输出结构本就不合适，则回到候选筛选。把编辑后的混音与原件分别命名，保留回退路径。

完成后保存工程、收集依赖素材，并导出一个可脱离原生成平台播放的参考混音。关掉原平台窗口后重新打开本地项目，确认文件没有只指向临时下载地址。
:::

::: en
## Know what the file can preserve

A stereo mix supports cutting, gain changes and spectral processing, but it is not a complete set of independent notes and instruments. Stems provide broader layer control. MIDI contains events that need a sound generator. Project files also depend on software versions, plug-ins and referenced assets. Inventory what you received before choosing an editing method.

## Import checklist

| Check | Action | If it fails |
|---|---|---|
| Original | Keep source files and work on copies | Restore or download again |
| Start | Align tracks at the agreed origin, retaining leading silence | Check separate trimming |
| Tempo | Audition the untreated file before enabling time stretching | Undo unnecessary warping |
| Pitch | Compare with a reference or score | Separate project transposition from source pitch |
| Tail | Listen through the complete reverb and delay ending | Extend the export range |
| Dependencies | Collect external assets into the project | Reopen from another location |

## Fictional example: an intro arrives late

If an intro is half a second late against picture, compare file placement with the picture marker before speeding up the music. Move the clip if placement is the only issue. For drifting tempo, use a small number of meaningful timing anchors and listen for damage to transients, pitch and texture. If the form itself is unsuitable, return to candidate selection. Keep edited mixes separate from the original files.

Save the project, collect its dependencies and export a reference mix that plays without the generation service. Reopen the local project independently and check that assets do not rely on temporary download links.
:::
