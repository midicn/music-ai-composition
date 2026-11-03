---
id: "prompt-grammar"
site: "ai"
cat: "B"
title: "提示语法与结构标记"
title_en: "Prompt Grammar and Section Tags"
summary: "把提示当分句写：先定骨架，再下约束，最后排除。"
summary_en: "Treat a prompt as clauses, fixing the skeleton, then constraints, then exclusions, in that order."
level: "standard"
tags: ["提示词", "语法", "段落标记", "约束"]
tags_en: ["prompting", "grammar", "section tags", "constraints"]
alias: ["提示语法", "结构标记", "prompt grammar"]
order: 129
links: ["[[glossary:tempo]]", "[[glossary:ternary-form]]", "[[glossary:texture]]"]
instances: []
sources: ["https://help.suno.com/en/articles/3726721", "https://help.udio.com/en/articles/10716221-create-a-song-with-your-own-lyrics"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "提示语法与段落标记取决于平台实际支持的字段和编辑方式；播放一首歌不能证明关键词优先级，也不能保证另一服务按同样标记生成。"
---

::: zh
## 逗号堆出来的不是语法

“温暖, 复古, 弦乐, 慢, 电影感, 不要鼓”这样的提示，模型只能按词频猜重点。提示有结构：段落标记告诉它歌长什么样，控制词告诉它哪里必须准确，排除项告诉它别做什么。顺序错了，后面的词会覆盖前面的。

## 标记与控制词

| 成分 | 写法示例 | 放在哪 | 作用 | 常见误用 |
|---|---|---|---|---|
| 段落标记 | [Intro] [Verse] [Chorus] | 歌词行之间 | 划分结构与进入点 | 标记语言与歌词语言混用 |
| 速度 | 92 BPM | 开头 | 锁定律动 | 写在长描述末尾 |
| 调性 | D minor | 速度之后 | 限定和声色彩 | 与参考音频的调性冲突 |
| 编制 | 弦乐四重奏、无鼓 | 中段 | 定音色与密度 | 同义乐器堆叠 |
| 排除 | no drums, no vocals | 最后 | 去掉不想要的部分 | 与正面词互相矛盾 |
| 长度 | 30 seconds | 结构之前 | 控制裁剪 | 与段落数不匹配 |

## 约束的先后

先体裁与编制，再速度与调性，然后段落与长度，最后情绪与排除。越靠前的词越像骨架，越靠后的词越像修饰。把“不要电子鼓”放在“电子鼓”前面，模型仍可能先看到后者。一个段落只改一个约束，才知道哪一句有效。

## 可复用的骨架

[Style] 90 BPM, A minor, [ensemble], [mood]. [Intro] 4 bars. [Verse] ... [Chorus] ... No [unwanted].

方括号只是给人看的边界，不是所有模型都识别。识别不了就换成普通行或空行分段，别让标记本身成为噪声。歌词与标记分行写，模型更容易把结构当成结构，而不是当成歌词内容。

## 语法失效的时候

模型不认标记、歌词与标记语言不同、约束互相打架、提示超过有效长度，都会让结构塌掉。这时删掉一半修饰，只留速度、编制、段落三样，再逐项加回。语法是减少歧义的工具，不是越长越准的咒语。若换了模型仍不认标记，就改用行序与重复副歌来表达结构，别在符号上较劲。
:::

::: en
## Commas are not grammar

A prompt like "warm, vintage, strings, slow, cinematic, no drums" leaves the model guessing by word frequency. Prompts have structure: section tags say what shape the song takes, control words say what must be exact, exclusions say what to leave out. Put them in the wrong order and later words overwrite earlier ones.

## Tags and control words

| Element | Example | Placement | Job | Common misuse |
|---|---|---|---|---|
| Section tag | [Intro] [Verse] [Chorus] | Between lyric lines | Marks form and entry points | Tag language differs from lyric language |
| Tempo | 92 BPM | Opening | Locks the pulse | Buried at the end of a long description |
| Key | D minor | After tempo | Narrows harmonic colour | Conflicts with the reference key |
| Ensemble | String quartet, no drums | Middle | Sets timbre and density | Stacking synonyms for one instrument |
| Exclusion | no drums, no vocals | Last | Removes unwanted elements | Contradicts a positive term |
| Length | 30 seconds | Before form | Controls trimming | Does not match the section count |

## The order of constraints

Genre and ensemble first, then tempo and key, then sections and length, then mood and exclusions. Earlier words act as skeleton, later words as trim. Put "no electronic drums" after "electronic drums" and the model may still see the latter first. Change one constraint per section so you learn which line did the work.

## A reusable skeleton

[Style] 90 BPM, A minor, [ensemble], [mood]. [Intro] 4 bars. [Verse] ... [Chorus] ... No [unwanted].

Brackets are human-facing boundaries, not a syntax every model understands. If they are ignored, use plain lines or blank-line paragraphs; do not let the notation become noise. Keep lyrics and tags on separate lines so structure reads as structure rather than lyric content.

## When the grammar fails

Structure collapses when tags are unrecognised, tags and lyrics use different languages, constraints contradict, or the prompt exceeds the effective length. Cut half the modifiers, keep tempo, ensemble and sections, then add items back one at a time. Grammar reduces ambiguity; it is not a spell that improves with length. If a new model still ignores tags, express form through line order and repeated choruses instead of fighting the notation.
:::

