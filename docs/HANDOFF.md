# MA Qi Homepage and Profile Handoff

更新时间：2026-10-18

这份文档是下一次继续修改个人 homepage 和 GitHub profile README 时的入口。先阅读本文件，再检查两个仓库的工作树；不要根据记忆重建内容。

## 2026-10-18 简历审核建议落实

- 用户同意后，唯一双语源稿已精简 LorewormGu、弱化无依据的能力宣传、明确工作职责，核实后补充 HemiSpec 源码安装/双语文档/pytest 测试交付物，并补入正文已有的 Linux、FreeIPA/SSSD、Slurm 技能；优化英文科研标题日期与表达。不添加准确参数量、新论文结果、R、TOEFL 日期或额外 Slurm 职责。
- 所有既定日期、公众号 95 篇与新增 1,200+ 关注者、948 人及利手 AUC/p 值保持不变。N-back 仍为项目末尾的单条课程项目；科学传播仍在全部项目之后。算子矫正独立存档不改动。
- 修改前快照为源稿仓库 `resume-before-review-edits-20261018`（`da30751`）和本仓库 `cv-before-review-edits-20261018`（`6b8eefc`）；详细文案与回滚流程见外部源稿仓库的 `RESUME_MAINTENANCE.md`。
- 本次仅同步两份 `files/` 下载 PDF 与本地提交，不推送、不部署，不改主页正文、Profile 或原有未跟踪文件。验证：双语各两页、四页视觉检查、XeLaTeX 零溢出/欠满/缺字、按语言五处 PDF SHA-256 一致、主页下载链接不变，Jekyll 替代构建通过，仅保留原有 Sass 弃用警告。
- 修改后的 Claude Code Sonnet 5.5 只读复核已成功，指定和实际模型一致，九个文件（含四图）全部读取成功；结论为“可以交付”，未见事实性或排版硬伤。外部审核没有重复执行构建或哈希验证。完整落实记录与主代理判断在外部源稿仓库 `RESUME_REVIEW_FOLLOWUP_20261018.md`，原始 CLI 证据在该仓库忽略的 `.omx/artifacts/`。

## 2026-10-18 简历可视化项目日期与 Claude 审核

- 按用户确认，将可视化 Codex Skills 项目改为 2026 年 5 月至 8 月，英文对应 May 2026–Aug 2026；HemiSpec 的进行中日期与其他内容不改。修改前快照分别为源稿仓库 `resume-before-visualization-date-20261018` 和本仓库 `cv-before-visualization-date-20261018`。
- 按要求完成本机 Claude Code Sonnet 5.5 只读审核，成功返回及模型元数据均确认 `claude-sonnet-5-5`。完整意见和主代理复核保存在外部唯一源稿仓库的 `RESUME_REVIEW_20261018.md`，原始返回留在其 Git 忽略的 `.omx/artifacts/`；不将审核输入或临时文件加入网站仓库，亦未自动应用需要事实核实的建议。
- 中英文各两页，源稿定向差异、四页渲染、PDF 副本与构建输出哈希均通过；主页替代构建仅有旧 Sass 弃用警告。仅本地提交与同步，不推送、不部署，主页正文、Profile 与原有未跟踪文件保持原状。

## 2026-10-18 简历栏目顺序与标题调整

- N-back / DecodeWM 移至项目经历末尾，以项目名称和一条实践说明呈现，仍明确为 Neuromatch Academy 课程项目，不恢复准确率或科研成果叙述。
- 公众号栏目缩短为“科学传播” / “Science Communication”，放在全部项目条目之后、技能之前，原有职责、运营数字和日期不变。此前“位于教育经历”“科学传播与内容创作”的记录是历史状态，以本节为准。
- 修改前快照分别为源稿仓库 `resume-before-section-reorder-20261018` 和本仓库 `cv-before-section-reorder-20261018`；继续从唯一源稿同步两份 PDF，仅本地提交，不推送、不部署，不改主页正文、Profile 或原有未跟踪文件。
- 验证：中英文各两页，项目章节从第一页开始，HemiSpec 未跨页，集群项目起另页；N-back 位于项目末尾，随后为“科学传播”，再到技能。四页渲染、其余内容不变、日期数字、公众号链接、五处 PDF 哈希与主页替代构建均已检查，仅保留既有 Sass 弃用警告。

## 2026-10-17 简历公众号经历与课程项目精简

