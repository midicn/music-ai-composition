---
id: vertical-video-scoring
site: ai
cat: F
title: 竖屏视频配乐
title_en: Scoring Vertical Video
summary: 竖屏先争三秒，字幕占掉下半屏，音乐只能在缝里做功
summary_en: Vertical video wins or loses in three seconds, captions own the lower half, and music works in the gaps.
level: standard
tags: [竖屏, 前奏, 字幕, 循环]
tags_en: [vertical video, hook, captions, loops]
alias: [竖屏配乐, 短视频配乐, vertical scoring]
order: 161
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:sync-license]]"
  - "[[glossary:cue]]"
instances:
  - giantmidi-007791 | 《致爱丽丝》，第一个动机两秒内成立，竖屏要的进入速度（C1）
  - pdmx-001170 | 莫扎特《土耳其进行曲》，主题不铺垫直接出现（C1）
  - pdmx-002097 | 《野蜂飞舞》，无前奏的连续音型怎样抓住注意力（C1）
  - pdmx-001524 | 格里格《在山魔王的宫殿里》，短循环里靠加速维持张力（C1）
sources:
  - TikTok 与 YouTube 官方创作者规范中关于字幕安全区与音频响度的要求。
  - 短视频配乐与声音设计的公开访谈，讨论开头与循环的处理。
  - 流媒体响度标准文档，用于说明手机外放与归一化后的听感。
updated: 2026-10-31
---

::: zh
## 三秒定生死

竖屏视频的前三秒决定划不划走，音乐没有时间做前奏。生成素材常带四到八小节引子，等主题进来，人已经在看下一条。做法是把最好的两小节剪到最前面，或者让生成时直接从主题开始。开头不一定要响，但一定要有识别度：一个音色、一个节奏型、一句人声，都行。

## 字幕安全区

竖屏的字幕通常压在下半屏，平台的按钮又占右侧和底部。音乐的中频要和字幕错开，这不是视觉问题，是注意力问题：观众在读数，音乐就别在同一时刻堆密集的字或尖锐的合成器。让副歌的密度避开字幕出现的段落，或者在字幕出现时把高频让一点，比整段降音量有效。

## 循环与结尾

很多竖屏内容会循环播放，结尾必须能接回开头。生成时要求无前奏、可循环，拿到后自己找接缝，切在拍点上，把尾巴收干净。十五到三十秒是常用长度，超过一分钟要考虑分段，不然重复感会先于内容出现。结尾不要渐弱，渐弱在循环里就是一次掉音量。

## 发布前过一遍

- 第一秒内出现动机或明确音色
- 前奏已剪掉，或本来就没有
- 字幕出现时中频没有抢戏
- 结尾能无缝接回开头
- 手机外放能听到钩子，低频不靠它
- 授权覆盖商业账号与投放
- 生成记录与提示词已留存
- 同一条画面备了两版音乐做对比

## 横屏习惯搬不过来

把横屏的配乐直接裁成竖屏用，落点和字幕全对不上。为了显得高级留长前奏，是最常见的死法。低频在手机外放几乎不存在，把钩子放在低频等于没有钩子。还有，别用一段音乐配所有视频，算法会把相似内容归到一起，观众也会腻。授权没理清就发布，流量越好，下架时越疼。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","D#4","E4","B3","D4","C4","A3","B3"],"label":"前三秒要出现的钩子","label_en":"A hook that has to arrive in three seconds","hint":"从第一个音开始数，动机在第几拍成立","hint_en":"Count from the first note and hear on which beat the motif lands"}
```
:::

::: en
## Three seconds decide

The opening three seconds of a vertical video decide whether a thumb moves on, so the music has no room for an intro. Generated material often arrives with four or eight bars of setup, and by the time the theme appears the viewer is elsewhere. Cut the best two bars to the front, or ask the tool to begin on the theme. The start does not have to be loud, but it has to be identifiable: a timbre, a rhythm, a single voice.

## The caption zone

Captions usually sit in the lower half of a vertical frame, while platform buttons claim the right edge and the bottom. The midrange has to avoid the caption, which is less a visual problem than a problem of attention: the viewer is reading, so do not stack dense words or sharp synths at that moment. Keep the chorus sparse where captions appear, or yield a little high end when they do, and it will work better than turning the whole track down.

## Loops and endings

Much vertical content replays, so the end has to lead back to the start. Ask for no intro and a seamless loop, then find the seam yourself, cut on the beat and clean the tail. Fifteen to thirty seconds is a common length; past a minute, consider sections or repetition will arrive before the content does. Do not fade out, because a fade in a loop is simply a drop in level.

## Before posting

- A motif or a clear timbre appears within the first second
- The intro is gone, or was never there
- The midrange does not fight the captions
- The ending joins the opening seamlessly
- The hook survives a phone speaker without low end
- The licence covers a commercial account and paid promotion
- The generation record and prompt are kept
- Two music versions exist for the same footage

## Habits that do not survive the crop

Cropping a landscape score into a vertical frame leaves hit points and captions misaligned. Keeping a long intro for polish is the most common way to lose viewers. Phone speakers reproduce almost no low end, so a hook placed there is no hook at all. Nor should one track serve every video, since recommendation systems group similar content and viewers tire of it. Posting before the licence is clear hurts most when a video does well.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["E4","D#4","E4","B3","D4","C4","A3","B3"],"label":"A hook that has to arrive in three seconds","label_en":"A hook that has to arrive in three seconds","hint":"Count from the first note and hear on which beat the motif lands","hint_en":"Count from the first note and hear on which beat the motif lands"}
```
:::
