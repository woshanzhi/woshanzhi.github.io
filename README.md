# woshanzhi.github.io

这是我的个人博客仓库，已经重构为一个**简洁、便于长期写作的 Jekyll + Chirpy 结构**。

## 现在的项目结构

- `_config.yml`：博客全局配置
- `index.html`：首页
- `_posts/`：所有博客文章都放这里
- `_tabs/about.md`：关于页面
- `_data/authors.yml`：作者信息
- `Gemfile`：本地运行依赖
- `README.md`：维护说明

以后写博客，最常用的其实只有两个地方：

- `_posts/`
- `_tabs/about.md`

---

## 如何写新博客

### 1. 新建一篇文章

在 `_posts/` 目录下新建文件，文件名格式必须是：

```text
YYYY-MM-DD-title.md
```

例如：

```text
2026-04-16-my-first-note.md
```

### 2. 文章开头写 Front Matter

每篇文章开头都要有：

```yaml
---
title: 我的第一篇博客
date: 2026-04-16 10:00:00 +0800
categories: [学习笔记]
tags: [Jekyll, GitHub Pages]
---
```

### 3. 正文直接用 Markdown 写

推荐用这个固定模板：

```markdown
## 背景

## 问题

## 原因分析

## 解决方法

## 总结
```

以后写：

- 论文写作经验
- 实验记录
- 工具踩坑
- 阅读论文总结

都会很顺。

---

## 本地运行

先安装 Ruby 和 Bundler，然后在项目根目录执行：

```bash
bundle install
bundle exec jekyll serve
```

浏览器打开：

```text
http://127.0.0.1:4000
```

---

## 发布到 GitHub Pages

你这个仓库名本身就是 `woshanzhi.github.io`，所以只要把内容推送到 GitHub，通常就能直接作为个人站点发布。

如果 GitHub Pages 没自动生效，可以去仓库设置里检查：

- `Settings`
- `Pages`
- 部署分支是否为默认分支

---

## 后续最常做的事

### 修改博客信息
改 `_config.yml`：

- 博客标题
- 简介
- GitHub 链接
- 时区
- 首页显示设置

### 修改关于页
改 `_tabs/about.md`

### 写文章
直接往 `_posts/` 新增 Markdown 文件

---


## 适合后面写的博客主题

- 论文图片格式选择
- LaTeX / Word 排版经验
- PlotNeuralNet 使用记录
- 深度学习实验笔记
- RISC-V 学习记录
- 嵌入式开发踩坑总结
