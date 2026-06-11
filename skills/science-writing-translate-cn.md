# 中文稿件专业翻译与润色技能

## 技能来源
本技能完全基于 **Hilary Glasman-Deal** 所著 *"Science Research Writing for Non-Native Speakers of English"* (Imperial College Press, 2010) 的写作原则和方法论。所有翻译策略、润色规则、词汇选择和语法规范均源自该书。

---

## 一、技能概述

本技能将中文科研/学术/技术稿件翻译为高质量英文，并自动应用Glasman-Deal书中的英文写作润色规则进行全面优化。翻译采用**三段对照式**：在原文每一段中文下方插入对应的英文译文，再紧跟一段中文翻译说明，形成"一段中文原文 → 一段英文翻译 → 一段中文说明"的上下排列对照格式，完整保留原文档的所有格式、样式和非文本元素。

### ⚠️ 核心铁律：每段必翻，无一遗漏

**文档中的每一个正文段落（Normal样式、List Paragraph样式等）都必须翻译，不允许跳过任何段落。**

- ✅ **公式周围文字必须翻译**：段落中包含数学公式、LaTeX表达式或符号时，公式/符号本身原样保留，但段落中的**所有文字内容必须完整翻译**
- ✅ **短段落也必须翻译**：即使是只有一句话的段落，也必须给出英文翻译和翻译说明
- ✅ **列表项必须翻译**：Highlights、贡献列表、规则列表等所有列表段落都必须翻译
- ❌ **严禁跳过**：不得以"公式较多"、"内容重复"、"段落太短"等任何理由跳过翻译
- ❌ **严禁遗漏**：翻译完成后必须逐段核对原文段落数，确保每个需要翻译的段落都有对应的英文译文和翻译说明

### 支持的文件格式

| 格式 | 输入 | 输出 | 说明 |
|------|------|------|------|
| 📝 `.docx` / `.doc` | ✅ | `原文件名_翻译润色版.docx` | Word文档，完整保留原格式 |
| 📄 `.tex` (LaTeX) | ✅ | `原文件名_翻译润色版.tex` | LaTeX文档，保留所有命令/环境 |

### LaTeX 公式支持
- **Word 文档中**：自动识别 LaTeX 公式语法（`$...$` 行内公式、`$$...$$` 块级公式、`\(...\)` / `\[...\]`），公式内容原样保留不翻译
- **Word 原生公式**：使用 Word 公式编辑器（OMML/MathML）的公式同样保留不动
- **LaTeX 文档中**：所有数学模式内容（`equation`, `align`, `$...$`, `$$...$$` 等）完整保留，仅翻译纯文本

### 核心方法论（源自该书Introduction）
> *"Carefully examine good examples of the kind of writing you would like to produce, identify and master the structure, grammar and vocabulary you see in these examples, and then apply them in your own writing."*

---

## 二、翻译前的稿件分析

### 2.1 识别文档文体类型
根据书中对科研论文IMRaD结构的定义，首先判断原文属于：

**按文件格式分类：**

**A. Word 文档 (.docx/.doc)**
- **研究论文全文** (含Introduction, Methodology, Results, Discussion)
- **论文单个部分** (仅Introduction / Methodology / Results / Discussion / Abstract)
- **综述/报告** (不严格遵循IMRaD)
- **技术说明/商务文档**

**B. LaTeX 文档 (.tex)**
- 识别文档类：`\documentclass{article}` / `{report}` / `{book}` / `{elsarticle}` 等
- 识别章节结构：`\section{}`, `\subsection{}`, `\subsubsection{}` 与 IMRaD 的对应关系
- 识别特殊环境：
  - `\begin{abstract}...\end{abstract}` → 对应 Abstract 部分
  - `\begin{keywords}...\end{keywords}` → 关键词，保留
  - `\maketitle` → 标题区，保留
  - `\begin{equation}...\end{equation}` / `\begin{align}...\end{align}` → 公式保护区
  - `\begin{figure}...\end{figure}` / `\begin{table}...\end{table}` → 浮动体，选择性处理
- 识别 preamble 区域（`\documentclass` 至 `\begin{document}` 之间）→ 完整保留

### 2.2 确定目标读者和用途
- 国际期刊投稿 → 严格遵循书中各单元的模型结构
- 学位论文 → 使用被动语态为主(书中Section 1.2.3)
- 会议报告 → 可适当简化

