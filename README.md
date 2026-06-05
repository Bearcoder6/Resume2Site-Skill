# Resume2Site-Skill

<p align="center">
  <img src="docs/images/Resume2Site.png" alt="Resume2Site-Skill banner">
</p>

<p align="center">
  <strong>✨ Turn a resume into a polished, desktop-first personal website with Codex or another coding agent.</strong>
</p>

<p align="center">
  <a href="#english">English</a> | <a href="#中文">中文</a>
</p>

<p align="center">
  <img alt="Skill" src="https://img.shields.io/badge/type-Agent%20Skill-111827">
  <img alt="GitHub Pages" src="https://img.shields.io/badge/output-GitHub%20Pages-2563eb">
  <img alt="No CLI" src="https://img.shields.io/badge/no%20CLI-lightweight-0f766e">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-475569">
</p>

<a id="english"></a>

## 🌍 English

Resume2Site-Skill is a lightweight Agent Skill. It helps Codex, Claude Code, Cursor, or another coding agent convert resumes, projects, papers, avatars, GitHub links, arXiv links, and optional style preferences into a polished GitHub Pages-ready personal website.

It is not a CLI, SaaS app, crawler, parser, Python package, npm package, or full website builder. The value is the workflow: fact extraction, style intake, design rules, privacy rules, asset rules, link preservation, and final quality review.

### ✨ What You Get

| Feature | What the Skill helps the agent do |
|---|---|
| 🎨 Style intake | Ask the user to choose from built-in polished styles before generating |
| 🧾 Resume extraction | Convert resume facts into `work/profile.json` first |
| 🖼️ Avatar recovery | Preserve resume portraits from uploaded avatars, DOCX images, or reliable PDF/page crops |
| 🔗 Link preservation | Keep GitHub, arXiv, DOI, Scholar, demo, project, and portfolio links |
| 🖼️ Asset judgment | Use licensed, high-resolution, role-appropriate visuals when helpful |
| 🔒 Privacy guard | Avoid publishing phone numbers or raw resumes by default |
| 🚀 Static output | Create a GitHub Pages-ready `output/site/` folder |
| 🪶 Lightweight review | Check generated files without requiring screenshots, Playwright, or a local browser setup |

### 🚀 Easiest Way

Give this repository link to Codex and paste a prompt like this:

```text
Please install and use this Skill:
https://github.com/Bearcoder6/Resume2Site-Skill.git

Use the Resume2Site Skill to turn my resume into a polished personal website.
Ask me to choose one of the built-in style variants before generating the site.
Do not publish my phone number unless I explicitly approve it.
Preserve public GitHub, arXiv, DOI, Scholar, demo, and portfolio links.
Create a GitHub Pages-ready static site.
```

If your Codex environment supports skill installation from GitHub, it can install the Skill directly. If not, use the manual install below.

### 🛠️ Manual Install

Clone the repository:

```bash
git clone https://github.com/Bearcoder6/Resume2Site-Skill.git
cd Resume2Site-Skill
```

Install into Codex's local skills folder:

```bash
mkdir -p ~/.codex/skills
cp -R skills/resume2site ~/.codex/skills/resume2site
```

Windows PowerShell:

```powershell
git clone https://github.com/Bearcoder6/Resume2Site-Skill.git
Set-Location Resume2Site-Skill
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
Copy-Item -Recurse -Force ".\skills\resume2site" "$env:USERPROFILE\.codex\skills\resume2site"
```

No package install is required. There is no `resume2site build` command.

### 🧭 How To Use

After installing, open Codex in the folder where you want the generated site and say:

```text
Use the Resume2Site Skill.
My resume is at ./input/resume.pdf.
Create the website in ./output/site.
Ask me which built-in style variant I want before generating.
```

Recommended input format: **Word `.docx` first**, **PDF second**. Plain text and Markdown inputs are currently experimental.

You can provide any of these files:

```text
input/
  resume.docx or resume.pdf
  resume.txt or resume.md   experimental
  avatar.png
  github_links.txt
  paper_links.txt
  website_links.txt
  style_preference.txt
  references/
```

The agent should create:

```text
work/
  profile.json
  site-plan.md
  asset-recommendations.md
  final-review.md

output/site/
  index.html
  styles.css
  assets/
  README.md
  .nojekyll
  ASSET_CREDITS.md
```

Open `output/site/index.html` to preview the generated website.

### 🌐 Publish The Site

