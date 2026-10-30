# Pitch 多视角评审汇总

评审对象：*Generative AI and the Productivity of Finance and Accounting Scholars*（Faff 模板 research pitch，2026 年 10 月 23 日版，面向潜在合作者）。
评审方式：6 个独立运行的评审 agent，各自只拿到 pitch 原文和一个评审视角，互不可见；外加主审（我）在看到评审前写下的独立笔记。每份评审都做了少量在线事实核查（部分站点在本环境不可达，核查结果都标注了“已核实 / 来自记忆 / 无法核实”）。完整评审见 `reviews/` 目录。

## 1. 评分与一句话结论

| 视角 | 评分（/10） | 一句话结论 |
|---|---|---|
| 01 文献贡献与新颖性 | 6 | 读得很全，但 (H) 把新颖性放错了位置：真正新的是 exposure/ITT 设计，而不是“scholar-level, working-paper stage”（那是 Kusumegi 自己的设计）。 |
| 02 识别与计量 | 5 | 核心想法正确（预先决定的暴露 + 日历日期的处理），但 headline 估计量不可识别、release 日历站不住、样本窗口与 pre-trend 窗口重叠。 |
| 03 意义与实践 | 6（重构后 8–9） | 设计能回答的最重要问题（which methods / who gains / marginal paper 是否过关）被埋在第四个假设里；“how much” 这个问题设计答不了。 |
| 04 可行性与数据 | 6（砍到 MVP 核心则 8） | 核心设计便宜可做；问题是把 8 个数据组件捆在一起，其中 3 个的路线已失效或未经验证。 |
| 05 写作与内部一致性 | 6 | 原材料强，但 3,750 词正文是 Faff 模板的三倍，且找到 13 处前后矛盾；没有写给合作者的 ask。 |
| 06 金融 / 会计领域编辑 | 金融 6 / 会计 4 | 金融视角可行但 JF 不现实；会计视角下 SSRN 不是产出的普查，JAR 几乎必被 desk reject；建议 Management Science 跨领域投稿为首选。 |

## 2. 高度一致的核心问题（按严重程度排序）

**（1）研究问题与识别策略不匹配（6/6 评审 + 主审）。**
(B) 问 “how much does generative AI raise output”，而 (K) 自己承认 field×quarter 固定效应吸收了所有方法共有的效应，只能识别方法之间的差异。原因很简单：每个学者的 method shares 加总为 1，所以 Σ_m Release(t)×Share_im = Release(t)，与 field×quarter FE 完全共线（Goldsmith-Pinkham–Sorkin–Swift / Borusyak–Hull–Jaravel 的 complete-shares 情形）。Table 2 里 “Part of output growth” 一列以及 “summing β×Share … gives the AI part of that group's output growth” 这句话与此直接矛盾。
改法：把研究问题重心改成 “which methods, when, for whom, and does the marginal paper hold up”；删掉 “AI part of growth” 的说法；如要报告总效应，必须明说锚定假设（最不暴露的方法效应为零）并给敏感性区间，或另找对照组（低暴露的 SSRN 网络 / 跨领域）。

**（2）Release 日历与 writing / coding / reasoning 标签站不住（01、02、03、05、06）。**
ChatGPT 上线当天就能写 Stata/R/Python；GitHub Copilot 2022 年 6 月已 GA（早于 ChatGPT）；GPT-4（2023 年 3 月）是写作和编码能力最大的一次跳跃；Code Interpreter（2023 年 7 月 6 日，已核实）只是代码执行功能；o1-preview（2024 年 9 月）与 Claude Code（2025 年 2 月 24 日，已核实）只隔一两个季度。三个嵌套的阶跃虚拟变量在约 15 个季度里只是给日历窗口贴上任务标签。另外 Nee et al. (2026) 把数学的激增定在 2026 年而非 2024 年末，并解释为 “delayed diffusion and capability threshold”，说明响应有滞后，H2 的 “late 2024” 和 “No common trend predicts this timing” 都过强。
改法：改成按方法的 flexible event study（半年系数），加上预先登记的日历窗口 W1–W4；任务标签只作为可被数据否定的解释；H2 改写成 “theory 只在 reasoning 模型之后、且带滞后地上升，2023 年应为零”。

