---
id: copyright-of-ai-output
site: ai
cat: G
title: AI 输出与版权
title_en: Copyright in AI Output
summary: 机器生成的成品不一定归你，人的选择才是可主张的部分
summary_en: A generated track may not belong to you; the human choices are what you can claim
level: standard
tags: [版权, 作者身份, 输出, 证据]
tags_en: [copyright, authorship, output, evidence]
alias: [AI 版权, 生成物权利, AI output rights]
order: 2
links:
  - "[[glossary:music-copyright]]"
  - "[[glossary:work-for-hire]]"
instances:
  - atepp-000115 | 韦伯恩钢琴变奏曲第二乐章，每个音都经过决定，人写的密度难以用平均值生成（C1）
  - mutopia-001093 | 乔普林《枫叶拉格》钢琴谱，切分与左手跳进是可指认的创作选择（C1）
  - cyberhymnal-004898 | 只标"老德国合唱曲"的赞美诗，旋律在公有领域，作者的名字却缺失（C1）
  - pdmx-000326 | 标着采集来源的《黑是颜色》，民间流传与作者身份之间隔着一段记录（C1）
sources:
  - 版权保护对作者身份的一般要求；公开法律评论是主要依据。
  - 生成内容的登记与维权差异——依据来自各地公开说明。这里不下结论。
updated: 2026-10-30
---

::: zh
## 为什么会用到

生成一段音乐只要几十秒，但"这段音乐归谁"没有同样快的答案。多数法域的版权制度把保护给"人"的创作，纯机器输出能不能登记、能登记到什么程度，各地做法不同，也在变。使用者最实际的问题不是打赢官司，而是交付时能不能说清"这版我能授权给你"。

## 它怎么运转

版权保护的是表达，而表达需要有人做出选择。提示词算不算选择，取决于你控制到多细。写"温暖钢琴曲"和指定调性、和声进行、曲式、每段乐器进出，控制程度差很远。挑选与编排也可能构成劳动，从几十个候选里选出四个、剪接成结构、改写声部，这些是人的判断。反过来，一次生成、原样导出、不做编辑，你能主张的部分就很薄。另外，输出可能与他人的作品实质相似，模型在某个风格上训练得越密，这种风险越具体。

## 从哪开始

做三件事。第一，留过程，提示词、迭代版本、你的编辑、工程文件、时间戳，都存下来，这些是"人做了选择"的证据。第二，做相似性检查，把成品与参照曲目比对旋律与和声，尤其是你明确模仿过的对象。第三，写清交付口径，合同里不要承诺"独家版权"这类你无法确认的权利，改成就你实际贡献的部分做授权，并披露使用了工具。登记与维权路径各国不同，发行量大的项目，先向律师核实当地规则。

## 耳朵要抓的点

在韦伯恩变奏曲第二乐章里听那种每个音都被决定过的密度，它不是风格平均值能长出来的；在《枫叶拉格》里听切分与低音跳进的具体写法，这些是可以指认的选择；在老德国合唱曲里听一条没有作者的旋律，它在公有领域里，也说明"作者"这个位置有时是空的。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A3","C4","E4","A4","G#4","E4","C4","A3"],"label":"可以指认的选择","label_en":"A choice you can point to","hint":"具体的音程与节奏决定，才是人能主张的部分","hint_en":"Specific interval and rhythm decisions are what a person can claim"}
```
:::

::: en
## Why you reach for it

Generating a track takes seconds. Deciding who owns it does not. Most copyright systems protect the work of a human author, and whether a purely machine-made output can be registered, and how far, differs between jurisdictions and is still moving. For a working musician the practical question is narrower. At delivery, can you honestly say what you are licensing.

## How it runs

Copyright protects expression, and expression requires someone to choose. Whether a prompt counts as choosing depends on how precisely you controlled the result. "Warm piano piece" and a brief that fixes key, harmonic motion, form and the entry of each instrument sit far apart. Selection and arrangement can also amount to labour, picking four takes from forty, cutting them into a structure, rewriting a bass line, these are human judgements. One generation exported untouched gives you very little to claim. There is a second exposure as well. Output may land close to an existing work, and the more densely a model was trained on one style, the more concrete that risk becomes.

## Where to start

Do three things. Keep the process, prompts, iterations, your edits, project files, timestamps, since these are the evidence that a person chose. Run a similarity check, comparing melody and harmony against your reference tracks, especially anything you deliberately imitated. Write the delivery language carefully, and do not promise "exclusive copyright" over something you cannot verify. License the part you actually contributed, and disclose the tools used. Registration and enforcement routes vary by country, so for a release with real reach, confirm the local position with a lawyer.

## What the ear catches

In the Webern variation, a density in which every note has been decided, something an average of a style does not produce. In Maple Leaf Rag, the specific syncopation and left-hand leaps, choices you can name. In the old German chorale, a tune with no author, sitting in the public domain and showing that the author slot is sometimes empty.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A3","C4","E4","A4","G#4","E4","C4","A3"],"label":"A choice you can point to","label_en":"A choice you can point to","hint":"Specific interval and rhythm decisions are what a person can claim","hint_en":"Specific interval and rhythm decisions are what a person can claim"}
```
:::
