---
id: model-netease-tianyin
site: ai
cat: I
title: 网易天音
title_en: NetEase Tianyin
summary: 作词、编曲、演唱分三段做，中文初稿快，成品要自己收。
summary_en: Lyrics, arrangement and singing in three stages; fast Chinese drafts, finish them yourself.
level: standard
tags: [模型档案, 中文歌曲, 作词, 编曲]
tags_en: [model profile, Chinese songs, lyric writing, arrangement]
alias: [天音, 网易天音, 天音 AI 写歌]
order: 204
model_vendor: 网易（网易云音乐）
model_form: 网页服务
model_input: [文本, 歌词, 参考音频]
model_output: [音频, 分轨]
model_licence: 词曲编唱的产出归属、商用与发行按网易天音与网易云音乐的服务条款；活动规则与付费档会变
model_verified: 2026-10-31
links:
  - "[[glossary:strophic-form]]"
  - "[[instrument:zheng]]"
  - "[[glossary:mechanical-license]]"
instances:
  - cyberhymnal-003336 | 中文歌词的短赞美诗，看声调与旋律的贴合（C1） | A short hymn with Chinese words, to hear tones fitting the melody (C1)
  - cyberhymnal-002209 | 十八秒的中国旋律，看一句里的字怎么排密（C1） | An eighteen second Chinese melody, to hear how syllables are packed into a line (C1)
  - mutopia-000782 | 九十九秒的艺术歌曲，长句多，适合看换气与句尾（C1） | A ninety-nine second art song with long phrases, to hear breath and line endings (C1)
  - mutopia-000527 | 六十三秒的分节歌，段落完整，适合对照编曲模板（C1） | A sixty-three second strophic song with complete sections, to compare arrangement templates (C1)
sources:
  - 网易天音官方产品页与网易云音乐创作入口（作词、编曲、演唱与导出）。
  - 网易天音公开更新说明中的一键写歌、词曲协同与发行入口。
  - 网易云音乐服务条款与 AI 创作活动规则（产出使用与商用）。
updated: 2026-10-31
---

::: zh
## 作词、编曲、演唱分三段

天音把写歌拆成三个工作区：AI 作词按主题与词格给候选，AI 编曲按风格出伴奏，AI 演唱把词与旋律合成人声。也可以一键从主题出整首初稿，再回到三个工作区改。它面向的是没有乐理基础的人，界面把和弦、配器等术语藏起来，代价是精细控制少。想改一个鼓的过门或一句和声，通常要导出到 DAW 再做。

## 从主题到初稿

输入可以是一句主题、一段随笔、几行歌词，或者一段参考音频；输出是带人声的立体声，部分版本与档位支持分轨导出。生成后能改词、改旋律、换声线、调混响。它的强项是把想法变成能听的 demo，不是把 demo 变成发行级母带。初稿出来以后，编曲的层次、鼓的律动、人声的呼吸，仍要自己补。

| 环节 | 能改的 | 交付时注意 |
|---|---|---|
| 作词 | 主题、词格、段落 | 声调与重音 |
| 编曲 | 风格、乐器、速度 | 低频与鼓的密度 |
| 演唱 | 声线、情绪、混响 | 咬字与换气 |
| 导出 | 混音、部分分轨 | 格式与采样率 |

## 中文词的口语感

天音在常见流行句上的中文咬字比较自然，轻声、儿化、句尾虚词接近口语；但声调仍会被旋律拉着走，一句里连续的高平调容易唱成念经。写词时把重音放在强拍，把长音留给开口音，结果会稳很多。古风、民谣、短视频配乐是它常见的用法，平台内的词库与模板也偏这些方向。

## 模板化与导出

编曲模板多，出活快，也容易听出“同一个伴奏换旋律”。分轨导出与音轨合并的权限按版本与档位不同，工程文件不一定能带走；换平台或进 DAW 重混，常要重新对齐。人声音色可选，但跨次生成的一致性一般，拼两句就可能像换人。一键发行省事，发行前的署名、AI 标识与版权信息仍要自己填。

## 发行前要问的事

要确认：AI 生成标识、词曲版权归属、能否发行到流媒体、分轨的商用范围、活动期间的额外授权。具体以网易天音与网易云音乐的服务条款为准。替代：要中文整曲与 API，换 MiniMax Music；要分轨与平台发行，换腾讯音乐天琴；要本地可控，换 YuE 或 DiffRhythm。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["A4","C5","D5","C5","A4","G4","A4","E4"],"label":"一句带声调起伏的旋律","label_en":"A line with room for tonal movement","hint":"听每个字的音高走向，是否像说话，而不是一个字一个平音","hint_en":"Hear whether each syllable moves like speech instead of sitting on one flat pitch"}
```
:::

::: en
## Lyrics, arrangement and singing in three stages

Tianyin splits songwriting into three work areas: lyric assistance proposes lines from a theme and a syllable pattern, arrangement builds a backing from a style, and singing synthesises words and melody into a voice. You can also generate a whole draft from a theme and return to the three areas to revise. It targets people without theory training, so chords and arrangement terms stay hidden, at the cost of fine control. Changing a drum fill or one harmony usually means exporting to a DAW.

## From a theme to a draft

Input can be a theme line, a short note, a few lyric lines or a reference clip; output is stereo with vocals, and some versions and tiers export stems. After generation you can rewrite words, adjust melody, swap voices and change reverb. Its strength is turning an idea into a listenable demo, not turning a demo into a release master. Arrangement depth, drum groove and vocal breath still need your work.

| Stage | What you can change | Check before delivery |
|---|---|---|
| Lyrics | Theme, syllable pattern, sections | Tones and stresses |
| Arrangement | Style, instruments, tempo | Low end and drum density |
| Singing | Voice, mood, reverb | Diction and breath |
| Export | Mix, some stems | Format and sample rate |

## Spoken naturalness in Chinese

Tianyin's Mandarin diction is natural on common pop lines; light tones, erhua and sentence-final particles sit close to speech. Tones still get pulled by the melody, and a run of high level tones can turn into chanting. Put stressed syllables on strong beats and long notes on open vowels and the result steadies. Guofeng, folk and short-video beds are its common uses, and the platform's word bank and templates lean that way.

## Templates and export

There are plenty of arrangement templates, which is fast but makes it easy to hear the same backing with a different tune. Stem export and track merging depend on version and tier, and the project file may not come with you; moving to another platform or into a DAW often means realigning. Voices are selectable but consistency across runs is modest, so two stitched lines can sound like two singers. One-click release saves steps, but credits, AI disclosure and rights data are still yours to fill in.

## Questions before release

Confirm: AI disclosure, ownership of words and music, whether streaming release is allowed, the commercial scope of stems, and any extra terms attached to campaigns. The current NetEase Tianyin and NetEase Cloud Music terms are the authority. Alternatives: MiniMax Music for stronger Mandarin full songs and an API; TME Tianqin for stems and platform release; YuE or DiffRhythm for local control.
:::
