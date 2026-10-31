---
id: work-game-loop
site: ai
cat: K
title: 游戏循环
title_en: A Game Loop
summary: 循环点、分层与状态切换，比音乐本身更容易出问题
summary_en: Loop points, layers and state changes break more often than the music itself.
level: standard
tags: [游戏, 循环, 分层, 中间件]
tags_en: [game, loops, layers, middleware]
alias: [游戏循环, 游戏配乐, game loop, 无缝循环]
order: 4
tool_kind: guide
tool_vendor: —
tool_form: 案例
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [游戏音频, 循环制作, 交互分层]
tool_verified: 2026-10-30
links:
  - "[[glossary:stems]]"
  - "[[glossary:tempo]]"
  - "[[glossary:reverb]]"
instances:
  - oga-000089 | 游戏用循环段落，长度与循环点必须写进验收标准（C1）
  - oga-000088 | 循环素材分层，听各层如何独立成立（C1）
  - groove-000037 | 八小节桑巴鼓循环，最小可复用单位，适合批量（C1）
sources:
  - 游戏音频的状态划分与循环做法，对照引擎文档与制作惯例整理。
  - 循环点与采样率的技术要求（中间件公开文档）。
updated: 2026-10-30
---

::: zh
## 需求长什么样

一段三十到九十秒的战斗或探索音乐要能无缝循环，还要分成几层供状态切换。策划会给 BPM、段落长度和进入时机。游戏在不同机器上跑，文件格式、采样率与循环点由引擎决定。素材会被程序重复调用几百次，任何接缝都会被玩家听出来。

## 工具组合

用 Suno 或 Udio 先生成整段素材，Udio 适合做同一素材的强弱两版。分层与剪辑在 Ableton Live、Logic Pro 或 REAPER 里做，Serum 与 Vital 补电子层。Demucs 可分参考曲的层，iZotope RX 修接缝噪声，Ozone 控响度。实现阶段用 Wwise 或 FMOD 管循环与状态切换。

## 步骤

先确认 BPM、循环长度与层数，文件名带上 BPM 与循环长度。逐层生成：底鼓与贝斯、和声垫、旋律、打击。每层裁到整小节，循环点落在零交叉。连续试听二十遍，修掉咔哒与多余尾音。导出各层与完整混音，标好 loop start 与 loop end。导入 Wwise 或 FMOD，做状态切换与淡入淡出。

## 验收标准

循环长度为整小节，BPM 与策划一致。连续二十遍无咔哒，接缝处没有可闻断层。各层相位对齐，单独播放也成立。层数控制在四层以内，程序好控。状态切换的淡入淡出为 0.5 到 2 秒。各状态响度差不超过 2 LU。格式与采样率符合引擎要求，导出统一 48 kHz、24 bit。授权覆盖游戏的全球发行与后续更新。

## 常见返工原因

尾音被硬切，循环点有咔哒。速度有漂移，十遍之后开始错拍。层与层没对齐，切换时鼓点跳一下。混响尾太长，接缝处越叠越厚。接缝处留了静音，循环听起来断一拍。采样率不匹配，导入后整体变调。授权只写宣传片，游戏本体不能用。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":124,"label":"一整小节，循环二十遍","label_en":"One bar, looped twenty times","hint":"听第二十遍的接缝，问题总在第三次之后出现","hint_en":"Listen to the seam on the twentieth pass; faults show up after the third"}
```
:::

::: en
## What the brief looks like

A thirty-to-ninety-second combat or exploration cue has to loop seamlessly and split into layers for state changes. The designer sets tempo, bar length and entry timing. The game runs on many machines, and the engine dictates file format, sample rate and loop points. The same asset is called hundreds of times, so any seam will be heard.

## Tool combination

Generate the body with Suno or Udio, and use Udio when a loud and a quiet version of one idea are needed. Layer and edit in Ableton Live, Logic Pro or REAPER, with Serum and Vital for electronic parts. Demucs can split a reference, iZotope RX cleans seam noise, Ozone controls loudness. Implementation runs through Wwise or FMOD for loops and state changes.

## Steps

Confirm tempo, loop length and layer count, and carry tempo and bar count in the file name. Generate layer by layer: kick and bass, pad, melody, percussion. Trim each to whole bars and place the loop point on a zero crossing. Listen through twenty times and remove clicks and stray tails. Export layers and a full mix with loop start and loop end marked. Import into Wwise or FMOD and build state transitions with fades.

## Acceptance criteria

The loop is a whole number of bars at the agreed tempo. Twenty consecutive passes produce no click and no audible break at the seam. Layers stay phase-aligned and each works alone; four layers is the practical ceiling before state control gets unwieldy. State changes fade over 0.5 to 2 seconds. Loudness differs by no more than 2 LU between states. Format and sample rate match engine requirements, exported at 48 kHz and 24 bit. The licence covers worldwide release and later updates.

## Common rework causes

A tail is hard-cut and the loop point clicks. Tempo drifts and the tenth pass is off the beat. Layers are not aligned and the drums jump on a switch. Reverb tails stack up at the seam. Export files carry silence before the downbeat and the loop stumbles. A sample-rate mismatch shifts pitch on import. The licence covers a trailer only and the game itself cannot use it.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":124,"label":"One bar, looped twenty times","label_en":"One bar, looped twenty times","hint":"Listen to the seam on the twentieth pass; faults show up after the third","hint_en":"Listen to the seam on the twentieth pass; faults show up after the third"}
```
:::
