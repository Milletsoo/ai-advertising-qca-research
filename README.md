# 数字广告平台 AI 技术能力组态与市场绩效研究

## 基于 fsQCA 的组态路径分析

> 本文档整理自 2026 年 9 月 29 日的系统调研与选题论证过程。
>
> 调研基础：学界文献调研（Google Scholar 多轮检索）、行业前沿调研（2024-2026 市场报告与技术文档）、QCA 方法论调研三维度综合分析。

---

## 一、研究背景

### 1.1 行业背景

AI 已从广告行业的"附加功能"变为"运营核心"：

- 87% 的营销人员已使用生成式 AI
- 全球数字广告 2025 年 $5,679 亿，2026 年预计 $6,623 亿（CAGR 14.3%）
- 中国数字广告 2025 年 7,257 亿元，AI 营销市场 636 亿元
- Google AI Max、Meta Advantage+、Amazon Ads AI 已实现竞价、定向、创意三大环节的全自动 AI 控制
- 中国平台布局：腾讯广告引擎升级至超长行为序列+毫秒级时效；阿里妈妈推出 UD 小智操盘助手；阿里妈妈×腾讯广告实现 3.0 联邦大模型跨平台打通

行业痛点催生研究需求：

1. 广告欺诈与 AI 反欺诈军备竞赛
2. 品牌安全与 AI 内容审核
3. 归因复杂性（Gartner 警告 AI 使广告更不透明、更难证明 ROI）
4. 透明度与信任（Google 2026 年 7 月实施 AI 广告强制披露标签）
5. 创意同质化问题

### 1.2 学界研究现状

AI+广告领域 2023-2026 年形成八大研究主题：

1. AI 广告基础理论与框架构建
2. AIGC 广告内容生成与消费者反应
3. AI 广告透明度披露与消费者信任
4. AI 广告"暗面"与伦理风险
5. LLM 在广告中的应用
6. 程序化广告中的 AI 应用
7. AI 虚拟影响者/数字人在广告中的应用
8. AI 广告效果与消费者行为机制

**关键发现**：使用 QCA 方法研究 AI+广告的论文仅约 8 篇，且全部发表于 2025-2026 年，属于极早期阶段。中文期刊中几乎空白。

### 1.3 已有 QCA+AI广告论文

| 序号 | 论文标题 | 作者 | 期刊 | 年份 | 方法 |
|------|---------|------|------|------|------|
| 1 | Does AI Advertising Persuade or Scaffold? | Bae | Behavioral Sciences | 2026 | SEM-fsQCA |
| 2 | Ethical requirements for generative AI in brand content creation | Du Plessis | Frontiers in Communication | 2025 | QCA |
| 3 | How do the attributes of AI-generated digital humans relate to online customer experience? | Zu et al. | APJML | 2026 | SEM + fsQCA |
| 4 | Driving Mechanisms of User Engagement with AIGC | Hou et al. | IEEE Access | 2025 | LDA + fsQCA |
| 5 | Exploring social media native advertising avoidance of Chinese users | Wang | APJML | 2026 | SEM + fsQCA |
| 6 | Impact of digital assistant attributes on millennials' purchasing intentions | Sharma et al. | ISF | 2024 | PLS-SEM + ANN + fsQCA |
| 7 | Beyond the Screen: AI Virtual Streamer on Consumer Purchase | Jen et al. | Preprints | 2026 | PLS-SEM + fsQCA |
| 8 | Exploring effectiveness of relationship marketing on AI adopting intention | Cheng et al. | Sage Open | 2023 | PLS-SEM + fsQCA |

### 1.4 研究缺口

1. AI 广告投放效果的组态路径研究（高优先级）：几乎完全空白
2. 企业 AI 广告采纳的驱动机制（高优先级）
3. AI 广告伦理治理的组态分析（中高优先级）
4. 跨文化/跨市场 AI 广告效果的组态比较（中优先级）
5. AIGC 广告创意质量与消费者反应的组态路径（中优先级）
6. LLM 广告投放系统的治理组态（中优先级）
7. 中文语境下的 AI 广告 QCA 研究（高优先级）

---

## 二、QCA 方法论基础

### 2.1 核心原理

QCA（Qualitative Comparative Analysis）由 Charles Ragin 于 1987 年提出，根植于集合论和布尔代数，核心思维方式是组态思维——结果不是由单个变量的线性叠加决定的，而是由多个条件以特定组合方式共同产生的。

