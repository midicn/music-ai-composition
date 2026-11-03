---
id: "prompt-templates"
site: "ai"
cat: "B"
title: "提示模板"
title_en: "Prompt Templates"
summary: "把反复验证有效的提示存成模板，换素材时只改变量。"
summary_en: "Save prompts that repeatedly work as templates and change only the variables per job."
level: "standard"
tags: ["模板", "提示", "复用", "效率"]
tags_en: ["template", "prompt", "reuse", "efficiency"]
alias: ["提示模板", "模板化", "prompt template"]
order: 10
links: ["[[glossary:tempo]]", "[[glossary:timbre]]", "[[glossary:daw]]"]
instances: []
sources: ["https://stability.ai/guides/stable-audio-3-prompt-guide", "https://facebookresearch.github.io/audiocraft/api_docs/audiocraft/models/musicgen.html"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "提示模板要列清固定描述与可变参数，并在所用模型上比较多个输出；任意一段音乐无法验证模板的控制范围或跨版本稳定性。"
---

::: zh
## 要解决的事

做过十个项目以后会发现，大部分提示是重复的：同样的结构描述、同样的排除项、同样的音色说明。每次重写既慢又容易漏。模板把稳定的部分固定下来，只让变量变化。

## 工作机制

一个好模板分三段：固定骨架（风格、编制、结构、质量要求）、变量槽（速度、调性、主题、情绪）、排除项。固定骨架保证输出稳定，变量槽保证每个项目不同。变量不宜太多，超过五个就难以追踪是哪一项在起作用。模板要带版本，改了要记下为什么改。

## 从哪开始

从成功的提示里提炼模板，而不是凭空设计。每个项目结束后回看，把有效句式补进模板。变量用方括号标出，替换时不要改动固定部分。为不同用途准备不同模板：歌曲、配乐、音效、人声。模板不是万能的，遇到新类型时先手写几次，再决定要不要模板化。
:::

::: en
## The problem to solve

After ten projects you notice most prompts repeat: the same structural description, the same exclusions, the same timbre notes. Rewriting each time is slow and error-prone. A template fixes what stays constant and leaves only variables to change.

## The working mechanism

A good template has three parts: a fixed skeleton (style, instrumentation, form, quality demands), variable slots (tempo, key, subject, mood) and exclusions. The skeleton keeps output steady while slots make each job different. Too many variables become untraceable, so keep them under five. Version the template and record why it changed.

## Where to start

Derive templates from prompts that already worked rather than designing them from scratch. After each project, review what succeeded and fold useful phrasing back in. Mark variables in brackets and never edit the fixed parts while substituting. Keep separate templates for songs, cues, effects and vocals. Templates are not universal, so write by hand a few times before templating a new type.
:::

