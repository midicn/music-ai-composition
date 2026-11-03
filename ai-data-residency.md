---
id: "ai-data-residency"
site: "ai"
cat: "A"
title: "数据驻留与隐私"
title_en: "Data Residency and Privacy"
summary: "上传之前先分清：素材去哪、留多久、会不会进入训练。"
summary_en: "Before uploading, establish where the material goes, how long it stays and whether it can enter training."
level: "standard"
tags: ["数据驻留", "隐私", "训练数据", "上传"]
tags_en: ["data residency", "privacy", "training data", "uploads"]
alias: ["数据驻留", "隐私检查", "data residency"]
order: 125
links: ["[[glossary:stems]]", "[[glossary:licensing]]", "[[glossary:public-domain]]"]
instances: []
sources: ["https://eur-lex.europa.eu/eli/reg/2016/679/oj/eng", "https://replicate.com/docs/topics/predictions/data-retention"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页讨论素材上传、保留和跨境处理，需要核对适用法规、服务保留政策及实际部署；普通MIDI回放不能证明数据存储地点或隐私措施。"
---

::: zh
## 上传就是一次授权

把客户未发行的分轨拖进网页生成器，等于把素材交给第三方处理。能不能传，不取决于文件大小，而取决于合同、素材权利和服务条款三件事是否同时对得上。三项里缺一项，最安全的动作是先停手。

## 四个必问

| 问题 | 要问什么 | 可接受的答案 | 留什么证据 |
|---|---|---|---|
| 上传到哪 | 服务器地区、子处理者 | 与合同约定一致 | 服务地区说明、处理附录 |
| 是否训练 | 默认开还是默认关 | 可关闭且有书面说明 | 账号设置截图、条款版本 |
| 保留多久 | 音频、提示、日志 | 有明确期限与删除方式 | 保留期条款、删除确认 |
| 地区差异 | 跨境传输、备份位置 | 有合法传输依据 | 传输附录、备份策略 |

训练与保留期最常被忽略。前者影响权利，后者影响保密。两者都不能只凭销售口头承诺，要落到可保存的文本。

## 上传前检查

- 客户合同是否允许第三方处理
- 素材是否含未清权的采样或人声
- 账号是否为企业版，成员权限是否最小化
- 训练开关、历史记录、自动保存是否关闭
- 删除后是否还有备份与日志残留
- 离队成员的访问是否可撤销
- 是否有本地或离线替代方案

## 地区不等于辖区

服务器在某个国家，不代表适用那里的法律；备份可能落在另一地；支持团队可能在第三地访问工单。跨境项目要把“数据在哪处理”和“由谁可访问”分开写进交付说明。遇到不能上传的素材，改用本地模型或只上传派生特征，比赌条款更稳。删除请求也要问清范围：主存储、备份、日志与训练副本是否同步清除，各自多久生效。
:::

::: en
## Uploading is granting access

Dragging a client's unreleased stems into a browser generator hands the material to a third party. Whether you may do so depends less on file size than on three things lining up: the client contract, the rights in the material, and the service terms. If one is missing, stop first.

## Four questions that decide it

| Question | What to ask | Acceptable answer | Evidence to keep |
|---|---|---|---|
| Where does it go | Server region, subprocessors | Matches the contract | Region statement, processing addendum |
| Is it trained on | Opt-in or opt-out by default | Can be disabled in writing | Account screenshot, terms version |
| How long is it kept | Audio, prompts, logs | Defined period and deletion route | Retention clause, deletion confirmation |
| Regional differences | Cross-border transfer, backups | lawful transfer basis | Transfer addendum, backup policy |

Training and retention are the two most often skipped. The first affects rights, the second confidentiality. Neither should rest on a sales claim; both need text you can archive.

## A pre-upload checklist

- Does the client contract permit third-party processing
- Does the material contain uncleared samples or voices
- Is the account a business tier with least-privilege access
- Are training, history and autosave switched off
- Do backups or logs survive deletion
- Can access be revoked when a collaborator leaves
- Is there a local or offline alternative

## Region is not jurisdiction

A server in one country does not mean that country's law applies; backups may sit elsewhere and support staff may open tickets from a third location. For cross-border work, state separately where processing happens and who can reach it. When material cannot be uploaded, a local model or derived features are safer than betting on a clause. Ask about deletion scope too: primary storage, backups, logs and training copies, and how long each takes to clear.
:::

