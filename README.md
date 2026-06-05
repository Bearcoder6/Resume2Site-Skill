# Resume2Site-Skill

<p align="center">
  <img src="docs/images/Resume2Site.png" alt="Resume2Site-Skill banner">
</p>

<p align="center">
  <strong>A lightweight Agent Skill for turning resumes, projects, and papers into polished GitHub Pages personal websites.</strong>
</p>

<p align="center">
  <a href="#english">English</a> · <a href="#中文">中文</a>
</p>

<p align="center">
  <img alt="Skill" src="https://img.shields.io/badge/type-Agent%20Skill-111827">
  <img alt="GitHub Pages" src="https://img.shields.io/badge/output-GitHub%20Pages-2563eb">
  <img alt="No CLI" src="https://img.shields.io/badge/no%20CLI-lightweight-0f766e">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-475569">
</p>

## English

Resume2Site-Skill helps coding agents extract structured profile information, choose an academic or personal landing-page style, plan the website narrative, generate desktop-first GitHub Pages-ready files, and polish the final design.

It is not a CLI, SaaS app, crawler, parser, Python package, npm package, or full website builder. It is a Skill: a compact workflow, prompt pack, design rule pack, style distillation pack, quality checklist, and GitHub Pages output convention for agents such as Codex, Claude Code, Cursor, and similar coding assistants.

### Why Use It

- Turns a raw resume into a structured `work/profile.json` before any page is generated.
- Supports two clear modes: Academic Homepage and Personal Landing Page.
- Prompts new users to choose from built-in style variants before generation, with a recommended default.
- Targets polished PC / desktop personal homepages by default.
- Guides factual writing without invented publications, metrics, titles, or awards.
- Encourages polished visual design instead of resume-to-HTML dumping.
- Provides built-in academic and landing style rules before release, so users do not need to distill style themselves.
- Provides asset search, license-checking, and credit rules for open or free visual sources.
- Keeps public output privacy-aware and GitHub Pages ready.

### Install

Depending on your agent environment, install the Skill by copying `skills/resume2site` into your skill directory, or by giving the agent access to this repository and asking it to use `skills/resume2site/SKILL.md`.

Codex-style local install:

```bash
mkdir -p ~/.codex/skills
cp -R skills/resume2site ~/.codex/skills/resume2site
```

Windows PowerShell:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
Copy-Item -Recurse -Force ".\skills\resume2site" "$env:USERPROFILE\.codex\skills\resume2site"
```

No package install is required. There is no `resume2site build` command in the core project.

### Basic Usage

Example academic prompt:

```text
Use the Resume2Site Skill to convert my resume into an academic personal homepage.
My files are in ./input.
Use academic mode.
Create the site in ./output/site.
Do not invent publications or affiliations.
Before finishing, run the final quality checklist.
```

Example landing-page prompt:

```text
Use the Resume2Site Skill to convert my resume into a polished personal landing page.
Use landing mode.
Make it suitable for GitHub Pages.
Create profile.json and site-plan.md before generating HTML.
```

Suggested input folder:

```text
input/
  resume.pdf or resume.docx or resume.txt
  avatar.png
  github_links.txt
  paper_links.txt
  website_links.txt
  style_preference.txt
  references/
```

Expected output:

```text
output/site/
  index.html
  styles.css
  assets/
  README.md
  .nojekyll
  ASSET_CREDITS.md
```

Intermediate files:

```text
work/
  profile.json
  site-plan.md
  asset-recommendations.md
  final-review.md