---

## 三、逐段翻译工作流

### 3.1 Word 文档 (.docx/.doc) 翻译流程

#### 第一步：逐段读取与理解
1. 从Word文档第一段开始，逐段读取中文原文
2. 识别该段落的**功能**（而非仅看内容）——这是Glasman-Deal的核心理念
3. 确定该段落对应论文的哪个部分
4. 记录原段落的格式信息（字体、样式、缩进等），用于英文译文段落格式的设置
5. **检查段落中是否包含 LaTeX 公式**（`$...$` / `$$...$$` / `\(...\)` / `\[...\]`），如有则标记为"含公式段落"

#### 第二步：逐段翻译 + 润色 + 三段式插入
对每一段中文，按以下顺序操作：
1. 将中文段落翻译为英文
2. 根据该段功能应用书中对应的润色规则（见下方）
3. **保留原中文段落格式完全不变**
4. 在原中文段落下方的**新段落**中写入英文译文：
   - 使用**深蓝色（RGB: 0, 51, 153）、斜体**
   - 段落缩进与中文原文保持一致
   - 英文译文内的具体修改处叠加对应的修改颜色（红/蓝/绿/紫，见6.5节）
5. 在英文译文下方再插入**第三个新段落**——中文翻译说明：
   - 字体颜色：**深绿色（RGB: 0, 102, 51）**
   - 字号比正文小0.5-1pt
   - 非斜体，与说明文字风格一致
   - 段前间距0.3行，段后与中文原文段保持一致
   - 内容格式：
     ```
     【翻译说明】本段应用了Glasman-Deal [Unit X, Section X.X]的[规则名称]：[简要说明为何在此处采用该规则]。 
     ```
     或（当未涉及特殊规则时）：
     ```
     【翻译说明】本段为直接翻译，保持原文语义和风格，未涉及书籍特殊规则调整。
     ```

#### 第三步：处理含公式的段落
1. 识别中文段落中的 LaTeX 公式边界（`$...$` 或 `$$...$$`）
2. 翻译时将公式视为不可分割的原子单元，原样保留在译文中
3. 公式周围的文字正常翻译
4. 如果 Word 使用原生公式编辑器（OMML），同样保留不动
5. 在翻译说明中标注：【翻译说明】本段含LaTeX公式/数学表达式，公式内容原样保留。

### 3.2 LaTeX 文档 (.tex) 翻译流程

#### 第一步：解析 .tex 文件结构
1. 读取完整 `.tex` 文件
2. 识别并标记以下区域：
   - **Preamble 区**（`\documentclass` → `\begin{document}`）：完整保留，不做任何修改
   - **数学模式区**：`$...$`, `$$...$$`, `\(...\)`, `\[...\]`, `\begin{equation}...\end{equation}`, `\begin{align}...\end{align}`, `\begin{aligned}...\end{aligned}` 等 → **完整保留**
   - **命令区**：`\cite{}`, `\ref{}`, `\label{}`, `\usepackage{}`, `\newcommand{}` 等 → **完整保留**
   - **注释区**：`% ...` → **保留不动**
   - **自动生成命令**：`\maketitle`, `\tableofcontents`, `\listoffigures`, `\listoftables` → **原位保留**
   - **浮动体**：`\begin{figure}...\end{figure}`, `\begin{table}...\end{table}` → **图注/表注翻译，其余保留**
   - **参考文献区**：`\bibliography{}`, `\bibliographystyle{}`, `\begin{thebibliography}...\end{thebibliography}` → **完整保留**
   - **纯文本段落**：以上区域之外的段落 → **需要翻译**

#### 第二步：逐段翻译纯文本内容
1. 对每个纯文本段落进行翻译
2. 根据段落所在的章节（`\section` / `\subsection` 等）判断其对应论文的哪个部分，应用对应的书中模型
3. LaTeX 命令（如 `\textbf{}`, `\emph{}`, `\textit{}`）的参数内容翻译，但命令本身保留
4. `\caption{...}` 中的内容翻译

#### 第三步：生成三段式 LaTeX 输出
输出文件采用以下组织方式：

