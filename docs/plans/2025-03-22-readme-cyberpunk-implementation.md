# README 赛博朋克风格实施计划

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**目标:** 将 GitHub Profile README 从当前黑客终端风格升级为赛博朋克风格，采用蓝青配色方案。

**架构:** 使用 Markdown + HTML 实现的静态页面，依赖外部服务（capsule-render, typing-svg, github-readme-stats 等）提供动态视觉效果。

**技术栈:** Markdown, HTML/CSS, 外部动态图像服务

---

## Task 1: 备份现有 README

**Files:**
- Modify: `README.md` (backup first)

**Step 1: 备份当前 README**

```bash
cp README.md README.md.backup
```

**Step 2: 验证备份成功**

```bash
ls -la README.md*
```
Expected: 显示 `README.md` 和 `README.md.backup`

**Step 3: Commit 备份**

```bash
git add README.md.backup
git commit -m "chore: backup original README before cyberpunk redesign"
```

---

## Task 2: 更新 Header 区域

**Files:**
- Modify: `README.md:1-10`

**Step 1: 替换 Header 为赛博朋克风格**

将现有的 capsule-render URL 更新为：

```markdown
<div align="center">

<!-- 赛博朋克风格 Header -->
<a href="https://github.com/Jasper-Wynn">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0A0E27&height=250&section=header&text=Jasper%20Wynn&fontSize=70&fontColor=00F0FF&animation=twinkling&fontAlignY=40&desc=Python%20Developer%20|%20Security%20Enthusiast%20|%20DevOps%20Practitioner&descAlignY=70&descAlign=50&descColor=4A90E2" />
</a>

<!-- 霓虹打字效果 -->
<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=22&pause=1200&color=00F0FF&center=true&vCenter=true&width=700&lines=System+Initializing...;Crafting+Cyber+Solutions;Penetration+Testing+Active;Building+DevOps+Arsenal&background=0A0E2700" alt="Typing SVG" />
</a>

</div>
```

**Step 2: 预览效果**

在浏览器中打开 GitHub 预览或使用本地预览工具。

**Step 3: Commit Header 更改**

```bash
git add README.md
git commit -m "feat(cyberpunk): update header with cyber-blue theme"
```

---

## Task 3: 重构技术栈展示区域

**Files:**
- Modify: `README.md:11-41`

**Step 1: 替换终端风格为全息卡片风格**

```markdown
---

## ⚡ 技术核心 // Tech Core

### 💻 核心语言

<table>
<tr>
  <td width="100">
    <img src="https://skillicons.dev/icons?i=py&theme=dark" />
  </td>
  <td>
    <b>Python</b><br>
    <sub>脚本开发、自动化、安全工具</sub>
  </td>
  <td>
    <img src="https://progress-bar.dev/95?title=Python&width=150&color=00F0FF&bcolor=0A0E27" />
  </td>
</tr>
<tr>
  <td>
    <img src="https://skillicons.dev/icons?i=js&theme=dark" />
  </td>
  <td>
    <b>JavaScript</b><br>
    <sub>前端开发、脚本编写</sub>
  </td>
  <td>
    <img src="https://progress-bar.dev/75?title=JavaScript&width=150&color=4A90E2&bcolor=0A0E27" />
  </td>
</tr>
<tr>
  <td>
    <img src="https://skillicons.dev/icons?i=bash&theme=dark" />
  </td>
  <td>
    <b>Bash/Shell</b><br>
    <sub>系统管理、自动化脚本</sub>
  </td>
  <td>
    <img src="https://progress-bar.dev/70?title=Bash&width=150&color=00F0FF&bcolor=0A0E27" />
  </td>
</tr>
</table>

### 🛠️ DevOps 工具链

<p align="center">
  <img src="https://skillicons.dev/icons?i=docker,kubernetes,git,linux,aws,nginx,jenkins,terraform&theme=dark" />
</p>

### 🔓 安全武器库

<table>
<tr>
  <td align="center">
    <img src="https://img.shields.io/badge/Nmap-v7.94-00F0FF?style=for-the-badge&logo=nmap&logoColor=0A0E27" />
  </td>
  <td align="center">
    <img src="https://img.shields.io/badge/Metasploit-Framework-4A90E2?style=for-the-badge&logo=metasploit&logoColor=0A0E27" />
  </td>
  <td align="center">
    <img src="https://img.shields.io/badge/Burp_Suite-Pro-7B2FFF?style=for-the-badge&logo=burpsuite&logoColor=0A0E27" />
  </td>
</tr>
<tr>
  <td align="center">
    <img src="https://img.shields.io/badge/Wireshark-Network-00F0FF?style=for-the-badge&logo=wireshark&logoColor=0A0E27" />
  </td>
  <td align="center">
    <img src="https://img.shields.io/badge/SQLmap-Injection-4A90E2?style=for-the-badge&logoColor=0A0E27" />
  </td>
  <td align="center">
    <img src="https://img.shields.io/badge/Kali_Linux-Pentest-7B2FFF?style=for-the-badge&logo=kali-linux&logoColor=0A0E27" />
  </td>
</tr>
</table>

---
```

**Step 2: 验证渲染效果**

确保所有图标和进度条正确显示。

**Step 3: Commit 技术栈更新**

```bash
git add README.md
git commit -m "feat(cyberpunk): redesign tech stack with holographic cards"
```

---

## Task 4: 重构项目展示区域

**Files:**
- Modify: `README.md:53-79`

**Step 1: 创建赛博朋克风格项目卡片**