- 中英文简历新增独立的科学传播栏目，记录「阿瞒的脑洞」的论文选题、方法解读、AI 辅助内容制作与证据审核职责，不将其列为科研成果或正式雇佣经历，也不混入「工心应援会」文章。
- 2026 年 6 月至今、累计 95 篇推文、新增 1,200+ 名关注者为用户于本日提供的数据；不改写为总粉丝数，不新增阅读量或商业成果。精神分裂症研究时间也按用户确认补为 2026 年 6 月至今。
- N-back / DecodeWM 移至教育经历，标明 Neuromatch Academy 课程项目，保留一条数据与方法说明，删除准确率及详细研究亮点。唯一源稿的修改前版本固定在 `resume-before-wechat-update-20261017`，本仓库旧 PDF 固定在 `cv-before-wechat-update-20261017`。
- 仍只从唯一源稿同步两份下载 PDF，并做本地提交；不推送、不部署，不改主页正文、Profile 或原有未跟踪文件。后续若要把运营数据也加入主页正文，应单独确认范围与统计日期。
- 验证：中英文各两页，四页渲染与源稿定向差异检查通过，公众号链接、运营数字及两处六月起始日期正确；课程项目各压缩为一条。所有 PDF 副本及 `_site/files/` 输出哈希一致，主页下载链接保持有效；使用既有替代命令构建通过，仅有旧 Sass 弃用警告。

## 2026-10-17 简历教育精简与集群项目更新

- 中英文简历移除小学、初中和高中经历，教育部分保留浙江大学本科；集群项目采用更正式的名称“实验室计算集群建设与运维” / “Laboratory Computing Cluster Deployment & Operations”，时间按用户确认更新为 2026 年 6 月至 10 月，项目要点不变。精神分裂症等其他科研经历及算子矫正独立存档不改动。
- 主页两份下载 PDF 继续从唯一中英文源稿生成并同步，不分别维护。修改前快照分别为源稿仓库 `resume-before-education-trim-20261017` 和本仓库 `cv-before-education-trim-20261017`；基础教育条目可从旧源稿取回。
- 本轮仅本地同步和提交，不推送、不部署，不改主页正文、Profile 或原有未跟踪文件。此前“当前稿包含完整基础教育经历”的条目是历史记录，以本节为准。
- 验证：中英文各两页，逐页渲染及源稿定向差异检查通过，项目章节统一从第二页开始，学校条目已移除，项目名称与日期正确。所有维护中的 PDF 副本与 Jekyll 输出哈希一致；使用既有替代命令构建通过，仅有旧 Sass 弃用警告。

## 2026-10-17 简历科研条目替换与算子矫正存档

- 按用户新要求，将两份简历中的 Operator-Corrector 条目替换为精神分裂症研究，并同步 `files/MAQi_CV_en.pdf` 与 `files/MAQi_resume_cn.pdf`。研究事实沿用主页和 Profile 已有口径：5 个站点、948 人、多尺度组间差异、临床与认知关联、疾病分类，论文撰写中。不借用另一个 OC 项目的结果数字，也不推定起始月份。
- 原 OC 中英文条目保存在外部简历仓库的 `archive/research/`；完整旧源稿与 PDF 固定于 `resume-before-schizophrenia-swap-20261017`。本仓库旧 PDF 固定于 `cv-before-schizophrenia-swap-20261017`，均不覆盖此前标签。
- 此次只替换简历条目，主页 Research 正文和 Profile 的在研项目列表不改动。主页 PDF 继续通过既有同步脚本从同一源稿生成，不分别编辑。
- 仅本地提交，不推送、不部署；原有未跟踪文件保持原状。
- 验证：中英文各两页，当前 PDF 不再包含 OC 条目；独立存档正文与替换前原文一致，补回章节分隔空行后可还原原始源稿，其余经历未改动。PDF 四处副本及 Jekyll 构建输出哈希一致，使用既有替代命令构建通过，仅保留旧 Sass 弃用警告。新版本标签分别为源稿仓库 `resume-schizophrenia-20261017` 和本仓库 `cv-schizophrenia-20261017`。

## 2026-10-17 简历源稿与主页下载文件同步

