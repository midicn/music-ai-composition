---
id: "synthetic-vocals"
site: "ai"
cat: "E"
title: "合成人声"
title_en: "Synthetic Vocals"
summary: "合成人声擅长小样、和声垫和你录不到的语言，长音与情绪仍会露馅"
summary_en: "Synthetic singing handles demos, backing and languages you cannot record; long notes and emotion still give it away."
level: "standard"
tags: ["合成人声", "小样", "和声", "多语言"]
tags_en: ["synthetic vocals", "demo", "backing vocals", "multilingual"]
alias: ["合成歌声", "AI 演唱", "synthetic vocals"]
order: 1
links: ["[[glossary:timbre]]", "[[instrument:voice]]", "[[glossary:vibrato]]"]
instances: []
sources: ["https://sv1.docs.dreamtonics.com/en/synthv/advanced-usage/note-properties", "https://sv1.docs.dreamtonics.com/en/synthv/basic-usage/pianoroll"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "合成人声要核对音符、音素时序、音高和表情参数之间的映射；普通器乐或现成歌声播放不能证明合成引擎的输入方式和可编辑程度。"
---

::: zh
## 容易停住的地方

合成人声是用模型直接唱出旋律和歌词，不是把你的录音变调。它已经能唱准音、念对词，适合三种活，给别人试听的小样、垫在真人后面的和声、以及你找不到人录的语言。它不会累，能唱你写不出的高音，也不占录音棚时间。它不适合直接当正式发行的主唱，除非听众事先知道那是合成的。

## 背后的机制

系统把音高、时长和音素分开处理。歌词转成音素，旋律给出音高与长短，音色来自录好的样本或训练出的声学模型。分开控制的好处是改词、改调、改速度都便宜；坏处是“怎么唱”必须有人做决定，哪里换气、哪个字加重、长音怎么收。你不决定，模型就给你一个平均值。音素切得越细，能改的地方越多，连贯性也越难保。

## 怎么调整

先定用途再动手。小样可以整段合成，正式版把主唱换成真人，只留合成和声。写旋律时给换气留位置，一句不超过八到十个音节，音域别超过一个八度半。长音在 MIDI 里做渐弱，再叠一层很轻的呼吸噪声。外语找母语者听一遍重音和连读。给合成声部单独建一条轨，方便随时换掉。混音时把合成人声收窄一点，二到五千赫兹留出空间给真人或对白。
:::

::: en
## Where people stall

Synthetic singing means a model performs the melody and the words, not that your own recording is shifted. It holds pitch and pronounces text well enough for three jobs: a demo someone else will sing, a backing layer under a real voice, and a language you cannot cast. It is a poor choice for the lead on a release unless listeners know the voice is synthetic.

## The mechanism

The system separates pitch, duration and phonemes. Lyrics become phonemes, the melody supplies pitch and length, and timbre comes from recorded samples or a trained acoustic model. Separate control makes changing words, key or tempo cheap. It also means someone must decide how the line is sung: where to breathe, which syllable to weight, how a long note ends. If nobody decides, the model returns an average of those choices.

## How to adjust

Decide the use first. A demo can be fully synthetic. On a release, replace the lead with a singer and keep the synthetic part as backing. Leave room for breaths when writing the melody, keep phrases under eight to ten syllables, and keep the range inside an octave and a half. Fade long notes in the MIDI and add a very low breath layer. Have a native speaker check stress and liaison in a foreign language. In the mix, narrow the synthetic voice slightly and clear space around 2 to 5 kHz for the real voice or dialogue.
:::

