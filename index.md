---
layout: default
title: 主页
permalink: /
---

# 👋 你好，我是 FANG050829

一名正在学习编程的学生，喜欢做 **3D 可视化** 和 **小程序** 方向的项目。这个网站用来记录我的学习笔记和作品。

- GitHub：[@FANG050829](https://github.com/FANG050829)

> 🚧 网站还在持续建设中，欢迎常来看看！

## 项目

{% for project in site.data.projects %}
### {{ project.name }}{% if project.subtitle %} · {{ project.subtitle }}{% endif %}

{{ project.description }}

{% for link in project.links %}- [{{ link.label }}]({{ link.url }})
{% endfor %}

技术栈：{% for tag in project.tags %}`{{ tag }}` {% endfor %}

{% endfor %}

## 技能

- **前端开发**：TypeScript、React / Next.js、Three.js、Tailwind CSS
- **桌面应用**：Electron、Node.js、LLM 智能体、工具调用与审计设计
- **小程序**：微信小程序、微信云开发、BLE 蓝牙通信
- **常用工具**：Git、Prisma / SQLite

## 联系方式

- GitHub：[@FANG050829](https://github.com/FANG050829)
- 邮箱：<3364235758@qq.com> <!-- 不想公开邮箱的话，删掉这一行即可 -->
