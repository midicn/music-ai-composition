---
id: "documentation-of-process"
site: "ai"
cat: "H"
title: "过程记录"
title_en: "Documenting the Process"
summary: "把工具、版本、提示词、种子和改动写下来，结果才站得住"
summary_en: "Log tool, version, prompt, seed and edits so the result can be defended."
level: "standard"
tags: ["记录", "提示词", "种子", "流程"]
tags_en: ["documentation", "prompts", "seeds", "process"]
alias: ["过程记录", "制作日志", "process log"]
order: 8
links: ["[[glossary:diffusion]]", "[[glossary:midi-protocol]]", "[[glossary:daw]]"]
instances: []
sources: ["https://replicate.com/docs/topics/predictions/lifecycle", "https://huggingface.co/docs/diffusers/en/using-diffusers/reusing_seeds"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论任务、模型设置与修改记录，需要核对真实服务任务及随机状态的记录方式；重复播放固定MIDI不能说明模型参数已完整记录或推理可重现。"
---

::: zh
## 问题

六周后客户问这条曲子怎么做的，或者权利方问有没有用某个模型，聊天记录已经没了，工具更新了，记忆也不可靠。没有记录，结果就无法辩护，也无法复现。过程记录不是给审计看的，它是给未来的自己和接手的人看的。

## 记什么

一条生成记一行，日期、操作人、工具与精确版本、模型、提示词原文、负面提示、种子、时长、速度、调性、参考音频及其授权、生成参数、候选数量、选中理由。后期也要记，替换了哪个音、谁改的、为什么。用到的采样、循环、人声，记来源与授权。最后记输出文件的校验值和存放位置。失败的尝试同样要记，它解释了为什么没走那条路，也防止下一个人重做。

## 怎么记

放在项目文件夹里，纯文本或 CSV，一行一条，生成完立刻写，不要凭记忆补。设置界面可以截图，但文字才能搜索。提示词存成与渲染同名的 txt，不要只留在网页里。团队项目加两列，谁改的、什么时候。记录不必好看，能查就行，字段固定比格式漂亮重要。判断标准很简单，另一个人拿到这份记录，能不能按步骤做出一个可辩护的结果，哪怕不是一模一样。
:::

::: en
## The problem

Six weeks later a client asks how the track was made, or a rights holder asks whether a certain model was used. The chat log is gone, the tool has updated and memory is unreliable. Without a record the result cannot be defended or reproduced. Documentation is not for auditors; it is for your future self and whoever takes over.

## What to log

One row per generation, date, operator, tool and exact version, model, prompt verbatim, negative prompt, seed, duration, tempo, key, reference audio and its licence, settings, number of candidates and why one was chosen. Log post work too, which note was replaced, by whom and why. Log samples, loops and voices with source and licence. Log the hash and location of each output. Log failures as well; they explain why a path was abandoned and stop the next person from repeating it.

## How to log

Keep it in the project folder as plain text or CSV, one row per generation, written immediately rather than from memory. Screenshots of settings are acceptable, but text is searchable. Save the prompt as a txt file named after the render, not only in a web page. For teams add two columns, who changed it and when. The record need not be pretty, only searchable; fixed fields matter more than formatting. The test is simple, can another person follow the record and produce a defensible result, even if not an identical one.
:::

