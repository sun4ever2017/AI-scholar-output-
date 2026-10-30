# 改稿说明（v1 2026-10-23 → v2 2026-10-30）

文件：`pitch_v2.docx`（Word，沿用原稿样式与页眉）与 `pitch_v2.md`（pandoc 源文件，便于继续修改；`pandoc pitch_v2.md -o pitch_v2.docx --reference-doc=<原 docx>` 即可重新生成）。
评审编号：01 文献与新颖性；02 识别与计量；03 意义与实践；04 可行性与数据；05 写作与一致性；06 金融/会计领域编辑；主审 = 我在看评审前写下的独立笔记。

## 1. 全局性改动

| 改动 | 来源 |
|---|---|
| 标题改为 *Which Research Does Generative AI Speed Up? Evidence from Finance and Accounting Working Papers*（备选 *More Papers or More Research?*）。原标题的 “productivity” 暗示总量效应，而设计识别的是方法间差异。 | 03、05、06 |
| 研究问题重心从 “how much” 改为 “which methods, by which wave, relative to the least-exposed methods; who gains; does the marginal paper hold up”。 | 全体 |
| 删除 Table 2（“Part of output growth” 一列）及 “summing β×Share … gives the AI part of that group's output growth” 的说法；新增 “What is identified” 段，明说只识别 method gradient，总效应只作为带锚定假设与 ±10/±25% 敏感性区间的次要展示（Appendix A2）。 | 02、05、06、主审 |
| 三个嵌套阶跃的 Release_k(t) 改为按方法的半年 event study（基期 2019H2）+ 预先固定的四个日历窗口 W1–W4；能力标签明确为 “可被估计否定的解释，而非识别假设”；给出完整发布日历（Appendix A1），承认 Copilot 早于 ChatGPT、2023 年写作与编码能力同时到来。 | 01、02、03、05、06 |
| 样本窗口解耦：按 2014–2018 ≥3 篇选样并测 shares；干净的 pre-period 为 2019Q1–2022Q3；2020–21 COVID 季度单独展示；原 2018–2021 定义与 ≥2/≥5 门槛作为稳健性（Appendix A3）。 | 02、05、06、主审 |
| 删去 “first stage / Wald ratio” 框架，AI 词汇改为描述性的机制检验。 | 02、05、主审 |
| 删去基于期刊文章的 posting-rate 控制变量，改为 ceiling test + 基于会议 program 的实时上传倾向 + 会计的 versions-per-paper / posting-stage 检验；新增期刊 pipeline（投稿即上传 SSRN）的识别与排除。 | 02、04、06、主审 |
| “inflation” 检验改写：说明 fixed-capacity 下发表份额下降是零假设而非证据（Appendix A3）；主要质量指标改为会议录用、同 cohort 同方法的 24 个月引用、同作者近重复；发表改用含右删失与期刊周转协变量的 hazard 模型；36/48 个月更新拆为预注册 companion paper；AI referee score 仅在通过 self-preference 检验后使用。 | 02、03、05、06、主审 |
| 篇幅：正文（Summary 至 K）从约 3,750 词压到约 3,450 词，协议细节（约 820 词）移入 Appendix A（发布日历、系数解读、样本窗口与 fixed-capacity、数据协议、推断计划），待办事项移入 Appendix B；原 Table 1 改为紧凑列表；删除重复的表格标题。仍长于 Faff 两页规范（约 1,700 词），如需短版可只保留 Summary、A–C、E 的 Core idea + 假设、H 表、I、K 的 ask。 | 05 |
| 人称改为 “we”（除 ask 一段），新增 “What I am looking for” 合作者 ask（角色、现有资产、待议事项用方括号留白）。 | 05 |

## 2. 分节改动

