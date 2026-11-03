---
id: "midi-post-editing"
site: "ai"
cat: "C"
title: "MIDI 后期编辑"
title_en: "MIDI Post-Editing"
summary: "音高对了还不够，力度、微时序与时值才决定它像不像演奏"
summary_en: "Correct pitches are only the start; velocity, microtiming and note length make it sound played."
level: "standard"
tags: ["MIDI", "力度", "微时序", "连断"]
tags_en: ["MIDI", "velocity", "microtiming", "articulation"]
alias: ["音符编辑", "MIDI 精修", "MIDI editing"]
order: 5
links: ["[[glossary:velocity]]", "[[glossary:rubato]]", "[[glossary:legato]]"]
instances: ["atepp-001283", "abcmisc-000554", "giantmidi-004005", "musicnet-000090"]
sources: ["MIDI 演奏信息的处理方法（音序器公开文档）。", "力度曲线与微时序的经验规则，参考制作惯例。"]
updated: "2026-11-03"
---

::: zh
## 门槛

生成的 MIDI 音高对了，听起来还是像打谱软件在放。问题通常在音符之外。所有音同一力度，起音全部贴在格子上，乐句没有呼吸，密集段落每个音都占满时值。直接换更好的音源能改善音色，改善不了这些。还有一类是音区问题，旋律被埋在伴奏中间，改力度也救不回来。

## 它怎么运转

演奏信息分三层，力度、时间、连接。三层互相影响，但改动有顺序。先修时值与连接，再修力度，最后动微时序，反过来做，前面调好的听感会被后一步推翻。音源对力度的响应曲线不同，同一组数值换一个音色库就变样，所以要在最终音源上定这套数值。

## 怎么调整

按声部处理，不要整轨刷同一条曲线。旋律先画一条跟音高走向有关的力度线，高音略强，长音做渐强。伴奏整体压低，和弦最高音略提，让和声有轮廓。密集段落用抽音处理，保留外声部与根音，内声部隔一个删一个，删完再听和声是否还成立。最后给旋律加五到十五毫秒的随机偏移，鼓不要动。每改完一个声部就静音其他声部复听，确认它单独也说得过去。

## 耳朵要抓的点

在外部 DAW 中打开一份可编辑的 MIDI，保留原件并另存副本，分别改变力度、音长或微时序，再比较结果。本页合成短句仅作固定音符与等力度回放参照，没有已经抽掉内声部或调整过力度的第二个版本。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4","E4","D4","C4","G3"],"label":"音色与短句练习","label_en":"Timbre and phrase exercise","hint":"浏览器合成示意；不是模型输出或处理前后对比。","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

::: en
## The threshold

The generated MIDI has the right pitches and still sounds like notation software playing back. The fault usually lies outside the notes. Every note has the same velocity, every onset sits on the grid, phrases have no breath, and dense passages fill every note to full length. A better sample library improves the tone and none of this. Another case is register, where the melody sits inside the accompaniment and no velocity change rescues it.

## How it runs

Performance information splits into three layers: velocity, timing and connection. They interact, but the order of work matters. Fix lengths and articulation first, then velocity, then microtiming; do it backwards and each earlier adjustment is undone by the next. Libraries map velocity to loudness and brightness differently, so the same numbers change with the instrument, and the values must be set on the final sound source.

## How to adjust

Work part by part rather than painting one curve across the whole track. For the melody, draw a velocity line related to pitch contour, a little stronger at the top, with swells on long notes. Bring the accompaniment down and lift the top note of each chord so the harmony has an outline. In dense writing, thin by removing inner voices every other note while keeping outer voices and roots, then check the harmony still stands. Finally offset melody notes by five to fifteen milliseconds at random, and leave the drums alone. Solo each part after editing it, to confirm it still makes sense on its own.

## What the ear catches

Open an editable MIDI file in a DAW, preserve the original and make a separate copy for changes to velocity, note length or microtiming. Compare those versions. The synthesized phrase here is a fixed-note, fixed-velocity reference; it does not supply a second version with inner parts removed or velocities edited.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","D4","E4","G4","E4","D4","C4","G3"],"label":"Timbre and phrase exercise","label_en":"Timbre and phrase exercise","hint":"A browser-synthesized exercise, not model output or a processing comparison.","hint_en":"A browser-synthesized exercise, not model output or a processing comparison."}
```
:::

