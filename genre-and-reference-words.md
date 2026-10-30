---
id: genre-and-reference-words
site: ai
cat: B
title: 风格与参考词
title_en: Genre Words and References
summary: 风格词是捷径也是陷阱，参考曲比风格标签更精确。
summary_en: Genre words are shortcuts and traps; a reference track is more precise than a genre label.
level: standard
tags: [风格, 参考, 提示, 描述]
tags_en: [genre, reference, prompt, description]
alias: [风格词, 参考曲, genre words, reference]
order: 2
links:
  - "[[glossary:timbre]]"
  - "[[glossary:tempo]]"
  - "[[instrument:piano]]"
instances:
  - groove-000005 | 87 BPM 嘻哈鼓组，风格词能否带出这种律动手感（C1）
  - thesession-020649 | 里尔舞曲，传统风格标签的模糊性（C1）
  - cyberhymnal-000001 | 赞美诗管风琴，宗教风格的音色联想（C1）
sources:
  - 风格标签在生成模型中的语义范围，依公开模型说明核对，未抄原文
  - 参考曲与风格描述的差别，依创作实践通识核对，未抄文本
updated: 2026-10-30
---

::: zh
## 问题

"爵士""电子""电影感"这类词很好用，但每个词背后是一大片互不相同的音乐。模型对风格词的理解是统计平均，写"爵士"往往得到最典型的那个版本。想要更具体的结果，光靠风格词不够。

## 判断标准

风格词适合定大方向，参考曲适合定细节。参考曲能同时传达音色、节奏、混音质感与情绪，但要注意模型是否允许使用受版权保护的参考。描述性词语介于两者之间：说清乐器、演奏法与录音响度，比堆风格标签有效。

## 做法

先用一个风格词定框，再用两三个具体描述收窄。需要特定质感时用参考曲，并说明参考的是哪一层。把"像某年代的某类唱片"拆成可执行的要素：乐器、鼓机、混响大小、失真程度。避免互相冲突的风格标签同时出现，模型会在中间取一个模糊的结果。

## 听什么

在嘻哈鼓组里听风格词能否带出律动，在里尔舞曲里听传统标签的模糊，在赞美诗里听宗教风格的音色联想。风格词决定方向，细节还得靠具体描述。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":87,"label":"风格词背后的律动","label_en":"The groove behind a genre word","hint":"同一个风格词可以对应很多种律动，听模型选了哪一种","hint_en":"One genre word covers many grooves; hear which one the model picks"}
```
:::

::: en
## The problem

Words like "jazz", "electronic" or "cinematic" are convenient, but each covers a wide field of very different music. A model reads genre words as statistical averages, so "jazz" tends to return the most typical version. For something specific, genre words are not enough.

## Judging it

Genre words set direction and references set detail. A reference track conveys timbre, rhythm, mix texture and mood at once, though the model's rules on copyrighted references must be checked. Descriptive language sits between the two: naming instruments, playing techniques and recording character works better than stacking labels.

## Practice

Frame with one genre word, then narrow with two or three concrete descriptions. Use a reference when a specific texture is needed and say which layer you mean. Break "like a record from a certain era" into executable parts: instruments, drum machine, reverb size, amount of distortion. Avoid contradictory labels, since the model will settle somewhere vague between them.

## What to listen for

On the hip-hop kit, whether the genre word brings the groove; in the reel, how blurry a traditional label is; in the hymn, the timbral associations of a religious style. Genre words set direction; detail still needs concrete description.

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"s s s s s s s s s s s s s s s s","bpm":87,"label":"The groove behind a genre word","label_en":"The groove behind a genre word","hint":"One genre word covers many grooves; hear which one the model picks","hint_en":"One genre word covers many grooves; hear which one the model picks"}
```
:::
