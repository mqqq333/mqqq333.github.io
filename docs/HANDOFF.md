# MA Qi Homepage and Profile Handoff

更新时间：2026-09-05（Asia/Shanghai）

这份文档是下一次继续修改个人 homepage 和 GitHub profile README 时的入口。先阅读本文件，再检查两个仓库的工作树；不要根据记忆重建内容。

## 0. 2026-09-02 至 2026-09-04 更新摘要

- 旧模板主页已作为 detached Git worktree 恢复到 `E:\mqqq333-old-homepage`，当前提交为 `f8b850471beeceb6c1ad19e6357c6d1e41e62899`。它只用于本地截图和新旧页面对比，不是第三个发布仓库；不要在其中提交或推送新的主页改动。
- schizophrenia 研究项目的 homepage 描述已改成与 profile 一致的简洁版本，不再在首页展开分类结果数字。对应 homepage 提交为 `eb5113ad62c23ffb200738a873c405b0622cc001`。
- `阿瞒的脑洞 (A Man's Brainhole)` 已在 homepage Writing 分区以静态卡片展示头像、介绍和官方关注二维码；GitHub Profile 使用较简洁的二维码和 homepage 链接。两边均未增加脚本、iframe、RSS、爬虫或第三方运行时。已部署提交分别为 homepage `54266c3359bfd33c5037bbd953be084bce022e5d`、profile `07f6cf9c58eac253447fb0cdd888f15142c0187a`。
- homepage 中原有的三篇文章继续明确归属于 `工心应援会`，位于 `阿瞒的脑洞` 卡片之外；不要把两个公众号的内容归属合并。
- 曾评估在 homepage/profile 展示“高阅读量文章”。测试链接 <https://mp.weixin.qq.com/s/NfqtEqxqo4DavqsuyvZaRw> 对应 `阿瞒的脑洞` 文章《心理学越接近统一，越需要保留差异？AI 时代的 Nexus 与 Babel》（2026-09-04 10:00）；公开标题、公众号、日期、简介和封面可以读取，但公开页面不提供真实阅读量。用户随后决定取消这一扩展，因此当前不新增精选文章区、不展示该链接，也不接入阅读量接口。若未来重新提出，需要作为新需求重新确认范围；不得把 WeChat `AppSecret`、`access_token`、cookie 或后台凭据放入 GitHub Pages/Profile。

## 0.1 2026-09-05 Homepage 审阅建议（仅保存，未执行）

本次只审阅 homepage，没有修改 homepage/profile 源码，也没有新的提交或部署。审阅依据包括当前 homepage 源码、线上 HTML、现有截图和公开链接检查。主页、两份 CV、banner、二维码、五个项目仓库、Cognomics Lab 和 Kong lab 链接本次检查均返回 HTTP 200；这只代表可访问，不代表外部页面内容永久不变。当前浏览器连接不可用，执行时仍需重新做 1440px、768px 和 390px 的视觉检查；现有 9 月 1 日截图早于公众号卡片提交，不能替代最新移动端截图。

### 第一批：建议优先修正

1. **停用空配置的 Google Analytics。** `_includes/analytics.html:1-10` 只要页面没有显式关闭 analytics 就会加载脚本，而 `_config.yml:15` 的 `google_analytics_id` 为空；线上 HTML 已实际请求带空 ID 的 Google Tag Manager。建议仅在 ID 非空时渲染统计代码，或直接移除该 include。默认不应向访客发起无用途的第三方统计请求。
2. **补齐移动端和图标链接的可访问名称。** `_includes/masthead.html:5` 的菜单按钮只有装饰性 `div`；`_includes/author-profile.html:119-163` 的移动端 Website、Email、GitHub 等链接只有被 `aria-hidden` 的图标。建议给菜单按钮添加 `aria-label`、`aria-expanded`、`aria-controls`，给每个图标链接添加明确标签，并复测键盘和屏幕阅读器可达性。
3. **补一个主内容 H1。** `_pages/about.md:14` 直接从介绍段落开始，`_layouts/default.html:20-25` 不会自动生成标题，线上页面当前没有 `<h1>`。建议在正文介绍开头加入唯一的 `MA Qi` H1，保留侧栏姓名作为紧凑身份信息，不把 H1 做成宣传式大标题。
4. **减轻首屏横幅资源。** `_pages/about.md:9` 使用的 `images/background.jpeg` 当前约 4093×1666、1.71 MB，而桌面和手机只显示约 360px/220px 高度。建议生成保持构图的压缩 WebP 或其他现代格式，并用 `srcset`/`sizes` 或等价的响应式资源选择；执行时比较桌面和移动端裁切，不直接删除原图，除非确认没有其他引用。
5. **修正重复 `<head>` 和全局新标签页策略。** `_includes/head.html:17-19` 在已有 `<head>` 内嵌套了第二个 `<head>`，并用 `<base target="_blank">` 影响所有链接。建议移除嵌套 head 和全局 base；站内锚点保持当前页，只有确需另开的外部链接显式设置 `target="_blank"` 并补 `rel="noopener"`，CV 链接按实际下载意图单独决定是否使用 `download`。