- 按用户要求，将 `files/MAQi_CV_en.pdf` 和 `files/MAQi_resume_cn.pdf` 与外部简历工作目录中的当前中英文稿同步；新增 FreeIPA / SSSD 身份迁移与四节点 Slurm 验收经历，只写已记录的成果。两份 PDF 均为两页。
- 当前稿还包含完整基础教育经历，旧主页 PDF 没有；此次按当前稿同步，未额外改写这些内容。主页正文、News、Education、Profile 等均未改动，不代表这些区域与 PDF 的个人信息已经逐项统一。
- 外部简历工作目录现在有独立的本地 Git 仓库；唯一源稿是 `resume-zh_CN.tex` 与 `resume_en.tex`。在该目录运行 `powershell -NoProfile -ExecutionPolicy Bypass -File .\sync-homepage-resume.ps1 -Build` 可重新编译并同步，`-Check` 可只读核对主页链接及 PDF 副本 SHA-256。详细流程与两种回滚边界见该目录的 `RESUME_MAINTENANCE.md`。不要分别维护主页 PDF，也不要将整个源稿目录加入公开仓库。
- 本仓库标签 `cv-before-sync-20261017` 保存同步前的公开 PDF；`cv-synced-20261017` 保存此次同步版本。仅恢复旧公开文件可运行 `git restore --source=cv-before-sync-20261017 -- files/MAQi_CV_en.pdf files/MAQi_resume_cn.pdf`，检查后显式提交；不要使用全仓库 `reset --hard`。
- 本次仅在本机同步和提交，未推送、未触发部署，也未改动原有三个未跟踪路径。更早条目中的“CV 尚未重生成”是历史状态，以本节为准。
- 验证：PowerShell 语法检查、同步前漂移拒绝、同步后四处 PDF 的 SHA-256 一致性、两页渲染、Git 旧源稿/旧 PDF 取回比对均通过。`bundle exec jekyll build` 仍因缺少既有 `wdm` 依赖失败；使用本文已记录的 `JEKYLL_NO_BUNDLER_REQUIRE=1` 替代命令构建成功，输出仅有旧模板的 Sass 弃用警告。

## 2026-10-03 大学名称链接

- 用户指定公开页面中的 Zhejiang University 链接为 `http://www.psych.zju.edu.cn/psychen/main.htm`，Heidelberg University 链接为 `https://www.cl.uni-heidelberg.de/english/`。
- homepage 简介、News、Education、侧栏以及 profile 顶部、About、Education 中的可见大学名称均使用上述院系链接；录取学位核对所用的官方项目页仍作为本文件的历史证据来源。

## 2026-10-02 海德堡大学录取信息更新

- 用户确认将赴海德堡大学就读计算语言学。用户指定材料目录中的录取通知书 `admission_letter.pdf` 确认项目为 Computational Linguistics，入学学期为 winter semester 2026/27，录取日期为 2026-09-11；[大学官方项目页](https://www.uni-heidelberg.de/en/study/all-subjects/computational-linguistics/computational-linguistics-master) 确认学位为 Master of Arts（M.A.）。
- 本次更新 homepage 的简介、News、Education、侧栏身份和站点标题/描述，并同步 profile 的顶部身份、About 和 Education。统一使用 `incoming` / `will join`，不要仅凭录取通知书写成已经入学、已经搬至德国或已离开 Cognomics Lab。
- 录取通知书仅用于核对，不复制到公开仓库。公开内容不含申请编号、私人地址、入学手续或本地材料路径。
- 两份公开 CV PDF 暂未重生成；当前简历工作目录中的 PDF 文本与公开版本已有其他差异，后续同步时先审阅源稿，避免连带公开无关更新。
- 验证：使用下述 `JEKYLL_NO_BUNDLER_REQUIRE=1` 替代命令构建成功；YAML/front matter、生成页面中的简介/News/教育/Open Graph 元信息、两仓库字段一致性及相关链接检查通过。浏览器连接当前不可用，桌面和移动端视觉检查未完成。
- 发布授权：用户于 2026-10-02 明确要求“上线”，授权提交并推送 homepage 和 GitHub Profile。发布后以线上页面核对为准，不将推送成功直接等同于部署完成。

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
- 当前侧栏身份：Incoming M.A. Student in Computational Linguistics, Heidelberg University.；正文仍保留当前 Cognomics Lab research assistant 经历。
- 正文介绍中保留 Cognomics Lab 和 Xiang-Zhen Kong (孔祥祯) 的链接；profile 中不放单独的 `PI:` 行。
- 位置：`Hangzhou, China`，不要再加 `Zhejiang`，以免侧栏换行溢出；尚未确认迁居，不提前改成 Heidelberg。
- 研究主线：计算神经科学、结构神经影像、脑半球偏侧化、跨半球重建和生成模型。
- News 按从新到旧排列；最新条目为 Sep 2026 获海德堡大学 M.A. Computational Linguistics 录取（winter semester 2026/27），另保留 2026 项目开发和 Jul 2025 的既有条目。
- Education 首项为 Heidelberg University, Master of Arts (M.A.) in Computational Linguistics, incoming, winter semester 2026/27；其次为浙江大学心理学学士经历。不推算毕业时间。
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