```latex
% ============================================
% 中文原文与英文翻译对照
% 翻译基于: Science Research Writing for Non-Native Speakers of English
%           Glasman-Deal, Imperial College Press, 2010
% 原文文件: xxx.tex
% 生成日期: YYYY-MM-DD
% ============================================

% === [原文] ===
中文原文段落内容...

% === [English Translation] ===
English translation content...

% === [翻译说明] ===
% 本节应用了Glasman-Deal Unit 1, Section 1.2.1: 使用Present Perfect表达研究空白，
% 因为此处需要强调该问题与当前研究的相关性。

% === [原文] ===
下一段中文原文...

% === [English Translation] ===
Next English translation...

% === [翻译说明] ===
% 本段为直接翻译，未涉及书籍特殊规则。
```

**双语对照两栏格式（可选）**：
如需生成可编译的双语对照 PDF，可在 preamble 中添加：
```latex
\usepackage{paracol}
```
然后使用 `\begin{paracol}{2}` 实现中英两栏对照。此时翻译说明可以脚注形式添加。

### 3.3 应用书中模型进行翻译

#### 如果是Introduction部分 → 应用Unit 1四组件模型：
```
组件1: 建立研究领域的重要性 + 提供背景事实 + 定义术语 + 呈现问题领域
组件2: 前人/当前研究和贡献（文献综述）
组件3: 定位研究空白 / 描述要解决的问题
组件4: 描述本论文
```

**关键翻译规则（Unit 1）：**
- 开头句：使用Present Perfect（has received much attention）或Present Simple（is a major issue）
- 背景事实：使用Present Simple表达公认事实
- 文献综述：使用Past Simple（showed, demonstrated）+ 作者姓名
- 研究空白：使用However/Although引导，用Present Perfect（little attention has been paid to）
- 本论文描述：使用Present Simple（This paper presents/focuses on）

#### 如果是Methodology部分 → 应用Unit 2四组件菜单模型：
```
组件1: 概述 + 重述目的 + 材料/设备来源 + 必要背景
组件2: 精确细节 + 理由说明 + 展示谨慎操作
组件3: 与已有研究关联
组件4: 指出问题（如适用）
```

**关键翻译规则（Unit 2）：**
- 标准程序：Present Simple被动（is collected, is inserted）
- 你实际做的：Past Simple被动（was collected, was inserted）
- 必须区分以上两者！这是书中强调的最常见错误
- 用in this study, in our experiments标记自己的贡献
- 必须为选择提供理由（justify choices）

#### 如果是Results部分 → 应用Unit 3四组件菜单模型：
```
组件1: 回顾研究目的/已有研究 + 回顾/扩展方法论 + 结果总览
组件2: 邀请查看图表 + 具体关键结果详情 + 与其他研究比较
组件3: 结果中的问题
组件4: 结果的可能含义
```

**关键翻译规则（Unit 3）：**
- 使用主观评价语言（significantly lower, dramatically increased）而非纯客观描述
- "Results do not speak for themselves" — 必须用文字解释结果的含义
- 频率语言准确使用（always → generally → frequently → sometimes → rarely → never）
- 数量语言影响读者感知（as many as 45% vs only 45%）
- 因果关系表达要有适当力度（caused vs was linked to vs may have been related to）

#### 如果是Discussion/Conclusion部分 → 应用Unit 4四组件模型：
```
组件1: 回顾前文 + 总结关键结果
组件2: 映射（与已有研究的关系）
组件3: 成就/贡献 + 深化含义
组件4: 局限性 + 当前和未来工作 + 应用
```

**关键翻译规则（Unit 4）：**
- 开头回顾前文（不要随机选择，回顾最重要的方面）
- 使用情态动词控制论断强度：may/might/could（可能）→ should/ought to（很可能）→ must（几乎确定）
- 明确指出贡献和成就（不要害羞！）
- 局限性应指向未来研究方向

#### 如果是Abstract部分 → 应用Unit 5双模型：
- **Model 1** (结构型): Background → Aim → Method → Results → Implications
- **Model 2** (结果导向型): 论文做了什么 + 方法 + 关键结果（更常见）

### 3.4 应用本书专属润色规则

#### 3.4.1 时态检查（书中最重要的语法点）
- [ ] Present Simple vs Present Continuous区分正确
- [ ] Past Simple vs Present Perfect区分正确
- [ ] Past Simple用于特定研究（showed），Present Perfect用于与现在相关的研究空白
- [ ] 在Abstract中时态一致且意义准确

