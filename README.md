# woshanzhi.github.io

我的个人博客仓库，基于 **Jekyll + Chirpy** 结构，便于长期写作和部署。

## 项目结构

- `_config.yml`：全局配置
- `index.html`：首页
- `_posts/`：所有博客文章（Markdown）
- `_tabs/about.md`：关于页面
- `_data/authors.yml`：作者信息
- `Gemfile`：本地运行依赖

日常写作只需关注：
- `_posts/` 新增文章
- `_tabs/about.md` 修改个人介绍

---

## 如何写新博客

### 1. 新建文章文件
在 `_posts/` 目录下，文件名格式：`YYYY-MM-DD-title.md`  
例如：`2026-04-16-my-first-note.md`

### 2. 添加 Front Matter（文件开头）
```yaml
---
title: 我的第一篇博客
date: 2026-04-16 10:00:00 +0800
categories: [学习笔记]
tags: [Jekyll, GitHub Pages]
---
---

## 后续维护

### 1. 修改博客标题、描述等 → 编辑 _config.yml

### 2. 修改关于页内容 → 编辑 _tabs/about.md

### 3. 写文章 → 在 _posts/ 新增 Markdown 文件