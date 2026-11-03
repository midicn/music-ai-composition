---
id: "ai-vendor-exit"
site: "ai"
cat: "A"
title: "退出与迁移"
title_en: "Leaving a Vendor"
summary: "能不能走，取决于手里有没有可重建的素材、提示与记录。"
summary_en: "Whether you can leave depends on owning rebuildable assets, prompts and records, not on export buttons alone."
level: "standard"
tags: ["迁移", "导出", "供应商锁定", "归档"]
tags_en: ["migration", "export", "vendor lock-in", "archiving"]
alias: ["退出供应商", "迁移", "vendor exit"]
order: 127
links: ["[[glossary:stems]]", "[[glossary:midi-protocol]]", "[[glossary:termination-right]]"]
instances: []
sources: ["https://www.ableton.com/en/manual/managing-files-and-sets/", "https://replicate.com/docs/topics/predictions/data-retention"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论平台退出和文件可取回性，需要实际导出、保存媒体并离开原平台重开检查；MIDI试听不能验证服务保留期或工程迁移成功。"
---

::: zh
## 先假设明天要搬

账号还能登录时，没人会检查导出。真正要搬的那天，才发现历史作品只有混合音频，提示散在聊天记录里，分轨从未导出。退出能力要在签约时评估，不是在涨价时补救。

## 能带走什么

| 资产 | 常见导出 | 迁移后的状态 | 要提前做 |
|---|---|---|---|
| 成品音频 | WAV、MP3 | 可用，但难再改 | 保留无损版本与母带 |
| 分轨 | WAV，有时限 | 可重混 | 每月导出一次全部分轨 |
| MIDI 与乐谱 | MIDI、MusicXML | 可换音源重建 | 核对速度、调号、音高 |
| 歌词与提示 | 文本、CSV | 可改写，不能直接复用 | 自建提示库与版本号 |
| 种子与参数 | 少见于导出 | 通常绑定模型版本 | 记录模型名、版本、日期 |
| 工程元数据 | 项目文件、JSON | 常缺失 | 截图与字段清单 |

导出按钮存在，不等于导出可用。分轨是不是干声、MIDI 有没有丢速度信息、文件名是否带版本，都要抽样验证。

## 提示与种子能带走多少

提示是自然语言，换模型后要重写，但结构、约束顺序和排除项可以照搬。种子只在同一模型同一版本内可复现，升级或换供应商后基本失效。把提示、种子、模型版本、生成日期一起存档，迁移时才知道哪些结果能重建，哪些只能当参考。歌词、段落标记与和弦进行是比种子更耐迁移的资产，应优先保存。

## 迁移步骤

1. 清点资产：成品、分轨、MIDI、歌词、提示、工程元数据。
2. 批量导出，保留无损格式与原始命名。
3. 校验：抽样对比时长、采样率、声道、峰值。
4. 在新服务重建三条代表性任务，比较返工量。
5. 双轨运行一个项目周期，再停旧账号。
6. 归档旧账号的条款版本与删除确认。

## 退出前的红旗

导出只给混合音频；分轨要额外付费且限时；删除账号即失去全部历史；许可随订阅终止而失效；没有批量导出或 API。出现两条以上，就该把这家当临时工具，而不是长期仓库。迁移成本高的真正原因通常不是音频，而是那些从未被当作资产保存的提示与工程记录。
:::

::: en
## Assume the move happens tomorrow

Nobody checks exports while the login still works. On moving day the archive turns out to hold only mixed audio, prompts are buried in chat history, and stems were never downloaded. Exit capability is a signing-time question, not a reaction to a price rise.

## What actually travels

| Asset | Usual export | State after migration | Do this early |
|---|---|---|---|
| Finished audio | WAV, MP3 | Usable, hard to revise | Keep lossless masters |
| Stems | WAV, sometimes time-limited | Remixable | Export all stems monthly |
| MIDI and scores | MIDI, MusicXML | Rebuildable with new sounds | Verify tempo, key, pitches |
| Lyrics and prompts | Text, CSV | Rewritable, not reusable as-is | Keep your own prompt library with versions |
| Seeds and settings | Rarely exported | Tied to a model version | Record model, version, date |
| Project metadata | Project files, JSON | Often missing | Screenshots and a field list |

An export button is not usable export. Check whether stems are dry, whether MIDI kept tempo information, and whether filenames carry versions.

## How far prompts and seeds travel

Prompts are natural language, so they need rewriting for another model, but structure, constraint order and exclusions carry over. A seed reproduces only within one model version and usually dies on upgrade or migration. Archive prompt, seed, model version and date together, and you will know which results can be rebuilt and which are merely references. Lyrics, section tags and chord progressions survive migration better than seeds and deserve priority.

## Migration steps

1. Inventory: masters, stems, MIDI, lyrics, prompts, project metadata.
2. Export in bulk, keeping lossless formats and original names.
3. Verify by sampling duration, sample rate, channels and peaks.
4. Rebuild three representative jobs in the new service and compare repair effort.
5. Run both systems for one project cycle before closing the old account.
6. Archive the old terms version and deletion confirmation.

## Red flags before exit

Mixed audio is the only export; stems cost extra and expire; deleting the account erases all history; the licence ends with the subscription; there is no bulk export or API. Two or more of these make the service a temporary tool, not a long-term archive. Migration is expensive less because of the audio than because prompts and project records were never treated as assets.
:::

