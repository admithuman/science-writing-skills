# 🔬 Science Writing Skills for Claude Code

> 基于 *Science Research Writing for Non-Native Speakers of English* (Glasman-Deal, Imperial College Press, 2010) 全书269页深度知识蒸馏，封装的两个专业级 Claude Code 学术写作技能。

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-2-brightgreen.svg)](#技能列表)
[![Book](https://img.shields.io/badge/based%20on-Glasman--Deal%202010-orange.svg)](#来源)

---

## 📖 背景

这两个技能基于 Hilary Glasman-Deal 在帝国理工学院30年学术英语教学经验的结晶。原书专为非英语母语的科研人员设计，教授如何按照国际期刊的约定俗成模式撰写研究论文。
<img width="254" height="373" alt="1796e58302d7cb77f1d3282db975327a" src="https://github.com/user-attachments/assets/4d52ba90-29ee-45e1-bdd8-40e36af8ba09" />

我们对全书269页进行了**完整知识蒸馏**，提取了：
- 5个单元的 IMRaD 论文结构模型
- 200+ 条语法与写作规则
- 600+ 篇真实论文中提炼的学术词汇表
- 4个附录的专业知识（缩写、前缀、拉丁/希腊语单复数、动词表）

---

## 🎯 技能列表

### 技能 1：中文稿件专业翻译与润色
**文件:** `skills/science-writing-translate-cn.md`

将中文科研/学术稿件翻译为高质量英文，采用**三段对照式**输出——在原文每一段下方依次插入英文译文和中文翻译说明（标注所应用的书籍要点），完整保留原文档格式。

| 功能 | 说明 |
|------|------|
| 📥 输入 | 中文 `.docx` / `.doc` / `.tex` (LaTeX) 文件 |
| 📤 输出 | `原文件名_翻译润色版.docx` 或 `.tex` |
| 🎨 格式 | 中文原文→英文译文(深蓝斜体)→翻译说明(深绿) 三段对照 |
| 🔢 公式 | Word中LaTeX公式(`$...$`/`$$...$$`)自动识别并保留；LaTeX文档数学环境完整保留 |
| ✏️ 标注 | 4色修改标注(红/蓝/绿/紫) + 批注 |
| 📊 报告 | 末尾附带完整翻译润色报告 + 书中规则应用统计 |

**核心能力：**
- 自动识别论文各部分（Introduction/Methodology/Results/Discussion/Abstract）
- 对每部分应用书中对应的写作模型和时态规则
- 翻译后自动润色：时态、冠词、信号语、学术词汇升级
- 支持 `.tex` LaTeX 文档读取与输出，保留所有命令/环境/数学公式
- Word中识别并保留LaTeX公式语法，公式内容不翻译
- 每段附带翻译说明，明确标注应用了书中哪个章节的具体规则

---

### 技能 2：英文稿件专业润色
**文件:** `skills/science-writing-english-polish.md`

对英文科研文本进行5层级递进式全面润色，严格遵循书中的写作标准。

| 功能 | 说明 |
|------|------|
| 📥 输入 | 英文文本（直接粘贴）或 `.docx` 文件 |
| 📤 输出 | 带修订标注的润色版文档 |
| 🔍 层级 | 结构→句子→语法→词汇→风格 |
| 📋 报告 | 末尾附带完整润色报告 |

**核心能力：**
- 验证论文各部分是否符合 IMRaD 结构模型
- 时态精确检查（书中"隐藏错误"预警）
- 冠词、情态动词、信号语使用规范
- 学术词汇升级（模糊词→精准学术用词）
- 频率/数量/因果关系表达的分级优化

---

### 附赠：知识蒸馏参考文档
**文件:** `skills/science-writing-knowledge-distillation.md`

全书269页的完整知识地图，可作为独立的写作参考手册。
包含各单元的模型总结、语法要点、完整词汇表和示例。

---

## 🚀 快速开始

### 安装

将本仓库克隆到你的 Claude Code 项目目录：

```bash
git clone https://github.com/YOUR_USERNAME/science-writing-skills.git
cp -r science-writing-skills/skills/* /your-project/.claude/skills/
```

或者直接复制技能文件到你的 `.claude/skills/` 目录下。

### 使用

在 Claude Code 对话中直接调用：

```
# 翻译中文稿件（Word）
请用中文稿件翻译技能处理我的论文 draft.docx

# 翻译中文稿件（LaTeX）
请用中文稿件翻译技能处理我的LaTeX论文 paper.tex

# 润色英文稿件
请用英文润色技能帮我优化这段 Introduction
```

---

## 📋 技能原理

两个技能共享同一套知识体系——Glasman-Deal 书中的核心方法论：

> *"Carefully examine good examples of the kind of writing you would like to produce, identify and master the structure, grammar and vocabulary you see in these examples, and then apply them in your own writing."*

### 五层 IMRaD 论文结构模型

```
                    ABSTRACT
                 ↗           ↘
           INTRODUCTION → DISCUSSION
              ↓               ↑
         METHODOLOGY → RESULTS
```

| 部分 | 模型组件数 | 关键语法 |
|------|-----------|----------|
| **Introduction** | 4组件 | 时态对(Past Simple/Present Perfect)、信号语 |
| **Methodology** | 4组件(菜单式) | 被动语态、冠词a/the、副词位置 |
| **Results** | 4组件(菜单式) | 顺序/频率/数量/因果关系表达 |
| **Discussion** | 4组件 | 情态动词(may/should/must等6类) |
| **Abstract** | 双模型 | 时态一致性、独立可读性 |

### 书中最重要的规则

1. ⚠️ **"隐藏错误"预警** — 语法正确但时态选错（如用 Past Simple 描述研究空白，读者会以为问题已解决）
2. 📊 **"Results do not speak for themselves"** — 必须用评价性语言表达你的理解
3. 🏗️ **"先展示墙，再检查砖"** — 先总览再细节
4. 🎯 **区分标准程序和你自己的操作** — 否则读者无法识别你的贡献
5. 📢 **不要害羞陈述成就** — 使用 compelling, striking, unprecedented 等"感叹号替代词"

---

## 📁 目录结构

```
science-writing-skills/
├── README.md                                      # 本文件
├── LICENSE                                        # MIT License
└── skills/
    ├── science-writing-knowledge-distillation.md   # 全书知识蒸馏总纲
    ├── science-writing-translate-cn.md             # 技能1: 中文翻译润色
    └── science-writing-english-polish.md           # 技能2: 英文稿件润色
```

---

## 📚 来源

**原书：**
- Glasman-Deal, H. (2010). *Science Research Writing for Non-Native Speakers of English*. Imperial College Press, London.
- ISBN: 978-1-84816-310-2

**知识蒸馏方法：**
- 逐页读取全书269页
- 逐章结构化总结（核心原则、操作方法、正反面案例、常见错误）
- 交叉验证各章节的一致性
- 整合为系统化知识框架

---

## ⚠️ 适用与限制

**适用场景：**
- 科研论文（期刊/学位论文）的写作、翻译和润色
- 实验报告、技术文档
- 基金申请书（部分适用）

**不适用场景：**
- 文学/创意写作
- 商务邮件/市场营销文案
- 新闻/社交媒体内容

**重要提示：**
- 所有修改均标注依据，不凭空创造规则
- 翻译优先保证准确性，其次才是流畅度
- 不确定之处保守处理，标注供作者确认

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request 来改进这些技能。

如果你在使用中发现了书中规则的例外情况、或希望添加新的学术写作资源，请通过 Issue 与我们讨论。

---

## 📄 许可证

MIT License — 详见 [LICENSE](LICENSE) 文件。

---

*If these skills help your research get published, please star this repo and share it with your colleagues!* 🌟
