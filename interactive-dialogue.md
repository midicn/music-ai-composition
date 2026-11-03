---
id: "interactive-dialogue"
site: "ai"
cat: "F"
title: "互动对白与音乐"
title_en: "Interactive Dialogue and Music"
summary: "对白在说，音乐就得让；状态切换要落在设计好的接缝上"
summary_en: "When dialogue speaks, music yields; state changes must land on seams you designed."
level: "standard"
tags: ["互动对白", "ducking", "状态切换", "游戏音频"]
tags_en: ["interactive dialogue", "ducking", "state changes", "game audio"]
alias: ["对白优先", "动态混音", "dialogue ducking"]
order: 156
links: ["[[glossary:stems]]", "[[glossary:loudness-normalization]]", "[[glossary:cue]]"]
instances: []
sources: ["https://www.fmod.com/docs/2.04/studio/authoring-events.html", "https://www.ableton.com/en/manual/live-audio-effect-reference/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论对白触发与音乐让位，需要在实际事件、路由和侧链处理中检查响应；无对白轨的固定MIDI不能证明ducking或状态切换正确。"
---

::: zh
## 对白优先是硬规则

玩家在听台词时，音乐只有一个任务：别挡路。人声的可懂区在一千到四千赫兹，音乐里最抓耳的也是这一段，两边一撞，词就糊了。做法不是把音乐整体拧小，而是先把中频让出来，再决定整体降多少。对白优先意味着音乐可以难听一点，台词必须清楚。

## ducking 不是拧小

侧链压缩能让音乐在对白出现时自动退，但退多少、多快、多久回来，都要设。退得太少没用，退得太多像有人拧旋钮，回来太快会抽气。常见做法是退六到九分贝，启动几十毫秒，释放半秒到一秒，并且只对一个中频段做，保留低频和空气感。旁白、喊话、无线电语音要分开设，无线电本身带宽窄，音乐退得可以少一些。

## 状态表

电平与时间按项目调，职责和切换方式先定下来。

| 状态 | 音乐 | 对白 | 切换方式 |
|---|---|---|---|
| 探索 | 环境层加稀疏动机 | 无 | 淡入二到四秒 |
| 对话 | 只留低频与和声垫 | 主 | 三百到五百毫秒内退六到九分贝 |
| 战斗 | 节奏层加主题 | 喊话 | 小节线切，保留一层不断 |
| 过场 | 完整 cue | 优先 | 预渲染，按时间码走 |
| 菜单 | 循环，无打击 | 无 | 交叉淡化 |

## 切换的接缝

状态切换最怕两件事：拍点对不上，尾巴拖进下一个状态。所有状态共享速度和调性，切换点落在小节线；做不到就预留一层不断的声音，把接缝盖住。对白开始前留半拍，让玩家有反应时间；对白结束后不要立刻把音乐推满，等一到两秒。过场用预渲染的 cue，按时间码走，不要交给实时系统即兴。

## 常见坏法

把 ducking 挂在对白总线上，音乐会被音效一起触发，战斗时忽大忽小。用生成音乐直接进引擎，往往没有干净的分轨，没法只留一层。台词密集的段落，音乐写得再好在混音里也听不见，不如写成稀疏的垫子。还有，别用音乐盖住语音压缩的瑕疵，那会把问题留到玩家耳机里。
:::

::: en
## Dialogue comes first

While a player listens to a line, the music has one job: stay out of the way. Speech is understood in roughly the one to four kilohertz region, which is also where music is most attention-grabbing, so the two collide and the words blur. The fix is not to turn the whole cue down but to clear the midrange first and then decide how much overall reduction is needed. Dialogue first means the music may sound worse; the line must stay clear.

## Ducking is not a volume knob

Sidechain compression can pull music down when dialogue appears, but depth, attack and release all need setting. Too little does nothing, too much sounds like someone turning a knob, and a fast release pumps. A common approach ducks six to nine decibels, attacks within tens of milliseconds and releases over half a second to a second, and touches only a midrange band so the low end and air survive. Narration, shouted lines and radio chatter need separate settings; radio is narrow-band, so the music can stay higher.

## States

Levels and timings follow the project; the job and the transition should be fixed first.

| State | Music | Dialogue | Transition |
|---|---|---|---|
| Exploration | Ambience plus sparse motif | None | Fade in over two to four seconds |
| Conversation | Low end and harmonic pad only | Primary | Duck six to nine decibels within three to five hundred milliseconds |
| Combat | Rhythmic layer plus theme | Shouts | Cut on a bar line, keep one layer running |
| Cinematic | Full cue | Primary | Prerendered, follows timecode |
| Menu | Loop without percussion | None | Crossfade |

## The seam

Two things break a state change: a mismatched beat and a tail that bleeds into the next state. Every state shares tempo and key, and the switch lands on a bar line; if that is impossible, keep one continuous layer running across the join. Leave half a beat before dialogue starts so the player can react, and do not push the music back to full the instant the line ends; wait a second or two. Use a prerendered cue for cinematics and follow timecode instead of letting a real-time system improvise.

## Common failures

Put ducking on the dialogue bus and sound effects will trigger it too, so the music jumps during combat. Generated music dropped straight into an engine often lacks clean stems, so there is no way to keep just one layer. In dialogue-heavy scenes, no music survives the mix, so write a sparse bed instead of a full cue. And never use music to hide artefacts in compressed speech; that only moves the problem into the player's headphones.
:::