| 概念 | 含义 | 与传统方法的差异 |
|------|------|------------------|
| 因果复杂性 | 同一结果可由多组不同条件组合产生 | 回归假设单一最佳模型 |
| 等价性 | 多条不同路径都能导向同一结果 | 回归只有一套系数 |
| 非对称性 | 导致结果出现的条件组合 ≠ 导致结果不出现的条件组合的简单反面 | 回归假设对称关系 |

### 2.2 主要变体

| 变体 | 校准方式 | 适用场景 | 使用频率 |
|------|----------|----------|----------|
| csQCA | 二值（0/1） | 条件可清晰二分 | 较少使用 |
| fsQCA | 连续值（0~1） | 条件为连续程度变量 | 目前最主流 |
| mvQCA | 多值离散 | 条件有多个离散类别 | 较少使用 |

### 2.3 QCA vs 传统回归分析

| 维度 | 回归分析 | QCA |
|------|----------|-----|
| 因果关系 | 线性/加性，净效应 | 组态性，组合效应 |
| 对称性 | 对称 | 非对称 |
| 样本量 | 大样本（N>200） | 中小样本（10~100+） |
| 案例导向 | 变量导向 | 案例导向，每个案例可追踪 |
| 等价性 | 不支持 | 支持 |

### 2.4 标准分析流程

1. 理论与案例选择：基于理论框架确定条件和结果，选择案例（10~100+）
2. 数据校准：将原始数据转换为模糊集隶属分数（0~1），设定三个锚点
3. 必要条件分析：检验单个条件是否为必要条件（一致性 ≥0.9）
4. 构建真值表：列出所有条件组合（2^k 行）
5. 布尔最小化：通过一致性阈值（≥0.8）和频率阈值筛选
6. 充分条件组态识别：分析中间解中的组态路径
7. 稳健性检验：调整参数验证稳定性
8. 案例层面的解释和讨论

### 2.5 推荐方法组合

| 方法组合 | 适用场景 | 优势 |
|----------|----------|------|
| fsQCA + NCA | 所有推荐选题 | NCA 识别必要条件（瓶颈），fsQCA 识别充分条件组态（配方）|
| PLS-SEM + fsQCA | 需要三角验证时 | SEM 检验线性关系，fsQCA 发现非线性组态 |
| 两步 QCA | 顺序因果链分析 | 区分远端条件和近端条件 |
| fsQCA + 机器学习 | 大数据预处理 | 用聚类/主题模型识别潜在条件 |

### 2.6 关键参考文献

**方法奠基**：
- Ragin (2008). *Redesigning Social Inquiry: Fuzzy Sets and Beyond.*
- Greckhamer et al. (2018). *Strategic Organization*, 16(4). 被引 1835 次.
- Dul (2016). *Journal of Business Research*. 被引 698 次.
- Vis & Dul (2018). *Sociological Methods & Research*. 被引 404 次.
- Pappas & Woodside (2021). *International Journal of Information Management*. 被引 2956 次.

**营销/广告应用**：
- Ordanini & Parasuraman (2014). *Journal of Service Research*. 被引 942 次.
- Pappas (2018). *European Journal of Marketing*. 被引 324 次.
- Mattke et al. (2021). *European Journal of Marketing*.

---

## 三、选题论证过程

### 3.1 选题约束条件

- QCA 作为核心研究方法（不是补充）
- 紧扣"计算广告""数字广告"专业背景
- 中切口（不微观不宏观）
- 数据公开可获取，不需要企业内部访谈/问卷
- 硕士论文可控可落地
- 导师容易认可研究价值

### 3.2 选题演进路径

**初始推荐 6 个方向** → 导师反馈三个问题（QCA 存疑/选题太大/变量不可操作）→ 诊断后收缩为 3 个替代方案 → 用户反馈需要中切口+计算广告背景+数据公开 → 重新打开思维构建"条件×单元×结果"三维矩阵 → 4 个精炼候选 → 最终确定

### 3.3 被淘汰的方案及原因

| 方案 | 淘汰原因 |
|------|----------|
| 跨国 AI 广告效果比较 | 太大，数据不可获取，硕士不可控 |
| 企业 AI 广告采纳（需问卷） | 需要企业访谈/问卷，资源不足 |
| AIGC 消费者接受度（实验法） | 切口偏小，局限于消费者层面 |
| AI 广告创意同质化 | 创意差异化程度难以客观编码 |
| AI 广告伦理治理 | 伦理变量难以操作化，容易流于规范研究 |

