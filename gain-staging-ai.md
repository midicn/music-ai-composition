---
id: gain-staging-ai
site: ai
cat: D
title: AI 分轨的增益结构
title_en: Gain Staging AI Stems
summary: 分轨电平不齐时先修峰值与响度，再动推子和插件
summary_en: When stem levels disagree, fix peaks and loudness before touching faders or plugins.
level: standard
tags: [增益结构, 分轨, 峰值, 响度]
tags_en: [gain staging, stems, peaks, loudness]
alias: [分轨增益, 电平结构, gain staging AI stems]
order: 140
links:
  - "[[glossary:gain-staging]]"
  - "[[glossary:headroom]]"
  - "[[glossary:stems]]"
instances:
  - groove-000000 | 138 BPM 放克鼓组，底鼓与军鼓的峰值差最能说明分轨电平不齐（C1）
  - musicnet-000090 | 贝多芬第十二四重奏，四把琴同时进来，分轨电平差会先毁掉声部层次（C1）
  - atepp-000239 | 肖斯塔科维奇第十号赋格，织体密，分轨叠加最容易顶穿总线（C1）
  - atepp-005385 | 拉威尔《绞刑架》，低音钟声与铺底争同一段电平余量（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer’s Handbook 与 Eargle, Handbook of Recording Engineering 中关于峰值、余量与响度的章节。
  - 分轨电平与总线余量的处理顺序，依据混音实践惯例。
updated: 2026-10-31
---

::: zh
## 分轨一进来电平就不齐

同一次生成导出的分轨，人声峰值到 +2 dBFS，铺底在 -20 dBFS，底鼓在 -4 dBFS。推子还没动，总线已经没有余量。这不是混音问题，是增益结构问题：每条轨带着自己的电平标准进来，先修这个，再谈平衡。

## 先峰值，后响度

峰值决定还有多少余量，响度决定推子该放哪里，两者混着调会来回改。先用片段增益把峰值压到 -6 dBFS 左右，鼓与贝斯留 6 dB 余量；再看短时响度，把同类素材放在相近的响度上。人声与主奏按峰值统一，不按响度统一，因为它们的瞬态差异大，按响度会把字头压掉。片段增益改的是素材本身，推子留给平衡，这样回头改平衡时不会破坏已经定好的电平。

## 检查表

- 每条分轨单独播，记录峰值与短时响度
- 峰值高于 -3 dBFS 的先做片段增益，不动推子
- 鼓与贝斯峰值统一到 -6 dBFS，留 6 dB 余量
- 人声与主奏按峰值统一，不按响度统一
- 铺底与效果轨比主奏低 6 到 10 dB
- 总线峰值不超过 -3 dBFS，进混音前不挂限制器
- 波形顶部已经平直的分轨，说明生成时已限幅，不要再压
- 记录每条的处理量，重生成后能照着复现

## 动过头的地方

把每条分轨都归一化到同一响度，看起来整齐，实际上把鼓的瞬态和铺底的起伏一起抹平了。已经带限幅的分轨再压一次，只会多一层失真。还有一类错误是在总线上先挂限制器求响，后面所有平衡判断都建立在被压扁的素材上。分轨阶段的响度只需要相对合理，绝对响度留到母带。

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["A2","A2","C3","E3","D3","C3","A2","G2"],"label":"一条需要留余量的贝斯","label_en":"A bass line that needs headroom","hint":"先听峰值是否贴顶，再听它与底鼓重叠时总线还有没有空间","hint_en":"Hear whether the peaks touch the ceiling, then whether the bus still has room where it meets the kick"}
```
:::

::: en
## Levels disagree before the first fader moves

Stems from one generation arrive with the vocal peaking at +2 dBFS, the pad at -20 dBFS and the kick at -4 dBFS. The bus has no headroom left and nothing has been mixed yet. This is not a mixing problem but a gain-structure problem: every track brings its own level reference, and that has to be fixed before balance is discussed.

## Peaks first, loudness second

Peaks decide how much headroom remains; loudness decides where the fader sits. Adjusting both at once means chasing your own changes. Use clip gain to bring peaks to roughly -6 dBFS, leaving 6 dB on drums and bass, then look at short-term loudness and place similar material at similar loudness. Vocals and leads should be matched by peak rather than loudness, because their transients differ widely and loudness matching shaves the attacks. Clip gain changes the source; faders stay for balance, so later balance moves do not undo the levels already set.

## Checklist

- Play each stem alone and log peak and short-term loudness
- Clip-gain anything peaking above -3 dBFS instead of pulling the fader
- Bring kick and bass peaks to -6 dBFS with 6 dB of headroom
- Match vocals and leads by peak, not by loudness
- Set pads and effect returns 6 to 10 dB below the lead
- Keep the bus below -3 dBFS and leave the limiter off before mixing
- Treat a flat-topped waveform as already limited and do not compress it again
- Write down the amount of every move so a regenerated stem can repeat it

## Where it goes too far

Normalising every stem to the same loudness looks tidy and flattens both the drum transients and the swells of the pad. Compressing an already limited stem only adds another layer of distortion. Another common mistake is putting a limiter on the bus to chase loudness first, after which every balance decision is made on squashed material. At the stem stage loudness only needs to be relatively sensible; absolute loudness belongs to mastering.

```audiolab
{"type":"instrument","gm":"Electric Bass (finger)","synth":"plucked","phrase":["A2","A2","C3","E3","D3","C3","A2","G2"],"label":"A bass line that needs headroom","label_en":"A bass line that needs headroom","hint":"Hear whether the peaks touch the ceiling, then whether the bus still has room where it meets the kick","hint_en":"Hear whether the peaks touch the ceiling, then whether the bus still has room where it meets the kick"}
```
:::
