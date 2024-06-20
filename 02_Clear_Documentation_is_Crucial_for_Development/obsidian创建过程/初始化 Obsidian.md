### 基本信息

- [Obsidian 官网](https://link.zhihu.com/?target=https%3A//obsidian.md/)
- [Obsidian 中文文档](https://link.zhihu.com/?target=https%3A//publish.obsidian.md/help-zh/%25E7%2594%25B1%25E6%25AD%25A4%25E5%25BC%2580%25E5%25A7%258B)
- [Obsidian 中文社区](https://link.zhihu.com/?target=https%3A//forum-zh.obsidian.md/)

## 配置

---

### 安装

首先将语言切换为**简体中文**

![[Pasted image 20231201232809.png]]

然后创建一个新的仓库。在 Obsidian 中，笔记的集合被称为**库**，本质是一个文件夹，其中可以包含许多子文件夹。我这里创建了一个名为`Obsidian`的库，接下来的操作都将在这个库里进行。

### 目录简介

> 接下来，Obsidian 简称 ob。

一个成熟的 ob 库目录如下：

```text
Obsidian
├── .obsidian
│   ├── app.json
│   ├── appearance.json
│   ├── community-plugins.json
│   ├── core-plugins.json
│   ├── daily-notes.json
│   ├── graph.json
│   ├── hotkeys.json
│   ├── plugins
│   ├── snippets
│   ├── templates.json
│   ├── themes
│   ├── workspace
│   └── workspaces.json
├── .trash
├── 日记
│   └── 2022-02-14.md
├── 书籍电影
├── ob-config
│   └── template
```

- `.obsidian`：存放 ob 与配置相关的所有内容
- `plugins`：安装的所有插件存放在该目录；也可以通过将插件放到该目录，让 ob 加载
- `snippets`：该文件夹放置一些自定义的 css 片段对视图进行自定义
- `themes`：安装的所有主题存放在该目录
- `.trash`：ob 自己的回收站
- `01-日记`：根据需要自定义的文件夹
- `ob-config`：该目录存放 ob 使用过程中保存的一些配置，例如模版、脚本文件