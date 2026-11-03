---
id: "versioning-ai-projects"
site: "ai"
cat: "H"
title: "版本管理"
title_en: "Versioning AI Projects"
summary: "版本不只是一个文件，而是提示词、种子与后期的组合"
summary_en: "A version is a prompt, a seed and a set of edits, not just an audio file."
level: "standard"
tags: ["版本", "命名", "种子", "归档"]
tags_en: ["versioning", "naming", "seeds", "archive"]
alias: ["版本管理", "版本命名", "version control"]
order: 6
links: ["[[glossary:daw]]", "[[glossary:diffusion]]"]
instances: []
sources: ["https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository", "https://huggingface.co/docs/diffusers/en/using-diffusers/reusing_seeds"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "生成项目版本管理需要保存参数、模型版本、输出和提交记录，以便回退与比对；只播放一份成品无法重建生成过程或证明版本可复现。"
---

::: zh
## 问题

final、final2、final_final、final_真的最后一版，这些名字说明一件事，版本已经失控。AI 项目比普通工程更容易失控，因为一次生成只要几十秒，一天能出几十条，提示词留在聊天窗口里，种子没有记，模型还悄悄更新过。等到客户说上周那版更好，你已经回不去了。

## 版本命名

一个版本不只是音频文件，而是提示词、种子、模型与版本、参数、后期改动的组合。命名用日期加序号，加一个短标签和状态，例如 20261030_v003_chorus_approved，不要用 final。状态词只留四个，探索、候选、通过、交付。通过的版本复制到只读目录，算一个校验值，之后任何新生成都从它分叉。编号只增不减，不覆盖，不复用。每次改完在表里写一句为什么改，下一版才知道在改什么。

## 与渲染同存

每条渲染旁边放一个同名文本，写提示词原文、负面提示、种子、模型版本、时长、速度、调性。工具不给种子，就记录它给的一切，模型名、日期、参考音频的校验值，并注明无法精确回溯。用一个表把文件、提示词、种子、结论连起来，一行一条，写完再关机。聊天记录不算记录，它会被清掉，也无法搜索。
:::

::: en
## The problem

final, final2, final_final, final_really_last. The names alone show that version control has collapsed. AI projects collapse faster than ordinary sessions because a generation takes seconds, a day produces dozens, prompts live in a chat window, seeds go unrecorded and the model quietly updates. When the client says last week's version was better, there is no way back.

## Naming

A version is not just an audio file; it is prompt, seed, model and version, settings and post edits. Name with a date and sequence plus a short slug and a state, such as 20261030_v003_chorus_approved, never final. Keep four state words only, explore, candidate, approved, delivered. Copy approved versions into a read-only folder, hash them, and branch every new generation from that point. Numbers only increase; never overwrite or reuse. Write one line on why each change was made, so the next version knows what it is changing.

## Storing with the render

Put a text file of the same name beside every render, holding the prompt verbatim, negative prompt, seed, model version, duration, tempo and key. If the tool exposes no seed, record everything it does expose, model name, date, hash of the reference audio, and state that exact recall is impossible. Keep a table linking file, prompt, seed and conclusion, one row per generation, written before shutting down. Chat history is not a record; it gets cleared and cannot be searched.
:::