**（3）样本选择窗口、share 测量窗口、pre-trend 窗口三者重叠，且含 COVID（02、05、06、主审；03 亦提 COVID 反弹）。**
样本按 2018–2021 ≥2 篇选取，shares 也在 2018–2021 测，pre-trend 又检验 2018–2022：在选择窗口内部检验平行趋势部分是人为的，干净的 pre-period 只剩 2022Q1–Q3 三个季度。2020–21 疫情对实验/田野研究的冲击与 archival 不同（Cui, Ding & Zhu 2022 显示封城后 SSRN 产出短期 +35%），反弹会被误读为处理效应。两篇论文的门槛使 shares 只能取 {0, 0.5, 1}，测量误差大且引发均值回归。
改法：解耦三个窗口——例如按 2014–2018 ≥3 篇选样并测 shares，2019Q1–2022Q3 作为干净的 pre-period，2020–21 单独展示；配 Roth (2022)、Rambachan & Roth (2023) 的敏感性分析。

**（4）“24 个月内发 ABDC A*/A 或 FT50” 的 inflation 检验没有功效，且混淆了拥堵与质量（02、03、05、06、主审）。**
会计 submit-to-accept 本身就约两年，金融顶刊周期 2–4 年，所以 24 个月内发顶刊的基准率接近零，无法再下降；金融里 24 个月内能发出来的多是 Finance Research Letters 之类快速 ABDC-A 期刊，恰恰是吸收低质量数量的出口；期刊版面短期固定，供给上升 50% 时发表份额机械下降约三分之一（tournament / fixed-capacity 问题）；AI 可能让学者更早上传草稿，posting-to-publication 间隔会机械变长；LLM referee score 评价可能由 LLM 写的论文存在 self-preference 偏差。
改法：把 “inflation” 换成 Gartenberg 的中性说法 “more versus better / quality of the marginal paper”；用不依赖期刊队列的指标（会议录用 AFA/WFA/EFA/Cavalcade/FIRS、AAA/FARS；同 cohort 同方法的 24 个月引用；同一作者的近重复论文）；发表用含右删失的离散时间 hazard 模型并把期刊周转作为协变量；36/48 个月的长窗口分析作为预注册的 companion paper。

**（5）“First stage / Wald ratio” 不成立；SSRN posting-rate 控制变量不可测且是结果变量的函数（02、04、05、06、主审）。**
Wald ratio 是 IV 估计量，排他性要求 release×share 只通过 AI 词汇影响产出——pitch 自己承认词汇只衡量写作，所以排他性必然失败。posting rate 按期刊文章计算，2024–26 年发表的文章是几年前写的，近期 cohort 根本观测不到；分子又是 SSRN 上传数，是典型的 bad control。
改法：AI 词汇降级为描述性的机制检验；posting rate 换成 “ceiling test”（pre-period 几乎全部上传 SSRN 的学者无法再提高上传率）和基于会议 program 的实时上传倾向；量化 Elsevier “First Look” 等投稿即上传的 pipeline 并做排除稳健性。

**（6）新颖性表述错位、关键文献列表不一致（01、05、06）。**
(C) 列的是 Kusumegi/Renault/Novy-Marx/Ciconte，(H) 却说 “四项最接近的研究” 是 Walther & Dutordoir/Arcila/Gardner/Barrick，两边不重合。真正可辩护的新意是：exposure 设计不需要 adoption date、识别从不使用学者自己的产出或文本、把在位学者的 intensive margin 与新进入者分开、在 Arcila 的 26 个 OpenAlex fields 看不到金融和会计的地方工作。Nee et al. 是 method-level timing 的直接竞争者而非脚注。缺引：Hao et al. (2026, Nature)、Korinek (2023)、Agrawal & Goldfarb (2008)、Ellison (2002)、Card & DellaVigna (2013)、Heckman & Moktan (2020)、Harvey (2017)、Harvey–Liu–Zhu (2016)、Mitton (2022)、Brodeur et al. (2020)，以及 shift-share / 连续处理 DiD 的计量文献。

