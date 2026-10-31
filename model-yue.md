---
id: model-yue
site: ai
cat: I
title: YuE
title_en: YuE
summary: 歌词换整曲，能在本地跑，显存与许可是两道门。
summary_en: Lyrics in, a full song out, runnable locally; VRAM and licence are the gates.
level: standard
tags: [模型档案, 开源权重, 歌词生歌, 本地部署]
tags_en: [model profile, open weights, lyrics to song, local deployment]
alias: [YuE, 乐, 歌词生歌]
order: 200
model_vendor: YuE 项目（M-A-P / 中国香港科技大学）
model_form: 本地模型
model_input: [歌词, 文本]
model_output: [音频]
model_licence: 代码多为 Apache 2.0，权重按版本另标；较新权重默认非商用、个人创作者另有豁免，商用前读仓库许可
model_verified: 2026-10-31
links:
  - "[[glossary:strophic-form]]"
  - "[[glossary:timbre]]"
  - "[[glossary:stems]]"
instances:
  - mutopia-000527 | 六十三秒的分节歌《Home, Sweet Home》，主歌反复，适合看长曲的段落回归（C1） | A sixty-three second strophic song, "Home, Sweet Home", with repeated verses, to hear sections return in a long song (C1)
  - cyberhymnal-002209 | 十八秒的中国旋律，短而完整，适合看极短素材的收束（C1） | An eighteen second Chinese melody, short but complete, to hear how a very short asset closes (C1)
  - mutopia-000622 | 四十四秒的分节歌，看主歌反复时旋律怎么变（C1） | A forty-four second strophic song, to hear how the tune changes across verses (C1)
  - cyberhymnal-003336 | 中文歌词的短赞美诗，看声调与旋律的配合（C1） | A short hymn with Chinese words, to hear tones meeting melody (C1)
sources:
  - YuE 项目仓库与模型卡（M-A-P / 中国香港科技大学）关于输入形式、显存建议与权重许可的说明。
  - YuE 技术报告对长曲生成与歌词对齐的公开描述。
  - 公开用户报告中的显存、速度与咬字问题，只取现象，不引用具体评测分数。
updated: 2026-10-31
---

::: zh
## 先算显存，再谈创作

YuE 是少数能把整首歌唱完的开放权重模型：给歌词和风格，它直接出人声加伴奏，长度到几分钟。它不适合当网页工具用，装好环境、下载权重、备一张够大的显卡，才算进场。官方与打包环境常给 24GB 显存的建议；量化版和社区推理栈能压到 8–12GB，代价是速度与稳定性。先确认这一步，再谈歌好不好听。

## 歌词怎么进去

输入是分行写的歌词，加上风格描述；主歌、副歌、桥段这类段标记可以写在歌词里。输出是混好的立体声，有的推理脚本会把伴奏与人声分别写出。它不提供“一句提示马上出歌”的即时反馈：一首三分钟的歌，在消费级显卡上通常要几十秒到几分钟，试错成本按分钟算。较新的版本会先把旋律与和弦落成可读的谱面，再渲染音频，改起来比纯黑箱方便。

## 长曲的连贯性是卖点

多数开源模型只能做几十秒的片段，YuE 的价值在整曲：主歌到副歌的抬升、桥段后的回归、尾奏的收束，能在同一次生成里完成。中文歌是它的强项之一，五声调式、字少腔长的句子，比英文快嘴更容易站住。做方言或古风 demo 时，它能给出一版结构完整的参照，再拿去做编曲或找人重唱。

## 三道坎：显存、咬字、重复

- 显存与速度：24GB 是舒服的线，低于 12GB 要靠量化，长歌容易中途崩。
- 咬字：中文声调在快句、叠字和高音区容易糊，逐句对歌词听，别只看波形。
- 重复：三分钟以后常回到前面的旋律与配器，第二次副歌最明显。
- 分轨：若用分别写出人声与伴奏的脚本，人声轨常带混响与残渣，重混前要修。

先拿一首短歌试，别一上来就做五分钟。

## 许可分层与替代

许可要分三层看：代码、权重、随附模型。早期版本以 Apache 2.0 放出，较新的权重默认非商用，个人创作者有豁免，公司商用要单独授权；具体以仓库里的许可文件为准。替代：要网页即开即用，换 Suno 或 MiniMax Music；要更快的本地整曲，换 DiffRhythm；要符号级可控，换 Magenta。三者都可能牺牲中文咬字或整曲连贯，按任务取舍。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["G4","A4","C5","A4","G4","E4","D4","E4"],"label":"一句五声音阶的歌词落点","label_en":"A pentatonic line for setting words","hint":"先让旋律站住，再看每个字落在哪一拍、哪个音","hint_en":"Let the melody stand first, then check which beat and pitch each word lands on"}
```
:::

::: en
## Count the VRAM first

YuE is one of the few open-weight models that finishes a whole song: give it lyrics and a style and it returns vocals plus backing, several minutes long. It is not a browser tool; you install an environment, download weights and bring a large enough GPU before anything starts. Official and packaged setups often recommend 24GB of VRAM; quantised builds and community inference stacks can squeeze into 8–12GB at the cost of speed and stability. Settle that before judging the music.

## How the lyrics get in

Input is line-broken lyrics plus a style description; verse, chorus and bridge tags can sit inside the lyric text. Output is a mixed stereo file, and some inference scripts write the backing and vocal separately. There is no instant one-line-to-song loop: a three-minute song usually takes tens of seconds to a few minutes on a consumer GPU, so experiments are measured in minutes. Newer builds first lay out melody and chords as a readable score plan, then render audio, which is easier to revise than a pure black box.

## Long-form coherence is the point

Most open models manage a few dozen seconds; YuE's value is the whole song, with the lift into the chorus, the return after the bridge and the closing all in one pass. Chinese songs are a strength: pentatonic lines and sparse, long-held syllables hold up better than rapid English verses. For a dialect or guofeng demo it gives a structurally complete reference that you can arrange or hand to a singer.

## Three walls: VRAM, diction, repetition

- VRAM and speed: 24GB is the comfortable line; under 12GB means quantisation and a higher chance of a long song collapsing.
- Diction: Mandarin tones blur on fast lines, stacked syllables and high notes. Check line by line against the lyric, not just the waveform.
- Repetition: past three minutes it often returns to earlier melody and orchestration, most audible in the second chorus.
- Stems: if a script writes vocals and backing separately, the vocal track carries reverb tails and residue and needs repair before remixing.

Start with a short song; do not open with five minutes.

## Licence layers and alternatives

Read three layers: code, weights and companion models. Early releases were Apache 2.0; newer weights default to non-commercial with an exemption for individual creators, and companies need a separate licence. The repository licence file is the authority. Alternatives: Suno or MiniMax Music for a browser service; DiffRhythm for faster local full songs; Magenta for symbolic control. Each may cost you Mandarin diction or whole-song coherence, so choose by the job.
:::
