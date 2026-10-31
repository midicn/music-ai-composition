---
id: reference-vs-description
site: ai
cat: B
title: 参考音频与文字的分工
title_en: Reference Audio vs Description
summary: 参考音频锁音色，文字锁结构；冲突时先保结构再调音色。
summary_en: Reference audio fixes timbre; words fix structure. When they conflict, protect structure first.
level: standard
tags: [参考音频, 提示词, 音色, 结构]
tags_en: [reference audio, prompting, timbre, structure]
alias: [参考与描述, 音频条件, reference vs text]
order: 133
links:
  - "[[glossary:reference-track]]"
  - "[[glossary:timbre]]"
  - "[[glossary:texture]]"
instances:
  - pdmx-000206 | 探戈改编，旋律与伴奏层次清楚，适合看参考能否保住声部关系（C1）
  - pdmx-000135 | 小编制歌曲，混响多，参考音频容易把空间感一起带过来（C1）
  - pdmx-000107 | 手风琴与弦乐舞曲，中频拥挤，文字与参考谁定配器（C1）
  - mutopia-001682 | 绿袖子单旋律，装饰与分句只能靠参考或演奏，文字写不出来（C1）
sources:
  - Copet et al., MusicGen（Meta AudioCraft, 2023）与 Stability AI 的音频条件生成技术说明。
  - 录音制作教材中关于音色、空间与演奏细节的描述方法。
  - 影视配乐沟通惯例，关于参考曲目在 Brief 中的角色。
updated: 2026-10-31
---

::: zh
## 参考音频不是万能钥匙

给一段参考，模型会连它的混响、演奏习惯和年代感一起带走，却未必听你的段落安排。参考与文字各管一半：前者擅长音色与质感，后者擅长结构与事件。把它们当同一种控制手段，结果就会互相拆台。

## 谁锁什么

| 维度 | 参考音频 | 文字描述 | 建议 |
|---|---|---|---|
| 音色 | 强 | 弱到中 | 用参考定音色 |
| 空间与混响 | 强，常被一起带走 | 中 | 需要干声就明说 |
| 律动 | 中 | 中 | 两者都给，接受近似 |
| 配器 | 中 | 强 | 用文字列编制 |
| 结构 | 弱 | 强 | 用段落标记与时长 |
| 调性与和声 | 弱到中 | 强 | 精确要求写文字 |
| 歌词与咬字 | 弱 | 强 | 只能靠文字 |

## 冲突时谁优先

| 冲突类型 | 先保 | 处理 |
|---|---|---|
| 段落数与时长 | 文字 | 裁参考或分段生成 |
| 主奏音色 | 参考 | 文字只写编制，不堆音色形容词 |
| 速度与调性 | 文字，若属硬需求 | 生成后在 DAW 对齐 |
| 混响与空间 | 参考 | 要干声就单独要求，或后期去混响 |
| 歌词与咬字 | 文字 | 参考无法提供语言控制 |

结构是交付的骨架，所以段落、时长、歌词优先；音色是表面，可以后期替换或再生成。速度与调性介于两者之间，看它是不是合同里的硬指标。

## 两种输入怎么配合

只有参考，适合找质感、做临时轨，结构要后期剪。只有文字，适合结构清楚的定制，音色靠形容词碰运气。两者都给，文字写骨架与排除项，参考只负责音色，并在提示里写明“参考仅用于音色”。这句限定能减少模型把参考的段落也照搬。把参考裁到八到十五秒的单段，通常比整首更听话。

## 锁不住的部分

演奏的微观时间、真实房间、歌手的即兴处理，参考和文字都锁不住。这些要么请人演奏，要么接受生成结果再修。参考是风格锚点，不是验收标准；验收要回到段落表、时长和歌词逐项核对。
```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["G3","B3","D4","G4"],"label":"参考锁音色，文字锁结构","label_en":"Reference for timbre, text for form","hint":"两者冲突时，先保结构","hint_en":"When they conflict, keep the form"}
```

:::

::: en
## A reference is not a master key

Give a model a reference and it brings the reverb, playing habits and era along with the tone, while ignoring your section plan. Reference and text split the job: the first owns timbre and surface, the second owns structure and events. Treat them as one control and they undermine each other.

## Who fixes what

| Dimension | Reference audio | Text | Practice |
|---|---|---|---|
| Timbre | Strong | Weak to moderate | Fix tone with the reference |
| Space and reverb | Strong, often carried over | Moderate | Ask for dry if you need dry |
| Groove | Moderate | Moderate | Supply both and accept approximation |
| Instrumentation | Moderate | Strong | List the ensemble in words |
| Structure | Weak | Strong | Use section tags and duration |
| Key and harmony | Weak to moderate | Strong | Put exact requirements in text |
| Lyrics and diction | Weak | Strong | Text only |

## Who wins in a conflict

| Conflict | Protect first | Move |
|---|---|---|
| Section count and duration | Text | Trim the reference or generate in parts |
| Lead timbre | Reference | Describe the ensemble, not a pile of tone adjectives |
| Tempo and key | Text, if contractual | Align in the DAW after generation |
| Reverb and space | Reference | Ask for dry separately or remove reverb later |
| Lyrics and diction | Text | A reference cannot control language |

Structure is the delivery skeleton, so sections, duration and lyrics come first; timbre is surface and can be replaced or regenerated. Tempo and key sit between the two, depending on whether they are hard requirements.

## Combining the two inputs

Reference alone suits texture hunting and temp tracks; structure is cut later. Text alone suits a clearly specified form, with timbre left to adjectives and luck. With both, let text carry skeleton and exclusions, let the reference carry tone only, and state "reference for timbre only" in the prompt. That sentence stops the model from copying the reference's sections too. A single eight-to-fifteen-second excerpt usually obeys better than a whole track.

## What neither can fix

Micro-timing, a real room and a singer's improvised delivery escape both controls. Hire a player or accept the generation and repair it. A reference is an anchor for style, not an acceptance test; acceptance returns to the section sheet, duration and lyric check.
:::