- **Project Summary**：重写为约 190 词；点明 Renault 问题与 exposure 设计、预期发现、第二部分（who gains + 是否过关）。来源：05（提供了改写稿）、03。
- **(B)**：主问题改为相对效应 + who gains；次问题改为 conference acceptance / citations / eventual publication。来源：全体。
- **(C)**：关键文献改为 Kusumegi–Renault–reply、Arcila、Walther & Dutordoir、Nee–Zhong–Ni，与 (H) 对齐；Novy-Marx & Velikov 与 Ciconte et al. 移入 (D) 作为机制证据；Kusumegi 回复的描述改为 “defends the direction of the association, not its magnitude”，删除无法核实的 “7–20%” 与 “concede”。来源：01、05、06。
- **(D)**：先事实后谜题；加入 multiple-testing / p-hacking 文献（Harvey 2017；Harvey–Liu–Zhu 2016；Mitton 2022；Brodeur et al. 2020）作为 “inflation by method” 的理论锚；注明 2023–24 计数与 SSRN 官方统计核对待补。来源：01、03、05。
- **(E)**：Core idea 改用 task-based 框架并加 Korinek (2023)；分类加入 G0/other、structural estimation、ML/LLM-as-method，并写明 archival-text 与 LLM-as-method 的编码规则；明确 data-source 拆分是本项目扩展而非 Coyne et al. 的；全部 2014–2026 论文都分类（为 paper-level 模型服务）；模型改为 event-study 形式并给出文字版；假设改写为参数陈述（参照组 = primary-data methods），H1 以 archival-standard 为主、review 为 W1 子预测，H2 改为 “只在 reasoning 模型之后、带滞后”，H3 以 hand-collected vs standard 为可检验对比，H4 改为 democratisation vs count-gaming 两个竞争性预测并纳入评价体制；新增 paper-level 补充模型。删除 “AI cannot have shaped it”、“without assuming it in advance”、“No common trend predicts this timing”。来源：01、02、03、05、06、主审。
- **(F)**：Crossref 作为 SSRN DOI 主干、OpenAlex 富化并与 SSRN 官方统计核对；删除 “JEL codes where authors report them”；新增作者身份验证计划（150–200 人）、600 篇双人盲编码与误分类校正、attrition 处理、pipeline 排除；删除 ICSR Lab/Scopus 作为既定渠道的表述（2025 年摘要缺口暂接受，Scopus 待测试）；异质性加入国家与评价体制；质量指标改列。来源：02、04、06。
- **(G)**：推断计划加入 exposure-robust SE（Adão–Kolesár–Morales）、randomisation inference、4 个预注册主对比 + Romano–Wolf、功效声明；识别检验加入 area×period FE 与 AI-topic share；posting vs production 与第二部分如上。来源：02、03、06。
- **(H)**：改为对照表（study / unit / outcome / AI measure / what changes here）+ 三条新增 + “why this is not Kusumegi on SSRN with another proxy”。来源：01、05。
- **(I)**：改为 actor → evidence → action（留 X/Y/Z 占位）；加入 AACSB、ABDC/ABS、ERA 继任者与 REF 2029、SSRN AI 披露政策；Keloharju 的论断改为 “H2 tests that claim”。来源：03、06。
- **(J)**：改为两条文献 + 一个机制 + 会计分支。来源：01、05。
- **(K)**：目标期刊改为 MS 跨领域首选、金融备选（JFE/RoF/JFQA）、会计 companion（CAR/AH）；风险合并为 5 条；限制段加入 “H1/H3 主要由会计学者识别、theory cells 小”；新增 HREC 时间、三阶段计划、预算、合作者 ask。来源：03、04、06。
- **Appendix A**：A1 发布日历与窗口；A2 系数解读（为何必须有参照方法、锚定假设、career-age 共线性）；A3 样本窗口 + fixed-capacity 推导；A4 数据协议；A5 推断计划。
- **Appendix B**：6 条待办（摘要覆盖率重推、OpenAlex 序列核对、Scopus 测试、引文核对、pipeline 量化、功效计算与预注册）。
- **References**：删除不再引用的 Brogaard et al. (2014)；新增 Adão et al. 2019、Agrawal & Goldfarb 2008、Brodeur et al. 2020、Card & DellaVigna 2013、Cohn–Liu–Wardlaw 2022、Correia et al. 2020、Cui–Ding–Zhu 2022、Ellison 2002、Hao et al. 2026、Harvey 2017、Harvey–Liu–Zhu 2016、Heckman & Moktan 2020、Korinek 2023、Mitton 2022、Rambachan & Roth 2023、Romano & Wolf 2005。

