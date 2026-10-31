---
id: mastering-ai-generated
site: ai
cat: D
title: 母带处理
title_en: Mastering AI-Generated Material
summary: 自动母带能修电平和亮度，判断不了结构、呼吸与取舍
summary_en: Automated mastering can fix level and brightness but cannot judge structure, breathing or intent.
level: standard
tags: [母带, 自动母带, 余量, 人工检查]
tags_en: [mastering, automated mastering, headroom, human checks]
alias: [AI 母带, 自动母带, automated mastering]
order: 5
links:
  - "[[glossary:mastering]]"
  - "[[glossary:headroom]]"
  - "[[glossary:limiter]]"
instances:
  - giantmidi-003263 | 萨蒂三首《裸体歌舞》，整首很轻，听母带后弱段是否还有退路（C1）
  - atepp-000239 | 肖斯塔科维奇第十号赋格，织体密，限幅器最容易在这里失真（C1）
  - musicnet-000090 | 贝多芬第十二四重奏首乐章，慢引子接快板，听对比是否被抹平（C1）
sources:
  - 自动母带的能力边界；公开工具文档与母带惯例是主要依据。
  - Automated mastering limits, summarized from public tool documentation and general mastering practice
updated: 2026-10-30
---

::: zh
## 卡住的地方

自动母带工具越来越多，上传一个立体声文件，几分钟后拿回一个更响、更亮、更完成的版本。它确实能修电平和整体音色，但它听到的只是一个文件。它不知道第二段是故意收住的，不知道人声那句该更近，也不知道结尾的淡出是不是设计。把判断全交出去，得到的是平均值。

## 它怎么运转

自动母带靠匹配目标曲线与响度，做宽频均衡、压缩和限幅。决策来自统计，不来自结构。它能处理整体亮度、低频量与峰值，处理不了声部关系、段落意图和编曲问题。素材里已经有的失真、遮蔽和相位问题，它只会放大。给它一条参考曲，它会靠得更近，但仍然不知道你的副歌为什么只比主歌高 2 dB。

## 从哪开始

送进去之前先把混音定稿。总线上不挂限幅器，留 4 到 6 dB 余量，单声道与真峰值都查过。导出 24 bit，不要先做响。给它一条同类型的参考曲，同时自己留一版未处理的。拿回两三个版本后做人工检查，开头十秒的电平、人声在手机上的清晰度、低频在小音箱上是否还在、段落转换有没有被压平、淡出是否自然。通过后再看表，真峰值不超过 -1 dBTP。不通过就回混音，不要用第二个母带插件去补第一个的坑。

## 耳朵要抓的点

萨蒂《裸体歌舞》整首很轻，母带容易把它推得没有退路，听弱段是否还留得住。肖斯塔科维奇《前奏曲与赋格》第十号的赋格织体密，限幅器在这里最容易产生失真。贝多芬第十二四重奏第一乐章开头是慢引子接快板，听自动母带有没有把这段对比抹平。三处都拿未处理版做对照。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D3","A3","D4","F4","A4","F4","D4","A3"],"label":"母带前的长音余量","label_en":"Headroom on a sustained line","hint":"听长音的尾部有没有被压扁，余量越少尾音越短","hint_en":"Hear whether the tail is squashed; less headroom shortens the decay"}
```
:::

::: en
## Where it snags

Automated mastering is everywhere. Upload a stereo file and minutes later a louder, brighter, more finished version comes back. It genuinely fixes level and overall tone, but all it hears is one file. It does not know the second verse is meant to hold back, that one vocal line should sit closer, or that the fade is deliberate. Hand over every decision and you get an average.

## How it runs

Automated mastering matches a target curve and loudness using broadband EQ, compression and limiting. The decisions are statistical, not structural. It can handle overall brightness, low-end weight and peaks; it cannot handle part relationships, section intent or arrangement problems. Distortion, masking and phase issues already in the material only get louder. Give it a reference and it moves closer, but it still cannot know why your chorus is only 2 dB above the verse.

## Where to start

Finish the mix before sending anything. Leave no limiter on the bus, keep 4 to 6 dB of headroom, and check mono and true peak. Export at 24 bit without pre-mastering loudness. Supply one reference of the same genre and keep an unprocessed version yourself. When two or three versions come back, do the human checks, starting with the first ten seconds, vocal intelligibility on a phone, whether the low end survives a small speaker, whether transitions were flattened, and whether the fade still works. Then look at the meters, with true peak at or below -1 dBTP. If a version fails, return to the mix rather than stacking a second mastering plugin on the first.

## What the ear catches

Satie's Gymnopedies are quiet throughout, and a master can push them past the point of no return, so hear whether the soft passages still have somewhere to go. Shostakovich's Fugue No. 10 is dense, the place where a limiter distorts first. Beethoven's String Quartet No. 12 opens with a slow introduction into an allegro, so hear whether automated mastering flattened that contrast. Compare all three against your unprocessed version.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["D3","A3","D4","F4","A4","F4","D4","A3"],"label":"Headroom on a sustained line","label_en":"Headroom on a sustained line","hint":"Hear whether the tail is squashed; less headroom shortens the decay","hint_en":"Hear whether the tail is squashed; less headroom shortens the decay"}
```
:::
