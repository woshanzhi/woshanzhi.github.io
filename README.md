



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

这个仓库现在使用 **GitHub Actions** 部署博客，而不是直接把仓库内容当作普通静态文件展示。

### 第一步：推送代码到默认分支

把当前修改推送到 GitHub 的默认分支（通常是 `main`）。

### 第二步：到 GitHub 打开 Pages 设置

进入：

- `Settings`
- `Pages`

然后把 `Build and deployment` 的 `Source` 设置为：

- `GitHub Actions`

### 第三步：等待工作流自动部署

以后每次你推送新文章或修改配置时，GitHub 都会自动重新构建博客。

你可以在这里查看部署状态：

- `Actions`
- `Deploy Jekyll site to Pages`

如果部署成功，访问：

- `https://woshanzhi.github.io`

就会看到真正的博客网页，而不是仓库 README 页面。

### 如果网站还是旧内容

可以按这个顺序检查：

1. `Actions` 里最新工作流是否成功
2. `Settings -> Pages` 的来源是否已切到 `GitHub Actions`
3. 浏览器是否缓存了旧页面，尝试强制刷新
4. 等待 1~5 分钟让 GitHub Pages 完成更新

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


## 后面可能会写的博客主题

修改 README.md 文件
README.md 文件是对仓库的说明，一般来说第一行标题都是仓库名称，后面就是关于仓库的一些介绍。我只填写了最简要的说明，你可以根据你自己的情况来写，或者不写也可以，它并不影响我们的网站页面。

要修改文件可直接点击文件名称，然后点击右上角的笔图案，即可开始编辑。

点击笔

.md 文件是 markdown 文件，使用的是 Markdown 语言。这一易学易用的语言将 HTML 里的一些常见标签都用带有特殊含义的符号来表示，大大方便了文档的书写。我们的博客文章也需要用 Markdown 进行写作。

github 支持对 markdown 文件进行预览。当在 github 上对 markdown 文件进行编辑的时候，点击 Edit 旁边的 Preview，即可预览当前的页面效果。这在编辑过程中经常用来检查文章排版是否符合预期。

切换预览

修改 _config.yml 文件
_config.yml 文件是博客网站的核心配置文件，里面包含了你想要显示在网站上的各种构造信息。下面我会一步一步告诉你哪些信息需要改。

网站名称和网站描述

名称和描述

这个根据你自己的喜好来设置，不一定要仿造我的模式。比如你可以给你的博客网站取一个有特色的名字，网站描述也可以是简短的自我介绍或个性签名等任何你想表达的内容。

个人头像和网站 logo

头像和 logo

avatar 代表头像，后面的链接是你想显示在页面的头像图片的 url。favicon 指网站图标，即显示在浏览器标签页和收藏夹里的 logo，通常以 32 * 32 像素大小的 .ico 图片为宜，也可以不设置。

咱博客网站里的所有图片不是上传到 github 仓库里就可以显示到页面上了，需要用到图床。我用的是 PicGo，只要与 github 仓库绑定就可以实现上传，且可以一键复制为 Markdown 形式，方便写文时插入图片。

PicGo 设置

Markdown 形式

个人社交链接

社交链接

填用户名就好，也可以不填。

脚注和网址

版权标注和网址

Gitalk 配置信息

Gitalk 配置

Gitalk 用于给博客文章引入评论功能，配置方法请参考 https://github.com/gitalk/gitalk?tab=readme-ov-file#usage。

其他

如果你不知道改了之后会有什么后果，不要去动它。

清空 _posts 文件夹
_posts 文件夹里放的是博客文章，你以后的文章也要放在这里。现在你的 _posts 文件夹里面放的还是我的文章，请把它们全部删除。直接在 GitHub 上操作似乎不支持批量删除文件，一个快捷的方法是删除整个文件夹再新建一个空文件夹，将其命名为“_posts”即可。

清空 images 文件夹
images 文件夹里放的是需要显示在网站上的图片。与 _posts 文件夹一样，这个文件夹也需要清空（删除文件夹并重建）。

修改 about.md 文件
about.md 里的内容是展示在“关于”页面上的。

好了，以上就是所有必须要你修改的文件。你现在再点进去你的博客页面看看，不出意外的话应该是成功修改了的。

Step 3. 开始写你的第

在 README.md 部分我有提到过怎么在 github 上编写 Markdown 文件，写文章也是一样的道理。当然，你完全可以在其他地方编辑你的文章源码，再上传到博客仓库，这其实也是我更为推荐的方法。

文章文件名请按照下面的例子呈现的格式命名：

2024-01-25-letter_to_you.md
还有一点需要注意，每篇文章开头记得附上说明，格式如下：

---
layout: post
title: "文章标题"
date: 2024-01-27
tags: [tag1, tag2]
toc: true
comments: false
author: xxx
---
tags 是文章标签，可以有 0 个或多个。
toc 用于控制是否开启文章侧栏目录。
comments 用于控制是否开启文章评论区。

- 论文图片格式选择
- LaTeX / Word 排版经验
- PlotNeuralNet 使用记录
- 深度学习实验笔记
- 嵌入式开发踩坑总结