```

The agent should create these folders as needed.

### Modes

Academic Homepage mode is for graduate students, PhD applicants, researchers, professors, publication-heavy users, lab users, and research project portfolios. It favors a clean profile card or sidebar, About Me, News, Research Interests, Education, Selected Publications, Selected Projects, Honors & Awards, Experience, and Contact.

Personal Landing Page mode is for job seekers, developers, designers, product people, creators, freelancers, and personal-brand users. It favors a strong hero, positioning, core strengths, selected works, experience highlights, skills, contact CTA, and optional resume download.

### Style And Assets

The Skill includes built-in style distillation notes for academic homepages and personal landing pages. Users do not need to research or distill style themselves. After reading the resume, the agent should recommend a style and ask the user to choose from the built-in variants: academic editorial, academic lab, engineering commercial, business polished, creative portfolio, or minimal resume site. User screenshots or preferences can supplement the selected variant.

For visuals, the Skill can guide the agent to search free, open-licensed, or clearly free-to-use sources such as Wikimedia Commons, Openverse, Unsplash, Pexels, Pixabay, and carefully verified China-friendly sources. It should create `work/asset-recommendations.md` and, when assets are used, `output/site/ASSET_CREDITS.md`.

### Privacy

Resume2Site-Skill does not promise automatic local masking. It instructs the agent to warn users before processing sensitive resumes, avoid copying raw resumes into public output, ask before publishing phone numbers, never hide raw resume text in HTML comments, and keep internal notes out of `output/site`.

### Repository Structure

```text
SKILL.md                         Root pointer for agents
skill.json                       Lightweight metadata
skills/resume2site/              Main installable Skill
skills/resume2site/prompts/      Directly usable agent prompts
skills/resume2site/templates/    Reference templates for generated sites
skills/resume2site/examples/     Fake academic and landing examples
docs/                            Install, usage, process, and style notes
```

### Roadmap

- Add more mode packs, such as designer portfolio and lab homepage.
- Add more built-in style packs and reviewed visual examples.
- Add optional agent-specific installation notes as platforms stabilize.
- Add community-reviewed example outputs.

### Contributing

Contributions are welcome when they improve workflow clarity, design quality, privacy safety, examples, or agent compatibility. See `CONTRIBUTING.md`.

### License

MIT.

## 中文

Resume2Site-Skill 是一个轻量级 Agent Skill，用来指导 Codex、Claude Code、Cursor 等编程智能体，把简历、项目、论文和可选风格参考转成精致的 GitHub Pages 个人网站。

它不是 CLI、SaaS、爬虫、解析器、Python 包、npm 包或完整建站系统。它的价值是：结构化工作流、prompt pack、设计规则、风格提炼、隐私规范、质量清单，以及 GitHub Pages 输出约定。

### 为什么用它

- 先生成 `work/profile.json`，再生成网页，避免直接把原始简历糊成 HTML。
- 支持两种主模式：学术主页和个人商业/求职落地页。
- 强制事实优先，不编造论文、奖项、指标、职位或背书。
- 让页面更像真正的个人网站，而不是简历换皮。
- 内置学术风和商业/求职落地页的风格蒸馏规则，用户不需要自己研究怎么设计。
- 给开放/免费素材检索、许可核验和署名规则，方便做出更精致的视觉。
- 对公开输出保持隐私意识，并适配 GitHub Pages。

### 安装方式

根据你的 Agent 环境，把 `skills/resume2site` 复制到对应的 Skill 目录，或者让 Agent 能访问这个仓库，并明确要求它读取 `skills/resume2site/SKILL.md`。

Codex 本地安装示例：

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
Copy-Item -Recurse -Force ".\skills\resume2site" "$env:USERPROFILE\.codex\skills\resume2site"
```

这个仓库不需要 `pip install`，也没有核心 CLI 命令。

### 使用示例

学术主页：

```text
使用 Resume2Site Skill，把 ./input 里的简历生成学术个人主页。
使用 academic mode。
输出到 ./output/site。
不要编造论文、导师、机构或奖项。
结束前执行 final quality checklist。
```

个人落地页：

```text
使用 Resume2Site Skill，把我的简历生成精致的个人落地页。
使用 landing mode。
适配 GitHub Pages。
先创建 profile.json 和 site-plan.md，再生成 HTML/CSS。
```

### 输入与输出

推荐输入：

```text
input/
  resume.pdf 或 resume.docx 或 resume.txt
  avatar.png                  可选
  github_links.txt             可选
  paper_links.txt              可选
  website_links.txt            可选
  style_preference.txt         可选
  references/                  可选截图或视觉参考
```

预期输出：

```text
output/site/
  index.html
  styles.css
  assets/
  README.md
  .nojekyll
  ASSET_CREDITS.md
```

中间文件：

```text
work/
  profile.json
  site-plan.md
  asset-recommendations.md
  final-review.md
```

### 两种模式

学术主页适合研究生、博士申请者、科研人员、教授、论文导向 CV、实验室经历和研究项目展示。它强调克制、可信、信息密度、清晰论文格式和学术主页气质。

个人落地页适合求职者、开发者、设计师、产品经理、创作者、自由职业者和个人品牌用户。它强调首屏定位、CTA、能力卡片、项目案例、经历亮点和更强的视觉表达。

### 风格与素材

`docs/style-distillation/` 提供发布前已经沉淀好的学术主页、个人落地页、UI 模式和反模式规则。用户不需要自己做风格蒸馏；Agent 默认应该调用这些内置风格规则。

如果需要更贴近某种审美，用户可以把小红书、GitHub、Dribbble、Behance、学术主页或个人网站截图放到 `docs/style-references/`，但这些只能作为补充 mood reference，不能照抄具体设计或素材。

素材方面，Skill 会指导 Agent 检索 Wikimedia Commons、Openverse、Unsplash、Pexels、Pixabay，以及许可清晰的国内/中文素材源。使用前必须核验具体素材页面的授权，并写入 `ASSET_CREDITS.md`。

### 隐私

Skill 不承诺自动解析或自动脱敏。它会要求 Agent 在处理敏感简历前提醒用户，不把原始简历复制进 `output/site/`，不默认公开手机号，不把原始简历藏在 HTML 注释里，也不把内部工作文件发布出去。
