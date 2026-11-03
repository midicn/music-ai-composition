---
id: "sound-design-with-ai"
site: "ai"
cat: "E"
title: "AI 声音设计"
title_en: "Sound Design with AI"
summary: "生成纹理容易，能用难，先过单声道和电平这两关"
summary_en: "Generating texture is easy; making it usable means passing the mono and level checks first."
level: "standard"
tags: ["声音设计", "纹理", "氛围", "电平"]
tags_en: ["sound design", "texture", "ambience", "levels"]
alias: ["音效生成", "氛围设计", "texture generation"]
order: 7
links: ["[[glossary:reverb]]", "[[glossary:phase-check]]", "[[glossary:monitoring]]"]
instances: []
sources: ["https://stability.ai/guides/stable-audio-3-prompt-guide", "https://elevenlabs.io/docs/eleven-api/guides/cookbooks/sound-effects"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "声音设计要核对声音来源、动作、时长和生成参数，再检查所需素材；普通旋律播放缺少纹理或音效的目标约束，不能证明工具满足设计要求。"
---

::: zh
## 常见卡点

生成一段纹理只要一句话，能用它的时间却很长。多数结果不可编辑、电平不可控、一按单声道就消失。声音设计需要的是能放进时间线的材料，不是一段好听的音频。区别在于你能否只改它的尾巴、只留它的低频，或者把它缩到两秒。判断标准很朴素，能不能在十秒内找到它的起点和终点。

## 背后的机制

生成模型输出的是成品波形，里面已经混了空间、失真和动态。你没法把它拆回低频、主体和高频，也没法单独改尾音。可用的素材至少要能分层，或者能同时导出干声与湿声两版。生成时的提示词只控制大致方向，具体频率分布要靠在 DAW 里补。另一个常被忽略的点是相位，宽 stereo 的纹理在单声道里常常塌掉一半，而游戏、手机和公共场所的播放大多是单声道。

## 怎么调整

先写功能，是转场、底噪、空间还是冲击。长度留两倍余量再剪，riser 的终点对齐剪辑点，不要对齐小节线。导出前做单声道检查，低频用一百赫兹左右的高通切掉，避免和音乐低频打架。峰值留六分贝给对白和人声。把成品和参考音效各放一轨，音量对齐再比。保存原始生成、提示词、模型版本和处理链，方便回头改。循环类素材要单独检查接缝，接缝处的电平跳变比噪声更明显。
:::

::: en
## Common snags

Generating a texture takes one sentence. Making it usable takes far longer. Most results cannot be edited, their level cannot be controlled, and they vanish in mono. Sound design needs material that drops into a timeline, not a pleasant audio file. The difference is whether you can change only its tail, keep only its low band, or shorten it to two seconds. A simple test is whether you can find its start and end within ten seconds.

## The mechanism

A generative model returns a finished waveform with space, distortion and dynamics already baked in. You cannot split it back into low, mid and high layers, and you cannot revise the tail alone. Usable material is either layered or available as both dry and wet versions. Phase is the other overlooked issue. A wide stereo texture often loses half of itself in mono, and games, phones and public playback are mostly mono.

## How to adjust

Define the function first: transition, room tone, space or impact. Generate twice the length you need and cut it down. Align the end of a riser to the edit point, not to the bar line. Run a mono check before export, high-pass the low end around 100 Hz so it does not fight the music, and leave six decibels of peak headroom for dialogue and vocals. Keep the raw generation, the prompt, the model version and the processing chain so the sound can be revised later. Check loops separately; a level jump at the seam is more audible than noise.
:::