#### 3.4.2 信号语检查（Section 1.2.2）
确保使用正确的连接词：
- **因果**: due to, because, since, on account of
- **结果**: therefore, consequently, hence, as a result
- **对比**: however, whereas, while, by contrast, on the other hand
- **意外**: although, even though, despite, nevertheless, nonetheless
- **添加**: in addition, moreover, furthermore, also

#### 3.4.3 被动/主动语态检查（Section 1.2.3 & 2.2.1）
- 研究团队可用we
- 个人研究用passive或dummy subject（This paper/This study）
- 明确区分标准程序（Present Simple被动）和你的操作（Past Simple被动）

#### 3.4.4 冠词检查（Section 2.2.2）
- 核心原则：**Use THE if both you and your reader know which thing/person you mean**
- **Use A if it doesn't matter or your reader doesn't know which**
- 检查每个the/a/∅的使用

#### 3.4.5 副词位置检查（Section 2.2.3）
- 避免歧义副词簇
- 修饰整句的副词放在句首
- 复杂副词关系拆分为短句

#### 3.4.6 段落组织检查（Section 1.2.4）
- 每段以主题句开头
- 一段一个主题
- 避免单句段落或过长段落

---

## 四、词汇应用（基于全书词汇表）

### 4.1 Introduction词汇
**建立重要性**: much research in recent years, plays a key role, of growing interest, widely recognised, considerable recent research interest, a major issue

**前人研究动词**: achieved, addressed, analysed, demonstrated, established, identified, proposed, showed, suggested (完整列表见Unit 1, Section 1.4)

**研究空白**: However, few studies have focused on, little attention has been paid to, remains unclear, not well understood, more work is needed, a limitation

**本论文描述**: This paper presents/focuses on/describes/reports, The purpose of this study is, In this paper we, The present work

### 4.2 Methodology词汇
**概述**: In this study, all tests were, most of the samples, the majority of, was/were carried out/performed/conducted

**精确细节**: was added, was calibrated, was measured, was calculated, was extracted (完整列表见Section 2.4.2)

**理由说明**: in order to, so as to, to enable, to ensure, to prevent, to facilitate, which allowed

**谨慎操作**: carefully, thoroughly, accurately, precisely, at least, immediately, repeatedly, freshly

### 4.3 Results词汇
**概述**: in general, in most cases, it is apparent that, the overall response, on the whole

**邀请查看图表**: as can be seen in Fig., Figure X shows, is displayed in, can be observed from

**主观评价**: significantly, dramatically, strikingly, remarkably, considerably, slightly, marginally

**比较**: consistent with, in good agreement with, in line with, compare well with, contrary to, inconsistent with

**含义**: suggests that, indicates that, implies that, it appears that, it seems that, presumably, potentially

### 4.4 Discussion/Conclusion词汇
**映射**: extends, confirms, contradicts, supports, differs from, is consistent with, provides support for, challenges

**成就**: compelling, dramatic, excellent, novel, remarkable, striking, unprecedented, for the first time

**局限性**: it should be noted that, although, nevertheless, minor deficit, not within the scope of this study

**未来工作**: future work should, further work is needed, should be replicated, remains to be determined

### 4.5 情态动词精确使用
- **may/might/could**: 可能（might稍弱于may）
- **should/ought to**: 很可能
- **must**: 几乎确定（但缺乏实际证据）
- **can**: 能够
- **cannot**: 不可能（不是"可能不"）

---

## 五、输出文档规范

### 5.1 核心原则：三段对照式翻译 + 格式完全保护

**在原文档基础上直接操作**，不创建全新的文档结构。保留原文档的每一页、每一段、每一个元素，仅在每段中文原文的下方依次插入英文译文段落和中文翻译说明段落。

**最关键的约束：不改变原生 Word 的任何格式。** 中文原文的字体、字号、颜色、加粗、斜体、下划线、高亮、段落缩进、行距、段前段后间距、对齐方式、样式模板等一切格式属性均原封不动。

### 5.2 Word 文档 (.docx/.doc) 输出规范

#### 步骤一：读取并保留原文档
1. 完整读取原始.docx/.doc文件
2. 保留所有原始格式：
   - 字体、字号、颜色、加粗、斜体、下划线、高亮
   - 段落缩进、行距、段前段后间距、对齐方式
   - 页码、页眉、页脚
   - 章节标题的样式（Heading 1/2/3等）
   - 样式模板和主题
