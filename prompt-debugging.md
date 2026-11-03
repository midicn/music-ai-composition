---
id: "prompt-debugging"
site: "ai"
cat: "B"
title: "提示排错"
title_en: "Debugging a Prompt"
summary: "结果不对先分层定位，别急着往提示里加形容词。"
summary_en: "Locate the faulty layer before rewriting adjectives, whether input, constraint, model or randomness."
level: "standard"
tags: ["提示词", "排错", "可复现", "调试"]
tags_en: ["prompting", "debugging", "reproducibility", "troubleshooting"]
alias: ["提示排错", "调试提示", "prompt debugging"]
order: 135
links: ["[[glossary:reference-track]]", "[[glossary:tempo]]", "[[glossary:texture]]"]
instances: []
sources: ["https://facebookresearch.github.io/audiocraft/api_docs/audiocraft/models/musicgen.html", "https://huggingface.co/docs/diffusers/en/using-diffusers/reusing_seeds"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "提示排错需固定模型、输入与可控随机条件，再逐项改变参数；单个音乐结果无法区分提示冲突、采样波动与模型能力限制。"
---

::: zh
## 先定位，再改词

生成结果不对，多数人第一反应是加形容词。更快的做法是先判断坏在哪一层：输入本身、约束写法、模型能力，还是随机性。四层的修法完全不同，改错层只会让提示越来越长。

## 四层排错

| 层 | 典型症状 | 先查什么 | 处理 |
|---|---|---|---|
| 输入 | 歌词错位、参考不相关 | 文本编码、音频长度、格式 | 换干净输入，缩短片段 |
| 约束 | 速度漂移、编制不对、段落缺失 | 约束是否冲突、位置是否太靠后 | 删到三条核心约束，逐条加回 |
| 模型 | 长结构塌、语言不支持、织体到顶 | 任务是否超出公开能力 | 分段、换形态或换模型 |
| 随机性 | 同一提示结果差异很大 | 种子、版本、候选数 | 固定种子，多次采样再判断 |

## 排查顺序

1. 同一提示原样重跑两次，确认差异是否来自随机性。
2. 固定种子，再跑一次，看问题是否仍在。
3. 删掉所有修饰，只留速度、编制、结构，逐条加回。
4. 换一段更短、更干净的输入，排除素材问题。
5. 用另一类工具做同样任务，确认是不是能力边界。
6. 记录每次改动，只动一个变量。

顺序本身就是成本控制。先换模型最贵，先加形容词最省事，却最容易把问题埋得更深。

## 记录表

- 提示全文与版本号
- 模型名与版本、日期
- 种子与候选数
- 输入文件与时长
- 本次只改了什么
- 结果问题与出现位置
- 是否可复现

没有记录，排错就变成凭记忆猜。三次以上的比较必须留下可复看的样本，否则下一轮会重复已经排除的假设。

## 修不好就换路

长结构反复塌、目标语言咬字始终不过关、精确和声无法落地，这些不是提示问题。继续加词只会让约束更挤。改成分段生成、换符号工具，或把生成结果当素材重做，通常比继续调提示更快。排错的终点是换方法，不是写出一条更长的提示。
:::

::: en
## Locate, then rewrite

When a generation misses, the reflex is to add adjectives. A faster move is to identify the layer that failed: the input itself, the way constraints are written, the model's capability, or plain randomness. Each layer needs a different repair; fixing the wrong one only lengthens the prompt.

## Four layers

| Layer | Symptoms | Check first | Action |
|---|---|---|---|
| Input | Displaced lyrics, irrelevant reference | Text encoding, audio length, format | Use clean input and a shorter excerpt |
| Constraints | Tempo drift, wrong ensemble, missing sections | Conflicting rules, placement too late | Cut to three core rules, add back one by one |
| Model | Long form collapses, language unsupported, texture ceiling | Whether the task exceeds public capability | Generate in parts, change tool type or model |
| Randomness | Same prompt, very different results | Seed, version, candidate count | Fix the seed and sample several times |

## Order of checks

1. Rerun the same prompt unchanged twice to see whether variance explains it.
2. Fix the seed and run again; does the fault persist.
3. Strip every modifier, keep tempo, ensemble and form, then add items back.
4. Swap in a shorter, cleaner input to rule out the material.
5. Try the same job in a different tool class to test the capability boundary.
6. Log each change and move one variable at a time.

The order controls cost. Changing models is expensive; adding adjectives is cheap and buries the cause deeper.

## A log worth keeping

- Full prompt and version number
- Model name, version and date
- Seed and candidate count
- Input file and duration
- The single change made this round
- The fault and where it appears
- Whether it reproduces

Without a log, debugging becomes memory. Anything compared more than three times needs a sample you can replay, or the next round repeats a hypothesis already eliminated.

## When to change the method

Long forms that keep collapsing, diction that never passes in the target language, exact harmony that will not land: these are not prompt problems. More words only crowd the constraints. Generate in parts, switch to a symbolic tool, or treat the output as raw material. Debugging ends in a change of method, not a longer prompt.
:::

