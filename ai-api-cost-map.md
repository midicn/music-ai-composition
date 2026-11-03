---
id: "ai-api-cost-map"
site: "ai"
cat: "A"
title: "调用成本与配额"
title_en: "API Cost and Quotas"
summary: "计费单位决定成本结构；先算一次任务真正跑几遍，再谈单价。"
summary_en: "Billing units shape the real cost. Estimate how many runs a task takes before comparing headline rates."
level: "standard"
tags: ["API", "成本", "计费", "配额"]
tags_en: ["API", "cost", "billing", "quotas"]
alias: ["调用成本", "计费口径", "API 配额"]
order: 123
links: ["[[glossary:licensing]]", "[[glossary:stems]]", "[[glossary:sync-license]]"]
instances: []
sources: ["https://replicate.com/docs/topics/billing", "https://replicate.com/docs/topics/predictions/rate-limits"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论请求计费、并发与额度，需要查服务账单口径和限流文档；曲目试听不能说明一次生成实际收费或可用配额。"
---

::: zh
## 单价便宜，返工很贵

一段三十秒的配乐，生成八次才有一条能用，成本就是标价的八倍，还要加上修分轨的时间。比较调用成本时，先看计费单位，再看一次任务实际要跑几遍。只比单价，得到的结论通常相反。

## 三种计费口径

| 计费口径 | 计费对象 | 成本随什么涨 | 适合 | 容易漏算 |
|---|---|---|---|---|
| 按秒 | 输入或输出的音频时长 | 时长、采样率、声道数 | 配乐、音效、长铺底 | 静音段与淡出尾巴也计费 |
| 按字符 | 提示、歌词、文本 | 字数、重试次数、上下文 | 歌词、描述、批量文案 | 系统提示与历史上下文 |
| 按任务 | 一次生成或一次编辑 | 候选数、分辨率、并发 | 整曲、分轨、母带 | 失败任务、排队与超时 |

有的服务混合计费：按月送额度，超出后按秒或按字符结算。额度月底清零，等于隐性涨价。按任务计费看似简单，候选数与重试规则仍会改变总量。

## 一次任务怎么估

成本 ≈ 单价 × 单次计费量 × 尝试次数 + 后处理工时 + 存储与传输。

举例：一段两分钟的器乐，按输出时长计费，平均生成六次留一条，其中两次因结构错误作废。计费量要按八次算，不是一次。若还要导出分轨再修，人工小时往往超过调用费。用计费单位做单位，不要用货币做单位，换供应商时公式仍然成立。

## 隐藏成本清单

- 失败、超时与取消的任务是否计费
- 候选之间的试听与筛选时间
- 分轨、MIDI、工程文件的导出是否另收费
- 存储、下载流量与长期归档
- 并发上限造成的排队与交付延期
- 汇率、税费与地区差价
- 条款变更后的重新测试

## 按量计费不划算的时候

短音效、批量循环、教学演示这类高频小任务，包月或本地部署通常更稳。反过来，一年只做几条长配乐，按量更省。别把“单价低”当成“总价低”；把配额、并发和返工一起算进去，才是可比的数字。预算表里还应留一列“重做”，否则一次失败的任务就会让整张表失真。
:::

::: en
## Cheap per call, costly per keeper

A thirty-second cue that needs eight generations before one is usable costs eight times the list rate, plus the time spent repairing stems. Compare billing units first, then count how many runs a task really takes. Comparing headline rates alone usually leads to the wrong choice.

## Three billing bases

| Basis | Charged on | What raises the bill | Good for | Easy to miss |
|---|---|---|---|---|
| Per second | Input or output duration | Length, sample rate, channels | Scores, effects, long beds | Silence and fade tails still count |
| Per character | Prompt, lyrics, text | Word count, retries, context | Lyrics, descriptions, bulk copy | System prompts and chat history |
| Per task | One generation or edit | Candidates, resolution, concurrency | Full songs, stems, mastering | Failed jobs, queuing, timeouts |

Some services blend the three: a monthly allowance, then per-second or per-character overage. Allowances that expire monthly are a quiet price increase. Per-task pricing looks simple until candidate count and retry policy multiply the total.

## Estimating one job

Cost ≈ unit rate × billable amount per run × number of attempts + repair hours + storage and transfer.

An example: a two-minute instrumental billed on output duration, six generations per keeper on average, two of them discarded for structural errors. Count eight runs, not one. If stems must be exported and cleaned, labour often exceeds the API charge. Keep the formula in billing units rather than currency so it survives a change of vendor.

## A checklist of hidden costs

- Whether failed, timed-out or cancelled jobs are billed
- Listening and selection time across candidates
- Extra charges for stems, MIDI or project-file export
- Storage, download traffic and long-term archiving
- Queueing caused by concurrency caps
- Exchange rates, tax and regional pricing
- Retesting after terms change

## When metered billing loses

High-frequency small jobs such as stingers, loop batches and teaching demos are usually steadier on a subscription or a local setup. A handful of long cues a year is cheaper metered. Low unit price is not low total price. Put quota, concurrency and rework into the same comparison, and keep a redo column in the budget, or the first failed job will distort the whole sheet.
:::

