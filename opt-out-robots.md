---
id: opt-out-robots
site: ai
cat: G
title: 退出、robots 与抓取
title_en: Opt-Out, Robots and Crawling
summary: robots 是请求不是锁，退出要落到合同与证据
summary_en: robots.txt is a request, not a lock; opt out in writing and keep evidence
level: standard
tags: [训练退出, robots, 抓取, 授权边界]
tags_en: [opt-out, robots, crawling, licensing boundaries]
alias: [训练退出, robots.txt, 抓取限制]
order: 155
links:
  - "[[glossary:music-copyright]]"
  - "[[glossary:sample-clearance]]"
  - "[[glossary:public-domain]]"
instances:
  - abcmisc-001404 | 只标“传统”的克莱兹默曲调，想退出也找不到可联系的权利主体（C1）
  - wikifonia-000434 | 采集者姓名留在标题里，说明“传统”之外还有具体的人（C1）
  - cyberhymnal-002828 | 灵歌被配上四部合唱与管风琴，改编与录音各有一层授权（C1）
  - groove-001118 | 一段 126 BPM 的 highlife 鼓循环，被剪成片段后很难追溯原始授权（C1）
sources:
  - robots.txt 的公开规范 RFC 9309，由互联网工程任务组发布。
  - 生成式 AI 训练数据退出与保留机制，参考模型与平台公开说明。
  - 版权许可与集体管理的公开资料，由行业组织发布。
updated: 2026-10-31
---

::: zh
## 三种退出，对象不同

把作品集挂在自己站上，页脚写“禁止 AI 训练”，不会拦住任何爬虫。退出至少分三种：平台内的训练退出、站点侧的抓取规则、合同里的授权边界。它们分别对平台、对爬虫、对合作方说话，混成一句就谁也管不住。

## 抓取边界

| 手段 | 能管什么 | 管不住什么 |
|---|---|---|
| robots.txt | 自愿遵守规则的爬虫 | 不读规则的抓取、已经存在的索引副本 |
| UA 与 IP 封禁 | 已知来源的访问 | 换标识、分布式抓取 |
| 登录与付费墙 | 未获账号的访问 | 有账号者的批量下载 |
| 合同与许可 | 签过字的合作方 | 无法识别的第三方 |

robots.txt 是请求，不是门锁。它写清哪些路径不希望被抓，但遵守与否取决于对方。真正想限制商用抓取，要回到许可文本：允许谁用、用来做什么、能不能再分发、能不能用于训练。条款写得越具体，出事时越好说明。

## 检查清单

- [ ] 站点根目录的 robots.txt 写明不希望被抓的路径与已知 AI 爬虫
- [ ] 每个生成平台的训练开关逐个关，截图保存日期与账号
- [ ] 授权书里单列“是否允许训练”，不要只写“复制与发行”
- [ ] 上传参考音频、干声、demo 前确认自己有权处理
- [ ] 发现抓取后保留访问日志、快照与时间
- [ ] 重要作品另存本地与离线副本，不把唯一版本放在公开页面

## 退出之后还剩什么

退出通常只对未来生效，已经进入训练的数据很难撤回；robots 改了，旧索引和第三方镜像还在；合同通常只约束签字的人。遇到争议，先看条款文本与适用法域，再决定要不要发函或找律师。把退出当成降低概率的动作，不要当成开关。
```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["A3","E4","C4","A3"],"label":"被索引与未被索引的素材","label_en":"Indexed and unindexed material","hint":"先确认这段素材是否可被检索到","hint_en":"Check whether this material can be found"}
```

:::

::: en
## Three opt-outs aimed at different parties

A footer notice saying "no AI training" on your portfolio site stops no crawler. Opting out is at least three separate acts: turning off training inside a platform, setting crawl rules on your own site, and writing licence boundaries into contracts. They speak to a platform, to crawlers and to partners respectively. Blended into one sentence, none of them works.

## Where crawling stops

| Measure | What it governs | What it cannot stop |
|---|---|---|
| robots.txt | Crawlers that choose to follow it | Crawlers that ignore it, index copies already made |
| User-agent and IP blocks | Access from known sources | Changed identifiers, distributed crawling |
| Login and paywall | Access without an account | Bulk downloads by account holders |
| Contract and licence | Partners who signed | Unidentified third parties |

robots.txt is a request, not a lock. It states which paths you would rather not have crawled, and compliance depends on the other side. If you need to limit commercial crawling, go back to the licence text: who may use the work, for what, whether they may redistribute it, and whether they may train on it. Specific terms are easier to point to when something goes wrong.

## A checklist

- [ ] Publish a robots.txt that names the paths and known AI crawlers you want excluded
- [ ] Turn off training switches platform by platform, and save a dated screenshot of each account
- [ ] Put a separate training clause in licences instead of folding it into "reproduction and distribution"
- [ ] Confirm you hold the rights to any reference audio, dry vocal or demo you upload
- [ ] If crawling is detected, keep access logs, snapshots and timestamps
- [ ] Keep an offline copy of important work; never leave the only version on a public page

## What remains after opting out

Most opt-outs apply going forward only, and data already used in training is usually hard to withdraw. Changing robots.txt does not remove old indexes or third-party mirrors. A contract usually binds only its signatories. When a dispute appears, read the terms and the applicable jurisdiction first, then decide whether to send a notice or consult a lawyer. Treat opting out as lowering a probability, not as flipping a switch.
:::
