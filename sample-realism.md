---
id: sample-realism
site: ai
cat: E
title: 让采样听起来真实
title_en: Making Samples Sound Real
summary: 采样假在三处，每次一样、力度一样、连奏一样
summary_en: Samples give themselves away in three places: every hit identical, every velocity equal, every join clean.
level: standard
tags: [采样, 轮替, 力度层, 连奏]
tags_en: [samples, round robin, velocity layers, legato]
alias: [采样真实感, 人性化, sample realism]
order: 147
links:
  - "[[glossary:velocity]]"
  - "[[glossary:sampler]]"
  - "[[glossary:legato]]"
instances:
  - groove-000000 | 放克鼓组，同一军鼓连击时听轮替，机械感最先从这里露出来（C1）
  - groove-000005 | 嘻哈鼓组，hi-hat 的力度与摇摆，平直就露馅（C1）
  - groove-000015 | 爵士放克过门，fill 的收尾每一下都不该相同（C1）
  - musicnet-000091 | 贝多芬四重奏慢乐章，换弓的缝与呼吸，是采样最难做的部分（C1）
sources:
  - Native Instruments Kontakt 手册与 Spitfire Audio 产品文档中关于轮替、力度层与连奏触发的工作方式。
  - 管弦乐配器与录音教材中关于换弓、换气与自然衰减的描述。
  - Sampler documentation on round robin and velocity layers, with reference to orchestration and recording texts.
updated: 2026-10-31
---

::: zh
## 假在哪

采样听起来假，通常不是音质不够好，而是同一件事重复得太完美。真鼓手每次落槌位置略偏，真弦乐换弓有缝，真长笛一个音里音高会轻微游移。采样库把这些差异录成了固定值，同一个键按十次得到十次一样的结果。真实感不是加混响，是把这些差异还回去。

## 轮替与力度

轮替是同一个音准备几个不同录音，按键时轮流取，避免机枪感。两次轮替只够应付慢句，快速连打要四到八次。力度层解决轻重，但层与层之间的跳变比层数更明显：轻层转中层的音量差要平滑，不然听起来像换了件乐器。真人的力度变化是连续的，MIDI 的 1 到 127 是台阶，写的时候在层边界附近多做几级。

## 连奏与释放

连奏采样在音符重叠时触发，问题常出在重叠长度。太短不触发，太长两个音一起响。弦乐的换弓、管乐的换气、吉他的换把，都是真实感所在；采样库若没有这些录音，就用极短的淡入淡出假装，但别把缝隙完全磨平。释放段同样重要，止音要按乐器来，鼓要留自然衰减，钢琴要留踏板，不能让所有音在同一毫秒消失。

## 逐项听一遍

- 同一音连打八次，听不出是同一个录音
- 快速过门里没有两次完全相同的击打
- 力度从轻到重扫一遍，没有突然换乐器的感觉
- 连奏处能听出换弓或换气，而不是一条无缝的线
- 长音结尾有自然衰减，不是统一淡出
- 不同音区的音色过渡合理，没有断层
- 人性化没有把拍点推乱，节奏仍然可跳
- 随机化参数写进工程，换台机器还能复现

## 过度修正的代价

过度人性化会把节奏弄散，尤其是鼓和低音，该准的地方必须准。轮替太多会吃掉动态，因为每次取到的样本强弱不一。用生成工具做 one-shot 时，先确认长度、调音和尾巴，再谈轮替；素材本身不齐，后面怎么调都补不回来。管弦乐里，采样再真也替代不了真乐队的融合，重要段落该录就录。

```audiolab
{"type":"instrument","drum":38,"synth":"perc","phrase":[38,38,38,38,38,38,38,38],"label":"同一个军鼓连打八次","label_en":"The same snare hit eight times","hint":"每次一模一样，就是采样露馅的地方","hint_en":"Eight identical hits are exactly where a sample gives itself away"}
```
:::

::: en
## Where the illusion fails

A sampled instrument rarely fails because the recording is poor. It fails because the same event repeats too perfectly. A drummer lands the stick a little differently each time, a string player's bow change leaves a small seam, a flute note wanders slightly in pitch. A library freezes those variations into fixed values, so ten presses of one key give ten identical results. Realism comes from putting the variation back, not from adding reverb.

## Round robin and velocity

Round robin means recording several takes of one note and cycling through them, which breaks the machine-gun effect. Two alternates are enough for a slow line; fast repeated notes want four to eight. Velocity layers handle weight, but the jump between layers is more audible than the number of layers: the level step from soft to medium has to be smooth or the instrument appears to change identity. A player's dynamics are continuous, while MIDI steps from 1 to 127, so add extra steps around each layer boundary.

## Legato and release

Legato samples trigger when notes overlap, and the usual fault is the overlap length. Too short and the legato never fires; too long and both notes sound. Bow changes, breaths and position shifts are where realism lives. If a library lacks those recordings, fake them with very short fades, but do not sand the seam completely flat. Releases matter as much: damping follows the instrument, drums need their natural decay, piano needs the pedal, and nothing should stop on the same millisecond.

## Listening through the list

- Eight repeated hits do not reveal a single recording
- No two strokes in a fast fill are identical
- A velocity sweep does not sound like switching instruments
- Legato passages show a bow change or a breath, not a seamless line
- Long notes decay naturally instead of fading by rule
- Tone crosses registers without a step
- Humanisation does not displace the beat beyond playability
- Randomisation is saved with the session and survives another machine

## The cost of over-correction

Too much humanisation pulls the rhythm apart, especially in drums and bass, where accuracy is the point. Too many round robins eat the dynamics, because each take was recorded at a different level. When generating one-shots, check length, tuning and tail before worrying about alternates; material that is uneven at the source cannot be repaired later. And no sample library replaces the blend of a real orchestra, so record the important passages when the budget allows.

```audiolab
{"type":"instrument","drum":38,"synth":"perc","phrase":[38,38,38,38,38,38,38,38],"label":"The same snare hit eight times","label_en":"The same snare hit eight times","hint":"Eight identical hits are exactly where a sample gives itself away","hint_en":"Eight identical hits are exactly where a sample gives itself away"}
```
:::