### 3.4 四个最终候选对比

| 维度 | 候选①平台能力组态 | 候选②产品功能组态 | 候选③技术条件组态 | 候选④隐私策略组态 |
|------|:-:|:-:|:-:|:-:|
| 计算广告相关度 | ★★★★★ | ★★★★★ | ★★★★ | ★★★★★ |
| QCA 作为核心方法 | ✅ | ✅ | ✅ | ✅ |
| 数据公开可获取 | ★★★★ | ★★★ | ★★★★ | ★★★ |
| 中切口 | ✅ | ✅ | ✅ | ✅ |
| 不需企业访谈 | ✅ | ✅ | ✅ | ✅ |
| 硕士可行 | ★★★★★ | ★★★★ | ★★★★★ | ★★★★ |
| 导师易认可 | ★★★★★ | ★★★★ | ★★★★ | ★★★★ |
| 案例数充足 | 20-25 | 25-40 | 30-50 | 15-20 |
| 前沿性 | ★★★ | ★★★★ | ★★★ | ★★★★★ |
| 理论深度 | ★★★★ | ★★★★ | ★★★ | ★★★★ |

---

## 四、最终选题设计

### 4.1 选题名称

**数字广告平台 AI 技术能力组态与市场绩效研究——基于 fsQCA 的组态路径分析**

### 4.2 研究问题

哪些 AI 技术能力的组合驱动数字广告平台获得高市场绩效？

### 4.3 理论框架

基于 TOE（Technology-Organization-Environment）框架扩展，结合计算广告技术体系，构建"平台 AI 能力→市场绩效"的组态分析模型。

QCA 的组态思维特别适合解答此问题——因为平台市场绩效不是由单一技术能力决定的，而是多种技术能力以特定组合方式共同产生的。不同平台可能通过不同的技术能力组合（等价性路径）都能获得高绩效。

### 4.4 分析单元

数字广告平台，包括：

**中国市场**（10-12 个）：
- 巨量引擎（字节跳动）
- 腾讯广告
- 阿里妈妈
- 百度营销
- 快手磁力引擎
- 小红书
- B站
- 微博广告
- 知乎
- 拼多多广告
- 美团广告
- 京东广告

**国际市场**（8-10 个）：
- Google Ads
- Meta (Facebook/Instagram)
- Amazon Ads
- TikTok Ads (全球)
- Microsoft Ads
- Pinterest Ads
- Snapchat Ads
- Reddit Ads
- LinkedIn Ads
- X (Twitter) Ads

**案例总数**：20-22 个平台

### 4.5 条件变量设计

每个条件变量都有明确的操作化方式、数据来源和编码规则：

| 条件变量 | 操作化方式 | 数据来源 | 校准方式 |
|----------|-----------|----------|----------|
| **AI 定向能力** | 计数：平台具备的 AI 定向技术数量（上下文定向/行为定向/Lookalike/AI预测定向，0-4） | 平台产品文档、官方技术博客 | 直接校准为模糊集（0→0, 2→0.5, 4→1） |
| **AI 创意能力** | 计数：平台具备的 AI 创意功能数量（文案生成/图片生成/视频生成/DCO动态创意优化，0-4） | 平台产品文档 | 直接校准为模糊集 |
| **投放自动化程度** | 4 级编码：①手动投放(0) ②半自动(0.33) ③程序化RTB(0.67) ④全自动AI投放(1) | 平台产品文档 | 直接校准为模糊集 |
| **数据生态规模** | 平台月活用户数（MAU），对数转换后按全样本分位数校准 | 财报、行业报告（eMarketer/QuestMobile/Statista） | 百分位校准（90th→1, 50th→0.5, 10th→0） |
| **隐私计算策略** | 计数：平台部署的隐私技术数量（联邦学习/安全多方计算/Clean Room/差分隐私/上下文广告转向，0-5） | 技术文档、行业报告（IAB/IDSA） | 直接校准为模糊集 |
| **广告形式丰富度** | 计数：平台支持的广告形式数量（信息流/搜索/视频/原生/程序化/直播/短剧/电商等，0-8） | 平台官网产品页 | 直接校准为模糊集 |

6 个条件变量 → 2^6 = 64 行真值表，在 fsQCA 的可操作范围内。

### 4.6 结果变量

**平台广告收入年增速**（近一年同比增速）

