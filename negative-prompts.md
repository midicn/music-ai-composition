---
id: "negative-prompts"
site: "ai"
cat: "B"
title: "反向提示"
title_en: "Negative Prompts"
summary: "说清不要什么，往往比反复强调要什么更有效。"
summary_en: "Saying what you do not want often works better than repeating what you do."
level: "standard"
tags: ["反向提示", "排除项", "生成", "控制"]
tags_en: ["negative prompt", "exclusions", "generation", "control"]
alias: ["反向提示", "排除项", "negative prompt"]
order: 5
links: ["[[glossary:timbre]]", "[[glossary:tempo]]", "[[glossary:daw]]"]
instances: ["groove-000000", "cyberhymnal-000003", "thesession-022200"]
sources: ["反向条件在生成模型中的实现，参考公开模型说明。", "排除项与正面描述的关系；创作实践惯例是主要依据。"]
updated: "2026-11-03"
---

::: zh
## 问题

有些生成器提供独立的排除项或 negative prompt，有些只提供普通文本描述。先确认当前模型是否支持负面条件；在普通提示里写“不带鼓”不等于调用独立的负面条件通道。效果应通过同一任务的对照生成来检查，不能保证加了排除项就一定生效。

## 怎么写

先把目标写成明确的正向描述，再列当前界面支持的排除项。一次改变一项，避免把音色、配器和空间要求同时混在一起。保留修改前后的提示与输出，检查排除鼓组时是否也损失了想保留的打击质感；不需要给所有模型规定固定的排除项数量。

## 做法

若没有专门排除功能，可以试写“独奏钢琴、无伴奏”等正向编制说明，并把不符合要求的候选剔除。不要不断加强同一句否定而忽略结果；必要时用剪辑、分离或重新演奏完成控制，但这些后续处理也须验证音质与许可。

## 听什么

保留相同正向描述、模型和其他参数，分别生成无排除项与有排除项的候选，记录目标元素是否减少、是否误伤其他声部。如果平台不能固定随机过程，应多取几次结果再判断。现有 MIDI 文件没有在生成器里应用反向提示，不能拿它证明排除电子鼓机或人声成功。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"单件乐器参照","label_en":"Single-instrument reference","hint":"这里只播放预设乐器，没有运行正向或反向提示。排除条件是否有效需要比较生成器的真实输出。","hint_en":"This plays a preset instrument without running positive or negative prompts. Evaluate exclusions using actual generator outputs."}
```
:::

::: en
## The problem

Some generators provide a separate exclusion or negative-prompt field; others accept ordinary descriptive text only. Confirm what the current model supports. Writing no drums in a normal prompt is not the same as using a dedicated negative-conditioning channel. Test controlled generations rather than assuming exclusions must work.

## How to write them

Start with a clear positive target, then use exclusions supported by the interface. Change one condition at a time rather than mixing timbre, instrumentation and space at once. Keep prompts and outputs before and after, checking whether removing drums also removes a wanted percussive texture. One fixed exclusion count does not suit every model.

## Practice

Without a dedicated exclusion feature, try a positive arrangement description such as solo piano, unaccompanied, and reject unsuitable candidates. Do not keep intensifying one negative phrase without examining the result. Editing, separation or a new performance may provide control, but those later steps also need quality and permission checks.

## What to listen for

Keep the positive description, model and other settings fixed, then generate candidates with and without exclusions. Record whether the target element decreases and whether other parts suffer. If randomness cannot be fixed, compare several samples. The existing MIDI files have not been generated with negative prompts and cannot demonstrate successful exclusion of drum machines or vocals.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"Single-instrument reference","label_en":"Single-instrument reference","hint":"This plays a preset instrument without running positive or negative prompts. Evaluate exclusions using actual generator outputs.","hint_en":"This plays a preset instrument without running positive or negative prompts. Evaluate exclusions using actual generator outputs."}
```
:::

