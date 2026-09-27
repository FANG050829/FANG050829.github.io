# FANG050829.github.io

我的个人主页，基于 **GitHub Pages + Jekyll** 搭建。

🌐 **在线访问**：<https://fang050829.github.io>

## 目录结构

```text
.
├── index.md      # 首页内容
├── 404.md        # 404 页面
├── _config.yml   # Jekyll 站点配置（标题、主题等）
└── Gemfile       # 本地预览所需依赖
```

## 本地预览

需要先安装 [Ruby](https://www.ruby-lang.org/) 与 Bundler，然后执行：

```bash
bundle install
bundle exec jekyll serve
```

打开浏览器访问 <http://localhost:4000> 即可预览。

## 如何修改

- **首页内容**：编辑 [index.md](index.md)，按注释提示替换技能、项目等信息
- **站点标题 / 描述**：编辑 [_config.yml](_config.yml)
- **新增页面**：在根目录新建 `xxx.md`，并加上 `title`，它会自动出现在顶部导航

修改推送到 `main` 分支后，GitHub Pages 会自动重新构建发布。
