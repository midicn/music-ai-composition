---
id: "arrangement-control"
site: "ai"
cat: "C"
title: "编曲控制"
title_en: "Controlling Arrangement"
summary: "密度靠分配音区与角色，不靠一层层往上加"
summary_en: "Density comes from assigning register and roles, not from stacking more layers on top."
level: "standard"
tags: ["编曲", "密度", "音区", "段落对比"]
tags_en: ["arrangement", "density", "register", "section contrast"]
alias: ["编曲控制", "配器密度", "arrangement control"]
order: 8
links: ["[[glossary:texture]]", "[[glossary:register]]", "[[glossary:voicing]]"]
instances: []
sources: ["https://www.orch-idea.org/intro/", "https://www.ableton.com/en/manual/editing-midi/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论音区、声部角色和可修改编配，需要对照配器方法与实际音符工程；普通MIDI不能证明生成器遵守编配指令或完成分层控制。"
---

::: zh
## 常见故障点

"再加一层弦乐""更丰满一点"，这类要求往往得到糊成一团的结果。模型把"多"理解成同时发声的数量，而不是角色分工。密度是编曲问题，不是音量问题。

## 原因在哪

听感上的厚薄由三件事决定。音区占用，低频、中频、高频各由谁负责；节奏角色，谁打底、谁推进、谁点缀；音色差异，相近音色叠在一起只会变响，不会变厚。音区重叠是另一种常见毛病，三件乐器挤在中音区，听上去很满，实际什么都听不清。段落对比来自这些变量的变化幅度。副歌比主歌多两件乐器，效果远不如让某一层在副歌前突然撤走。

## 怎么修

先把段落写成一张表，每段列出低频、和声层、旋律、点缀四行，各填一到两个乐器。写提示时给具体分工，比如低音只走根音、每小节一次，中音区用长音铺底，高频只在前八小节出现。要加厚时先换音区，再换音色，最后才加声部。每段只留一个主角，其余声部退到背景，这是最省力的对比。段落之间做减法比做加法有效，撤掉一层再放回来，同一层会显得更有分量。提示里也写明不要什么，比如不要铺满中频、不要连续八分音符的弦乐。生成后逐段数声部，超过四层就删。
:::

::: en
## Common failure points

Add another string layer, make it fuller. Requests like these tend to return mush. The model reads more as the number of simultaneous sounds rather than a division of roles. Density is an arranging problem, not a volume problem.

## Where the cause is

Thickness is decided by three things. Register occupancy, meaning who owns the low, middle and high range. Rhythmic role, meaning who anchors, who pushes and who decorates. Timbre difference, because similar sounds stacked together only get louder, never thicker. Register overlap is the usual culprit, three instruments crowded into the middle sounding full while communicating nothing. Section contrast comes from how far these variables move. A chorus with two extra instruments matters far less than one layer dropping out just before it.

## How to fix it

Write each section as a table with four rows, low end, harmonic layer, melody and decoration, and fill one or two instruments into each. Give the prompt explicit jobs, for instance the bass plays roots once per bar, the middle range sustains long notes, the top appears only in the first eight bars. To thicken, change register first, then timbre, and add a part last. Subtraction between sections works better than addition, since a layer removed and brought back carries more weight. Say what you do not want as well, no wall of midrange and no continuous eighth-note strings, and keep one lead per section with everything else behind it, which is the cheapest contrast available. After generation, count the parts section by section and delete anything beyond four.
:::

