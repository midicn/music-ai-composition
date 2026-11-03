---
id: "quality-checklists"
site: "ai"
cat: "H"
title: "质量清单"
title_en: "The Quality Gate"
summary: "交付前的清单按修改成本排序，不靠再听一遍"
summary_en: "A pre-delivery gate sorted by cost to fix, not by another listen."
level: "standard"
tags: ["清单", "交付", "质检", "验收"]
tags_en: ["checklist", "delivery", "QC", "acceptance"]
alias: ["质量清单", "交付检查", "delivery checklist"]
order: 3
links: ["[[glossary:true-peak]]", "[[glossary:headroom]]", "[[glossary:stems]]"]
instances: []
sources: ["https://www.itu.int/rec/R-REC-BS.1770-5-202311-I/", "https://tech.ebu.ch/publications/r128"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "质量清单中的响度、真峰值和交付口径需要文件测量与目标规范核对；普通播放受播放器音量影响，不能代替对完整成品的技术验收。"
---

::: zh
## 问题

交付前最容易出的错都很无聊，结尾多了两秒静音，剪切点有一声咔哒，真峰值超了零点几 dB，单声道一叠人声就没了，元数据没写，权利来源说不清。这些问题靠再听一遍发现不了，因为听的时候注意力在音乐上。清单的作用不是显得专业，而是把注意力从音乐挪到可验证的项目上。

## 清单的顺序

按修改成本排，从结构开始。时长对不对，开头结尾是否干净，循环点接得上吗，淡入淡出有没有做到位。然后听伪影，剪切点、直流偏移、降噪的水声、立体声的相位感、削波、尾部噪声。再测响度，用表不用耳朵，整体响度按平台目标，真峰值留一 dB 余量，短时响度不要忽大忽小。再做单声道检查，低频和主唱是否还在。最后查元数据和权利，曲名、作者、ISRC、版本号、模型条款、样本授权、人声同意书。

## 怎么用

每次交付都跑同一张表，顺序不变，逐项写通过或不通过，并写下检查人和时间。做的人不能是唯一的检查人。任何一项无法验证，就算不通过，不要用应该没问题放过去。改完任何一处，整张表重跑，因为修一个咔哒可能带来新的淡出问题。把表贴在工程目录里，交付时连同记录一起归档。清单尽量短，超过二十项就会有人跳着看。
:::

::: en
## The problem

Most delivery failures are boring. Two extra seconds of silence, a click at the edit, true peak a fraction over, the vocal vanishing in mono, empty metadata, an unclear rights chain. Re-listening does not catch them because attention is on the music. A checklist is not a badge of professionalism; it moves attention from the music to verifiable items.

## The order

Sort by cost to fix, starting with structure. Is the duration right, are the head and tail clean, does the loop point join, are the fades complete. Then artifacts, edit clicks, DC offset, denoiser gurgle, stereo phase, clipping, noise in the tail. Then measure loudness with a meter rather than ears, integrated to the platform target, true peak one dB in reserve, short-term level steady. Then the mono check, whether the bass and lead survive a sum. Finally metadata and rights, title, creator, ISRC, version, model terms, sample licences, voice consent.

## Using it

Run the same list in the same order for every delivery, mark pass or fail per item, and record who checked and when. The person who made the track cannot be the only checker. Any item you cannot verify is a fail, not a should be fine. After any change, rerun the whole list, because fixing a click can introduce a new fade problem. Keep the list in the project folder and archive it with the delivery. Keep the list short; past twenty items people start skipping.
:::

