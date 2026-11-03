---
id: "hybrid-human-ai-performance"
site: "ai"
cat: "E"
title: "人机混合演奏"
title_en: "Hybrid Human and AI Performance"
summary: "真人加生成声部，先定谁定拍，再谈音色"
summary_en: "With a human performance plus generated parts, decide who owns the beat before discussing tone."
level: "standard"
tags: ["人机协作", "时间", "律动", "演奏"]
tags_en: ["human and AI", "timing", "groove", "performance"]
alias: ["混合演奏", "人机合奏", "hybrid performance"]
order: 9
links: ["[[glossary:rubato]]", "[[glossary:tempo]]", "[[glossary:dynamics]]"]
instances: []
sources: ["https://www.ableton.com/en/manual/audio-clips-tempo-and-warping/", "https://www.ableton.com/en/manual/editing-midi/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论真人演奏与生成声部的时间衔接，需要核对实际速度图、音符和演奏录音；普通曲库回放不是人机合奏，不能证明跟随演奏或同步成功。"
---

::: zh
## 哪里不对

真人演奏加生成声部，最容易散架的不是音色，是时间。真人会提前、会拖、会在乐句末尾呼吸，生成部分如果锁死 BPM，两条时间线就会互相拉扯。听众说不清哪里不对，只觉得“不在一起”。这种不一致在耳机里更明显，在小喇叭上反而被掩盖。

## 为什么会这样

合奏的时间基准有两种。一种是独奏者定拍，其他人跟随，速度随乐句伸缩；另一种是节奏声部定拍，独奏在上面自由。生成部分必须明确属于哪一种。让它同时跟拍又跟表情是做不到的，只能选一个，再用 tempo map 把另一部分补上。速度图记录的是每一拍的实际位置，比一个固定 BPM 更接近真人的时间。速度图不必精确到每一毫秒，但段与段之间的伸缩要留住。

## 怎么修

让真人先录一版不带节拍器的参考，从录音里提取 tempo map。生成声部按速度图走，不用固定 BPM。先对齐重音，再对齐音符起点，顺序反了会越调越乱。保留真人十到三十毫秒的提前与延后，不要量化到网格。生成部分音量低三到六分贝，加同样的房间声，放进同一个混响。生成声部不要抢独奏的换气口。检查乐句的呼吸是否同步，尤其段尾和转句。最后由演奏者听一遍，觉得“被拖着走”就重来，不要用压缩或延迟去掩盖。
:::

::: en
## What is off

When a human performance meets generated parts, the first thing to fall apart is rarely tone. It is time. Players push, drag and breathe at the end of phrases. If the generated part is locked to a fixed BPM, two timelines pull against each other. Listeners cannot name the fault; they just say it does not sit together.

## Why it happens

Ensemble timing follows one of two models. Either the soloist sets the pace and everyone follows, with tempo flexing by phrase, or the rhythm section holds the beat and the soloist floats above it. A generated part must belong clearly to one model. It cannot track the beat and the expression at the same time; choose one and supply the other through a tempo map. A tempo map records where each beat actually falls, which is closer to human time than a single BPM value.

## How to fix it

Record the human first without a click, then extract a tempo map from that take. Drive the generated part from the map, not from a fixed tempo. Keep the player's ten to thirty milliseconds of push and drag instead of quantising to the grid. Set the generated part three to six decibels lower, give it the same room sound, and place both in one reverb. Check that breaths line up, especially at the end of sections and at turns. Finally, have the player listen. If it feels like being dragged, start again rather than hiding it with compression or delay.
:::

