---
id: "evaluation-rubric"
site: "ai"
cat: "H"
title: "生成结果评估量表"
title_en: "An Evaluation Rubric"
summary: "四个维度分开打分，别让总分遮住一个一分"
summary_en: "Score four dimensions separately; a total hides the one that failed"
level: "standard"
tags: ["评估", "量表", "可改性", "权利"]
tags_en: ["evaluation", "rubric", "editability", "rights"]
alias: ["评估量表", "评分表", "generation rubric"]
order: 185
links: ["[[glossary:timbre]]", "[[glossary:stems]]", "[[glossary:music-copyright]]"]
instances: []
sources: ["https://www.itu.int/rec/R-REC-BS.1116-3-201502-I/en", "https://www.itu.int/rec/r-rec-bs.1534/en"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论分维度评价与主观听测，需要设定任务目标、对照样本和一致播放条件；普通MIDI回放不能替代真实候选的盲听记录或交付评分。"
---

::: zh
## 四个三分，为什么还是不能用

四个维度都打三分，总分十二，看起来整齐。可用性三分说明要修，可改性三分说明客户改不动，一致性三分说明下次复现不了，权利三分说明文件还缺。总分把四个问题平均掉了，任何一个维度的一分都该否决。

## 评分表

| 维度 | 1 分 | 3 分 | 5 分 | 看什么 |
|---|---|---|---|---|
| 可用性 | 结构散，无法直接用 | 能用，但要修剪 | 可直接进后期 | 段落、音准、伪影 |
| 可改性 | 只有立体声 | 有分轨，缺 MIDI 或干声 | 分轨、MIDI、干声齐全 | 分轨数量与起点 |
| 一致性 | 同提示差异很大 | 大致稳定，偶有漂移 | 同种子可复现 | 种子、版本、参数 |
| 权利 | 来源不清，文件缺失 | 基本齐全，仍有待确认项 | 来源与授权文件齐全 | 工具条款、样本、声音同意 |

## 打分不飘的做法

先盲听，两位评分人独立打，再对差异；每个分数写一句理由，指向具体位置，例如“第二段副歌低音与底鼓打架”；按用途加权，客户交付看可用性与可改性，素材库看一致性与权利；保留历史分数，改版后重打，不覆盖旧记录。分数不是给作品排座次，是让下一次修改有落点。

## 量表不适合判断的事

新鲜感、艺术家匹配、受众喜好、商业成败都不在四个维度里。权利分打的是文件与授权是否齐全，不是法律意见；有授权文件也可能有范围问题，需要另行清权。量表是筛子，把明显不能用的版本挡住，剩下的仍要人听、人判断。四个维度都过线，也只说明它可以进入下一轮，不说明它该被发布。
:::

::: en
## Four threes, and still unusable

Score all four dimensions at three and the total is twelve, which looks tidy. A three for usability means it needs work; a three for editability means the client cannot change it; a three for consistency means the next run will not reproduce it; a three for rights means documents are missing. The total averages four problems into one number, and a single one should veto the version.

## The scoring table

| Dimension | 1 | 3 | 5 | What to inspect |
|---|---|---|---|---|
| Usability | Form is loose, unusable as is | Usable after trimming | Ready for post | Sections, intonation, artefacts |
| Editability | Stereo only | Stems, but no MIDI or dry vocal | Stems, MIDI and dry vocal complete | Stem count and start points |
| Consistency | Same prompt, very different results | Broadly stable, occasional drift | Reproducible from the same seed | Seed, version, parameters |
| Rights | Source unclear, documents missing | Mostly complete, open questions remain | Sources and licence files complete | Tool terms, samples, voice consent |

## How to keep scores from drifting

Listen blind. Have two raters score independently, then discuss the gaps. Require one sentence of justification per score, tied to a position: "the bass and kick collide in the second chorus". Weight by use: client delivery leans on usability and editability, a library leans on consistency and rights. Keep past scores and re-score a revision without overwriting the earlier record. The numbers are not a ranking; they tell the next revision where to land.

## What the rubric should not judge

Novelty, artist fit, audience taste and commercial success are outside these four dimensions. The rights score measures whether files and permissions are complete, not a legal opinion; documents can exist and still leave a scope question that needs separate clearance. The rubric is a sieve that stops versions which clearly cannot be used. What passes still needs a person to listen and decide. Four passing scores mean it earns another round, not that it should be released.
:::

