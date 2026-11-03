---
id: "game-trailer-ai"
site: "ai"
cat: "F"
title: "游戏预告片音乐"
title_en: "Music for Game Trailers"
summary: "预告片按 hit point 写，三段式只是骨架，留白才是力气"
summary_en: "A trailer is built around hit points; the three-act shape is only the frame, and silence does the lifting."
level: "standard"
tags: ["游戏预告片", "落点", "三段式", "版本裁切"]
tags_en: ["game trailer", "hit points", "three-act", "version cuts"]
alias: ["预告片配乐", "trailer cue", "游戏预告"]
order: 151
links: ["[[glossary:cue]]", "[[glossary:sync-license]]", "[[glossary:tempo]]"]
instances: []
sources: ["https://www.ableton.com/en/manual/working-with-video/", "https://www.wipo.int/web-publications/rights-clearance-a-guide-for-independent-filmmakers/en/3-rights-assessed-during-clearance.html"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论游戏预告片的画面落点与音乐交付，需要对真实画面版本、时间线和使用权检查；普通MIDI试听没有影片同步或正式授权证据。"
---

::: zh
## 画面先定落点

游戏预告片的音乐不是先写一首史诗，再往上贴画面。剪辑师先给出几个必须响的点：logo 出现、角色转身、发售日弹出。音乐围着这几个点组织，其他部分都为它们让路。生成工具能给气势，给不了落点，落点要自己在 DAW 里对。

## 三段不是三首

九十秒的预告和长片一样按三幕走：建立、累积、爆发。区别在于每一段都很短，建立只有十几秒，累积靠加层而不是靠旋律发展，爆发往往只有一个主题完整出现一次。三段之间不是硬切，是用一次抽空或一次静音换气。把三段写成三首独立的曲子，接起来一定散。

## 时间轴

以九十秒为例，时间点按版本微调，职责不变。

| 时间 | 段落 | 音乐要做的 | 常见错误 |
|---|---|---|---|
| 0:00–0:15 | 建立 | 一个动机、一点环境声 | 一上来就满编制 |
| 0:15–0:45 | 累积 | 加层、加节奏、留半拍空 | 每四小节加一层，变成楼梯 |
| 0:45–1:00 | 转折 | 抽掉低频，或全部静音 | 静音太短，观众没反应过来 |
| 1:00–1:15 | 爆发 | 主题完整出现，落点对齐 logo | hit 落在画面之后 |
| 1:15–1:30 | 收尾 | 短尾、留混响、准备循环 | 尾巴拖进下一支片子 |

## 版本裁切

同一支预告片常有九十秒、六十秒、三十秒和十五秒几个版本，还有竖版和社媒前贴。做法不是把长版等比缩小，而是先保住 logo hit 和主题出现，再压掉建立段。三十秒版通常只剩一个累积加一个爆发，十五秒版只留爆发和收尾。每个版本单独导出，速度与调性保持一致，方便平台替换。交付时把 hit point 的时间码写进文件名或文档。

## 写满就失效

最容易坏的是把爆发写满。整段都是铜管和鼓，观众到 logo 时已经麻木，hit 不再 hit。第二个问题是 riser 用得太规矩，每次都是四小节上行，听两遍就能预测。第三个是静音不敢留，怕空，结果所有段落一样密。生成素材常带前奏和渐弱，剪的时候要切干净，不要让尾巴拖进下一个镜头。
:::

::: en
## Picture first, then music

A game trailer is not scored by writing an epic and laying it against the edit. The editor marks the moments that must land: the logo, the turn of a character, the release date. The music is organised around those points and everything else gets out of their way. A generation tool can supply scale but not placement; placement is done in the DAW against timecode.

## Three acts, not three songs

A ninety-second trailer follows the same three acts as a full trailer: establish, accumulate, release. The difference is compression. The setup lasts fifteen seconds or so, accumulation works by adding layers rather than developing melody, and the release usually states the theme in full exactly once. The acts are joined by a drop-out or a held silence, not by a hard cut. Write them as three separate pieces and the joins will show.

## Timeline

Ninety seconds is the example; timings shift with the cut, the jobs do not.

| Time | Section | What the music does | Common mistake |
|---|---|---|---|
| 0:00–0:15 | Establish | One motif, a little ambience | Full orchestra on the first frame |
| 0:15–0:45 | Accumulate | Add layers and pulse, leave half a beat open | One new layer every four bars, like stairs |
| 0:45–1:00 | Turn | Pull the low end, or go silent | Silence too brief to register |
| 1:00–1:15 | Release | State the theme, land on the logo | Hit arrives after the picture |
| 1:15–1:30 | Close | Short tail, leave reverb, prepare the loop | Tail bleeds into the next spot |

## Cutting versions

One trailer usually ships at ninety, sixty, thirty and fifteen seconds, plus a vertical cut and a social pre-roll. The method is not to scale the long version down but to protect the logo hit and the theme statement, then remove the setup. A thirty-second cut often keeps one accumulation and one release; fifteen seconds keeps the release and the close. Export each version separately with the same tempo and key so a platform can swap them. Put hit point timecodes in the file name or the delivery notes.

## When the release is already full

The usual failure is a release that is already full. If brass and drums run for the whole cut, the audience is numb by the logo and the hit stops hitting. The second fault is a riser that always climbs for four bars, predictable after one viewing. The third is fear of silence, which leaves every section equally dense. Generated material arrives with intros and fades, so cut them cleanly and keep tails out of the next shot.
:::