| 平台 | 广告收入 | 数据来源 |
|------|----------|----------|
| Google Ads | 约 $3,500亿+ | Alphabet 财报 |
| Meta | 约 $1,600亿+ | Meta 财报 |
| Amazon Ads | 约 $500亿+ | Amazon 财报 |
| 巨量引擎 | 约 4,000亿元+ | 字节跳动估值报告 |
| 腾讯广告 | 约 1,200亿元+ | 腾讯财报 |
| 阿里妈妈 | 约 3,000亿元+ | 阿里财报 |
| ... | ... | ... |

校准方案：按全样本分位数校准（90th percentile → 完全隶属=1, 50th → 交叉点=0.5, 10th → 完全不隶属=0）

备选结果变量（如果增速数据不全）：
- 广告收入绝对规模（对数）
- 市场份额变化
- 广告主数量增速

### 4.7 数据来源汇总

| 数据类型 | 来源 | 可获取性 |
|----------|------|----------|
| 平台广告收入 | 上市公司财报（Alphabet/Meta/Amazon/腾讯/阿里/百度/快手/B站/微博/知乎/拼多多/美团） | ✅ 公开 |
| 非上市公司收入 | 估值报告（字节跳动→彭博/路透估值报道）、行业估算（QuestMobile/艾瑞） | ✅ 公开 |
| 技术能力信息 | 平台官方产品文档、技术博客、开发者文档 | ✅ 公开 |
| MAU 数据 | 财报、Statista、QuestMobile | ✅ 公开 |
| 隐私技术部署 | 平台技术博客、IAB报告、行业新闻 | ✅ 公开 |
| 广告形式 | 平台官网广告产品页 | ✅ 公开 |
| 行业报告 | eMarketer、IAB、QuestMobile、艾瑞、Magna Global | ✅ 公开 |

### 4.8 研究设计流程

```
第一步：案例收集（20-22个数字广告平台）
  ↓
第二步：条件变量编码（基于产品文档/财报/行业报告）
  ↓
第三步：结果变量测量（广告收入年增速）
  ↓
第四步：数据校准（设定锚点，转换为模糊集隶属分数）
  ↓
第五步：必要条件分析（NCA + QCA必要性检验，一致性≥0.9）
  → 识别"瓶颈能力"：什么技术能力必须具备才能有高绩效
  ↓
第六步：充分条件组态分析（fsQCA真值表 + 布尔最小化，一致性≥0.8）
  → 识别"成功配方"：哪些技术能力组合足以产生高绩效
  ↓
第七步：非对称性分析
  → 分别分析"高绩效"和"低绩效"的组态路径
  → 揭示二者不是简单反面
  ↓
第八步：稳健性检验
  → 调整校准锚点、一致性阈值、频率阈值
  → 验证结果稳定性
  ↓
第九步：案例层面的解释和讨论
  → 对每个组态路径中的代表性案例进行追踪分析
  → 结合行业知识解释为什么这些能力组合有效
```

### 4.9 预期研究发现（示例性）

- **必要条件**：可能发现"数据生态规模"是高绩效的必要条件（没有足够大的用户基数，再好的AI也无法产生高广告收入）
- **等价路径**：可能发现不同类型的平台通过不同路径获得高绩效：
  - 路径1：大规模数据 + 全自动AI投放 + 高创意自动化（如Google/Meta）
  - 路径2：中等数据 + 深度隐私计算 + 跨平台整合（如腾讯/阿里联邦生态）
  - 路径3：垂直数据 + 高AI定向精度 + 电商闭环（如Amazon/拼多多）
- **非对称性**：导致低绩效的路径可能完全不同（如：低数据规模 + 低自动化 + 低创意能力，但也可能高数据规模 + 低技术整合导致低效率）

### 4.10 研究价值

**理论贡献**：
- 首次用 QCA 组态视角分析数字广告平台技术能力与市场绩效的关系
- 将 TOE 框架扩展至广告平台层面，填补计算广告领域的组态研究空白
- 揭示平台技术能力的"组态效应"而非"单一效应"

**实践价值**：
- 为广告平台提供技术能力建设优先级的决策依据
- 为广告主选择平台提供技术维度的参考框架
- 为行业分析师评估平台竞争力提供新视角

**发表前景**：
- 中文期刊：营销科学学报、管理科学、南开管理评论
- 英文期刊：Journal of Interactive Marketing、International Journal of Advertising、Information Systems Frontiers

---

## 五、论文结构建议

