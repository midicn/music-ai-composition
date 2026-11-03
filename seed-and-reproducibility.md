---
id: "seed-and-reproducibility"
site: "ai"
cat: "C"
title: "种子与可复现"
title_en: "Seeds and Reproducibility"
summary: "记下种子与全部参数，但别指望两次生成完全一样"
summary_en: "Log the seed and every parameter, but do not expect two runs to match exactly."
level: "standard"
tags: ["种子", "复现", "参数记录", "版本"]
tags_en: ["seed", "reproducibility", "parameter log", "versions"]
alias: ["可复现性", "随机种子", "reproducibility"]
order: 11
links: ["[[glossary:daw]]", "[[glossary:midi-protocol]]", "[[glossary:stems]]"]
instances: []
sources: ["https://huggingface.co/docs/diffusers/en/using-diffusers/reusing_seeds", "https://facebookresearch.github.io/audiocraft/api_docs/audiocraft/models/musicgen.html"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "种子与可复现性要连同模型版本、随机状态、设备及生成参数记录并重复运行；只播放一次结果无法证明相同输入能复现相同波形。"
---

::: zh
## 哪里不对

调出一个满意的结果，第二天想再要一版，参数照抄，结果却不一样。种子只是众多变量之一，把它当成唯一开关，复盘就会落空。更麻烦的是，有些服务根本不提供种子，只给一个重新生成的按钮。

## 机制上的解释

结果由模型版本、权重、采样设置、提示文本、参考音频与处理顺序共同决定。服务在后台更新后，旧种子指向的是新的分布。即使这些全部冻结，浮点运算在不同显卡上也可能给出微小差异，再经过多轮迭代放大成可听的不同。真正稳定的只有符号类输出，音符写下来就是写下来了。同一段提示放在不同长度的批次里，切分位置不同，结果也会不同。

## 怎么修

每次生成都记一份日志，写清日期、工具与版本、模型名、种子、步数、引导强度、时长、提示原文、参考文件与输出文件名。日志和被采纳的那一版音频放在一起，隔几个月还能对上。日志用纯文本写，和工程文件放在同一目录，交接时别人也能读懂。要长期复现，就把满意的结果导出成分轨或 MIDI，把生成物转成可编辑资产，别把可复现性押在服务上。重生成时一次只动一个变量，并保留对照版本，这样即使不能完全重复，也能说清是哪一步改变了结果。
:::

::: en
## What is off

You tune a result you like, ask for another version the next day with the same settings copied across, and get something else. The seed is only one variable among many, and treating it as the single switch makes any later review collapse. Worse, some services offer no seed at all, only a regenerate button.

## The mechanism explains it

A result is decided by model version, weights, sampling settings, prompt text, reference audio and processing order together. Once a service updates in the background, an old seed points into a new distribution. Even with all of that frozen, floating-point arithmetic on different cards can yield small differences that repeat after repeat turns audible. Only symbolic output stays stable, because a written note stays written. The same prompt placed in batches of different length is also cut at different points and returns different results.

## How to fix it

Keep a log for every run, recording the date, tool and version, model name, seed, steps, guidance strength, duration, the prompt as written, any reference file and the output filename. Store the log beside the take you accepted so the pair still matches months later, and keep it in plain text beside the project file so a collaborator can read it. For long-term reproduction, export the accepted result as stems or MIDI and turn the generation into an editable asset, rather than staking reproducibility on the service. When regenerating, move one variable at a time and keep a control version, so that even without an exact repeat you can say which step changed the outcome.
:::

