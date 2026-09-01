# MA Qi Homepage and Profile Handoff

更新时间：2026-09-01（Asia/Shanghai）

这份文档是下一次继续修改个人 homepage 和 GitHub profile README 时的入口。先阅读本文件，再检查两个仓库的工作树；不要根据记忆重建内容。

## 1. 当前状态

| 页面 | 本地工作树 | 远端仓库 | 分支 | 当前公开版本 | 地址 |
| --- | --- | --- | --- | --- | --- |
| Academic homepage | `E:\mqqq333.github.io` | `git@github.com:mqqq333/mqqq333.github.io.git` | `master` | 当前 HEAD 以 `git log -1` 为准；页面源码行为基线为 `8d18178842c24d49e865990acdb3bfe2fbd53265` | <https://mqqq333.github.io> |
| GitHub profile | `E:\mqqq333-profile`（homepage 仓库的同级目录） | `https://github.com/mqqq333/mqqq333.git` | `master` | `f373e70bcddd5c33f4a6ca13b6cd7d2aa02e91cc` | <https://github.com/mqqq333> |

当前本地状态：

- homepage 还有未跟踪的 `.chrome-tmp/` 和 `online-profile.png`，它们是浏览器验证产物；不要自动加入提交，也不要未经确认删除。
- `.omx/`、`.jekyll-cache/`、`_site/`、`test-results/` 等属于生成或运行目录，保持忽略状态。
- profile 工作树在最后一次推送后是干净的。
- homepage 本地 Jekyll 服务目前没有作为长期服务运行。

## 2. 用户约定和审批流程

- 重要的视觉或内容改动：先写计划，交给 Claude 审阅，再等待用户明确说“执行”或“更新”后实施。
- 用户希望 homepage 和 profile 彼此保持一致，但 profile 是 homepage 的简略版，不要机械复制整页内容。
- 公开页面只放已经确认可以公开的内容；不要把本地路径、凭据、浏览器数据或未发表材料写入页面。
- 中文文件按 UTF-8 读写。Windows PowerShell 查看中文时使用 `Get-Content -Encoding UTF8`，不要根据乱码的默认终端显示误判文件损坏。
- 修改后分别提交并推送对应仓库，提交前先确认没有把另一个仓库或生成文件一起加入。

## 3. Homepage 结构

Homepage 基于 AcadHomepage/Jekyll 模板，模板基线为：
`RayeRen/acad-homepage.github.io@2cc1577eeaf2f74dede6d016a70722dbd409ea2f`。

主要入口：

- `_pages/about.md`：首页正文和所有分区内容，锚点为 `about-me`、`news`、`research`、`projects`、`education`、`writing`、`cv`、`skills`、`languages`。
- `_config.yml`：站点标题、作者信息、头像、位置、邮箱、实验室链接和作者侧栏配置。
- `_data/navigation.yml`：顶部导航及其锚点链接。
- `_layouts/default.html`、`_includes/masthead.html`、`_includes/author-profile.html`：页面骨架、顶部导航和侧栏。
- `_includes/head/custom.html`：favicon、manifest、MathJax 和自定义 head 内容。
- `assets/css/main.scss`：本项目的主要覆盖样式；基础变量在 `_sass/_variables.scss`。

本地开发和构建：

```powershell
bundle exec jekyll serve
bundle exec jekyll build
```

`run_server.sh` 目前写的是 `bundle exec jekyll liveserve`，疑似拼写错误，不要依赖这个脚本启动服务。

## 4. Homepage 内容事实

- 姓名：`MA Qi (马琦)`。
- 当前简介：Research Assistant, Cognomics Lab, Zhejiang Uni.。
- 正文介绍中保留 Cognomics Lab 和 Xiang-Zhen Kong (孔祥祯) 的链接；profile 中不放单独的 `PI:` 行。
- 位置：`Hangzhou, China`，不要再加 `Zhejiang`，以免侧栏换行溢出。
- 研究主线：计算神经科学、结构神经影像、脑半球偏侧化、跨半球重建和生成模型。
- News 按从新到旧排列；当前条目包括 2026、Jul 2025 加入 Cognomics Lab、Jul 2025 完成浙江大学心理学学士学位。
- Research 当前有三个项目：
  1. Cross-Hemisphere Reconstruction-Derived Neuroanatomical Specificity in Schizophrenia：5 个站点、948 名受试者、ANS/RNS、混合效应模型和分类验证；结果稿为 `in preparation`。
  2. Cross-hemisphere reconstruction and handedness：研究重建残差与利手性的关系，状态为 `in preparation`。
  3. Operator-corrector validation of residual measures：跨人口学、行为和疾病场景验证校正残差，状态为 `in preparation`。
