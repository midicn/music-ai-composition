---
id: negative-prompts
site: ai
cat: B
title: 反向提示
title_en: Negative Prompts
summary: 说清不要什么，往往比反复强调要什么更有效。
summary_en: Saying what you do not want often works better than repeating what you do.
level: standard
tags: [反向提示, 排除项, 生成, 控制]
tags_en: [negative prompt, exclusions, generation, control]
alias: [反向提示, 排除项, negative prompt]
order: 5
links:
  - "[[glossary:timbre]]"
  - "[[glossary:tempo]]"
  - "[[glossary:daw]]"
instances:
  - groove-000000 | 138 BPM 放克鼓组，排除"电子鼓机"后音色更接近原声（C1）
  - cyberhymnal-000003 | 管风琴赞美诗，排除"人声"避免合唱混入（C1）
  - thesession-022200 | 传统曲调，排除"现代鼓组"保持原声编制（C1）
sources:
  - 反向条件在生成模型中的实现，参考公开模型说明。
  - 排除项与正面描述的关系；创作实践惯例是主要依据。
updated: 2026-10-30
---

::: zh
## 问题

模型喜欢补全：你说"弦乐"，它可能加上鼓；你说"安静"，它可能加一层铺底。反复强调"不要太吵"通常没用，因为否定词在语言模型里容易被忽略。反向提示把排除项单独列出，效果更直接。

## 怎么写

排除项要具体：写"不要电子鼓机"比写"不要太现代"有效。一次列三到五项，太多会互相冲突。常见排除项包括人声、鼓组、失真、混响过大、突然的转调。排除的是类别而不是个别音符，别写"不要那个高音"。

## 做法

先写正面描述，再补排除项。生成后听是否还有被排除的元素，有就加强那一条。排除项也可能误伤：排除"混响"会让声音发干，排除"低频"会让整体变薄。定期清理不再需要的排除项，避免提示越写越长。

## 听什么

在放克鼓组里听电子鼓机是否被排除干净，在赞美诗里听是否混入人声，在传统曲调里听现代鼓组是否消失。排除项做得好，正面描述才有空间。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"没有加料的原声","label_en":"Acoustic, nothing added","hint":"排除掉多余层之后，听原本的乐器是否更清楚","hint_en":"With extra layers excluded, hear whether the instrument stands clearer"}
```
:::

::: en
## The problem

Models like to complete: ask for strings and drums may appear, ask for quiet and a pad may creep in. Repeating "not too busy" rarely helps, because negation is easily lost in language models. Negative prompts list exclusions separately and work more directly.

## How to write them

Be concrete: "no electronic drum machine" beats "not too modern". List three to five items, since more start to conflict. Common exclusions include vocals, drum kit, distortion, heavy reverb and sudden modulations. Exclude categories rather than single notes; "not that high note" is not actionable.

## Practice

Write the positive description first, then add exclusions. After generation, listen for anything excluded that survived and strengthen that line. Exclusions can overshoot: removing reverb dries the sound out and removing low end thins it. Prune exclusions you no longer need so the prompt does not grow without limit.

## What to listen for

On the funk kit, whether the drum machine is truly gone; in the hymn, whether vocals have crept in; in the traditional tune, whether a modern kit has vanished. Good exclusions give the positive description room.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","E4","G4","C5","G4","E4","C4","G3"],"label":"Acoustic, nothing added","label_en":"Acoustic, nothing added","hint":"With extra layers excluded, hear whether the instrument stands clearer","hint_en":"With extra layers excluded, hear whether the instrument stands clearer"}
```
:::
