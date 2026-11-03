---
id: "sample-generation"
site: "ai"
cat: "E"
title: "样本生成"
title_en: "Sample Generation"
summary: "生成 one-shot 和 loop 之后，长度、音高、尾巴和权利都要重新核对"
summary_en: "After generating one-shots and loops, recheck length, tuning, tail and rights."
level: "standard"
tags: ["采样", "循环", "one-shot", "权利"]
tags_en: ["sampling", "loops", "one-shots", "rights"]
alias: ["采样生成", "循环生成", "sample making"]
order: 8
links: ["[[glossary:sampler]]", "[[glossary:sample-clearance]]", "[[glossary:velocity]]"]
instances: []
sources: ["https://stability.ai/guides/stable-audio-3-prompt-guide", "https://support.image-line.com/action/knowledgebase?ans=717"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "样本生成需要核对模型输入、输出用途及采样素材再分发限制；播放任意采样既不能证明它由指定模型生成，也不能证明其许可范围。"
---

::: zh
## 为什么会用到

生成 one-shot 和 loop 现在很容易，难的是采进 sampler 之后。长度不对、根音不明、尾巴被切、循环点有咔哒声，还有权利没写清。生成一次三十秒，整理可能要三小时，问题都出在没有按采样而不是按音频的标准来做。采样不是把声音存下来，而是把它变成可以演奏的材料。

## 运行方式

one-shot 要的是单音、干净起音、可控的尾巴。它会被移调、拉伸、叠层，任何混响和延迟都会被重复放大。loop 要的是整数小节、明确速度和调性，首尾能无缝接上。一个样本的可用性，取决于它在不同音高和力度下还像不像原来的乐器。生成模型习惯给“完整的声音”，带空间、带氛围、带收尾，这恰好和采样的要求相反。采样的价值在于可重复使用，不在于一次好听。

## 具体做法

生成时关掉混响和延迟。one-shot 前面留五十毫秒静音，尾巴让它自然衰减，不要硬切。loop 做一、二或四小节，文件名写清速度和调性，命名用速度、调性、小节数三件事，不要用日期。采进 sampler 后先测根音，再试移调十二个半音，听有没有共振峰偏移。打击类要检查每一击的相位，同一条轨道不要放两个相位相反的底鼓。权利上确认生成服务的商用条款，保存生成日期、提示词和账号。不要把有版权的录音处理一下就说成自己生成的。
:::

::: en
## Why you reach for it

Generating one-shots and loops is easy. What comes after sampling them is not. The length is wrong, the root note is unclear, the tail is cut, the loop point clicks, and the rights are undocumented. Thirty seconds of generation can turn into three hours of housekeeping, because the material was judged as audio rather than as a sample.

## How it runs

A one-shot needs a single note, a clean attack and a tail you can control. It will be transposed, stretched and layered, so any reverb or delay gets multiplied. A loop needs whole bars, a stated tempo and key, and ends that join without a seam. Generative models tend to deliver a complete sound with space, atmosphere and an ending, which is the opposite of what a sampler wants. A sample earns its place by being reusable, not by sounding good once.

## In practice

Turn off reverb and delay when generating. Leave fifty milliseconds of silence before a one-shot and let the tail decay naturally instead of cutting it. Make loops one, two or four bars long, and put tempo and key in the filename. After sampling, find the root note, then transpose by twelve semitones and listen for formant drift. For percussion, check the phase of each hit and never stack two kicks that oppose each other. On rights, confirm the commercial terms of the generation service and keep the date, prompt and account. Never process a copyrighted recording and present the result as generated.
:::

