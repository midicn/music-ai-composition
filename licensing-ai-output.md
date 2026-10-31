---
id: licensing-ai-output
site: ai
cat: G
title: 授权 AI 输出
title_en: Licensing AI Output
summary: 你能授权的是自己做的那部分，别把不确定的权利写进合同
summary_en: License the part you actually made, and keep uncertain rights out of the contract
level: standard
tags: [授权, 合同, 保证条款, 赔偿]
tags_en: [licensing, contracts, warranties, indemnity]
alias: [AI 授权, 输出授权, licensing AI output]
order: 10
links:
  - "[[glossary:sync-license]]"
  - "[[glossary:mechanical-license]]"
  - "[[glossary:master-rights]]"
instances:
  - atepp-001114 | 肖邦第一叙事曲现场录音，作品、表演、录音三层权利叠在一起（C1）
  - atepp-001116 | 同一首曲子的重制版，母带处理产生新的版本与权利问题（C1）
  - mutopia-001411 | 公有领域的《裸体歌舞》谱面，原作免费，你的制作另算（C1）
  - giantmidi-003011 | 《致敬萨蒂》，风格接近不等于侵权，但必须在说明里讲清（C1）
sources:
  - 音乐授权中的权利层次，对照公开行业说明整理。
  - 保证与赔偿条款的常见写法（公开合同惯例）。
updated: 2026-10-30
---

::: zh
## 容易停住的地方

把 AI 生成的曲子授权给客户，合同上最危险的一句是"保证不侵犯任何第三方权利"。你无法诚实地给出这个保证，因为训练数据你不掌握，输出与既有作品的相似性你也没有查遍全球曲库。能给的，是对你实际做过的事做出承诺。

## 它怎么运转

一首成品叠着几层权利。作品本身，包括旋律、和声与歌词；某一次表演；某一份录音；以及编辑与制作。公有领域的作品不收费，但新的编曲、演奏与录音可能各自产生权利。AI 输出处在这套结构之外，它的可保护性本身有争议，所以你给客户的，更像是"使用这段音频的许可"加上"你贡献部分的转让"，而不是完整的版权转让。客户真正关心的是能不能用、会不会被下架、出事谁承担，这些可以用保证、赔偿与保险来分配，而不是靠一句空泛的承诺。

## 怎么调整

合同里分开写三件事。授权范围，媒介、地区、期限、是否独家、能否转授。披露义务，说明使用了哪些工具、哪些部分由人完成、是否包含合成人声。责任分配，你承担什么，例如你已知的第三方素材与你签署过的样本授权，客户承担什么，例如使用场景与修改后的版本。保证条款写成你能验证的事实，例如"据我所知的检索未发现实质相似""所用样本均已获授权"，并写明检索方法与范围。赔偿设上限，常见做法是以合同金额为限，是否可执行要按当地法律核实。客户要求独家或买断时，先确认你有没有权利给出独家。

## 耳朵要抓的点

在现场版叙事曲里听作品、表演与录音如何叠在一起；在重制版里听母带处理怎样产生另一个版本；在《裸体歌舞》的谱面里听原作本身，再把你的制作放在旁边；在《致敬萨蒂》里听风格上的接近，它提醒你相似与侵权是两件事，需要分别说明。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["D4","F4","A4","D5","C5","A4","F4","D4"],"label":"你能授权的范围","label_en":"What you can license","hint":"音符、演奏、录音各算一层，别混成一句保证","hint_en":"Notes, performance and recording are separate layers, not one promise"}
```
:::

::: en
## Where people stall

The most dangerous sentence in a contract for AI-generated music is a warranty that the work infringes no third-party rights. You cannot honestly give it, because you do not control the training data and you have not searched the world's repertoire for similarity. What you can give is a promise about what you actually did.

## How it runs

A finished track stacks several rights. The work itself, melody, harmony and lyrics, a particular performance, a particular recording, and the editing and production. A public-domain work is free to use, but a new arrangement, a new performance and a new recording may each generate rights. AI output sits outside that structure, and its protectability is itself contested, so what you hand a client is closer to a licence to use this audio plus an assignment of your own contribution, not a clean transfer of copyright. What clients need to know is whether they can use it, whether it may be taken down, and who bears the loss; warranties, indemnities and insurance allocate that.

## How to adjust

Write three things separately. The scope of the licence, media, territory, term, exclusivity and sublicensing. The disclosure obligation, which tools were used, which parts a person made, whether synthetic voice is present. The allocation of responsibility, what you cover, such as known third-party material and sample licences you signed, and what the client covers, such as the context of use and versions they alter. Phrase warranties as facts you can verify, for example "a search to the best of my knowledge found no substantial similarity" or "all samples used are licensed", and state the method and extent of that search. Cap indemnities, commonly at the contract value, and confirm enforceability under local law. When a client asks for exclusivity or a buyout, first confirm that you hold the rights to grant it.

## What the ear catches

In the live Ballade, how composition, performance and recording stack. In the remaster, how mastering produces another version. In the Gymnopedie score, the original itself, with your production placed beside it. In Homage to Satie, how close a style can come, a reminder that similarity and infringement are two separate questions to be answered separately.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["D4","F4","A4","D5","C5","A4","F4","D4"],"label":"What you can license","label_en":"What you can license","hint":"Notes, performance and recording are separate layers, not one promise","hint_en":"Notes, performance and recording are separate layers, not one promise"}
```
:::