**（7）数据路线与可行性（04、06）。**
已核实：ICSR Lab 于 2023 年 12 月 31 日关闭，pitch 把它作为 2025 年摘要的许可渠道是错的；Scopus API 是否返回 SSRN 预印本未经确认；SSRN 条款禁止任何自动查询，所以 “JEL codes where authors report them” 拿不到；CWTS 对 2025 年 1 月 Crossref 快照的分析称 SSRN 预印本的 Crossref 元数据不含摘要，与 pitch 的覆盖率数字冲突，需用可复现的查询重新推导（并补 2018–21 覆盖率，这才是分类最需要的）。最大的测量风险是作者身份：OpenAlex 作者 ID 会分裂/合并，且 SSRN 记录的输入源恰好在 2021/22 边界改变；“92% ORCID” 很可能是 has_orcid 过滤器（任一作者 profile 带 ORCID），不说明记录级身份质量。8 个数据组件合计 40–50 人周，必须定义 MVP。

**（8）写作与模板（05）。**
正文 3,750 词是 Faff 模板的三倍，(E) 一节 1,231 词；假设是方向性散文而非参数陈述；“AI cannot have shaped it”、“without assuming it in advance”、“No common trend predicts this timing” 三句过度声称；(C) 说 “standard archival designs are the easiest to automate, a prediction this project tests (H1)” 但 H1 原文说的是 writing release→review/commentary；三种还是四种 release 类型前后不一致；样本描述（“long-term posters” vs “≥2 papers in 2018–2021”）不一致；面向合作者却没有 ask。

## 3. 评审之间的分歧与本次改稿的取舍

| 争议点 | 各方意见 | 本次取舍 |
|---|---|---|
| 质量/inflation 分析的地位 | 05：要么升为 co-primary 要么改写 (D) 的 puzzle；03：重构为 “supply shock to the journal system”，长窗口拆成 Paper 2；06：换成会议录用、引用、长窗口顶刊 | 保留为第二部分，但换成不依赖期刊队列的近期指标，明确 fixed-capacity 的零假设；36/48 个月更新作为预注册的 companion paper；(D) 的 puzzle 改写为 “where does the boom come from, and does the marginal paper hold up” |
| 定位 | 06：金融主导，会计作为方法异质性对照；03：MS 跨领域，以 H4 为组织结构 | 以 Management Science 跨领域为首选，金融主导作为备选（JFE/RoF/JFQA），会计 companion（CAR/AH）；明说 H1/H3 主要由会计学者识别 |
| 要不要报告总效应 | 02：必须说明锚定假设；03：给上下界；06：另找低暴露对照 | 主估计量是相对效应；锚定的总效应作为带敏感性区间的次要展示，附上固定面板自身增长作为上界 |
| 会议匹配的阶段 | 04：3–4 人周，放到 stage 3；02/03/06：应是主要的近期质量指标 | 放到 stage 2，先限于 AFA/WFA/AAA |
| 样本窗口 | 02：2012–17 选样、2015–19 测 share；05：保留 2018–21 | 2014–2018 选样并测 share（≥3 篇），2019Q1–2022Q3 作为干净 pre-period，原 2018–21 定义作为稳健性（它能纳入更多年轻学者） |
| H4 是否升为主线 | 03：应成为组织结构甚至进标题；06：作为 “best heterogeneity test” | 升为与 H1–H3 并列的研究问题之一（“who gains”），写成 democratisation vs count-gaming 两个竞争性预测，但标题仍以 “which research” 为主 |

## 4. 评审一致认为应保留的优点

- 以 Renault 批评为约束条件、用 pre-ChatGPT method mix 作为预先决定的暴露：正确且可一句话讲清，是整个项目的卖点。
- AI 词汇只作为机制检验而非处理变量；固定的在位学者面板；field×quarter 固定效应；PPML；按方法的 event study。
- H2（theory 只对 reasoning 模型响应）是设计里最锐利、可证伪的 timing 检验。
- 数据部分具体（OpenAlex/Crossref 路线、不爬 SSRN、许可与伦理意识）。
- “Limitations stated upfront” 一段诚实，应保留并让它约束 (B) 和 Table 2。
- (I) 有具体受众。

