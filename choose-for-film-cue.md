---
id: choose-for-film-cue
site: ai
cat: K
title: 影视 cue 选型
title_en: Choosing a Tool for a Film Cue
summary: 画面先定落点，工具只决定你用什么去填这几个落点。
summary_en: The picture sets the hit points; the tool only decides what you fill them with.
level: standard
tags: [选型, 影视配乐, cue, 同步]
tags_en: [selection, film scoring, cue, sync]
alias: [配乐选型, 影视音乐工具, film cue]
order: 13
links:
  - "[[glossary:sync-license]]"
  - "[[glossary:incidental-music]]"
  - "[[glossary:lufs]]"
tool_kind: guide
tool_vendor: 本站
tool_form: 网页
tool_platforms: [浏览器]
tool_price: 免费
tool_jobs: [选型, 影视配乐]
tool_verified: 2026-10-30
instances:
  - atepp-000398 | 门德尔松《仲夏夜之梦》戏剧配乐，场景转换处如何换气（C1）；这是该用途常见产出的参照，不是本站工具的演示
  - atepp-005536 | 穆索尔斯基《图画展览会》的侏儒，性格小品的配器密度参照（C1）；这是该用途常见产出的参照，不是本站工具的演示
  - pdmx-002038 | 圣桑《骷髅之舞》，悬念与推进的节奏参照（C1）；这是该用途常见产出的参照，不是本站工具的演示
  - mutopia-001411 | 萨蒂《裸体歌舞》第一首，稀疏底乐的留白参照（C1）；这是该用途常见产出的参照，不是本站工具的演示
sources:
  - 影视配乐与同步授权的公开流程说明，对照2026-10-30 复核整理。
  - 响度与交付规格的行业通识（制作实践）。发行结论不在本文范围。
updated: 2026-10-30
---

::: zh
## 能替你做完什么

这一页把「给画面配一段音乐」拆成三种可交付的活：三十秒短片要一版粗剪能看的配乐；九十秒预告要三个落点都踩住的版本；长片里四分钟的底乐要能随对白让路。三种活对控制力的要求差一个量级，路线选错，返工全发生在剪辑台上。

## 它怎么工作

四种做法，按控制力、交付形态、学习成本、权利风险分。

文本生成加剪辑（Suno、Udio 一类）：控制力停在段落层面，能要到「前十五秒铺、三十秒抬、四十五秒收」的走向，要不到第二十七点四秒的落点。交付是立体声成品，贴画面靠剪与拉伸。学习成本最低，一晚十条。权利风险最高，影视同步、署名与平台的再分发条款都得另核。

生成加 DAW 重做：控制力中高，生成只负责音色与氛围，节奏与落点回到工程里重排。交付是分轨，能交给混音师。学习成本中高，要会看时间码、会切开生成的尾巴。风险中等，原生成物的条款仍跟着用。

采样音源手工写（DAW 加管弦或合成音源）：控制力最高，每一拍都能对齐画面。交付是分轨与总谱，改一版不用重录。学习成本最高，要会写和声、会配器。权利风险最低，音源授权写得清楚。

免版税曲库加粗剪：控制力最低，只能挑不能改。交付是可直接使用的授权文件。学习成本几乎为零。风险中等，授权范围、期限与同曲撞车都要看。

## 哪里会坑你

第一是精度错配。生成给你的是「感觉对」，画面要的是「第几帧对」，两者之间必须有人工剪辑这一层。第二是交付规格。片子要上流媒体，响度、真峰值、cue sheet 与许可文件缺一不可，生成工具一条都不管。第三是模仿的界线，用提示去复刻仍在版权期的电影主题，旋律轮廓一像就麻烦。

不要用生成曲直接当交付母版交给客户。不要在需要精确落点的段落靠反复重生成。不要拿同一段配乐同时喂给两个品牌的片子，平台条款常限制再分发。不要用没写清授权范围的曲库曲去投标。

## 换成什么

只是要提案、要看感觉，用 Suno 或 Udio，快且便宜；要交片，就把生成降到出草稿，成品回 DAW 里写。片子长、要随对白起伏，用分轨交给混音做闪避。最常见的搭配是：生成找音色，DAW 写结构，iZotope 那一类工具走单独的母带流程。

## 先学三件事

先学三件事：把时间码与拍速对上、把落点标在工程里、把成品导出成与画面同长。然后读这里的影视配乐、同步与 cue 剪辑、响度目标三篇。

```audiolab
{"type":"instrument","gm":"Tremolo Strings","synth":"bowed","phrase":["D3","F3","A3","D3","C#4","A3","F3","D3"],"label":"一段绷紧的弦乐","label_en":"Tightened strings","hint":"配乐草稿先定张力，再定落点","hint_en":"Set the tension first, the hit points second"}
```
:::

::: en
## What it finishes for you

This page turns scoring a picture into three deliverables: a thirty-second short that needs a cuttable sketch; a ninety-second trailer that needs three hit points landed; four minutes of underscore that must step aside for dialogue. The control each job demands differs by an order of magnitude, and a wrong route sends every revision back to the edit suite.

## How it works

Four approaches, judged on control, deliverable, learning cost and rights exposure.

Text generation plus editing, with services such as Suno and Udio, stops at section level: you can ask for fifteen seconds of bed, a lift at thirty, a close at forty-five, but not an event at 27.4 seconds. The deliverable is stereo, aligned to picture by cutting and stretching. Learning cost is lowest, ten versions a night. Rights exposure is highest, since sync terms, credit and platform redistribution all need separate checks.

Generate then rebuild in a DAW gives medium-high control: generation supplies timbre and atmosphere while rhythm and placement are re-laid in the session. The deliverable is stems that a mix engineer can take. Learning cost is medium-high, because you must read timecode and cut the generated tails.

Writing by hand with sampled instruments gives the most control; every beat can sit on a frame. The deliverable is stems plus a score, and a revision needs no re-recording. Learning cost is highest, since harmony and orchestration are yours. Rights exposure is lowest, because library licences are explicit.

A royalty-free library plus rough cutting gives the least control: you choose, you do not change. The deliverable is a usable licence file. Learning cost is nearly zero. Risk is moderate and lies in licence scope, term and the same track turning up in a rival's film.

## Where it bites

First, a precision mismatch: generation gives you a feeling, the picture wants a frame, and human editing is the layer between them. Second, delivery specs: streaming release needs loudness, true peak, a cue sheet and licence paperwork, none of which a generator handles. Third, the line of imitation: using prompts to recreate a film theme still in copyright gets awkward the moment the melodic contour matches.

Do not deliver a generated track as the master to a client. Do not chase a precise hit point by regenerating over and over. Do not feed one cue to two different brands' films, since platform terms often limit redistribution. Do not bid with a library track whose scope is unstated.

## What to swap in

For a pitch or a mood check, use Suno or Udio, because it is fast and cheap; for delivery, demote generation to drafting and write the master in a DAW. For long edits that breathe with dialogue, work in stems and let the mix duck them. The usual pairing: generation for timbre, a DAW for structure, a suite such as iZotope RX for a separate mastering pass.

## First three things

Learn to match timecode with tempo, to place hit points as markers in the session, and to export at exactly the picture's length. Then read this site's pages on film scoring, sync and cue editing, and loudness targets.

```audiolab
{"type":"instrument","gm":"Tremolo Strings","synth":"bowed","phrase":["D3","F3","A3","D3","C#4","A3","F3","D3"],"label":"Tightened strings","label_en":"Tightened strings","hint":"Set the tension first, the hit points second","hint_en":"Set the tension first, the hit points second"}
```
:::
