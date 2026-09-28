# FANG050829.github.io

我的个人主页，基于 **GitHub Pages + Jekyll** 搭建。

🌐 **在线访问**：<https://fang050829.github.io>

## 目录结构

```text
.
├── index.md              # 首页内容
├── 404.md                # 404 页面
├── _config.yml           # Jekyll 站点配置（标题、主题等）
├── Gemfile               # 本地预览所需依赖
├── _includes
│   └── head-custom.html  # 深色 / 浅色主题切换
└── assets
    └── css
        └── style.scss    # 在官方 minimal 主题基础上的样式与主题变量
```

## 主题

沿用官方 `jekyll-theme-minimal`，通过覆盖主题预留的 `assets/css/style.scss` 与
`_includes/head-custom.html` 两个入口增强。配色抽成 CSS 变量，首次访问跟随系统偏好，
用户切换后按 `localStorage` 记忆。
