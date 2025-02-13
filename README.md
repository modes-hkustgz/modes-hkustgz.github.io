# 主页修改手册
**本手册的目的是便于直接在github仓库中对老师的个人主页进行修改，确保任何人使用手册都能够快捷完成主页更新任务**

![老师的照片](images/Xiaotong_Portrait_2019-683x1024.png)


## 项目结构

这个项目是一个展示研究组信息和科研成果的个人网站，主要分为以下几个部分：

- **`group`**：展示研究组成员信息，包括他们的个人简介、研究兴趣和照片等。
- **`publications`**：展示研究组成员的科研成果，包括论文、会议、报告等内容。
- **`updates`**：展示个人的近况更新，记录所有重要的学术活动、演讲、奖项等。
- **`experience`**：展示个人的经历，包括教育背景和职业经历等。
- **`resources`**：展示与研究相关的有用资源，包括书籍、论文、数据资源等。

### 项目目录结构
```
根目录
├── /docs
│   ├── about.md                 # 个人介绍主页面
│   ├── group.md                 # 研究组概览入口
│   ├── publications.md          # 论文总览索引
│   ├── updates.md               # 新闻动态聚合
│   ├── experience.md            # 个人履历时间轴
│   └── resources.md             # 学术资源导航
│
├── /_data
│   └── navigation.yml           # 全局导航栏配置
│
├── /_group
│   ├── haoyumo.md               # 组员 Haoyu Mo 档案
│   └── manlianpan.md            # 组员 Manlian Pan 档案
│
├── /_publications
│   ├── 2023-03-01-paper-title-number-1.md  # 论文《Paper Title 1》
│   └── 2023-03-01-paper-title-number-2.md  # 论文《Paper Title 2》
│
├── /_updates
│   ├── 2023-09-26-xiaotong-presentation-at-sysu.md  # "Xiaotong 中大演讲"动态
│   └── 2023-06-02-hangyu-thesis-defense.md          # "Hangyu 论文答辩"动态
│
├── /_experience
│   ├── 2020-07-01-phd-next-gen-transportation.md      # 博士经历：新一代交通系统
│   ├── 2016-08-01-msc-civil-coastal-engineering.md    # 硕士经历：海岸工程
│   └── 2021-06-01-postdoctoral-research-fellow.md     # 博士后研究员经历
│
├── /_resources
│   ├── lab-for-innovative-mobility-systems.md         # 创新交通系统实验室指南
│   ├── shoam-leyton-brown-multiagent-systems.md       # 《多智能体系统》参考书
│   ├── roughgarden-twenty-lectures-algorithmic-game-theory.md  # 算法博弈论讲义
│   ├── borgers-introduction-theory-mechanism-design.md         # 机制设计导论
│   └── kahneman-thinking-fast-slow.md                 # 《思考，快与慢》精读笔记
│
├── /_layouts
│   ├── single.html                   # 单页面布局（组员/资源详情）
│   ├── archive.html                  # 聚合列表布局（更新/论文）
│   └── archive-single-resource.html  # 资源卡片定制模板
│
├── /_includes
│   ├── archive-single.html           # 论文列表项模板
│   └── archive-single-update.html    # 动态列表项模板
│
└── _config.yml                       # 全局配置文件（主题/插件/元数据）
```
## 跳转逻辑

项目的跳转主要是通过导航栏来实现，`_data/navigation.yml` 文件定义了顶栏的跳转逻辑。每个条目都指向一个具体的页面或集合，例如：

- **Group**：指向 `/group/`，展示研究组成员的汇总。
- **Publications**：指向 `/publications/`，展示所有论文的列表。
- **Experience**：指向 `/experience/`，展示个人的教育和职业经历。
- **Updates**：指向 `/updates/`，展示所有最新的个人更新。
- **Resources**：指向 `/resources/`，展示所有有用的资源。

你可以通过更新 `navigation.yml` 来改变页面的显示顺序或添加新的页面。

## 关键改动

在部署过程中，我们做了以下几项关键改动：

1. **修改 `baseurl`**：为了确保站点链接正确，我们将 `_config.yml` 中的 `baseurl` 设置为空字符串 (`baseurl: ""`)，这样站点将部署在根目录。
2. **优化了 `group` 页面布局**：我们使用了现有的 `archive.html` 布局来展示组员信息，每个组员信息放在一个独立的 Markdown 文件中，点击后可以查看详细信息。
3. **自定义了 `publications` 页面布局**：借鉴了现有的论文列表展示方式，使用 `archive.html` 布局展示论文，点击后进入论文的详细页面。
4. **新增 `updates` 页面**：我们新增了一个 `updates` 页面，用来展示个人的学术活动、演讲、奖项和讲座等更新。
5. **新增 `experience` 页面**：我们新增了一个 `experience` 页面，展示个人的教育背景和职业经历等内容。
6. **新增 `resources` 页面**：我们新增了一个 `resources` 页面，展示所有与研究相关的资源，包括书籍、论文、数据源等。



