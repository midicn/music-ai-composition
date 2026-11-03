---
id: "delivery-qc"
site: "ai"
cat: "H"
title: "交付前检查"
title_en: "Delivery QC"
summary: "以接收方确认的规格检查实际文件，记录分轨、响度和完整性限制。"
summary_en: "Check actual files against the agreed specification and document stem, loudness and integrity limitations."
level: "standard"
tags: ["交付", "质检", "真峰值", "响度"]
tags_en: ["delivery", "QC", "true peak", "loudness"]
alias: ["交付检查", "交付质检", "delivery QC"]
order: 170
links: ["[[glossary:true-peak]]", "[[glossary:lufs]]", "[[glossary:stems]]"]
sources: ["https://www.ableton.com/en/manual/managing-files-and-sets/", "https://tech.ebu.ch/publications/r128", "https://www.itu.int/rec/R-REC-BS.1770-5-202311-I/"]
updated: "2026-11-03"
example_mode: "references"
example_basis: "本页说明实际制作流程与文件核验方法，工作表示例为虚拟教学项目；须以工具说明和自己的输出文件核对，普通MIDI或合成试听不能证明生成服务的效果。"
---

::: zh
## 验收依据是交付约定

用途不同，文件与响度要求可能不同。先确认格式、声道、采样率、位深、时长、起点与尾音范围，再检查实际导出文件。不能把工程设置直接当作导出结果，也没有适合所有项目的固定1dB余量或统一响度值。

## 四轮检查

1. 文件轮：清单中每项都能打开，命名与版本一致，实际规格符合约定。
2. 时间轮：检查开头、结束、循环点和对白或画面同步；保留要求的尾音。
3. 声音轮：完整试听并检查峰值、真峰值或响度等约定指标；同时听失真和伪影。
4. 交接轮：注明输入来源、实际可编辑范围与缺失项，附上确认过的参考混音。

分轨需要共同起点和清楚的导出说明，不应预设相加必能精确恢复混音。经过非线性母线处理或混音分离的文件尤其要记录差异。元数据按接收用途填写，不必把与项目无关的字段全部补齐。

## 独立复查

把交付包复制到新位置，照清单再打开一次。若附工程，检查外部依赖；若只提供混音，就明确没有原始工程。使用“交付清单”模板把每项实际文件和验收状态对应起来。
:::

::: en
## The agreement defines acceptance

Confirm file format, channels, sample rate, bit depth, duration, origin and tail range for the intended use. Inspect exported files rather than assuming they inherit the project settings. No fixed one-decibel margin or single loudness value suits every delivery.

## Four passes

1. Files: open each listed item, verify names and versions, and inspect actual properties.
2. Timing: check starts, endings, loops and synchronization with dialogue or picture.
3. Sound: hear the full result and measure agreed peaks, true peaks or loudness; listen for distortion and artefacts as well.
4. Handoff: describe input sources, remaining editability and missing material, with an approved reference mix.

Stems need a common origin and export notes. Do not assume they reproduce the reference exactly when summed, particularly after nonlinear bus processing or mix separation. Supply metadata relevant to the recipient's use rather than filling unrelated fields.

## Reopen independently

Copy the package to another location and open it using the manifest. For a project, verify external dependencies. If only a mix is available, state that an original project is absent. The delivery-manifest template connects each file with its acceptance state.
:::
