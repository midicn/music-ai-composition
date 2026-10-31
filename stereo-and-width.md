---
id: stereo-and-width
site: ai
cat: D
title: 声场与宽度
title_en: Stereo Field and Width
summary: 宽度不等于深度，生成的混响撑开的声场要先过单声道这一关
summary_en: Width is not depth, and a field widened by generated reverb has to survive the mono sum first.
level: standard
tags: [声场, 宽度, 单声道, 相位]
tags_en: [stereo field, width, mono, phase]
alias: [立体声, 宽度, stereo width]
order: 7
links:
  - "[[glossary:stereo-technique]]"
  - "[[glossary:panning]]"
  - "[[glossary:phase-check]]"
instances:
  - musicnet-000248 | 坎比尼第一木管五重奏，五件管乐靠声像与音色分开（C1）
  - groove-000005 | 87 BPM 嘻哈鼓组，底鼓与军鼓必须居中，单声道下不能塌（C1）
  - mutopia-001412 | 萨蒂《裸体歌舞》第二首，稀疏织体在单声道下还剩多少空间（C1）
sources:
  - 宽度的来源与单声道兼容（立体声与混音惯例）。
  - Width sources and mono compatibility (general stereo and mixing practice).
updated: 2026-10-30
---

::: zh
## 卡住的地方

AI 素材听起来很宽，戴上耳机像有空间。切到单声道，人声变薄，鼓组塌在中间，铺底少了一半。宽度是生成模型与混响最容易伪造的东西，也是最容易在手机、厨房音箱和俱乐部里消失的东西。先保证单声道站得住，再谈宽。

## 运行方式

真实的深度来自到达时间差、早期反射和高频吸收，声音有前后，也有明确的位置。声像只是左右，深度要靠电平与反射，两者不是一回事。伪造的宽度来自左右声道的相位去相关，两耳听是宽的，相加就抵消。AI 生成的空间常常整段铺开，连低频也带着立体声残响，单声道一合就漏。低频波长长，左右不一致时抵消最明显，所以 120 Hz 以下通常应该居中。

## 具体做法

先把工程切到单声道听整首，再逐个 solo 找塌掉的轨。相位表长期偏左或偏右要查极性，宽度插件先在单声道里通过再用。低频与主唱放中间，宽度交给配器和声像，左右各摆一件真实的乐器比插件更稳。检查左右电平是否对称，主唱或主奏偏在一侧时，另一侧要有东西补回来，否则声场会歪。中侧均衡只做小幅调整，侧声道高频可以略提，中声道低频不要削。最后用一只音箱在房间另一头听，宽度消失后还清楚的，才是真的。

## 耳朵要抓的点

在坎比尼《第一木管五重奏》里，听五件管乐怎样靠声像与音色分开，这是编曲给的宽度。在 87 BPM 的嘻哈鼓组里，听底鼓与军鼓是否都在中间，单声道下不能塌。在萨蒂《裸体歌舞》第二首里，听稀疏织体在单声道下还剩下多少空间感。三处都在单声道里再听一遍。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","G3","B3","E4","B3","G3","E3","D3"],"label":"单声道检查","label_en":"The mono check","hint":"在单只音箱上听，宽度消失后剩下的才是实心","hint_en":"Listen on one speaker; what remains after the width disappears is the real body"}
```
:::

::: en
## Where it snags

AI material sounds wide, and on headphones it seems to have space. Sum it to mono and the vocal thins, the drums collapse to the centre, and half the pad disappears. Width is the easiest thing for a generator or a reverb to fake, and the first thing to vanish on a phone, a kitchen speaker or a club system. Make mono work before asking for width.

## How it runs

Real depth comes from arrival time, early reflections and high-frequency absorption, so sounds have a front-to-back position and a defined place. Panning only places a sound left or right, while depth comes from level and reflection; the two are not the same. Fake width comes from decorrelating the left and right channels; it reads as wide on headphones and cancels when summed. Generated space is often spread across the whole mix, with stereo reverb even in the low end, so the mono sum leaks. Long wavelengths cancel most easily, which is why everything below 120 Hz usually belongs in the centre.

## In practice

Switch the project to mono and listen through, then solo tracks to find the ones that collapse. A correlation meter that leans left or right calls for a polarity check, and any width plugin has to pass in mono before it stays. Keep bass and lead vocal centred, and get width from arrangement and panning, placing real instruments left and right rather than relying on a plugin. Check that left and right levels are symmetric; if the lead sits to one side, give the other side something to answer, or the field leans. Use mid-side EQ in small amounts, perhaps lifting the side highs, but never scooping the mid lows. Finish by listening on one speaker across the room; what stays clear after the width is gone is real.

## What the ear catches

In Cambini's Wind Quintet No. 1, hear how five winds separate through panning and timbre, which is width from arrangement. In the 87 BPM hip-hop groove, hear that kick and snare stay centred and do not collapse in mono. In Satie's Gymnopedie No. 2, hear how much space a sparse texture retains after summing. Listen to all three again in mono.

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","G3","B3","E4","B3","G3","E3","D3"],"label":"The mono check","label_en":"The mono check","hint":"Listen on one speaker; what remains after the width disappears is the real body","hint_en":"Listen on one speaker; what remains after the width disappears is the real body"}
```
:::
