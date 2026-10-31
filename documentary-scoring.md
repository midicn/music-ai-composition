---
id: documentary-scoring
site: ai
cat: F
title: 纪录片配乐
title_en: Scoring Documentary
summary: 纪录片音乐要能铺十分钟，也要在采访开口时立刻消失
summary_en: Documentary music must sustain ten minutes and vanish the moment an interview begins.
level: standard
tags: [纪录片, 铺底, 采访, 历史质感]
tags_en: [documentary, underscore, interview, period texture]
alias: [纪录片音乐, 纪实配乐, documentary score]
order: 166
links:
  - "[[glossary:cue]]"
  - "[[glossary:dynamics]]"
  - "[[glossary:incidental-music]]"
instances:
  - pdmx-001010 | 马勒第五，一个乐章铺十分钟情绪，长段铺底的耐力参照（C1）
  - mutopia-001411 | 萨蒂《裸体歌舞》，稀疏底乐的留白，采访段落的参照（C1）
  - pdmx-000160 | 圣桑《骷髅之舞》，固定音型写场面，历史段落的质感参考（C1）
  - atepp-000398 | 门德尔松《仲夏夜之梦》，场景转换处如何换气（C1）
sources:
  - Sheila Curran Bernard, Documentary Storytelling（Focal Press）中关于采访优先与音乐让位的章节。
  - 纪录片作曲家的公开访谈，讨论长段铺底与历史质感的做法。
  - 影视音乐编辑惯例中关于 cue 进出与画面同步的说明。
updated: 2026-10-31
---

::: zh
## 音乐托着信息，不抢戏

纪录片里最重要的是信息：采访、旁白、现场声。音乐的工作是让这些信息更容易被听进去，而不是替它们说话。判断一段配乐合不合格，把画面关掉只听声音：如果音乐抢走了注意力，它就太满了。好的纪录片配乐常常让人记不住旋律，只记得某个时刻的感觉。

## 长段怎么铺

纪录片的一个段落可能长达十分钟，音乐要在里面持续存在又不重复到烦。做法是用一个很小的材料，几个音、一个音色、一个低频脉动，靠配器和音区变化维持，而不是靠旋律不断展开。每两到三分钟换一次织体，让耳朵有新的东西抓，但不要换主题。生成工具擅长给八小节，不擅长给十分钟，长段要自己拼。

## 段落表

| 段落 | 音乐职责 | 密度 | 进出方式 |
|---|---|---|---|
| 开场 | 建立时间与地点 | 中，一个有特征的音色 | 从环境声淡入 |
| 采访 | 让位 | 低或无 | 句首前收，句尾后回 |
| 叙述蒙太奇 | 维持推进 | 中，节奏稳定 | 画面切换处切 |
| 历史资料 | 提供年代感 | 低，偏原声 | 与档案声音错开 |
| 情绪高潮 | 托住观点 | 高，但短 | 全片只出现一次 |
| 结尾 | 留白 | 低或只留环境 | 不做总结 |

## 历史质感

历史段落不是加一段古乐就够。时代感来自录音质感、乐器编制和演奏习惯：更窄的频响、更少的低频、轻微的噪声底、不平均的律动。用合成器模仿这些要克制，噪声加太多会像收音机故障。真实乐器加一点带限和失真，往往比纯合成更可信。别让整部片子都泡在同一种复古里，会腻。

## 让位与边界

采访开口前一到两秒把音乐收到很低或直接停，句尾再回来，回来时不要从原音量突然出现。如果采访有背景噪声，音乐可以填它的缝，但不要盖过语音的辅音。多个受访者切换时，音乐保持一条线，别每换一个人就换一首。最常见的问题是音乐从头铺到尾，观众疲劳，真正的高潮也没了；另一种是情绪替观众下结论，画面还在陈述，音乐已经哭了。生成素材的长渐弱和循环尾巴要处理干净，不然采访一开始，音乐还在慢慢消失。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A3","E4","D4","C4","B3","A3","G3","A3"],"label":"采访前的一层铺底","label_en":"A bed before the interview","hint":"听它退出的地方，比听旋律更重要","hint_en":"Hear where it gets out of the way; that matters more than the tune"}
```
:::

::: en
## Music supports, it does not lead

Documentary carries information first: interviews, voice-over, location sound. Music exists to make that information easier to take in, not to speak in its place. A simple test is to close the picture and listen: if the music takes attention, it is too full. A good documentary score is often hard to hum afterwards; what stays is the feeling of a particular moment.

## Sustaining a long stretch

A single sequence can run ten minutes, and the music has to remain present without becoming repetitive. Use a small cell, a few notes, one timbre, a low pulse, and hold it through changes of orchestration and register rather than through continuous melodic development. Change the texture every two or three minutes so the ear has something new to hold, but do not change the theme. Generation tools are good at eight bars and poor at ten minutes, so long spans have to be assembled.

## Section map

| Section | Musical job | Density | Entry and exit |
|---|---|---|---|
| Opening | Establish time and place | Medium, one distinctive timbre | Fade in from location sound |
| Interview | Yield | Low or none | Duck before the first word, return after the last |
| Narration montage | Maintain momentum | Medium, steady pulse | Cut on the picture edit |
| Archive material | Suggest period | Low, mostly acoustic | Sit clear of the archival audio |
| Emotional peak | Support the argument | High but brief | Once in the whole film |
| Ending | Leave space | Low, or ambience only | Do not summarise |

## Period texture

A historical section is not solved by adding generic old music. Period comes from recording character, instrumentation and playing habits: narrower bandwidth, less low end, a little noise floor, uneven timing. Imitating those with synths takes restraint, because too much noise sounds like a broken radio. Real instruments with gentle band-limiting and distortion often convince more than pure synthesis. And do not let the whole film sit in the same retro wash, or it becomes a mannerism.

## Yielding, and the limits

Pull the music down or stop it one or two seconds before an interview begins, bring it back after the sentence, and never return at the previous level in one jump. If the interview has background noise, music can fill the gaps but must not cover the consonants. When the subject changes, keep one musical thread instead of changing tracks with each face. The commonest failure is wall-to-wall music that tires the audience and leaves the real climax with nowhere to go; the next is music that concludes before the picture does, already weeping while the film is still stating facts. Clean the long fades and loop tails in generated material, or the music will still be fading out as the interview starts.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A3","E4","D4","C4","B3","A3","G3","A3"],"label":"A bed before the interview","label_en":"A bed before the interview","hint":"Hear where it gets out of the way; that matters more than the tune","hint_en":"Hear where it gets out of the way; that matters more than the tune"}
```
:::
