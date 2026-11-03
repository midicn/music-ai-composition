---
id: "vocal-pronunciation-checksheet"
site: "ai"
cat: "E"
level: "standard"
order: 207
tags: ["制作流程", "工作表"]
tags_en: ["production", "worksheet"]
alias: ["AI歌声校对表：逐句检查咬字与换气", "AI Vocal Pronunciation Checksheet"]
title: "AI歌声校对表：逐句检查咬字与换气"
title_en: "AI Vocal Pronunciation Checksheet"
summary: "把歌词、音节、音符和问题时间点对应起来，再检查修改后的完整乐句。"
summary_en: "Align lyrics, syllables, notes and problem timestamps, then recheck the complete phrase."
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
sources: ["https://docs.acestudio.ai/ai-vocal-synth/creating-ai-vocals/vocal-parameters", "https://docs.acestudio.ai/project/file-management/export-files"]
---

::: zh
## 把问题记到词和音符上

先确认所用歌声工具支持哪些歌词、音素、音符或表现参数。不同产品的音素系统与语言支持不同，不能把一个产品的拼写直接当成通用输入。真实声音或参考录音的使用范围在上传前确认，并与项目素材记录放在一起。

| 句子与位置 | 问题 | 修改候选 | 回听检查 |
|---|---|---|---|
| 第2句、00:12附近 | 虚拟例：“归”字尾部模糊 | 查看音节与音符是否对应，按工具规则调整 | 元音是否稳定，辅音是否清楚 |
| 长句末尾 | 换气位置影响语义 | 在乐句边界安排停顿或调整时值 | 是否破坏连贯与拍点 |
| 高音或连音 | 咬字与旋律衔接生硬 | 分别试音符长度、音素与表现参数 | 先独听，再放回伴奏 |

这些是自拟排查案例，不是任何音色的测试结果。一次先改一个主要问题，并保存前一版本；不要用“全部更自然”代替具体修改单。

## 修改顺序

先检查歌词是否输错，再检查音符与音节的对应，之后处理句内时值、辅音和换气，最后调表现参数。短片段听清后，把前后乐句也一起播放；单个字清楚却破坏整句节奏，仍需回退。实际歌唱要结合语言、旋律和演唱风格判断，工作表不能替代所有演唱决策。

## 导出时保留可比较版本

若工具支持，分别保存带效果参考和不带人声效果的编辑版，并记录实际导出范围。导回工程后检查共同起点与尾音，再与伴奏合听。分离出来的人声不应标成原始干声；没有音符级数据时，也不要把音频文件描述为可逐音编辑的工程。
:::

::: en
## Locate the word and note

Check which lyric, phoneme, note and expression controls the chosen singing tool provides. Phoneme systems and language support differ, so spelling accepted by one product is not a universal input. Confirm the permitted use of a real voice or reference recording before uploading it, and retain that record with the assets.

| Phrase and position | Problem | Candidate revision | Recheck |
|---|---|---|---|
| Phrase 2, around 00:12 | Fictional example: an unclear final syllable | Check syllable-to-note alignment and supported phoneme edits | Stable vowel and clear consonant |
| End of a long line | Breath interrupts the meaning | Move the pause to a phrase boundary or revise duration | Continuity and timing |
| High or connected notes | Abrupt articulation | Test note duration, phoneme and expression separately | Solo, then with accompaniment |

These are invented troubleshooting examples, not tests of a particular voice. Change one main issue at a time and retain the previous version. “Make everything natural” is not a precise revision request.

## A useful revision order

Correct lyric entry, check syllable alignment, adjust local timing and articulation, then work on expression. After testing the short section, play surrounding phrases. A clear word that disrupts the musical line may still need reverting. Language, melody and style remain part of the judgement.

## Preserve comparable exports

Where supported, save an effected reference and an editing version without vocal effects, recording their actual export range. Import them at the same origin, check tails and audition with accompaniment. A separated vocal is not necessarily an original dry track, and an audio file without note data is not a note-editable project.
:::