## 5. 优先行动清单

**本次改稿已做（见 `change_log.md`）：** 重写研究问题与 Summary；删除总效应/“AI part” 的说法并写明识别对象；event study + 预先登记窗口替代嵌套阶跃；解耦样本/share/pre-trend 窗口；假设改写为参数陈述；H4 改为 democratisation vs count-gaming；质量分析改用 slot-free 指标并声明 fixed-capacity 零假设；删去 first stage/Wald ratio；posting-rate 控制改为 ceiling test + 会议 program；补作者身份验证、600 篇双人编码、First Look 诊断、ICSR 已关闭；(C)/(H) 对齐并加 “why not a replication”；(I) 改成 actor→evidence→action；(J) 改为两条文献 + 一个机制；(K) 加目标期刊的现实路径、分阶段计划、预算、合作者 ask；正文从约 3,750 词压到约 3,450 词，协议细节移到附录（仍长于 Faff 两页规范，change_log 里给了进一步压成短版的取舍）；参考文献只保留被引且补齐计量/科学学文献。

**作者需要亲自做的（改稿里标在 Appendix B）：**
1. 用可复现的查询重新推导摘要覆盖率（Crossref vs OpenAlex，按年份与 deposit type），补 2014–2018 覆盖率。
2. 用 SSRN 自己的统计数据验证 OpenAlex 的 SSRN 序列，解释 2021→2022 总上传量翻倍（索引变化还是产出变化），补 2023、2024 年金融/会计计数。
3. 第一周测试 Scopus API 是否返回 SSRN 预印本（20 个已知 2025 DOI）；考虑 Dimensions 的免费研究申请。
4. 核对引文细节：Hurley et al. 的 “26 个月”（早期版本为约 23 个月，改稿暂写 “about two years”）；Walther & Dutordoir 的版本与样本量（55,964 vs 早期 41,489）；Kusumegi 2026 回复里的 “7–20%”（摘要中找不到）；Arcila 的 SSRN 编号；Renault et al. 的 PNAS article number；Barrick et al. 已 forthcoming *Accounting Horizons*；Nee et al. 作者名；Hao et al. 卷期页码。
5. 从元数据模式量化期刊 pipeline（投稿即上传 SSRN）的比例并定排除规则。
6. 在估计前用 2014–2021 面板做功效计算，固定主要对比，预注册分析计划。
7. HREC 低风险申请本月第一周提交（4–8 周）。

## 6. 各评审的要点摘录

**01 文献与新颖性（6/10）。** (H) 的第 1 条 “scholar-level at the working-paper stage” 正是 Kusumegi 的设计；应改写为 “exposure design rather than adoption design” 并加一段 “why this is not a replication”。Arcila 的 26 个 “disciplines” 是 OpenAlex 的 26 个 fields，金融在 “Economics, Econometrics and Finance” 内、会计在 “Business, Management and Accounting” 内，他看不到两者，也分不开在位者与新进入者。Nee et al. 是 method-level timing 的最近竞争者，其摘要并未提 reasoning models，“verifiable derivations” 是 pitch 自己的解读。“research vs inflation” 是 Gartenberg/Novy-Marx/Walther 已有的对话；新的部分是按方法的 inflation 预测，应锚定在金融/会计的 multiple-testing 文献（Harvey 2017；Harvey–Liu–Zhu 2016；Mitton 2022；Brodeur et al. 2020）。Kusumegi 回复的 “7–20%” 与 “concede” 无法支持，回复摘要说的是 “existence and direction … not a specific magnitude”。(J) 的三条文献结构弱，应为两条文献 + 一个机制。

**02 识别与计量（5/10）。** 见第 2 节 (1)(2)(3)(5)。此外：shares 与研究领域共线（会计以 archival 为主、实验集中在 auditing/managerial、理论集中在 G1/G3），β_km 会吸收任何领域特有的 2022 后冲击（AI 作为话题、crypto、银行危机），建议加 area×quarter FE 与 pre-period AI/ML 话题份额×quarter；推断应加 exposure-robust (AKM) 标准误、对安慰剂日期与 share 置换的 randomisation inference、预注册 4–5 个主要对比 + Romano–Wolf；career age 与学者/时间 FE 共线（age–period–cohort），需粗分箱；建议同时估计 paper-level（scholar×method×quarter）模型区分 acceleration 与 substitution。给出了建议的方程和三张首稿图。