The generated site is just static files. To publish it with GitHub Pages:

1. Create a GitHub repository for your personal website.
2. Copy everything inside `output/site/` into that repository.
3. Push the repository to GitHub.
4. Open repository `Settings` → `Pages`, then deploy from the `main` branch root.

For a user site such as `username.github.io`, name the repository exactly `username.github.io`. For a project site, GitHub Pages will usually publish it under `https://username.github.io/repository-name/`.

### 🎨 Built-In Styles

After reading the resume, the agent recommends one style and asks the user to choose:

| Variant | Best for |
|---|---|
| `academic-editorial` | Academic homepages with papers, education, research, advisors, or grants |
| `academic-lab` | AI, data, engineering, robotics, systems, or applied research profiles |
| `engineering-commercial` | Developer, algorithm, data, cloud, security, and job-seeking technical profiles |
| `business-polished` | Product, consulting, operations, finance, management, and enterprise-facing profiles |
| `creative-portfolio` | Design, media, writing, marketing, creators, and client-facing work |
| `minimal-resume-site` | Conservative, sparse, formal, or fast one-page personal sites |

The default output is desktop-first. Mobile is a simple fallback unless the user asks for mobile-first design.

### 🔒 What The Skill Protects

- Creates `work/profile.json` before writing HTML.
- Does not invent jobs, awards, publications, metrics, titles, advisors, or affiliations.
- Does not copy raw resumes into public output.
- Does not publish phone numbers unless the user approves.
- Tries to preserve real resume portraits and records a note if extraction fails.
- Preserves public GitHub, arXiv, DOI, Scholar, website, demo, dataset, video, and portfolio links.
- Uses official or reputable open icons when brand icons are available; otherwise uses text labels.
- Checks visual assets for license, resolution, and fit before use.
- Runs a lightweight file-based quality checklist and makes a polish pass.
- Does not block completion on screenshots, Playwright, browser automation, or local preview tooling.

### 📁 Repository Structure

```text
SKILL.md                         Root pointer for agents
skill.json                       Lightweight metadata
skills/resume2site/              Main installable Skill
skills/resume2site/prompts/      Agent prompts
skills/resume2site/templates/    Reference output structures
skills/resume2site/examples/     Fake academic and landing examples
docs/                            Supporting notes and images
```

### 📄 License

MIT.

<a id="中文"></a>

## 中文

Resume2Site-Skill 是一个轻量级 Agent Skill，用来让 Codex、Claude Code、Cursor 等编程智能体把简历、项目、论文、头像、GitHub 链接、arXiv 链接和可选风格要求，转换成精致的 GitHub Pages 个人主页。

它不是 CLI、SaaS、爬虫、解析器、Python 包、npm 包或完整建站系统。它的价值是给 Agent 一套稳定工作流：事实抽取、风格询问、设计规则、隐私规则、素材规则、链接迁移和最终质量检查。

### ✨ 你会得到什么

| 能力 | Skill 会帮助 Agent 做什么 |
|---|---|
| 🎨 风格询问 | 生成前让用户从内置精致风格里选择 |
| 🧾 简历抽取 | 先把简历事实整理成 `work/profile.json` |
| 🖼️ 头像恢复 | 优先保留上传头像、DOCX 内嵌图或可靠的 PDF/页面裁剪头像 |
| 🔗 链接迁移 | 保留 GitHub、arXiv、DOI、Scholar、Demo、项目、作品集链接 |
| 🖼️ 素材判断 | 需要图片时优先找授权清晰、分辨率足够、适合职业气质的素材 |
| 🔒 隐私保护 | 默认不公开手机号，也不把原始简历塞进网页 |
| 🚀 静态输出 | 生成可直接部署到 GitHub Pages 的 `output/site/` |
| 🪶 轻量检查 | 只检查生成文件，不强制依赖截图、Playwright 或本地浏览器环境 |

### 🚀 最无脑用法

把这个 GitHub 链接发给 Codex，然后直接说：

```text
请安装并使用这个 Skill：
https://github.com/Bearcoder6/Resume2Site-Skill.git

用 Resume2Site Skill 把我的简历生成一个精致的个人主页。
生成前先让我选择内置风格。
除非我明确同意，不要公开我的手机号。
保留简历里的 GitHub、arXiv、DOI、Scholar、Demo、作品集等公开链接。
输出一个适配 GitHub Pages 的静态网站。
```