3. 保留所有非文本元素：
   - 表格（含表格样式、合并单元格）
   - 图片、图表（含图注）
   - **公式**（含LaTeX公式语法 `$...$` / `$$...$$`、Word原生公式OMML/MathML、公式编号）
   - 超链接
   - 分页符、分节符

#### 步骤二：逐段翻译并三段式插入
对文档正文中的每一段中文：
1. 读取当前段落 → **保留其格式完全不动**
2. 检查段落中是否包含 LaTeX 公式语法或数学表达式，如有则标记
3. 翻译该段为英文 → 进行书中规则润色 → 公式原样保留
4. 在该段下方**插入新段落**，写入英文译文：
   - 与上方中文段落使用相同的段落样式基础
   - **字体颜色设为深蓝色（RGB: 0, 51, 153）**以视觉区分
   - **字体设为斜体**，进一步与中文原文区分
   - 段落缩进与中文段保持一致
   - 段前间距0.5行
5. 在英文译文下方**再插入新段落**，写入中文翻译说明：
   - **字体颜色设为深绿色（RGB: 0, 102, 51）**
   - 字号比正文小0.5-1pt
   - 非斜体，使用常规字体
   - 段前间距0.3行
   - 内容格式为 `【翻译说明】...`

#### 步骤三：格式保护
- 中文原文段落的格式**完全不变**
- 不删除、不移动任何原始内容
- 表格中的文字单独处理：在表格单元格内翻译，译文和说明放在同一单元格原文下方（用换行符分隔）
- 图注/表注：在图注下方依次插入英文翻译和翻译说明

### 5.3 最终文档结构示例

```
[原文档标题 - 保留原格式]

[中文段落1 - 原格式完全不变]
[↓ 英文译文段落1 - 深蓝色、斜体]
[↓ 翻译说明段落1 - 深绿色、小字号]

[中文段落2 - 原格式完全不变]
[↓ 英文译文段落2 - 深蓝色、斜体]
[↓ 翻译说明段落2 - 深绿色、小字号]

[原文档中的表格 - 保留不动]
[表注中文 - 保留不动]
[↓ 表注英文翻译 - 深蓝色、斜体]
[↓ 表注翻译说明 - 深绿色、小字号]

[中文段落3 - 原格式完全不变（含LaTeX公式 $E=mc^2$）]
[↓ 英文译文段落3 - 深蓝色、斜体（公式 $E=mc^2$ 原样保留）]
[↓ 翻译说明段落3 - 深绿色: 【翻译说明】本段含LaTeX行内公式，公式内容原样保留。翻译采用Unit 1...]
```

### 5.4 LaTeX 文档 (.tex) 输出规范

#### 文档命名
生成新文档：`原文件名_翻译润色版.tex`
保存位置：与原文件相同目录

#### Preamble 处理
- `\documentclass{...}`、`\usepackage{...}`、`\newcommand{...}` 等所有 preamble 内容**完整保留**
- 如果原文 preamble 缺少中文支持，可自动添加（但不删除已有配置）：
  ```latex
  % 如需要中文编译支持，添加以下宏包（已自动添加）
  % \usepackage[UTF8]{ctex}
  ```

#### 正文翻译组织方式（默认：注释对照式）
```latex
\begin{document}

% ============================================
% 翻译说明
% 基于: Science Research Writing for Non-Native Speakers of English
%       Glasman-Deal, Imperial College Press, 2010
% ============================================

% === [原文] ===
\section{引言}

近年来，机器学习在医学影像分析中得到了广泛应用...

% === [English Translation] ===
% In recent years, machine learning has been widely applied in medical image analysis...

% === [翻译说明] ===
% 本段应用了Glasman-Deal Unit 1, Section 1.2.1: 开头句使用Present Perfect
% (has been widely applied) 建立研究领域的重要性，符合Introduction组件1的写作模型。

% === [原文] ===
然而，关于小样本学习的应用仍然存在诸多挑战...

% === [English Translation] ===
% However, many challenges remain regarding the application of few-shot learning...

% === [翻译说明] ===
% 本段应用了Unit 1, Section 1.2.1: 使用However + Present Simple (remain) 
% 来定位研究空白，这是Introduction组件3的标准写法。
```