- Projects 当前包括 HemiSpec、Cortex Visualization Skill、Subcortex Visualization Skill、DecodeWM 和 LorewormGu。
- Writing：`阿瞒的脑洞` 是个人公众号；当前两个页面均只保留该公众号的简介，不再列出 `工心应援会` 或文章清单。
- TOEFL 固定写法：`TOEFL iBT: 5/6 (100/120)`。
- CV 下载文件：`files/MAQi_CV_en.pdf` 和 `files/MAQi_resume_cn.pdf`。简历源文件在仓库外；如需重新生成，原始工作目录曾为 `C:\Users\mqqq3333\Desktop\my_info\resume-master`，不要把该目录整体复制进仓库。
- 目前没有 Google Scholar 链接，不要自行编造账号或统计。

## 5. Homepage 资源和视觉约定

资源位置：

- `images/background.jpeg`：首页 banner，桌面高度约 360px，移动端约 220px。
- `images/photo.png`：侧栏头像。
- `images/lab_icon.png`：Cognomics Lab 侧栏链接图标，来源为用户提供的 lab icon。
- `images/favicon.ico`、`favicon-16x16.png`、`favicon-32x32.png`、`apple-touch-icon.png`、`site.webmanifest`：网站图标配置。
- `images/aman_brainhole_favicon.png`：公众号相关 favicon 资源。

当前视觉规则：

- 正文主文字为黑色（`$text-color: #000`），链接使用蓝色。
- 分区使用 Font Awesome 小图标，并按内容使用四组颜色：
  - Research/CV：`#2563EB`
  - Projects：`#059669`
  - News/Writing：`#E4572E`
  - Education/Skills/Languages：`#7C3AED`
- banner 下方不保留额外横线。
- 顶部蓝色规则是 3px，使用 `.masthead__inner-wrap::before` 绘制；左右边界跟随内容网格，左侧对齐 MA Qi 内容边框，右侧对齐 banner 右边界。
- 所有正文句子遵循内容列宽，在 banner 宽度范围内换行；调整布局时同时检查桌面和移动端。
- 侧栏中的 lab 图标使用 `.author__link-icon`，不要改回无色占位图。

## 6. Profile README 结构

profile 仓库只有一个主要入口：`README.md`。它是 homepage 的缩写版，当前顺序为：

1. 固定版本的 banner
2. 姓名、职位和三个入口链接
3. About
4. Research Interests
5. Selected Research
6. Selected Projects
7. Writing
8. Education and Skills
9. Languages
10. GitHub Stats

当前视觉约定：

- 分区标题使用 GitHub 原生彩色 emoji：`🧠`、`🧭`、`🔬`、`🛠️`、`✍️`、`🎓`、`🌐`、`📊`。
- C、C++、Python、PyTorch 使用 `flat-square` 彩色徽章；不要恢复旧的 `for-the-badge` 大徽章，除非重新做移动端检查。
- banner 当前使用 Images 仓库的 commit-pinned raw URL：
  `https://raw.githubusercontent.com/mqqq333/Images/3c0356dae72b6fc3d0eac6de7d3455227d010f93/blob/main/banner.jfif`
- GitHub Stats 当前使用：
  `https://github-readme-stats-fast.vercel.app/api?username=mqqq333&show_icons=true&hide_border=true&theme=default`
  官方 `github-readme-stats.vercel.app` 在此前检查时返回 503，因此每次修改后都要重新检查第三方 endpoint。
- LeetCode Stats 已删除。
- README 中的 contribution snake 引用已删除；profile 仓库里仍保留 `assets/github-contribution-grid-snake.svg` 和 `.gif` 文件，但它们不再显示。只有在用户明确要求清理仓库资产时才删除文件。
- GitHub 自带的 contribution graph 已经足够，不要为了恢复旧 snake 图增加新的外链。

## 7. 两边需要同步的字段

修改个人事实时，以 homepage 为长版源头，再同步 profile：

| 字段 | Homepage | Profile |
| --- | --- | --- |
| 姓名/职位 | `_pages/about.md`、`_config.yml` | `README.md` 顶部 |
| 研究概述 | Research 三个项目 | Selected Research 三个缩写条目 |
| 项目 | Projects 分区 | Selected Projects |
| 托福 | Languages 分区 | Education and Skills |
| 公众号 | Writing 分区 | Writing |
| 外链 | 侧栏和正文 | 顶部入口和文章链接 |