| 章节 | 内容 |
|------|------|
| 第一章 绪论 | 研究背景（AI广告爆发+平台竞争+效果不确定性）、研究问题、研究意义、研究方法概述 |
| 第二章 文献综述 | 2.1 计算广告与AI广告技术发展<br>2.2 数字广告平台研究综述<br>2.3 QCA方法论综述<br>2.4 研究缺口识别 |
| 第三章 理论框架 | 3.1 TOE框架扩展<br>3.2 计算广告技术能力维度<br>3.3 组态视角的理论依据<br>3.4 条件变量选择依据 |
| 第四章 研究设计 | 4.1 案例选择与依据<br>4.2 变量编码手册<br>4.3 数据校准方案<br>4.4 分析方法与流程 |
| 第五章 数据分析 | 5.1 描述性统计<br>5.2 必要条件分析（NCA）<br>5.3 充分条件组态分析（fsQCA）<br>5.4 非对称性分析<br>5.5 稳健性检验 |
| 第六章 结果讨论 | 6.1 组态路径解读<br>6.2 案例层面解释<br>6.3 与已有研究的对话<br>6.4 理论贡献<br>6.5 实践启示 |
| 第七章 结论与展望 | 7.1 研究结论<br>7.2 研究局限性<br>7.3 未来研究方向 |

---

## 六、关键参考文献清单

### 方法论

1. Ragin, C. C. (2008). *Redesigning Social Inquiry: Fuzzy Sets and Beyond.* University of Chicago Press.
2. Greckhamer, T., Furnari, S., Fiss, P. C., Aguilera, R. V., & Fleming, P. (2018). Studying configurations with QCA: Best practices in strategy and organization research. *Strategic Organization*, 16(4), 482-495. (被引 1835 次)
3. Dul, J. (2016). Identifying single necessary conditions with NCA and fsQCA. *Journal of Business Research*, 69(4), 1516-1523. (被引 698 次)
4. Vis, B., & Dul, J. (2018). Analyzing Relationships of Necessity Not Just in Kind But Also in Degree: Complementing fsQCA With NCA. *Sociological Methods & Research*, 47(4), 872-899. (被引 404 次)
5. Pappas, I. O., & Woodside, A. G. (2021). Fuzzy-set Qualitative Comparative Analysis (fsQCA): Guidelines for research practice in Information Systems and marketing. *International Journal of Information Management*, 58, 102310. (被引 2956 次)

### AI 广告研究

6. Li, H. (2023). Artificial Intelligence (AI) Advertising. *Marketing Science*.
7. Huh, C. A., Nelson, M. R., & Russell, C. A. (2023). ChatGPT, AI advertising, and advertising research and education. *Journal of Advertising*. (被引 278 次)
8. Strycharz, B., Maslowska, E., & Kim, J. (2024). Computational advertising: Where are we and where are we going? *International Journal of Advertising*.
9. Reisenbichler, M., et al. (2026). Applying large language models to sponsored search advertising. *Marketing Science*. (被引 43 次)
10. Nguyen, T., Dang, N., & Duc, D. (2025). The dark sides of AI advertising. *Social Science Computer Review*. (被引 67 次)
11. Diwanji, P., Lee, S., & Cortese, J. (2024). Deconstructing the role of AI in programmatic advertising. *Journal of Strategic Marketing*. (被引 52 次)
12. Bae, J. (2026). Does AI Advertising Persuade or Scaffold? *Behavioral Sciences*. (SEM-fsQCA 应用于 AI 广告)

### QCA 在营销/数字化转型中的应用

13. Ordanini, A., & Parasuraman, A. (2014). When the recipe is more important than the ingredients: A QCA of service innovation configurations. *Journal of Service Research*. (被引 942 次)
14. Pappas, I. O. (2018). User experience in personalized online shopping: a fuzzy-set analysis. *European Journal of Marketing*. (被引 324 次)
15. Mattke, J., et al. (2021). In-app advertising: a two-step QCA to explain clicking behavior. *European Journal of Marketing*.
16. Fainshmidt, S., et al. (2020). The contributions of QCA to international business research. *JIBS*. (被引 589 次)
17. Koska, A. (2026). Country-Level Configurations Associated with Enterprise AI Diffusion in Europe: An fsQCA. *Technology in Society*.

---

*本文档基于 2026 年 9 月 29 日的三路并行调研（学界文献、行业前沿、QCA 方法论）综合分析及多轮选题论证产出。所引用的论文信息来自 Google Scholar 实际检索结果。*
