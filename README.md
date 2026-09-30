# FANG050829.github.io

我的个人主页，基于 **GitHub Pages + Jekyll 官方主题**搭建。

🌐 **在线访问**：<https://fang050829.github.io>

## 目录结构

```text
.
├── index.md              # 首页内容（自我介绍 / 项目 / 技能 / 联系方式）
├── 404.md                # 404 页面
├── _config.yml           # Jekyll 站点配置（标题、主题等）
├── Gemfile               # 本地预览所需依赖
└── _data
    └── projects.yml      # 首页「项目」数据，改这里即可增删项目
```

## 主题

直接使用 GitHub Pages 官方主题 [`jekyll-theme-minimal`](https://github.com/pages-themes/minimal)（`_config.yml` 中 `theme: jekyll-theme-minimal`），
未做任何布局或样式覆盖，页面内容全部写在 `index.md` 的 Markdown 里，
由 Liquid 循环读取 `_data/projects.yml` 生成项目列表。

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
    - label: GitHub 仓库
      url: https://github.com/用户名/仓库
```