profile 可以更短，但不要出现与 homepage 冲突的姓名、机构、地点、日期或成绩。

## 8. 发布与验证

先分别检查状态：

```powershell
Set-Location E:\mqqq333.github.io
git status --short
Set-Location E:\mqqq333-profile
git status --short
```

Homepage 修改后至少执行：

```powershell
Set-Location E:\mqqq333.github.io
git diff --check
bundle exec jekyll build
```

当前这台 Windows 环境的 `Gemfile` 声明了 `wdm (~> 0.1.0)`，但本机未安装该 gem，所以 `bundle exec jekyll build` 目前会在依赖解析阶段失败。已验证的临时替代命令是：

```powershell
$env:JEKYLL_NO_BUNDLER_REQUIRE = '1'
jekyll build
```

替代构建在本轮成功；输出中的 Sass deprecation warning 来自旧模板依赖，不是本 handoff 文档引入的错误。长期修复应在依赖允许时补齐 `wdm`，不要把环境变量写进页面源码。

然后在本地或线上检查：banner、侧栏头像和 lab icon、所有彩色分区图标、News 顺序、CV 链接、移动端换行，以及顶部蓝线和内容列宽。

Profile 修改后至少执行：

```powershell
Set-Location E:\mqqq333-profile
git diff --check
rg -n -i "leetcode|file://|[A-Z]:\\|github-contribution-grid-snake" README.md
```

上面的扫描应当不返回 LeetCode、本地路径或 snake 引用。再检查以下地址的 HTTP 状态和 Content-Type：

- `https://github.com/mqqq333`
- banner raw URL
- GitHub Stats endpoint
- 四个 shields.io badge URL
- homepage 和实验室链接，以及页面中仍保留的其他公开链接

提交时只加入目标文件：

```powershell
git add <目标文件>
git commit -m "<message>"
git push origin master
```

推送后以公开页面为准，而不是只看 raw README：确认 emoji 标题、徽章、banner、Stats、中文文本都已渲染，并在移动宽度下确认没有横向溢出。

## 9. 已知风险和可选待办

- Stats endpoint 是第三方服务，存在未来失效或限流风险；替换前先测试新的 endpoint，并保留一个可回退方案。
- banner 使用外部 Images 仓库的固定 commit；如果源图迁移，先更新 URL，再验证图片类型和裁切。
- `wechat_channel.jpg` 二维码目前不在 homepage 仓库中；用户曾提供过本地来源，但没有把它作为当前公开资源。若未来添加，先确认公开授权、文件位置和移动端尺寸。
- 公众号 favicon 已纳入网站，但不要把本地公众号项目目录整体复制进网页仓库。
- CV 是二进制文件，修改 TOEFL 或教育日期时要同步检查英文和中文 PDF，再检查下载链接。
- 研究日期、`in preparation` 状态和 News 年份需要用户确认后再更新；不要自行把未发表工作写成已发表。
- Claude 之前提出过的可选建议包括评估 anime 头像、减少侧栏与正文重复链接、统一图标色彩，以及增加 hosted-build smoke verification；这些不是当前必做项。
- 不要提交 `github-recovery-codes.txt`、`.chrome-tmp/`、浏览器截图或其他临时文件。

## 10. 相关审阅记录

以下文件是本轮计划和 Claude 审阅的本地记录，`.omx/` 默认不发布到网站：

- `.omx/artifacts/claude-act-as-a-senior-visual-designer-reviewing-an-academic-person-2026-09-01T12-10-11-904Z.md`
- `.omx/artifacts/ask-claude-acad-homepage-plan-review-20260901.md`
- `.omx/artifacts/profile-readme-plan-20260901.md`
- `.omx/artifacts/claude-review-the-proposed-plan-in-e-mqqq333-github-io-omx-artifact-2026-09-01T14-14-21-295Z.md`

下次开始时，优先执行：

1. 阅读本文件并检查两个仓库的 `git status`。
2. 读取 `_pages/about.md`、`_config.yml`、`_data/navigation.yml` 和 profile `README.md`。
3. 明确改动范围；重要改动先计划和 Claude 审阅。
4. 先改 homepage，再按同步字段更新 profile。
5. 运行构建、链接/图片扫描和桌面/移动端检查。
6. 分别提交、推送，并复核两个公开 URL。
