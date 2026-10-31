# 交接说明：在本地 session 跑初步结果

日期：2026-10-31。来源：云端会话（pitch 评审与改稿）。

## 文件在哪
- GitHub：`sun4ever2017/AI-scholar-output-`，分支 `claude/elegant-babbage-3cmulf`，目录 `genai-productivity-pitch/`。
- `pitch_v2.md` 是当前版本的源文件（pandoc），`pitch_v2.docx` 由它生成；`change_log.md` 记录每处改动及对应评审意见；`reviews/` 是六份独立评审；`00_feedback_summary.md` 是中文汇总。

## 已经拍板的设计决定
1. 研究对象是方法梯度（which methods, by which wave, relative to primary-data methods），不做总效应声称。
2. 两个样本：主样本 2014–2018 年 ≥3 篇 SSRN 金融/会计论文（shares 也在此窗口测），干净 pre-period 为 2019Q1–2022Q3，承担识别主张；第二样本为 2018–2021 年 ≥2 篇，服务 H4 的年轻学者检验。
3. 事件研究按方法、半年系数，基期 2019H2；四个预先固定的窗口 W1 2022Q4–2023Q2、W2 2023Q3–2024Q3、W3 2024Q4–2025Q1、W4 2025Q2–2026Q2；主样本止于 2026Q2。
4. 参照方法为 primary-data methods（实验、问卷、访谈、田野）。
5. 质量分析用不依赖期刊队列的指标（会议录用、同 cohort 同方法 24 个月引用、同作者近重复）；AI referee score 已删。
6. 目标期刊限 FT50：Management Science 首选；JFE/RFS/JFQA/RoF 备选；会计 companion 投 CAR。
7. 分类走订阅路线：用 Claude Code 的 agent 标注 1,500–2,000 篇分层样本（Opus 5.5，effort low/medium 足够），本地训练 TF-IDF + logistic 分类器给其余论文打标签，再抽 600 篇人工双盲校验。全量 LLM 分类留作稳健性。

## 尚未决定（开跑前要定）
- HREC：pitch 写明批准前不开始研究。初步结果是只做聚合层面（按方法份额分组的季度计数，不保留身份），还是直接建 scholar-level 面板？
- OpenAlex polite pool 请求里是否附作者邮箱（`mailto=`）。
- Crossref 上 SSRN DOI 从哪一年起全量注册；若 2014–2016 不全，主样本窗口后移。
- 初步结果的定义：建议为三件套——按年计数并与 SSRN 官方统计核对、分类校准表（κ、混淆矩阵）、主样本按方法的 event-study 图（含 H2 的 theory 路径）。

## 建议的 stage-0 流水线
1. 数据主干：Crossref `prefix 10.2139` 取全部 SSRN DOI 与 `created` 日期（抽 50 条人工核对上传日期）；OpenAlex 按 DOI 富化（作者 ID、topics、机构、引用、期刊版本）。不爬 SSRN 页面，不用 SSRN 的 JEL codes 与下载量。
2. 先出按年计数（Finance subfield 2003、Accounting 1402；同时用 `locations.source.issn:1556-5068`）并与 SSRN 官方统计对照，解释 2021→2022 的全站翻倍。
3. 作者身份：OpenAlex author ID 只作种子；按姓名规范化 + 合作者重叠 + 主题相似 + ORCID 做独立归并；抽 150–200 人分 2022 前后人工核对。
4. 分类：见上面第 7 条；类别至少为 analytical / archival-standard / archival-text / archival-hand-collected / experimental+survey+field / review；金融另加 structural、ML/LLM-as-method。
5. 估计：PPML（Python `pyfixest.fepois`），学者 FE + 五年 career-age 分箱 + field×半年 FE，方法份额 × 半年虚拟变量；按学者聚类的标准误，另报 exposure-robust 标准误；安慰剂日期与 share 置换的 randomisation inference 可后补。
6. 输出：Figure 1（分方法 event study）、W1–W4 窗口均值表、分类校准表、按年计数核对表，连同代码一起提交到上述分支。

## 环境与成本提示
- 需要 Python 包：statsmodels、pyfixest、pyarrow、requests。
- OpenAlex 匿名访问限速明显低于 polite pool；每日约 10 万次请求上限，面板所需的请求量在此之内但要做断点续传与本地缓存。
- 作者要求 agent 用 Opus 5.5 + effort xhigh；拉数据和回归是确定性脚本，不需要 agent；标注用 low/medium 即可。
- 不要把任何 API key 写进仓库。