## 如何添加新的论文、组员、经历或资源
### 添加新的论文

1. 在 `_publications` 文件夹中创建一个新的 Markdown 文件，命名格式为：`YYYY-MM-DD-论文标题.md`。
2. 在文件中添加以下内容：

```
---
title: "论文标题"
collection: publications
category: 论文类型（如：manuscripts, journal papers, conference）
permalink: /publication/YYYY-MM-DD-论文标题
excerpt: "论文摘要"
date: YYYY-MM-DD
venue: "期刊或会议名称"
slidesurl: "幻灯片链接（如果有）"
paperurl: "论文链接（如果有）"
citation: "论文引用信息"
---
```
3. 你可以为每篇论文提供 slidesurl 和 paperurl，但这些字段可以根据需要省略。

### 添加新的组员
1. 在 _group 文件夹中创建一个新的 Markdown 文件，命名格式为：组员名字.md。
2. 在文件中添加以下内容：
```
---
layout: single
title: "组员名字"
author_profile: true
collection: group
role: "Ph.D. Student"
research_interests: "研究兴趣"
bio: "简短的个人简介"
photo: "../images/组员照片.jpg"
---
```
3. 在 group.md 中，你可以添加组员的概览，展示每个组员的角色和研究兴趣等信息。

### 添加新的更新
1. 在 _updates 文件夹中创建一个新的 Markdown 文件，命名格式为：YYYY-MM-DD-更新标题.md。
2. 在文件中添加以下内容：
```
---
title: "更新标题"
collection: updates
date: YYYY-MM-DD
permalink: /updates/YYYY-MM-DD-更新标题
image: "../images/更新图片.png"  # 如有相关图片
---
更新内容描述，具体说明事件的细节。
![Image](../images/更新图片.png)  # 如果有图片，添加图片

``` 
### 添加新的资源
1. 在 _resources 文件夹中创建一个新的 Markdown 文件，命名格式为：资源名称.md。
2. 在文件中添加以下内容：
```
---
title: "资源标题"
collection: resources
permalink: /resources/资源名称
---
资源描述，具体说明该资源的内容或链接。

```

### 注意事项
确保每篇论文和组员的 permalink 唯一，以避免 URL 冲突。
组员和论文文件的 title 和 permalink 中不要使用特殊字符，例如空格、逗号等。
对于每个新添加的论文或组员，记得在相关页面（如 group.md 和 publications.md）中进行更新。

## 常见错误及解决方案
1. Page Not Found 错误
原因：可能是 permalink 配置错误或忘记提交文件。
解决方案：
确保每个页面的 permalink 是唯一的，并且文件名称与 permalink 对应。
检查 group.md 和 publications.md 文件中是否已包含最新的组员和论文链接。
提交并推送更改到 GitHub，确保 GitHub Pages 会重新构建站点。
2. 顶栏跳转到 academic page 默认页面
原因：navigation.yml 配置错误，导致跳转逻辑没有正确更新。
解决方案：
确保 _data/navigation.yml 文件中的所有链接都指向正确的页面（如 /group/ 和 /publications/）。
确保 baseurl 配置正确，如果站点在根目录，baseurl 应为空字符串 (baseurl: "")。
强制重新构建 GitHub Pages，通过修改 GitHub Pages 设置来触发站点的重新部署。
3. 页面布局没有正确显示
原因：可能是因为使用了不正确的布局或文件路径。
解决方案：
确保在页面头部的 layout 字段设置正确。比如，组员页面使用 single 布局，论文页面使用 archive 布局。
检查是否在 _layouts 文件夹中创建了适当的布局文件，并确保它们没有语法错误。
4. 图片无法显示
原因：图片路径错误或图片未正确上传。
解决方案：
确保图片文件被放置在 images 文件夹中，并且路径引用正确。
确保图片文件名没有空格或特殊字符。


## Bugfixes and enhancements

If you have bugfixes and enhancements that you would like to submit as a pull request, you will need to [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) this repository as opposed to using it as a template. This will also allow you to [synchronize your copy](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork) of template to your fork as well.

Unfortunately, one logistical issue with a template theme like Academic Pages that makes it a little tricky to get bug fixes and updates to the core theme. If you use this template and customize it, you will probably get merge conflicts if you attempt to synchronize. If you want to save your various .yml configuration files and markdown files, you can delete the repository and fork it again. Or you can manually patch.

---
<div align="center">
    
![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)
[![GitHub contributors](https://img.shields.io/github/contributors/academicpages/academicpages.github.io.svg)](https://github.com/academicpages/academicpages.github.io/graphs/contributors)
[![GitHub release](https://img.shields.io/github/v/release/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/releases/latest)
[![GitHub license](https://img.shields.io/github/license/academicpages/academicpages.github.io?color=blue)](https://github.com/academicpages/academicpages.github.io/blob/master/LICENSE)

[![GitHub stars](https://img.shields.io/github/stars/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io)
[![GitHub forks](https://img.shields.io/github/forks/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/fork)
</div>