如果你的 Codex 环境支持从 GitHub 安装 Skill，它可以直接安装。如果不支持，就用下面的手动安装方式。

### 🛠️ 手动安装

先克隆仓库：

```bash
git clone https://github.com/Bearcoder6/Resume2Site-Skill.git
cd Resume2Site-Skill
```

安装到 Codex 本地 Skill 目录：

```bash
mkdir -p ~/.codex/skills
cp -R skills/resume2site ~/.codex/skills/resume2site
```

Windows PowerShell：

```powershell
git clone https://github.com/Bearcoder6/Resume2Site-Skill.git
Set-Location Resume2Site-Skill
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
Copy-Item -Recurse -Force ".\skills\resume2site" "$env:USERPROFILE\.codex\skills\resume2site"
```

不需要 `pip install` 或 `npm install`，也没有 `resume2site build` 命令。

### 🧭 使用方式

安装后，在你希望生成网站的文件夹里打开 Codex，然后说：

```text
使用 Resume2Site Skill。
我的简历在 ./input/resume.pdf。
请把网站生成到 ./output/site。
生成前先让我选择内置风格。
```

推荐输入格式：**优先 Word `.docx`**，其次是 **PDF**。纯文本和 Markdown 目前还在测试开发中。

你可以提供这些文件：

```text
input/
  resume.docx 或 resume.pdf
  resume.txt 或 resume.md   测试中
  avatar.png
  github_links.txt
  paper_links.txt
  website_links.txt
  style_preference.txt
  references/
```

Agent 会创建：

```text
work/
  profile.json
  site-plan.md
  asset-recommendations.md
  final-review.md

output/site/
  index.html
  styles.css
  assets/
  README.md
  .nojekyll
  ASSET_CREDITS.md
```

打开 `output/site/index.html` 就能预览网页。

### 🌐 发布网页

生成结果就是一组静态文件。想挂到 GitHub Pages，可以这样做：

1. 新建一个 GitHub 仓库，用来放个人主页。
2. 把 `output/site/` 里面的所有文件复制到这个仓库。
3. 推送到 GitHub。
4. 进入仓库 `Settings` → `Pages`，选择从 `main` 分支根目录部署。

如果你想做 `username.github.io` 这种用户主页，仓库名要写成自己的 `username.github.io`。如果只是项目主页，一般会发布到 `https://username.github.io/repository-name/`。

### 🎨 内置风格

Agent 读取简历后，会推荐一个风格，并让用户选择：

| 风格 | 适合场景 |
|---|---|
| `academic-editorial` | 学术主页，适合论文、教育经历、研究方向、导师、基金等内容 |
| `academic-lab` | 学术实验室感，适合 AI、数据、工程、机器人、系统、应用研究 |
| `engineering-commercial` | 工程商业风，适合开发、算法、数据、云原生、安全等求职主页 |
| `business-polished` | 商务精致风，适合产品、咨询、运营、金融、管理、企业服务 |
| `creative-portfolio` | 创意作品集，适合设计、媒体、写作、营销、创作者、客户作品 |
| `minimal-resume-site` | 极简正式风，适合内容较少、保守正式、快速生成的一页式主页 |

默认产物是 PC / 桌面端优先。移动端只做基础降级，除非用户明确要求移动优先。

### 🔒 Skill 会保护什么

- 先生成 `work/profile.json`，再生成网页。
- 不编造工作、奖项、论文、指标、职位、导师或机构。
- 不把原始简历复制进公开输出。
- 不默认公开手机号。
- 尽量保留简历里的真实头像；如果提取失败，会记录原因。
- 保留 GitHub、arXiv、DOI、Scholar、个人网站、Demo、数据集、视频、作品集等公开链接。
- 有可靠来源时使用官方或可信开源图标；没有可靠图标时使用文字标签。
- 使用图片素材前检查授权、分辨率和视觉适配度。
- 生成后执行轻量文件级质量检查，并进行一次 polish。
- 不会因为缺少截图、Playwright、浏览器自动化或本地预览环境而卡住。

### 📁 仓库结构

```text
SKILL.md                         Agent 入口提示
skill.json                       轻量元数据
skills/resume2site/              可安装的主 Skill
skills/resume2site/prompts/      Agent prompts
skills/resume2site/templates/    输出结构参考
skills/resume2site/examples/     虚构学术/求职示例
docs/                            辅助说明和项目图片
```

### 📄 License

MIT.
