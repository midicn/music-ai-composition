---
id: "stem-naming"
site: "ai"
cat: "H"
title: "分轨命名规范"
title_en: "Stem Naming"
summary: "三套名字要能互相对上，而不是各自好看"
summary_en: "Three naming schemes have to map onto each other"
level: "standard"
tags: ["分轨", "命名", "交付", "DAW"]
tags_en: ["stems", "naming", "delivery", "DAW"]
alias: ["分轨命名", "文件命名", "stem naming"]
order: 175
links: ["[[glossary:stems]]", "[[glossary:stem-mastering]]", "[[glossary:sample-rate]]"]
instances: []
sources: ["https://studiopartner.netflix.net/studio/branded-sound-mix-spec-and-best-practices", "https://www.ableton.com/en/manual/managing-files-and-sets/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "分轨命名属于交付与资产管理，具体规则须按接收方的声轨或章节文件要求核对；音乐播放不会显示文件名、起点、版本和元数据是否一致。"
---

::: zh
## 一个压缩包里的三种命名

客户发回压缩包，里面是“人声最终版2”“人声最终版2 改”“BASS final”。工程无法自动对轨，混音师只能一个个试听。命名不是审美问题，是让文件在 DAW、平台和客户之间能被自动识别。

## 三套名字，三个目的

| 场景 | 字段顺序 | 示例 | 不要 |
|---|---|---|---|
| DAW 内 | 序号_角色_音色_版本 | 03_bass_di_v04 | 只写“贝斯2” |
| 平台上传 | 项目_曲名_版本_类型 | spring_ad_15s_v03_master | 中文、空格、括号 |
| 客户交付 | 项目_曲名_版本_分轨_速度_日期 | spring_ad_15s_v03_stems_120bpm_20261031 | 大小写混用、版本不补零 |

三套不必长得一样，但字段要能对上。DAW 里按序号排，平台按曲名和版本排，客户按项目收。映射关系写在交付说明里，比让所有人背同一套规则可靠。

## 一条规则管三套

全部小写 ASCII，下划线分隔，不用空格；版本两位补零；速度与调性固定放在同一位置；同一项目跨版本只改版本号，不改字段顺序；分轨名与 DAW 轨道名保持一致。平台对长度和字符有限制，上传前先试一个文件，别等批量失败。

## 改名之前先做映射

改名会打断工程引用、插件自动化与客户模板。先导出一张旧名到新名的 CSV，冻结版本之后再改，交付说明里附上映射表。客户有自己的命名规范时，按客户的来，内部保留一套稳定名，用映射表对齐。

## 名字救不了的情况

分轨内容贴错，名字再整齐也没用，必须听一遍；客户把“伴奏”和“纯音乐”混用，先在邮件里定义；平台不接受某些字符，规则要提前测。命名解决的是可查找，不解决可理解，后者靠交付说明。
:::

::: en
## Three naming schemes in one zip

A client returns a zip containing "vocal_final2", "vocal_final2 edit" and "BASS final". The session cannot relink automatically, so the mixer auditions each file. Naming is not a matter of taste; it is what lets a DAW, a platform and a client identify the same file without asking.

## Three schemes, three jobs

| Context | Field order | Example | Avoid |
|---|---|---|---|
| Inside the DAW | index_role_source_version | 03_bass_di_v04 | "bass2" alone |
| Platform upload | project_title_version_type | spring_ad_15s_v03_master | Chinese characters, spaces, brackets |
| Client delivery | project_title_version_stem_tempo_date | spring_ad_15s_v03_stems_120bpm_20261031 | Mixed case, unpadded versions |

The three do not have to look identical, but their fields must correspond. The DAW sorts by index, the platform by title and version, the client by project. Put the mapping in the delivery note; that is more reliable than making everyone memorise one scheme.

## One rule that survives all three

Use lowercase ASCII and underscores, never spaces. Pad versions to two digits. Keep tempo and key in a fixed position. Between versions of one project, change only the version number, never the field order. Keep stem names identical to DAW track names. Platforms limit length and characters, so test one upload before sending a batch.

## Build a map before renaming

Renaming breaks session references, plug-in automation and client templates. Export a CSV mapping old names to new ones, freeze the version first, and attach the map to the delivery note. When a client has a house style, follow it and keep a stable internal name aligned through the map.

## What a name cannot fix

If the stems themselves are swapped, tidy names will not help; someone has to listen. If a client uses "instrumental" and "backing track" interchangeably, define both in writing. If a platform rejects certain characters, test the rule early. Naming makes files findable, not understandable; the delivery note does the second job.
:::

