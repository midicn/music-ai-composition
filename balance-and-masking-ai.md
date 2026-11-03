---
id: "balance-and-masking-ai"
site: "ai"
cat: "D"
title: "平衡与遮蔽"
title_en: "Balance and Masking"
summary: "生成的声部先抢频段，再谈均衡，顺序反了只会越修越薄"
summary_en: "Generated parts fight over the same register first, so fix register and density before reaching for EQ."
level: "standard"
tags: ["平衡", "遮蔽", "音区", "编曲密度"]
tags_en: ["balance", "masking", "register", "density"]
alias: ["遮蔽", "声部打架", "balance and masking"]
order: 2
links: ["[[glossary:eq]]", "[[glossary:register]]", "[[glossary:mix-bus]]"]
instances: []
sources: ["https://www.ableton.com/en/manual/mixing/", "https://www.ableton.com/en/manual/live-audio-effect-reference/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论轨间平衡和频段遮蔽，需要在实际混音中检查声部及处理链；固定独奏或曲库MIDI不能证明多轨遮蔽诊断或均衡前后效果。"
---

::: zh
## 难在哪

AI 编曲最常见的毛病不是音色差，是声部挤在一起。铺底、吉他、人声、合成器都站在 200 Hz 到 4 kHz 这一段，谁都想被听见，结果谁都不清楚。多数人的第一反应是打开均衡，给每轨切一刀。切完整体变薄，问题还在，只是换了个位置。

## 它怎么工作

遮蔽发生在音区与时间重叠的地方，不只在频响上。两个声部占同一段音域、同一拍点起音，弱的那个就被掩住。生成的编曲按风格统计堆叠素材，容易在同一声部加层，密度上去，空隙没有。均衡只能改变已有能量的分布，补不回编曲里不存在的空位。先用八度、删层和时间错开解决重叠，再动均衡，效率高得多。

## 具体做法

先列一张声部表，写清每件乐器占据的音区与出现的段落。同一段里超过三件乐器落在中音区，就移走一件，向上或向下一个八度，或者干脆删掉。然后错开起音，让铺底比人声晚十几毫秒进入，或把和弦音缩短，留出字与字之间的缝。音量平衡在这一步做完，推子能解决六成的遮蔽。均衡只做窄切，200 到 500 Hz 的堆积切 2 到 3 dB，2 到 4 kHz 的人声区让给人声。需要更强的分离时用侧链，让铺底在人声出现时退 1 到 2 dB。最后在单声道里复查一遍。
:::

::: en
## Where it gets hard

The usual fault in an AI arrangement is not bad tone but crowded parts. Pad, guitar, vocal and synth all sit between 200 Hz and 4 kHz, each asking to be heard, so none is clear. The first instinct is to open an EQ and cut every track. The mix gets thinner, the problem stays, only its address changes.

## How it works

Masking happens where register and timing overlap, not only in the frequency response. When two parts share a range and start on the same beat, the weaker one disappears. Generated arrangements stack material by style statistics, so layers accumulate in the same register and no gaps are left. EQ can redistribute energy that exists; it cannot restore space the arrangement never had. Solve overlap with octaves, deleted layers and offset attacks before touching EQ.

## In practice

Write a part map first, listing the register each instrument occupies and the sections where it plays. If more than three parts sit in the midrange at once, move one up or down an octave, or delete it. Offset the attacks next, letting the pad enter a few milliseconds after the vocal, or shortening chord notes to leave gaps between words. Do the level balance here, since faders solve most masking. Use EQ only for narrow cuts, 2 to 3 dB out of a 200 to 500 Hz pile-up, and hand the 2 to 4 kHz presence range to the vocal. For stronger separation, sidechain the pad down 1 to 2 dB while the voice is in. Check the result in mono.
:::

