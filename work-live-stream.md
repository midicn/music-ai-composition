---
id: "work-live-stream"
site: "ai"
cat: "K"
title: "直播配乐与音效"
title_en: "Music and SFX for Live Streams"
summary: "循环要能一直转，触发要短，版权要覆盖直播与回放"
summary_en: "Loops must run indefinitely, triggers stay short, and the licence must cover the feed and the replay."
level: "standard"
tags: ["直播", "循环", "触发", "版权"]
tags_en: ["live stream", "loops", "triggers", "licensing"]
alias: ["直播配乐", "直播音效", "stream music", "live stream audio"]
order: 266
tool_kind: "guide"
tool_vendor: "—"
tool_form: "案例"
tool_platforms: ["通用"]
tool_price: "不适用"
tool_jobs: ["直播音频", "循环制作", "音效触发"]
tool_verified: "2026-10-31"
links: ["[[glossary:sync-license]]", "[[glossary:music-copyright]]", "[[glossary:loudness-normalization]]"]
instances: []
sources: ["https://legal.twitch.com/en/legal/music/20233107/", "https://obsproject.com/kb/filters-guide"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "直播配乐涉及现场音源路由、闪避设置及直播和回放的许可范围，需在直播工程中测试；普通音乐播放不能证明直播路由或 VOD 使用权正确。"
---

::: zh
## 直播要的不是歌单

直播的音频是一套状态，不是一串歌。开播等待、正题、游戏、休息、结束，每个状态有自己的循环与音量。交给主播的是三到五条六十秒以上的无缝循环、六到十个三秒内的触发音、两套场景预设、一份离线备份与授权说明。直播与回放是两条授权线，平台会在 VOD 上做识别，直播时能放不等于回放能留。

## 循环、触发、留白

第一步列场景表，写清每个状态用哪条循环、哪些触发、主播说话时降多少。第二步做循环：整小节、零交叉、连续听二十遍，接缝不能有咔哒；循环里留出中频空洞，人声才放得下。第三步在 OBS 里建音频源，设好监听、压缩与闪避，触发音控制在三秒内，警报类音效单独一条轨道。

## 推流软件与音效板

循环在 Ableton Live 或 REAPER 里做，Suno 或 Udio 生成底稿，Demucs 只处理参考曲。OBS Studio 管场景与监听，Voicemeeter 或 BlackHole 做路由，音效板用 Elgato Stream Deck 或 Soundpad。iZotope RX 清口水音与底噪，Ozone 把循环统一到 -16 LUFS 左右，触发音再低 6 dB。

## 开播前十分钟的检查

| 场景 | 音频状态 | 触发 | 规则 |
|---|---|---|---|
| 等待 | 低密度循环 | 欢迎音 | 循环 -26 LUFS |
| 正题 | 无音乐或极轻垫 | 切段提示 | 说话时闪避 12 dB |
| 游戏 | 中密度循环 | 胜利、失败 | 触发不超过 3 秒 |
| 休息 | 单条循环 | 回来提示 | 不放版权歌曲 |
| 结束 | 收尾循环 | 感谢音 | 淡出 8 秒 |

监听耳机里听一遍，再用手机外放听一遍；两处都清楚才算过。录一段十分钟的测试 VOD，回放检查有没有被静音或替换。

## 版权与现场失灵

用个人订阅账号放歌，直播可能没事，回放会被静音或下架。触发音太长，盖住主播的第一句话。循环接缝在安静段落特别明显。警报音比人声高 15 dB，观众戴耳机被吓到。网络断了以后没有离线备份，整场只剩麦克风。
:::

::: en
## A stream is a set of states

Stream audio is a set of states, not a playlist. Waiting, the main segment, gameplay, a break and the close each need their own loop and level. The streamer receives three to five seamless loops of at least sixty seconds, six to ten triggers under three seconds, two scene presets, an offline backup and a licence note. Live and on-demand are separate rights; platforms scan VODs, so clearing a track for the broadcast does not keep it in the replay.

## Loops, triggers, room

Start with a scene table: which loop belongs to each state, which triggers, how far the music drops under speech. Then build the loops: whole bars, zero crossings, twenty consecutive passes without a click, and a hole in the mids for the voice. Finally set up sources in OBS with monitoring, compression and ducking, keep triggers under three seconds, and put alerts on their own track.

## OBS and a sound board

Build loops in Ableton Live or REAPER, sketch with Suno or Udio, and use Demucs only on references. OBS Studio handles scenes and monitoring, Voicemeeter or BlackHole handles routing, and an Elgato Stream Deck or Soundpad fires the triggers. iZotope RX cleans mouth noise and room tone, Ozone sets loops around -16 LUFS, and triggers sit 6 dB lower.

## Ten minutes before going live

| Scene | Audio state | Trigger | Rule |
|---|---|---|---|
| Waiting | Sparse loop | Welcome | Loop at -26 LUFS |
| Main | None or a light bed | Segment cue | Duck 12 dB under speech |
| Gameplay | Mid-density loop | Win, loss | Trigger under 3 s |
| Break | One loop | Return cue | No licensed songs |
| Close | Outro loop | Thanks | Fade over 8 s |

Check once on headphones and once on a phone speaker; it passes only when both are clear. Record a ten-minute test VOD and play it back to see whether anything was muted or replaced.

## Rights and on-air failures

A personal subscription plays fine live and gets muted or swapped in the replay. A trigger runs long and covers the streamer's first sentence. The loop seam is obvious in a quiet segment. An alert sits 15 dB above the voice and startles headphone listeners. The connection drops with no offline backup, and only the microphone is left.
:::