#### 环境选择性处理规则
| LaTeX 环境 | 处理方式 |
|------------|----------|
| `abstract` | 翻译内容，保留环境 |
| `equation` / `align` / `eqnarray` | **完整保留** |
| `figure` | 保留环境，翻译 `\caption{}` |
| `table` | 保留环境和表格主体，翻译 `\caption{}` 和单元格中的纯文本 |
| `thebibliography` | **完整保留** |
| `keywords` | 翻译关键词 |
| `algorithm` | 保留环境和伪代码，翻译 `\caption{}` |
| `lstlisting` / `verbatim` | **完整保留** |
| 用户自定义环境 | 保守处理，保留环境和内容 |

#### 命令选择性处理规则
| LaTeX 命令 | 处理方式 |
|------------|----------|
| `\cite{}`, `\ref{}`, `\label{}`, `\pageref{}` | **完整保留** |
| `\textbf{}`, `\textit{}`, `\emph{}` | 保留命令，翻译参数内容 |
| `\section{}`, `\subsection{}` | 保留命令，翻译标题内容 |
| `\caption{}` | 保留命令，翻译图注/表注 |
| `\footnote{}` | 保留命令，翻译脚注内容 |
| `\url{}`, `\href{}` | **完整保留** |
| `\maketitle`, `\tableofcontents` | **原位保留** |
| `\includegraphics{}` | **完整保留** |

### 5.5 修改标注颜色系统
英文译文中的润色修改通过以下颜色标识：

| 颜色 | 含义 | 适用范围 |
|------|------|----------|
| 🔴 **红色** | 语法错误修正 | 时态、冠词、主谓一致、拼写等 |
| 🔵 **蓝色** | 句子结构优化 | 拆分长句、消除歧义、调整语序 |
| 🟢 **绿色** | 用词改进 | 替换模糊/不精确词汇为学术词汇 |
| 🟣 **紫色** | 风格/语体调整 | 正式化、符合学科惯例 |

注意：以上颜色用于标注英文译文**内部的润色修改痕迹**（在英文段内以不同颜色字体区分修改部分）。英文译文整体的默认颜色为深蓝色（与中文原文区分），具体某处修改再叠加上述颜色。翻译说明段落始终使用**深绿色**，不叠加修改颜色。

### 5.6 批注要求
对英文译文中的重大修改，使用Word批注功能添加说明，格式：
```
【修改类型】[语法/结构/用词/风格]
【修改原因】引用书中具体章节和原则
【效果说明】为什么这样改更好
```

### 5.7 翻译润色报告
在文档末尾（最后一段翻译说明之后）添加"翻译润色报告"页（新页），包含：

1. **总览**：原文段落数、总字数、翻译字数、含公式段落数
2. **修改统计**：
   - 总修改次数
   - 按类型分布（语法N处、结构N处、用词N处、风格N处）
3. **书中规则应用统计**：各部分应用了哪些书中模型和规则
4. **重点修改类别**：最常见的问题类型及频次
5. **各部分处理说明**：
   - Introduction：应用的模型和修改要点
   - Methodology：时态/被动语态检查结果
   - Results：评价语言使用情况
   - Discussion：成就声明和局限性处理
6. **LaTeX公式处理**（如适用）：公式保留数量
7. **整体质量评估**（基于Glasman-Deal标准）
8. **进一步改进建议**

---

## 六、书中重点常见错误排查清单

翻译完成后逐项检查：

### Critical Errors (书中强调的严重错误)
- [ ] 自己的工作和标准程序时态混淆（Section 2.2.1）
- [ ] 引用参考文献的位置不当，导致"credit"归属错误（Section 2.3.2）
- [ ] 研究空白未用Present Perfect而误用Past Simple（Section 1.2.1）
- [ ] 结果纯客观描述未加主观评价（Section 3.2.3）

### Major Errors
- [ ] 句子间缺乏连接词/信号语（Section 1.2.2）
- [ ] a/the/∅使用错误（Section 2.2.2）
- [ ] 副词位置造成歧义（Section 2.2.3）
- [ ] 未为方法论选择提供理由（Section 2.3.2）
- [ ] 在Discussion中没有明确陈述成就（Section 4.3.2）

### Minor Errors
- [ ] 重复使用however和therefore，未使用多样化信号语
- [ ] 段落过长或过短
- [ ] 标题中复合名词过多造成歧义

---

## 七、特殊处理规则

