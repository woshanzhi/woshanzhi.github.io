# woshanzhi.github.io

我的个人博客仓库，基于 **Jekyll + Chirpy** 主题构建，便于长期写作与一键部署。

---

## 📁 项目结构

| 文件/目录 | 说明 |
|-----------|------|
| `_config.yml` | 全局站点配置 |
| `index.html` | 博客首页 |
| `_posts/` | 所有博客文章（Markdown 格式） |
| `_tabs/about.md` | “关于我”页面 |
| `_data/authors.yml` | 作者信息配置 |
| `Gemfile` | 本地运行所需的依赖 |

> 💡 **日常维护只需关注**：  
> - `_posts/` 新增/编辑文章  
> - `_tabs/about.md` 更新个人介绍

---

## ✍️ 如何撰写新博客

### 1. 新建文章文件

在 `_posts/` 目录下创建文件，**文件名必须遵循以下格式**：
YYYY-MM-DD-title.md

**示例**：  
`2026-04-16-my-first-note.md`

---

### 2. 添加 Front Matter（文件头信息）

每篇文章开头必须包含 YAML 格式的 Front Matter，示例如下：

```yaml
---
layout: post
title: "文章标题"
date: 2026-07-08
tags: [tag1, tag2, tag3]
toc: true
comments: false
author: your_name
---

tags 是文章标签，可以有 0 个或多个。
toc 用于控制是否开启文章侧栏目录。
comments 用于控制是否开启文章评论区。