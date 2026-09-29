# FANG050829.github.io

我的个人主页，基于 **GitHub Pages + Jekyll** 搭建。

🌐 **在线访问**:<https://fang050829.github.io>

## 目录结构

```text
.
├── index.md              # 首页内容（hero / 项目 / 技能 / 联系方式）
├── 404.md                # 404 页面
├── _config.yml           # Jekyll 站点配置（标题、主题等）
├── Gemfile               # 本地预览所需依赖
├── _data
│   └── projects.yml      # 首页「项目」卡片数据，改这里即可增删项目
├── _layouts
│   └── default.html      # 自定义布局（吸顶导航 + 单栏内容，覆盖主题默认布局）
├── _includes
│   └── head-custom.html  # 深色 / 浅色主题切换
└── assets
    └── css
        └── style.scss    # 站点设计系统：设计变量、卡片、响应式与动效
```

## 主题

在官方 `jekyll-theme-minimal` 基础上，通过自定义 `_layouts/default.html` 覆盖默认布局，
改为「吸顶导航栏 + 单栏居中」的现代作品集结构;样式集中在 `assets/css/style.scss`,
配色抽成 CSS 变量，首次访问跟随系统偏好，用户切换后按 `localStorage` 记忆。

## 新增一个项目

编辑 `_data/projects.yml`，按现有格式追加一段即可，无需改动页面代码：

```yaml
- name: 项目名
  subtitle: 副标题（可选）
  description: 简介，支持 **Markdown** 行内加粗
  tags: [标签1, 标签2]
  links:
    - label: 在线体验
      url: https://example.com
      icon: globe
    - label: GitHub 仓库
      url: https://github.com/用户名/仓库
      icon: github
```