### 7.1 专业术语
- 保持统一译法，首次出现时给出全称+缩写
- 参考原文领域的国际期刊术语使用习惯

### 7.2 图表引用
- 使用书中标准表达：as shown in Fig., can be seen from, is displayed in
- from表示"从图表中推断"，in表示"出现在图表中"

### 7.3 引用和参考文献
- 保持原格式
- 引用位置准确：放在被引用信息之后，而非总是句尾

### 7.4 数学公式和特殊符号
- 保留原样
- 公式编号格式统一
- **LaTeX 公式**（`$...$` / `$$...$$` / `\(...\)` / `\[...\]`）在 Word 中识别后原样保留
- **Word 原生公式**（OMML/MathML）直接保留对象

### 7.5 LaTeX 文件特殊处理

#### 7.5.1 自动生成命令
以下命令在原位保留，不做任何修改：
- `\maketitle` — 标题生成
- `\tableofcontents` — 目录
- `\listoffigures` — 插图目录
- `\listoftables` — 表格目录
- `\printbibliography` — biblatex 参考文献

#### 7.5.2 浮动体处理
- `\begin{figure}...\end{figure}`：图片路径（`\includegraphics{}`）和排版参数保留不变，仅翻译 `\caption{}` 中的内容
- `\begin{table}...\end{table}`：表格结构（`tabular`/`tabularx` 等）保留不变，翻译 `\caption{}` 和单元格中的纯文本内容
- `\begin{algorithm}...\end{algorithm}`：伪代码保留，翻译 `\caption{}`

#### 7.5.3 自定义宏/命令
- `\newcommand{...}{...}`、`\renewcommand{...}{...}`、`\newenvironment{...}{...}{...}` 等定义区完整保留
- 未知的自定义命令保守处理：完整保留不翻译

#### 7.5.4 参考文献
- `\bibliography{...}` — 完整保留
- `\bibliographystyle{...}` — 完整保留
- `\begin{thebibliography}...\end{thebibliography}` — 完整保留
- `\cite{}`, `\citep{}`, `\citet{}` — 完整保留

#### 7.5.5 中文支持
如果原文 `.tex` 文件的 preamble 中缺少中文编译支持，生成的新文件应自动添加必要的配置：
- 对于 pdfLaTeX：`\usepackage[UTF8]{ctex}`
- 对于 XeLaTeX/LuaLaTeX：`\usepackage{xeCJK}` 或 `\usepackage{ctex}`

### 7.6 Word 中 LaTeX 公式处理

#### 识别模式
| 公式类型 | 语法模式 | 示例 |
|----------|----------|------|
| 行内公式 | `$...$` | `$E = mc^2$` |
| 行内公式 (LaTeX) | `\(...\)` | `\(x^2 + y^2 = z^2\)` |
| 块级公式 | `$$...$$` | `$$\sum_{i=1}^n x_i$$` |
| 块级公式 (LaTeX) | `\[...\]` | `\[\int_0^\infty f(x)dx\]` |

#### 处理规则
1. 公式内容（包括数学符号、LaTeX 数学命令、上下标、分式、矩阵等）**完全不翻译**
2. 公式编号（如 `\tag{1}`、`\label{eq:1}`）保留不动
3. 公式前后的中文文字正常翻译，公式作为原子插入译文
4. 翻译示例：
   - 原文：`由公式 $E = mc^2$ 可知，能量与质量成正比。`
   - 译文：`From the equation $E = mc^2$, it can be seen that energy is proportional to mass.`
   - 说明：`【翻译说明】本段含LaTeX行内公式，公式原样保留。应用Unit 3的结果描述模式。`
5. 如果 Word 段落中混用 Word 原生公式和 LaTeX 公式，两者均保留

---

## 八、质量保证标准

1. 所有翻译修改必须能在书中找到依据
2. 不凭空创造规则
3. 不改变原文学术含义
4. 翻译准确度优先，其次才是语言流畅度
5. 对不确定之处保守处理，标注供作者确认
6. **Word 文档**：中文原文格式100%不变，仅做翻译插入
7. **LaTeX 文档**：所有 LaTeX 命令、环境、数学公式完整保留，仅翻译纯文本内容
8. 三段式输出的每一段（中文原文、英文翻译、翻译说明）层次清晰，互不干扰
9. 翻译说明必须具体、有针对性，说明采用了书中哪个具体章节的哪条规则
