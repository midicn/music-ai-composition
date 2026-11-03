---
id: "environmental-cost"
site: "ai"
cat: "G"
title: "算力与环境"
title_en: "Compute and Environment"
summary: "生成有算力成本，规模一上来，账单与环境账都要算"
summary_en: "Generation costs compute, and at scale both the invoice and the environmental bill arrive"
level: "standard"
tags: ["算力", "能耗", "批量", "小模型"]
tags_en: ["compute", "energy", "batching", "small models"]
alias: ["算力成本", "能耗", "compute cost"]
order: 8
links: []
instances: []
sources: ["https://www.iea.org/reports/energy-and-ai", "https://docs.codecarbon.io/3.3/explanation/methodology/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论生成任务的资源与环境影响，需要依据能耗研究和实际任务测量记录；音乐时长或编制试听不能代替硬件功耗、运行时间和碳强度数据。"
---

::: zh
## 难点在哪

生成一首歌要耗电，训练一个模型更耗。厂商很少公布单次生成的能耗，公开数字又常把训练与推理混在一起。对使用者来说，能做的不是精确核算，而是减少浪费，并在对外的环保说法上保持诚实。

## 它怎么运转

成本大致跟三件事走，时长、声部密度、迭代次数。生成三分钟立体声比生成三十秒单声道贵得多；一次出八个候选再挑一个，等于八倍推理。训练是集中一次的大开销，推理是分散持续的小开销，用户量一大，后者总量可能超过前者。机房的水与电、显卡的生产与报废也要计入总账，但这些数字依赖具体电网与设备，跨地区差别很大，不能拿一个平均值套所有服务。

## 怎么调整

先减少无效生成，写清提示词再点生成，别用抽卡代替思考。批量任务集中跑，避免反复冷启动。能本地跑的小模型就本地跑，短素材、单声部、循环类需求，小模型常常够用。定长输出，需要三十秒就不要生成三分钟再剪。缓存与复用，同一段背景音乐不必每个视频重新生成。项目结束删掉不用的中间文件与云端副本。对外宣传避免"绿色 AI""零碳"这类没有依据的说法，改为说明具体措施。真要比较，先问清对方统计的是训练还是推理、包含哪些环节。
:::

::: en
## Where it gets hard

Generating a track draws power, and training a model draws far more. Vendors rarely publish the energy of a single generation, and public figures often blur training with inference. A user cannot audit this precisely, but can cut waste and stay honest in any environmental claim.

## How it runs

Cost tracks three things, duration, density and iterations. Three minutes of stereo costs much more than thirty seconds of mono, and asking for eight candidates to keep one means eight times the inference. Training is one large concentrated expense, inference is many small continuous ones, and at volume the second can outweigh the first. Water and power at the data centre, plus the manufacture and disposal of accelerators, belong in the total as well, but those figures depend on a specific grid and a specific machine, vary widely by region, and cannot be averaged across all services.

## How to adjust

Cut useless generation first. Write the prompt properly before pressing generate, and do not use the slot machine in place of thought. Batch jobs and avoid repeated cold starts. Run a small local model where it is enough, since short, monophonic and loop-based needs rarely require the largest one. Fix output length, thirty seconds of need should not produce three minutes of audio to trim. Cache and reuse, one background cue does not need regenerating per video. Delete unused intermediates and cloud copies when a project ends. In public claims, avoid "green AI" and "zero carbon" without evidence, and state the concrete measures instead. If you must compare providers, ask whether the number covers training or inference, and which stages.
:::

