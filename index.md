---
layout: default
title: 主页
permalink: /
---

<section class="hero">
  <p class="hero-hi">👋 你好，我是</p>
  <h1>FANG050829</h1>
  <p class="hero-role">一名正在学习编程的学生，喜欢做 3D 可视化和小程序方向的项目。</p>
  <p class="hero-bio">这个网站用来记录我的学习笔记和作品。</p>
  <div class="hero-actions">
    <a class="btn btn-primary" href="https://github.com/FANG050829" target="_blank" rel="noopener noreferrer">GitHub 主页</a>
    <a class="btn btn-ghost" href="#contact">联系方式</a>
  </div>
  <p class="hero-status">🚧 网站还在持续建设中，欢迎常来看看！</p>
</section>

<section id="projects" class="section">
  <h2>项目</h2>
  {% for project in site.data.projects %}
  <article class="card project-card">
    <div class="card-head">
      <h3>{{ project.name }}</h3>
      {%- if project.subtitle -%}
      <span class="card-sub">{{ project.subtitle }}</span>
      {%- endif -%}
    </div>
    <div class="project-body">{{ project.description | markdownify }}</div>
    <div class="tags">
      {%- for tag in project.tags -%}
      <span class="tag">{{ tag }}</span>
      {%- endfor -%}
    </div>
    {%- if project.links -%}
    <div class="card-links">
      {%- for link in project.links -%}
      <a class="card-link" href="{{ link.url }}" {% if link.url contains 'http' %}target="_blank" rel="noopener noreferrer"{% endif %}>
        {%- case link.icon -%}
        {%- when 'globe' -%}
        <svg class="icon" viewBox="0 0 16 16" aria-hidden="true" fill="currentColor"><path d="M8 0a8 8 0 1 1 0 16A8 8 0 0 1 8 0ZM5.78 8.75a9.64 9.64 0 0 0 1.363 4.177c.255.426.542.832.857 1.215.245-.296.551-.705.857-1.215A9.64 9.64 0 0 0 10.22 8.75Zm4.44-1.5a9.64 9.64 0 0 0-1.363-4.177c-.307-.51-.612-.919-.857-1.215a9.927 9.927 0 0 0-.857 1.215A9.64 9.64 0 0 0 5.78 7.25Zm-5.944 1.5H1.543a6.507 6.507 0 0 0 4.666 5.5c-.123-.181-.24-.365-.352-.552-.715-1.192-1.437-2.874-1.581-4.948Zm-2.733-1.5h2.733c.144-2.074.866-3.756 1.58-4.948.12-.197.237-.381.353-.552a6.507 6.507 0 0 0-4.666 5.5Zm10.181 1.5c-.144 2.074-.866 3.756-1.58 4.948-.12.197-.237.381-.353.552a6.507 6.507 0 0 0 4.666-5.5Zm2.733-1.5a6.507 6.507 0 0 0-4.666-5.5c.116.171.233.355.353.552.714 1.192 1.436 2.874 1.58 4.948Z"/></svg>
        {%- when 'github' -%}
        <svg class="icon" viewBox="0 0 16 16" aria-hidden="true" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
        {%- endcase -%}
        {{ link.label }}
      </a>
      {%- endfor -%}
    </div>
    {%- endif -%}
  </article>
  {% endfor %}
</section>

<section id="skills" class="section">
  <h2>技能</h2>
  <div class="skill-grid">
    <div class="skill-item">
      <h3>前端开发</h3>
      <div class="tags">
        <span class="tag">TypeScript</span>
        <span class="tag">React / Next.js</span>
        <span class="tag">Three.js</span>
        <span class="tag">Tailwind CSS</span>
      </div>
    </div>
    <div class="skill-item">
      <h3>桌面应用</h3>
      <div class="tags">
        <span class="tag">Electron</span>
        <span class="tag">Node.js</span>
        <span class="tag">LLM 智能体</span>
        <span class="tag">工具调用与审计设计</span>
      </div>
    </div>
    <div class="skill-item">
      <h3>小程序</h3>
      <div class="tags">
        <span class="tag">微信小程序</span>
        <span class="tag">微信云开发</span>
        <span class="tag">BLE 蓝牙通信</span>
      </div>
    </div>
    <div class="skill-item">
      <h3>常用工具</h3>
      <div class="tags">
        <span class="tag">Git</span>
        <span class="tag">Prisma / SQLite</span>
      </div>
    </div>
  </div>
</section>

<section id="contact" class="section">
  <h2>联系方式</h2>
  <div class="contact-grid">
    <a class="contact-card" href="https://github.com/FANG050829" target="_blank" rel="noopener noreferrer">
      <span class="contact-icon" aria-hidden="true">
        <svg class="icon" viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27s1.36.09 2 .27c1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
      </span>
      <span class="contact-text">
        <span class="contact-k">GitHub</span>
        <span class="contact-v">@FANG050829</span>
      </span>
    </a>
    <a class="contact-card" href="mailto:3364235758@qq.com">
      <span class="contact-icon" aria-hidden="true">
        <svg class="icon" viewBox="0 0 16 16" fill="currentColor"><path d="M1.75 2h12.5c.966 0 1.75.784 1.75 1.75v8.5A1.75 1.75 0 0 1 14.25 14H1.75A1.75 1.75 0 0 1 0 12.25v-8.5C0 2.784.784 2 1.75 2ZM1.5 12.251c0 .138.112.25.25.25h12.5a.25.25 0 0 0 .25-.25V5.809L8.38 9.397a.75.75 0 0 1-.76 0L1.5 5.809Zm13-8.181v-.32a.25.25 0 0 0-.25-.25H1.75a.25.25 0 0 0-.25.25v.32L8 7.88Z"/></svg>
      </span>
      <span class="contact-text">
        <span class="contact-k">邮箱</span>
        <span class="contact-v">3364235758@qq.com</span>
      </span>
    </a> <!-- 不想公开邮箱的话，删掉这一行即可 -->
  </div>
</section>
