---
id: "model-izotope-ai"
site: "ai"
cat: "I"
title: "iZotope 的 AI 助手"
title_en: "iZotope Assistants"
summary: "修复、混音与母带里的助手，把判断变成可修改的建议。"
summary_en: "Assistants inside repair, mixing and mastering that turn judgement into suggestions you can edit."
level: "standard"
tags: ["模型档案", "修复", "母带", "混音", "插件"]
tags_en: ["model profile", "restoration", "mastering", "mixing", "plugin"]
alias: ["iZotope", "RX", "Ozone", "Neutron", "母带助手", "Music Rebalance"]
order: 13
model_vendor: "iZotope"
model_form: "插件"
model_input: ["音频", "分轨"]
model_output: ["音频", "母带", "分轨"]
model_licence: "买断或订阅、机器授权与离线激活、EULA 对产出的权利主张需自行核对，助手不会替你做法律判断"
model_verified: "2026-10-30"
links: ["[[glossary:mastering]]", "[[glossary:noise-floor]]", "[[glossary:limiter]]"]
instances: []
sources: ["https://www.izotope.com/en/products/ozone/engineers", "https://downloads.izotope.com/guides/iZotopeMasteringGuide_MasteringWithOzone.pdf"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页介绍iZotope辅助母带与音频处理，应以相应版本官方功能说明和实际处理文件核对；普通MIDI没有降噪或母带前后版本，不能当作助手效果测评。"
---

::: zh
## 实际用途

修一段底噪明显的老录音：去嗡声、去咔嗒、去混响、用频谱笔刷补掉一声咳嗽；把人声、贝斯、鼓与其他从成品里重新配比；给混音一条平衡建议当作起点；给母带一条参考曲线与响度目标；批量处理一季播客或一张专辑。

## 输入与产出

输入是音频或分轨，插件跑在 DAW 里，独立应用可以不进 DAW 直接处理文件。输出是处理后的音频、母带文件，或再平衡后的一组分轨。处理在本机完成，素材不上传。助手给的是参数与曲线，全部可以手改，也可以整段关掉。

## 最好用的地方

- 与 DAW 工作流贴合，修复完直接往下混，不用导出再导入。
- 频谱编辑可以精确到笔刷，处理个别噪声事件比整段降噪干净。
- 助手给的是起点，参数可见可改，适合当教学参照。
- 修复能力强于纯分离：去嗡、去齿音、去混响各有专门模块。
- 可以批量，适合播客、有声书这类重复性工作。
- 本地处理，保密素材不必上传。

## 会翻车的地方

- 过度处理：母带助手偏亮偏压，直接接受建议会把动态压平，鼓的冲击最先消失。
- 去混响：抹掉空间的同时抹掉瞬态，钢琴与鼓的起音会变软，尾巴变干。
- 再平衡：Music Rebalance 一类的分轨质量不如专用分离模型，拿它当分轨工具会失望。
- 理解边界：助手听不出总线处理、侧链与编曲意图，对复杂工程给的建议常常不适用。
- 授权与激活：换机、离线现场、团队协作都可能卡在激活上，出发前要试一遍。
- 学习曲线：助手省的是起点，不是判断；不会听的人更容易被"建议"带着走。

## 收费、授权与替代品

要确认的问题：买断版与订阅版的差别在哪里？升级是否另付费？一台机器能装几份、可否离线激活？EULA 对处理后的产出有没有额外主张？把处理结果交给客户是否受限？

价格是买断加升级计划或订阅，套装覆盖多个模块；地区与教育折扣以官方页面为准。

替代：Adobe Enhance——只做语音清理、要零学习成本时换它；SpectraLayers——要做更细的频谱手术时换它；Demucs 加手动处理链——要开源、批量、可脚本化时换它。
:::

::: en
## In practice

Repair an old recording with audible noise: hum, clicks, reverb, or a cough removed with a spectral brush; rebalance vocals, bass, drums and other from a finished mix; get a starting balance for a mix; get a reference curve and loudness target for a master; batch a season of podcasts or a whole album.

## Input and output

You input audio or stems, running as a plug-in inside a DAW, or as a standalone application on files without a DAW. The output is processed audio, a master file, or a set of rebalanced stems. Processing is local and nothing is uploaded. The assistants produce parameters and curves that can all be edited by hand or switched off.

## Where it shines

- Fits the DAW workflow: repair and keep mixing without export and re-import.
- Spectral editing down to a brush removes single noise events more cleanly than broadband denoising.
- Assistants give a starting point with visible, editable parameters, useful as a teaching reference.
- Repair goes beyond separation: hum, sibilance and reverb each have dedicated modules.
- Batch processing suits repetitive work such as podcasts and audiobooks.
- Local processing keeps confidential material off the network.

## Where it falls over

- Over-processing: master suggestions lean bright and compressed, and accepting them flattens dynamics, with drum impact going first.
- De-reverb: removing space also removes transients, so piano and drum attacks soften and tails dry out.
- Rebalancing: stem quality from a rebalance module is below dedicated separators, and treating it as a stem tool disappoints.
- Blind spots: assistants do not hear bus processing, sidechains or arrangement intent, so advice on complex sessions often misses.
- Licensing and activation: machine changes, offline shows and team work can stall on activation, so test before you travel.
- Learning curve: assistants save the starting point, not the judgement; anyone who cannot hear is led further astray.

## Cost, licence, alternatives

Questions to check: how do perpetual and subscription licences differ? Are upgrades charged separately? How many machines are covered, and is offline activation possible? Does the EULA claim anything over processed output? Are there limits on delivering the result to clients?

Pricing is a purchase plus an upgrade plan or a subscription, with bundles covering several modules; regional and educational pricing is as stated on the official pages.

Alternatives: Adobe Enhance when you only need speech cleanup with no learning curve; SpectraLayers when you need finer spectral surgery; Demucs plus a manual chain when you need open, batchable, scriptable processing.
:::