## 3. 未采纳或部分采纳的意见（及原因）

- **02 建议按 2012–2017 选样、2015–2019 测 share**：会把 2018 年后入行的年轻学者全部排除，而 H4 恰恰关心他们；折中为 2014–2018，并保留原定义作为稳健性。
- **03 建议把 H4 提到标题 / 作为全文组织结构**：已升为研究问题之一并写成竞争性预测，但标题仍以 “which research” 为主，因为 H1–H3 的 timing 检验是识别上最干净的部分；若首批结果显示异质性更强，可再调整。
- **03 建议的 country-level ChatGPT 可得性工具变量**、**02 的 split-sample IV**、**continuous capability index**：作为次要规格写进 Appendix A1/A2，不进正文。
- **04 建议把会议 program 匹配放到 stage 3**：与 02/03/06 的质量指标需求冲突，放在 stage 2 并先限于 AFA/WFA/AAA。
- **06 建议金融主导定位**：采用 “MS 跨领域首选 + 金融备选 + 会计 companion”，并在限制段明说 H1/H3 主要由会计样本识别。
- **05 的 1,700 词目标**：未完全达到（正文约 3,450 词，较原稿减少约 8%），原因是评审同时要求补充推断计划、质量指标、分阶段计划与合作者 ask；已把协议细节移入附录。
- **01 建议的 ex ante exposure index（按任务给每个方法打分）**：有价值但会改变处理变量的定义，建议作为第二规格由计量合作者评估后再加入；正文只保留 task-based 框架的叙述。

## 4. 改稿中沿用但评审未能核实、需作者确认的事实

见 pitch Appendix B 第 4 条：Hurley et al. (2025) 的具体月数（改稿写 “about two years”）；Walther & Dutordoir 的版本与样本量；Kusumegi et al. (2026) 回复中的数字；Arcila (2026) 的 SSRN 编号；Renault et al. (2026) 的 article number（05 查到 DOI 10.1073/pnas.2618638123）；Barrick et al. 已 forthcoming *Accounting Horizons*；Nee et al. 作者名；Hao et al. (2026) 卷期页码。另外：Cui–Ding–Zhu (2022) 与 Hao et al. (2026) 的书目信息来自评审与我的记忆，未在线核对。

## 5. 技术说明

- v2 由 Markdown 经 pandoc 生成，使用原 docx 作为样式模板，因此字体、标题、页眉（已更新为新标题）、页脚页码与原稿一致。公式以 Word 原生 OMML 写入，在 Word 中正常显示；本环境的 LibreOffice 渲染缺少数学字体，预览 PDF 中公式位置会显示为空白，原稿 docx 在同一环境下也是如此，并非文件问题。
- 没有使用 Word 修订模式：改动是整体重写，逐句 redline 不可读；本说明即为变更记录。

## 6. Grill 第一轮后的改动（2026-10-30，作者决定）

1. 样本：明确写成两个样本。主样本 2014–2018 ≥3 篇（干净 pre-period，承担识别主张）；第二样本沿用原定义 2018–2021 ≥2 篇，纳入 2018 年后入行的学者，服务 H4 的 career-stage 检验，但不承担识别主张。
2. 总效应：作者确认方法梯度足够。删除正文与 (K) 中的锚定总效应展示；Appendix A2 只保留一句 “不作总效应声称”。
3. AI referee score（Lu, Luo & Yu 2026）：按作者要求删除，参考文献同步删除。
4. 目标期刊：作者要求 FT50。(K) 改为 Management Science 首选（唯一跨领域 FT50 出口）；金融备选 JFE/RFS/JFQA/Review of Finance；会计 companion 改为 Contemporary Accounting Research（FT50），删除 Accounting Horizons；JF 标注为不现实。
5. 合作者 ask：作者暂不写，整段删除；正文仍用 “we”。
