
**文件名：`2026-07-14-journal-latex-template.md`**

---
layout: post
title: "Image and Vision Computing 期刊投稿｜Elsevier LaTeX 模板完整使用指南"
date: 2026-07-14
tags: [论文, SCI期刊, LaTeX, Elsevier, Image and Vision Computing]
toc: true
comments: true
author: 日暮秋烟起
---

# Image and Vision Computing 期刊投稿｜Elsevier LaTeX 模板完整使用指南

## 一、期刊简介与投稿入口
本文以 **Elsevier 旗下 SCI 期刊 Image and Vision Computing** 为例，整理官方投稿规范、LaTeX 模板选择、写作配置与投稿注意事项。

### 1.1 期刊基本信息
- 期刊：Image and Vision Computing
- 出版社：Elsevier
- Impact Factor：5.0
- CiteScore：7.7
- 收录：SCI 检索、Open Access 可选
- 主攻方向：图像解析、计算机视觉、人脸识别、生物特征、场景建模、监控视觉、多模态视觉等，**完全适配视觉隐私、人脸识别方向论文**

### 1.2 官方权威链接
- 期刊作者指南（必看）：https://www.sciencedirect.com/journal/image-and-vision-computing
- Elsevier 官方 LaTeX 模板说明：https://www.elsevier.com/authors/policies-and-guidelines/latex-instructions

---

## 二、Elsevier 三类官方 LaTeX 模板区别
Elsevier 提供三种主流投稿模板，**核心区别为参考文献格式**，投稿前务必对照期刊往期论文格式选择：

1. **`elsarticle-template-num.tex`**
   - 数字顺序引用 `[1], [2]`
   - **绝大多数 CV/视觉期刊默认使用（本文选用）**

2. **`elsarticle-template-num-names.tex`**
   - 数字引用 + 作者名展示
   - 较少使用

3. **`elsarticle-template-harv.tex`**
   - 哈佛格式（作者年份）
   - 视觉类期刊几乎不用

> 建议：**Image and Vision Computing 统一使用 num 数字引用模板**。

### 模板使用方式
1. 从 Elsevier 官网下载 `elsarticle.zip` 压缩包
2. 直接上传至 Overleaf 在线编译
3. 以 `elsarticle-template-num.tex` 作为主文件开始写作

---

## 三、标准论文结构填写规范（可直接复用）

### 3.1 基础头部信息
```latex
\title{你的论文标题}
\author{作者姓名}
\affiliation{学校、学院、地址信息}
```
- 多单位、跨校作者可叠加多个 `\affiliation`

### 3.2 核心模块顺序（期刊强制顺序）
```latex
\begin{abstract}
论文摘要
\end{abstract}

% 图形摘要（Elsevier 期刊特有）
\begin{graphicalabstract}
\includegraphics[width=0.96\textwidth]{xxx.pdf}
简要图形说明文字
\end{graphicalabstract}

% 创新点 Highlights（必填）
\begin{highlights}
\item 创新点1
\item 创新点2
\item 创新点3
\end{highlights}

% 关键词
\begin{keyword}
关键词1, 关键词2, 关键词3
\end{keyword}
```

### 3.3 正文层级
```latex
\section{Introduction}        % 一级标题
\subsection{Related Work}      % 二级标题
\subsubsection{Detail}        % 三级标题
```
- LaTeX **空行自动分段**，无需手动缩进

### 3.4 图片与公式
- 图片锁定位置：`[H]` 强制固定排版位置
```latex
\begin{figure}[H]
\centering
\includegraphics[width=0.96\textwidth]{xxx.pdf}
\caption{caption}
\label{fig:xxx}
\end{figure}
```
- 公式使用标准 `equation` 环境

### 3.5 参考文献配置
两种方式任选其一：

#### 方式1：bib 自动生成（推荐）
```latex
\bibliographystyle{unsrt}
\bibliography{reference}
```
- `unsrt`：**按正文引用顺序排序**，最适配 CV 期刊

#### 方式2：手动 bibitem
```latex
\begin{thebibliography}{99}
% 参考文献
\end{thebibliography}
```
- `{99}` 代表支持最多两位数文献编号

### 3.6 分页
```latex
\clearpage
```

### 3.7 正文引用
```latex
\cite{paper1}
```

---

## 四、必备宏包配置（适配视觉论文）
在模板默认基础上，**视觉/人脸识别论文建议全部添加**，解决公式、表格、子图、算法排版问题：

```latex
\usepackage{mathptmx}
\usepackage{newtxmath}
\usepackage{mathstyle}

\usepackage{booktabs}
\usepackage{multirow}
\usepackage{graphicx}
\usepackage{float}
\usepackage{algorithm}
\usepackage{algorithmic}
\usepackage{url}
\usepackage{hyperref}
\usepackage{caption}
\usepackage{subcaption}
\usepackage{indentfirst}
\usepackage{amsmath,bm}

% 超链接配色（期刊要求黑白）
\hypersetup{colorlinks=true,citecolor=black,linkcolor=black,urlcolor=black}
\pagestyle{plain}
```

---

## 五、Elsevier 投稿硬性规则（避坑重点）
1. **禁止二级文件夹**
   所有图片、tex、bib、sty 文件必须**全部放在根目录**，投稿系统不识别子文件夹。

2. **插图优先 PDF 矢量图**
   论文所有图片统一 `.pdf` 格式，高清无模糊，符合期刊印刷标准。

3. **首次投稿可仅上传 PDF**
   大修/终稿再上传全套源码。

4. **图形摘要 Graphical Abstract 为 Elsevier 期刊必填项**

---

## 六、个人总结
1. 视觉方向论文首选 **Image and Vision Computing**，审稿速度适中、认可度高、适配人脸隐私、视觉识别研究。
2. 固定使用 **num 数字引用模板**，适配期刊格式。
3. 全套宏包直接复用，无需每次重新配置。
4. 所有图片使用 PDF、文件平铺根目录，**完美规避投稿格式问题**。
```

---