**03 意义与实践（6/10；重构后 8–9）。** 电梯陈述：“把一个有争议的总量（AI 使产出增加 7%–60%）变成一张地图：激增来自哪里、值多少。” 承载全文的图：把 2022 年后 SSRN 激增分解为新进入者、在位学者按方法的 AI 归因产出、上传率变化、未解释的共同部分——即使 β 很小也能挽救论文（“激增不是在位学者的生产率”本身就是结论）。(I) 只点名受众不给动作：评价者应 within-method 比较或停止计数 working paper；编辑应做 targeted screening 而非一刀切收费；缺失受众包括 AACSB、ABDC/FT 名单管理者、ERA 的继任者（ERA 已于 2023 年终止，已核实）与 REF 2029、资助机构、招聘委员会。H4 应成为组织结构（democratisation vs count-gaming，Kim–Morse–Zingales 的续篇）。给出 “home run / nothing to see” 两种结果的概率估计（约 30% / 45%）与功效声明的要求。

**04 可行性与数据（6/10；MVP 8/10）。** 见第 2 节 (7)。可行性表：Crossref spine 1 周；OpenAlex 富化 1.5 周；面板与身份验证 2–3 周；LLM 分类 + 600 篇双人编码 2 周 + RA 120 小时；PPML 2 周；First Look 诊断 1 周；SSRN↔期刊匹配 2–3 周（stage 2）；会议 program 3–4 周（stage 3）；posting-rate 测度 3 周（建议替换）。分阶段：Stage 1 MVP 2026-11 至 2027-02（含 HREC 第一周提交、AFA 2028 投稿）；Stage 2 2027-03 至 06；Stage 3 2027 下半年起。预算：stage 1 约 A$8–10k（LLM 约 US$1–1.5k，RA 编码约 A$6–8k），全部约 A$18–25k。另：OpenAlex topic 的 top-1 准确率 0.72（已核实），无摘要时更低；建议按期刊组合定义学者而非 OpenAlex 话题标签；最后一两个季度不完整，主样本止于 2026Q2。

**05 写作与一致性（6/10）。** 13 处矛盾逐条列出（见第 2 节 (8)）；各节目标字数（正文约 1,700 词 + 一页技术附录）；重写了 Summary（179 词）、H1–H4（参数陈述）和 111 词的合作者 ask；核对 8 篇 2026 年文献均存在（Renault PNAS 123(33)，DOI 10.1073/pnas.2618638123 已确认；Ciconte 页码 RePEc 与 Springer 不一致；Arcila 的 SSRN 编号未能确认，但 Zenodo 上有同名复现包）。

**06 领域编辑（金融 6 / 会计 4）。** 金融编辑：归入 Barber et al. (2021) / Kim–Morse–Zingales (2009) 一类 “finance about finance” 论文；一审会要求按方法分类的产出（papers *of* method m 而非 papers *by* scholars whose past mix was m）、排除 ML asset pricing/climate/crypto 等话题潮流、用会议录用和引用做质量指标、量化 Elsevier 投稿→SSRN pipeline、对安慰剂日期做 randomisation inference；方法分类缺 structural、ML/LLM-as-method、methodological。会计编辑：JAR 几乎不发 research-on-research 且一半是金融；SSRN 在会计里是 stage-dependent 的窗口（与会议/R&R 阶段绑定；pitch 自己的 15–72% 链接率就是证据）；“archival by data source” 的拆分是作者的扩展而非 Coyne et al. 的；“business schools count papers” 是 ABDC/ABS 体制的前提，对美国顶校编辑陌生——应把它变成最好的异质性检验而非前提。Desk-reject 风险：MS（Finance）约 55%，JF 85–90%，JAR >90%。已核实 Kusumegi SSRN +59.8%、Ciconte 页码、Lu–Luo–Yu（2026-10-13 上传）等 10 条引文。
