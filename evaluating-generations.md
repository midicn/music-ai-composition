---
id: "evaluating-generations"
site: "ai"
cat: "H"
title: "评估生成结果"
title_en: "Judging a Generation"
summary: "判断生成结果要有顺序，先听结构，最后才听混音"
summary_en: "Judge in order, form first and mix last, and ignore what post can fix."
level: "standard"
tags: ["评估", "听辨", "判断顺序", "质检"]
tags_en: ["evaluation", "listening", "judgement order", "QC"]
alias: ["评估生成", "结果判断", "judging output"]
order: 1
links: ["[[glossary:timbre]]", "[[glossary:mixdown]]", "[[glossary:mastering]]"]
instances: []
sources: ["https://www.itu.int/rec/R-REC-BS.1116-3-201502-I/en", "https://huggingface.co/facebook/musicgen-small"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论模型结果的质量与失败判断，需要在明确比较条件下审查真实生成文件和模型限制；曲库MIDI不是受评生成器输出，不能作为质量评分证据。"
---

::: zh
## 问题

生成结果最难判断的地方，是它在前十秒往往很像样。鼓够响、混响够宽、音色够新，于是人先被混音说服，再回头发现结构是散的。评估失败通常不是耳朵不行，而是顺序错了，先听最容易改的，最后才听最难改的。

## 判断顺序

按可修改成本从高到低听。第一遍只听形式，有没有开头、发展、回来，段落边界是否清楚，循环有没有变化。第二遍听和声，调性是否稳定，终止式落不落得住，低音是否只是跟着根音走。第三遍听演奏，时值、重音、连奏是否像一个人在做决定。第四遍听音色，乐器是否可信，有没有相位感、金属味、突然的采样切换。最后才听混音，平衡、宽度、响度。前四层在后期几乎改不动，混音层反而最容易补。

## 打分与忽略

每层打一到五分，写一句理由，任何一层低于三分就退回重做，不要用混音去救结构。可以忽略的东西也要列清楚，响度、单声道兼容、某一个错音、混响多少、立体声宽度，这些是后期问题，不该影响要不要这一版的决定。也不要因为提示词写对了就给分，提示词符合不等于音乐成立。把分数和理由发给合作者看，别人能否同意，比分数本身重要。听完三遍再下结论，第一遍的好感最不可靠。
:::

::: en
## The problem

A generation often sounds convincing for the first ten seconds. The drums are loud, the reverb is wide, the timbre is novel, so the mix persuades you before you notice the form is a pile of loops. Evaluation usually fails on order, not on ears, because the cheapest layer gets judged first and the most expensive layer last.

## The order

Listen from the most expensive layer to the cheapest. Pass one, form only: is there an opening, a development, a return; are section boundaries audible; does the loop change. Pass two, harmony: does the key hold, do cadences land, is the bass doing more than doubling roots. Pass three, performance: are timing, accent and articulation making decisions like a player. Pass four, timbre: are instruments plausible, is there phasing, metallic residue, an audible sample switch. Mix comes last, balance, width, loudness. The first four are nearly impossible to fix in post; the mix is the easiest to repair.

## Scoring and ignoring

Score each layer from one to five and write one sentence of justification. Any layer under three sends the version back; do not use the mix to rescue the form. The ignore list matters just as much: loudness, mono compatibility, one wrong note, reverb amount, stereo width. These are post problems and should not decide whether the version is kept. Prompt adherence is not a score either; a track can match the brief and still fail as music. Send the scores and reasons to a collaborator; whether they agree matters more than the numbers. Listen three times before deciding, since the first impression is the least reliable.
:::

