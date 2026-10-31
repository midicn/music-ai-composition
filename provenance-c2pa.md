---
id: provenance-c2pa
site: ai
cat: G
title: 来源凭证与 C2PA
title_en: Provenance and Content Credentials
summary: 文件里的标记说明怎么做的，不说明归谁
summary_en: A manifest records how a file was made, not who owns it
level: standard
tags: [来源凭证, C2PA, 生成标记, 元数据]
tags_en: [provenance, C2PA, content credentials, metadata]
alias: [C2PA, 内容凭证, provenance]
order: 150
links:
  - "[[glossary:music-copyright]]"
  - "[[glossary:isrc]]"
  - "[[glossary:master-rights]]"
instances:
  - wikifonia-000434 | 采集者姓名直接进了标题，来源靠命名而不是文件记录（C1）
  - cyberhymnal-002684 | 一行“蒙克据克吕格改编”保住了改编链，换个人重写就会断（C1）
  - mutopia-001411 | 公有领域只覆盖萨蒂原作，录成什么样是另一层凭证（C1）
  - giantmidi-003011 | 《致敬萨蒂》把风格来源写进标题，文件里却未必留得下（C1）
sources:
  - C2PA 内容凭证的技术规范，由行业联盟公开。
  - 合成内容标注的平台规则，来自主要发行与社交平台的公开政策。
  - 广播与发行中的音频元数据字段，参考行业组织公开资料。
updated: 2026-10-31
---

::: zh
## 文件里能留下的三层记录

一条生成音频发给客户，对方看到的来源通常只剩文件名。可核对的信息其实分三层：技术层记录文件经过哪些处理，创作层记录谁写了什么、用了什么工具，发布层记录观众能看到的标注。三层各写各的，断一层，后面的人就只能靠猜。

## 凭证落在哪个字段

| 层 | 载体与字段 | 记什么 | 常见缺口 |
|---|---|---|---|
| 文件层 | C2PA manifest、XMP、BWF 的 originator | 生成、编辑、转码的操作与签名 | 平台转码或截图后丢失 |
| 作品层 | 曲名、作者、ISRC、版权行 | 作品与这一次录音的身份 | 新混音沿用旧 ISRC |
| 发布层 | 平台披露开关、简介、片尾 | 观众读得到的说明 | 与文件内记录不一致 |

C2PA 是一套把操作记录与签名装进文件的技术规范。manifest 里可以写生成、裁剪、转码、导出这些动作，也可以挂上素材来源。它回答的是“谁声明了什么操作”，不是“谁拥有这段音乐”。ISRC 则只标一次录音，换混音或剪辑版本要另取号，不能拿作品名代替。

## 平台披露补的是另一段

文件标记给工具读，平台披露给人看。两者不能互相顶替：文件里有 manifest，平台未必展示；平台标了“含生成内容”，文件转手、转码、录屏之后又可能什么都不剩。对外披露要短而具体，写清哪一段是生成的、哪一段由人完成、用了什么工具，比一句“AI 辅助”有用。

## 凭证靠不住的地方

签名只证明某个主体声明了这些操作，不证明素材已获授权，也不证明输出与既有作品无关。元数据可以手填，manifest 可以被剥离，截图更不是原始文件。反过来，没有凭证也不等于有问题。把凭证当成证据链的一环：原始导出、manifest、工具版本、编辑记录放在一起，才经得起追问。
```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C4","G4","E4","C4"],"label":"带元数据的导出与裸音频","label_en":"Export with metadata vs bare audio","hint":"听感可能一样，来源信息不一样","hint_en":"They may sound alike; the provenance differs"}
```

:::

::: en
## Three layers a file can carry

A client receives a generated track and sees a filename. The checkable record actually has three layers: the technical actions applied to the file, the creative attribution of who made what with which tool, and the label the audience sees. Each layer fails at a different point, and one missing layer leaves the next person guessing.

## Which field holds which record

| Layer | Carrier and field | What it records | Usual gap |
|---|---|---|---|
| File | C2PA manifest, XMP, BWF originator | Generation, editing, transcoding and signatures | Lost in platform transcodes or screenshots |
| Work | Title, author, ISRC, copyright line | Identity of the work and of this recording | A new mix reuses the old ISRC |
| Release | Platform disclosure, notes, end credits | The explanation an audience can read | Does not match the file record |

C2PA is a technical specification for embedding action records and signatures in a file. A manifest can list generation, trimming, transcoding and export, and can point to source material. It answers who asserted which actions, not who owns the music. An ISRC identifies one recording; a new mix or edit needs its own code, and a title is not a substitute.

## A platform label is a separate layer

File metadata is read by tools, while a platform label is read by people. Neither replaces the other. A file may carry a manifest that the platform never displays; a platform may mark a track as containing generated content, and that mark disappears after a download, transcode or screen recording. Public disclosure should be short and specific: which section was generated, which was made by a person, which tool was used. "AI-assisted" explains nothing.

## Where credentials fail

A signature proves only that some party asserted these actions. It does not prove that the source material was licensed, nor that the output avoids existing works. Metadata can be typed by hand, a manifest can be stripped, and a screenshot is not the original file. The reverse also holds: no credentials does not mean a problem. Treat provenance as one link in a chain, kept together with the original export, the manifest, the tool version and the edit log.
:::
