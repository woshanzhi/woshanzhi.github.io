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
- 引用评分：7.7
- 收录：SCI 检索、Open Access 可选
- 主攻方向：图像解析、计算机视觉、人脸识别、生物特征、场景建模、监控视觉、多模态视觉等，**完全适配视觉隐私、人脸识别方向论文**

查看分区相关信息可以查询中科院期刊分区表

### 1.2 官方权威链接
- 期刊作者指南（必看）：https://www.sciencedirect.com/journal/image-and-vision-computing
- Elsevier 官方 LaTeX 模板说明：https://www.elsevier.com/authors/policies-and-guidelines/latex-instructions


改代码加数据不等于水
很多同学觉得只有从零搞一个全新的算法才算创新。其实完全不是这样。很多paper里大部分都是在现有工作基础上做改进的。
	
关键不在于你改了多少代码,而在于你的改动解决了什么问题,带来了什么新的insight。问题是你得搞清楚，为什么要加这些数据,加了之后解决了什么问题,带来了多少提升,为什么会有这样的提升。如果你能把这些问题回答清楚,你的工作就有价值。
	
看看你的工作有没有这些
是否解决了一个真实存在的问题。可以是现有方法的局限性,可以是某个特定场景下的需求。如果只是为了改而改,没有明确的问题导向,那确实比较危险。
	
改进是否有充分的motivation。为什么要这么改,这个改动的理论依据是什么。这些问题你得想清楚并且能说服别人。
	
实验是否充分。至少要在3个以上的数据集上验证,要有消融实验,要有跟state-of-the-art方法的对比。提升幅度一般来说在主流数据集上涨2到3个点以上会比较有说服力。
	
怎么把工作写得有深度
把motivation写透。不要只说现有方法效果不好,要分析为什么不好,是哪个环节出了问题。最好能有一些实验或者可视化来支撑你的分析。
	
实验部分要有分析而不只是堆数字。要分析为什么涨点,在什么情况下涨得多,什么情况下涨得少。做一些失败案例分析,说明你的方法的局限性在哪。
	
related work要梳理清楚。把你的工作放在整个领域的发展脉络里,说清楚你的工作跟已有工作的区别和联系。
	
投还是不投
如果你确实解决了一个有价值的问题,方法有清晰的motivation,实验结果有说服力,那就大胆投。就算被拒了也没关系,审稿意见会告诉你哪里做得不够好。
	
反过来,如果你自己都说不清楚你的工作解决了什么问题,或者实验只在一个数据集上跑了一次,那我建议你先把工作做扎实再投。与其投出去被拒,不如多花点时间把实验做完整。

投稿时需要参考guide-for-authors，可以查看所需要提交的文件以及一些要求
---
2.选刊。在自己文章水平内的，不要妄自菲薄也不要好高骛远。但可以冲一下比自己好一点的期刊。(去期刊官网)大致浏览他们的工作。(两个网站:爱科学，letpub)
3.选刊完成之后，官网主页找到Guide forauthors，查询你需要做的事，例如格
式，图片，投稿的要求。
4.按照要求改完之后，准备好自己的所有文件，创一个文件夹里面放所有需要
提交的单独文件，例如:Graphical Abstract，Highlights模板，CoverLetter模板，
declarationStatement, manuscript.
5.登录期刊官网账号，准备提交。
9.完成提交后会跳转页面。这时候需要检查自己提交的有没有问题，选择view PDF，
检查。检查没问题后点击approve提交成功。

注意:
1.关注重要的节点，例如revise的截止时间。2.第一次投稿的手稿自己要对他百分百熟悉，说一个点能立马知道在什么位置，说了什么。格式，文字，图表整理完全一致，增加审稿人印象分，因为图片和文字内容，格式决定了审稿人读的舒不舒服，读的不舒服肯定不给你好评。3.修改稿:首先观察审稿人对的评价，是正向还是反向，正向的话要好好对待。反向不知道。其次对于审稿人的话需要谨慎对待，让补实验的话，能补就补，这个看每个人的感觉，因为你自己的文章自己肯定是最熟悉的。可以保留他的意见，但可以不做，做出自己的解释。
4.修改稿同样要通顺逻辑有序。可能加了实验和内容，导致文章不连续，这里需要自己完善。其次，修改稿自己也要无限熟悉，跟第一次手稿一样。


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


写的时候可以使用Einsia这个插件，目前支持谷歌浏览器，可以使用到ai模型。
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


第一次投稿期刊时可以先不提交数据根据
Select an option that describes the availability of your research data
选择no 
Data will be made available on request需要的时候再提供


免费预印本服务
本期刊提供免费服务，将您的手稿作为预印本发布在ssRN7，爱思唯尔的预印本和早期研究档案库。选择加入后，您的提交手稿将在通过期刊的初步桌面审查后立即在ssRN上公开可用。(注意:一小部分期刊在提交时发布)。
作为SSRN上的预印本，您的手稿将受益于:
提前注册并获得预印本DOI(数字对象标识符)如果在该爱思唯尔期刊上正式发表，请将预印本链接至正式版本。预印本发布、共享和下载，从而促进合作和早期引用
您决定是否发布预印本将不会对期刊的编辑过程或出版结果产生任何影响。要了解更多信息，请阅读SsRN使用条款7和常见问题7或访问期刊的Guide for Authors 7输入:.
你想早期分享你的研究吗作为preprint7?
是的，我想在预印本阶段早期且公开地分享我的研究。
不，我不想在预印本阶段早期公开分享我的研究。

需要选择no 如果选择yes会让论文提前公开，但是没有DOI，导致不能在其他地方投稿了



投稿时尽量用通讯作者的邮箱账号登录投，方便一些，我是一作投稿，后面需要通讯作者登录来确认，投稿之后作者们会受到信息需要ORCID记录，可以按要求注册就可以了