```markdown
---

## 🚀 核心项目 // Core Projects

<table align="center">
<tr>
<td width="48%">

<div align="center">

### 🔐 服务弱口令扫描器
**Weak Password Scanner**

基于 Python + Nmap 的服务弱口令爆破工具，支持多种协议扫描与自动化检测。

<br>

**技术栈:**

`Python` `Nmap` `Socket` `Threading` `Regex`

<br>

[![Execute Project](https://img.shields.io/badge/▶_ACCESS-000000?style=for-the-badge&logo=github&logoColor=00F0FF&color=0A0E27&borderColor=00F0FF)](https://github.com/Jasper-Wynn/python-nmap-brute-force)

</div>

</td>
<td width="4%"></td>
<td width="48%">

<div align="center">

### 🚢 DevOps 自动化平台
**DevOps Automation Platform**

深度集成 Docker + Git + K8s，实现完全自动化的 CI/CD 流水线部署平台。

<br>

**技术栈:**

`Docker` `Kubernetes` `Git` `Jenkins` `Terraform`

<br>

[![Execute Project](https://img.shields.io/badge/▶_ACCESS-000000?style=for-the-badge&logo=github&logoColor=00F0FF&color=0A0E27&borderColor=00F0FF)](https://github.com/Jasper-Wynn/devops-platform)

</div>

</td>
</tr>
</table>

---
```

**Step 2: 验证卡片布局**

确保两个项目卡片并排显示，按钮样式正确。

**Step 3: Commit 项目区域更新**

```bash
git add README.md
git commit -m "feat(cyberpunk): redesign project cards with neon buttons"
```

---

## Task 5: 更新统计数据区域

**Files:**
- Modify: `README.md:44-50`

**Step 1: 更新为蓝青配色主题**

```markdown
---

## 📊 数据中心 // Analytics

<p align="center">
  <!-- GitHub Stats - 自定义赛博蓝主题 -->
  <img src="https://github-readme-stats.vercel.app/api?username=Jasper-Wynn&show_icons=true&theme=github_dark&hide_border=true&bg_color=0A0E27&title_color=00F0FF&icon_color=4A90E2&text_color=ffffff&border_color=00F0FF" alt="GitHub Stats" width="49%"/>

  <!-- Streak Stats - 蓝青配色 -->
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Jasper-Wynn&theme=github_dark&hide_border=true&background=0A0E27&ring=00F0FF&fire=4A90E2&currStreakNum=ffffff&sideNums=00F0FF&sideLabels=4A90E2&dates=7B2FFF" alt="GitHub Streak" width="49%"/>
</p>

<p align="center">
  <!-- 贡献热力图 - 青蓝渐变 -->
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Jasper-Wynn&theme=github-dark&bg_color=0A0E27&color=00F0FF&line=4A90E2&point=7B2FFF&area=true&hide_border=true" alt="GitHub Activity Graph" width="90%"/>
</p>

---
```

**Step 2: 验证统计数据渲染**

检查所有图表是否使用蓝青配色。

**Step 3: Commit 统计数据更新**

```bash
git add README.md
git commit -m "feat(cyberpunk): update stats with cyber-blue color theme"
```

---

## Task 6: 更新页脚区域

**Files:**
- Modify: `README.md:80-89`

**Step 1: 创建霓虹按钮页脚**

```markdown
---

<div align="center">

## 🔗 神经连接 // Neural Link

<p align="center">
  <a href="mailto:cjwpython@163.com">
    <img src="https://img.shields.io/badge/📧_EMAIL-cjwpython@163.com-00F0FF?style=for-the-badge&logo=minutemailer&logoColor=0A0E27&color=0A0E27&borderColor=00F0FF" />
  </a>
  <a href="https://github.com/Jasper-Wynn">
    <img src="https://img.shields.io/badge/💻_GITHUB-Jasper--Wynn-4A90E2?style=for-the-badge&logo=github&logoColor=0A0E27&color=0A0E27&borderColor=4A90E2" />
  </a>
</p>

---

<i><b>"The code is law. The terminal is truth."</b></i>

<br>
<br>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0A0E27&height=80&section=footer" />
</div>

</div>
```

**Step 2: 验证页脚渲染**

确保联系方式按钮和底部波浪正确显示。

**Step 3: Commit 页脚更新**

```bash
git add README.md
git commit -m "feat(cyberpunk): add neon footer with wave separator"
```

---

## Task 7: 最终验证和清理

**Files:**
- Verify: `README.md`

**Step 1: 完整预览检查**

在浏览器中完整预览 README，检查：
- [ ] Header 显示正确，蓝青配色
- [ ] 技术栈图标和进度条渲染正常
- [ ] 项目卡片布局正确
- [ ] 统计图表颜色统一
- [ ] 页脚按钮样式正确
- [ ] 整体无渲染错误

**Step 2: 删除备份文件（可选）**

```bash
# 确认满意后删除备份
rm README.md.backup
```

**Step 3: 最终 Commit**

```bash
git add README.md
git commit -m "chore: finalize cyberpunk README redesign"
```

**Step 4: 推送到 GitHub**

```bash
git push origin main
```

---

## 测试清单

在最终推送前，验证：

- [ ] 所有外部图片链接可访问
- [ ] 移动端显示正常
- [ ] 深色/浅色模式下均可用（优先深色）
- [ ] 无拼写错误
- [ ] GitHub README 预览正确渲染

---

## 回滚计划

如需回滚到原设计：

```bash
git checkout e7f3a8c -- README.md
git commit -m "revert: rollback to original README design"
git push
```
