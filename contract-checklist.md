---
id: contract-checklist
site: ai
cat: G
title: AI 合同清单
title_en: AI Contract Checklist
summary: 一份能落地的清单，把范围、披露、权利、修改与退出写清楚
summary_en: A working checklist covering scope, disclosure, rights, revisions and exit
level: standard
tags: [合同, 清单, 交付, 修改轮次]
tags_en: [contract, checklist, delivery, revisions]
alias: [AI 合同, 项目清单, contract checklist]
order: 11
links:
  - "[[glossary:sync-license]]"
  - "[[glossary:termination-right]]"
  - "[[glossary:work-for-hire]]"
instances:
  - oga-000089 | 游戏用循环段落，长度与循环点必须写进验收标准（C1）
  - groove-000037 | 八小节桑巴鼓循环，交付单位小，修改次数容易界定（C1）
  - mutopia-000497 | 贝多芬第五第一乐章，长作品的分段交付与修改范围要提前约定（C1）
  - atepp-001115 | 肖邦第一叙事曲的常规录音，交付格式与版本要写明（C1）
sources:
  - 音乐委托制作合同的常见条款，依公开合同通识整理，未抄模板原文
  - 生成内容的使用与标注要求，依公开平台规则归纳，未作法律判断
updated: 2026-10-30
---

::: zh
## 问题

AI 让制作变快，合同却常常还是旧模板。旧模板假设作者是人、交付是成品、修改是有限次的。现在这三条都松动了，争议集中在，这算一次修改还是新做一版，交付的是分轨还是混好的立体声，客户能不能拿去做训练数据。

## 原理

合同的作用不是预测所有情况，而是把可预见的歧义提前定死。AI 项目里最容易含糊的五处。范围，几首、多长、什么编制、要不要分轨与 MIDI。披露，是否允许使用生成工具，是否需要在成片标注。权利，授权还是转让、是否独家、客户能否转授或用于训练。修改，几轮、每轮包含什么、超出怎么计费。责任，相似性争议、平台下架、第三方索赔由谁处理。再加一条退出，项目中止时已付款项与已交付文件怎么处理。

## 做法

逐条落到纸面。写明交付物清单与格式，采样率、声道、分轨数量、是否含工程文件。写明生成工具的使用与披露方式，附上条款快照的日期。写明授权范围与限制，客户不得将交付物用于训练模型，如需另议。写明修改轮次与判定标准，例如"同一段落的结构性调整计一轮，音量与平衡调整不计"。写明相似性检查由谁做、做到什么程度。写明验收期与逾期视为通过的规则。争议解决地与适用法律写清，跨境项目尤其要确认。签字前让律师看一遍，模板不等于适用。

## 听什么

在游戏循环里听长度与循环点如何决定验收；在桑巴鼓循环里听小单位交付怎样让修改边界清楚；在贝多芬第五第一乐章里听长作品为什么必须分段验收；在叙事曲录音里听格式与版本怎样影响交付。把这些听清楚，条款才写得具体。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":116,"label":"可验收的单位","label_en":"A unit you can accept","hint":"交付单位越小，修改边界越清楚","hint_en":"The smaller the unit, the clearer the edge of a revision"}
```
:::

::: en
## The problem

AI speeds up production while contracts stay on old templates. Those templates assume a human author, a finished deliverable and a finite number of revisions. All three assumptions have loosened, and disputes now settle on whether this counts as a revision or a new version, whether delivery means stems or a mixed stereo file, and whether the client may use the material for training.

## How it works

A contract cannot predict everything, but it can fix the foreseeable ambiguities. Five are most often left vague in AI work. Scope, how many pieces, how long, what instrumentation, whether stems and MIDI are included. Disclosure, whether generation is allowed and whether the finished piece must be labelled. Rights, licence or assignment, exclusivity, whether the client may sublicense or train on it. Revisions, how many rounds, what a round contains, how overruns are billed. Liability, who handles similarity claims, platform takedowns and third-party demands. Add an exit clause, covering payment already made and files already delivered if the project stops.

## Practice

Put each point on paper. List deliverables and formats, sample rate, channels, stem count, whether project files are included. State how generation is used and disclosed, with the date of the terms snapshot you relied on. State the licence and its limits, including that the client may not train models on the delivery without a separate agreement. Define revision rounds and the test, for example "a structural change to the same section counts as one round, level and balance adjustments do not". Say who runs the similarity check and to what extent. Set an acceptance period and a rule for deemed approval. Name the governing law and forum, and confirm it for cross-border work. Have a lawyer read it before signing, since a template is not advice.

## What to listen for

In the game loop, how length and loop points define acceptance. In the samba loop, how small units make revision boundaries obvious. In the first movement of the Beethoven symphony, why a long work must be accepted in sections. In the Ballade recording, how format and version shape delivery. Hear these clearly and the clauses become specific.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":116,"label":"A unit you can accept","label_en":"A unit you can accept","hint":"The smaller the unit, the clearer the edge of a revision","hint_en":"The smaller the unit, the clearer the edge of a revision"}
```
:::