### 第二批：内容和信息架构建议

6. **让两个公众号的归属在视觉上更分明。** `_pages/about.md:66-87` 目前事实表述正确，但 `阿瞒的脑洞` 卡片后紧接着 `工心应援会` 文章列表，访客快速扫读时仍可能混淆。建议给文章列表增加清晰的 `工心应援会` 小标题或独立标签；保留两个账号分离，也不要恢复已取消的高阅读量文章区。
7. **精简顶部导航层级。** `_data/navigation.yml:3-28` 的 `About Me` 与 masthead 的 `Homepage` 都指向同一 `#about-me`，九个入口也把 Research、Writing 和只有 TOEFL 一行的 Languages 放在同一层级。建议保留约 4--6 个主要入口（About、Research、Projects、Writing、CV），其余内容仍留在长页或作为次级入口；这是信息架构建议，不要求重写模板。
8. **突出最能代表你的公开项目。** `_pages/about.md:49-52` 当前四个项目都是同等权重的文字列表。建议优先突出 HemiSpec 和脑可视化工具，并在已有公开许可的前提下增加一张真实输出图或明确 demo 链接；不要为了装饰新增未确认公开的材料。
9. **统一 Languages/Skills 的含义。** homepage 的 `Languages`（`_pages/about.md:104-109`）目前只有 TOEFL，而 profile 将编程徽章放在 Languages、把 TOEFL 放在 Education and Skills。建议将 TOEFL 移入 Education 或把该区改名为 `English Proficiency`，技术徽章另命名为 `Technical Stack`；如调整 profile，仍以 homepage 为长版源头同步。
10. **让 News 只承载明确的时间线事件。** `_pages/about.md:23-25` 的 `2026: Developing HemiSpec...` 更像当前工作概述，不像有日期的新闻。建议提供具体月份/里程碑后再保留，或移到 Research/Projects；没有用户确认的日期时不要自行补写。

### 建议执行顺序和边界

- 用户明确说“执行”后，先把选定批次写成短计划并交 Claude 审阅，再修改；本节当前只是备忘，不代表已获执行授权。
- 默认先做第一批 1--5，再单独决定第二批 6--10；每批修改后运行 Jekyll 构建、HTML 结构检查、公开链接检查和桌面/移动端截图。
- 本方案不包含更换模板、重启高阅读量公众号文章展示、接入 RSS/爬虫/动态 WeChat API、恢复 Delta AUC/q 值，或自动修改 profile 的无关内容。
- 若只执行 homepage 技术修正，profile 不需要同步；只有导航名称、个人事实或可见内容发生变化时，才按两边同步字段规则单独修改 profile。

## 1. 当前状态

| 页面 | 本地工作树 | 远端仓库 | 分支 | 当前内容基线 | 地址 |
| --- | --- | --- | --- | --- | --- |
| Academic homepage | `E:\mqqq333.github.io` | `git@github.com:mqqq333/mqqq333.github.io.git` | `master` | `54266c3359bfd33c5037bbd953be084bce022e5d` | <https://mqqq333.github.io> |
| GitHub profile | `E:\mqqq333-profile`（homepage 仓库的同级目录） | `https://github.com/mqqq333/mqqq333.git` | `master` | `07f6cf9c58eac253447fb0cdd888f15142c0187a` | <https://github.com/mqqq333> |

当前本地状态：

- homepage 还有未跟踪的 `.chrome-tmp/`、`images/wechat_QRCode.jpg` 和 `online-profile.png`。其中 `.chrome-tmp/` 是浏览器验证数据，`images/wechat_QRCode.jpg` 是用户提供的二维码源文件，`online-profile.png` 是截图；不要自动加入提交，也不要未经确认删除。
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
  1. Cross-Hemisphere Reconstruction-Derived Neuroanatomical Specificity in Schizophrenia：homepage 和 profile 均使用简洁表述，即 5 个站点、948 名受试者、ANS/RNS、多尺度组间差异、临床及认知关联和疾病分类；稿件状态为 `in preparation`。不要自行恢复主页此前展开的 Delta AUC 和 q 值。
  2. Cross-hemisphere reconstruction and handedness：研究重建残差与利手性的关系，状态为 `in preparation`。
  3. Operator-corrector validation of residual measures：跨人口学、行为和疾病场景验证校正残差，状态为 `in preparation`。
- Projects 当前包括 HemiSpec、Cortex Visualization Skill、Subcortex Visualization Skill、DecodeWM 和 LorewormGu。
- Writing：homepage 使用静态卡片展示 `阿瞒的脑洞` 的头像、简介、官方关注二维码和扫码说明；卡片下方继续保留明确归属于 `工心应援会` 的三篇英文文章清单。profile 是缩写版，展示 `阿瞒的脑洞` 简介、180px 二维码、扫码说明和 homepage Writing 锚点链接，不展示 `工心应援会` 清单。
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
- `images/aman_brainhole_qr.png`：`阿瞒的脑洞` 官方关注二维码，已公开并由 homepage 和 profile 共用；profile 通过 `https://mqqq333.github.io/images/aman_brainhole_qr.png` 引用。

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
- Writing 分区使用 GitHub 支持的基础 HTML：居中的 180px 二维码、可见扫码说明和指向 `https://mqqq333.github.io/#writing` 的非扫码入口。不要加入自定义 CSS、JavaScript、iframe 或动态公众号组件。

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
- `images/aman_brainhole_qr.png` 是当前发布中的官方关注二维码；用户提供的源文件 `images/wechat_QRCode.jpg` 仍为未跟踪文件，不要加入提交。以后替换二维码时使用新的版本化文件名，并同时更新 homepage/profile，避免 GitHub 图片代理缓存旧图。
- 公众号 favicon 已纳入网站，但不要把本地公众号项目目录整体复制进网页仓库。
- “高阅读量/精选文章”扩展已由用户取消，不是待办。公开微信公众号文章页通常能提供标题、日期、公众号、简介和封面，但不提供可验证的真实阅读量；不要为此增加抓取脚本、RSS 服务或前端 API。官方数据接口需要服务端凭据，也不适合静态 GitHub Pages/Profile。
- `E:\mqqq333-old-homepage` 是同一 homepage 仓库的 detached worktree，仅用于旧模板截图对比。不要把它复制进当前仓库，也不要从该 worktree 推送或覆盖 `master`。
- CV 是二进制文件，修改 TOEFL 或教育日期时要同步检查英文和中文 PDF，再检查下载链接。
- 研究日期、`in preparation` 状态和 News 年份需要用户确认后再更新；不要自行把未发表工作写成已发表。
- Claude 之前提出过的可选建议包括评估 anime 头像、减少侧栏与正文重复链接、统一图标色彩，以及增加 hosted-build smoke verification；这些不是当前必做项。
- 不要提交 `github-recovery-codes.txt`、`.chrome-tmp/`、`images/wechat_QRCode.jpg`、浏览器截图或其他临时文件。

## 10. 相关审阅记录

以下文件是本轮计划和 Claude 审阅的本地记录，`.omx/` 默认不发布到网站：

- `.omx/artifacts/claude-act-as-a-senior-visual-designer-reviewing-an-academic-person-2026-09-01T12-10-11-904Z.md`
- `.omx/artifacts/ask-claude-acad-homepage-plan-review-20260901.md`
- `.omx/artifacts/profile-readme-plan-20260901.md`
- `.omx/artifacts/claude-review-the-proposed-plan-in-e-mqqq333-github-io-omx-artifact-2026-09-01T14-14-21-295Z.md`
- `.omx/plans/wechat-official-account-showcase.md`
- `.omx/artifacts/claude-review-the-implementation-plan-at-e-mqqq333-github-io-omx-pl-2026-09-04T14-03-49-512Z.md`
- `.omx/artifacts/claude-re-review-the-revised-plan-at-e-mqqq333-github-io-omx-plans--2026-09-04T14-10-24-028Z.md`

下次开始时，优先执行：

1. 阅读本文件并检查两个仓库的 `git status`。
2. 读取 `_pages/about.md`、`_config.yml`、`_data/navigation.yml` 和 profile `README.md`。
3. 明确改动范围；重要改动先计划和 Claude 审阅。
4. 先改 homepage，再按同步字段更新 profile。
5. 运行构建、链接/图片扫描和桌面/移动端检查。
6. 分别提交、推送，并复核两个公开 URL。
