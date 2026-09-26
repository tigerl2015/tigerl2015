# 执行摘要：AI/ML 在企业网络安全与应用监控中的真实应用

> 面向：IT Manager / IT Architect / Cybersecurity Manager / Engineering Manager
> 调研日期：2026-09-24 ｜ 证据基础：64 个已验证企业案例、170 条来源（官方文档优先，营销话术已剥离）

## 一句话结论

**AI/ML 在监控领域的真实价值，不是"发现更多问题"，而是"把海量信号压缩为少数可行动的高置信信号，并把根因定位从小时级压缩到分钟级"。** 主流平台的"AI"主体是**统计方法 + 经典机器学习**；深度学习仅在少数场景真实落地；LLM/GenAI 是 2023 年后的新层，职责是**人机交互与调查加速**，不替代检测引擎。

## 三个核心发现

**1. 平台技术路线已明显分化，选型即选技术哲学**
- **Splunk**：分层结构——规则（ES correlation search）→ 统计加权（RBA 风险评分，官方明确不是 ML）→ 无监督 ML（UBA/UEBA 行为基线）→ GenAI（AI Assistant，Splunk 托管 LLM、基座未公开）。可观测侧（ITSI）的 ML 是统计型自适应阈值（标准差/分位数等），诚实但朴素。
- **Dynatrace**：唯一走**确定性因果 AI**（Davis：Smartscape 拓扑上做故障树分析，可复现、可解释），明确宣称"不是传统机器学习"；LLM 仅作 CoPilot。
- **Datadog**：统计 ML（Watchdog，专利级算法文档）+ 自研开源时间序列基础模型 **Toto**（transformer，生产集成未获公开确认）+ Bits AI（LLM 层）。
- **Microsoft/Google/CrowdStrike**：检测以规则/ML 混合为主，GenAI 是最大投入方向（Security Copilot、Gemini in SecOps、Charlotte AI）。
- **Elastic**：零配置经典 ML（聚类/贝叶斯/时间序列分解，100+ 预置任务）+ LLM 连接器模式（可选 OpenAI/Azure/Bedrock/Vertex/自托管）。

**2. "Deep Learning" 被系统性夸大了**
- 公开技术证据显示：绝大多数平台的检测引擎是**统计基线 + 经典 ML**（scikit-learn 类、贝叶斯、聚类、季节分解）。
- 学术界的 DeepLog/LogBERT 等深度学习日志异常检测方法，**没有任何厂商公开部署证据**。
- 深度学习的真实位置：CrowdStrike 云端 ML（架构未公开）、Splunk DSDL（TensorFlow/PyTorch 容器，用户自建模型）、Datadog Toto（开源权重）、各家 LLM 本身。
- **强化学习：所有主流厂商均无生产使用公开证据。**
- 采购与架构评审时，"AI-powered"必须拆解为：规则？统计？经典 ML？DL？LLM？本报告附录给出了每个平台的逐项证据表。

**3. 有据可查的效果集中在四个数字上**
- **告警量/误报**：Kroger 工单 -99%（Dynatrace）；Hexaware 误报 -96%（Elastic）；Johnson Matthey 61% 钓鱼全自动关闭（Splunk）；Louisiana 86% 事件自动解决（XSIAM）。
- **MTTR/MTTD**：Lenovo 30→<5 分钟（Splunk）；BT MTTI -90%（Dynatrace）；Konecta MTTD/MTTR -90%（XSIAM）；Green Bay Packers 42 分钟→40 秒（XSIAM）；Chegg -87%（New Relic）。
- **成本**：BT 目标 £28m 节省（Dynatrace）；Skyscanner 遥测成本 -90%（New Relic）；Cisco IT 可观测成本 -86%（媒体转述）；Oneida Nation -20%（XSIAM）。
- **人力**：St. Luke's 月省约 200 小时（Security Copilot）；TAMUS 月省 100+ 工时（Elastic）。
- **注意**：以上几乎全部为厂商发布口径，无独立第三方审计；横向比较不可直接引用。

## 需要警惕的陷阱

1. **"告警减少 90%+"类数字均为厂商自报**（Splunk RBA 50-90%、Dynatrace 99.9% 降噪、XSIAM SmartGrouping 75%），可作方向参考，不可作验收指标。
2. **GenAI 助手不等于检测能力**：LLM 的职责是摘要、翻译（自然语言→查询语言）、报告与调查辅助；检测精度仍取决于底层的规则+ML 层。且多家厂商（Splunk、Dynatrace、CrowdStrike、Palo Alto）**不披露底层 LLM 模型**，数据治理评估需要单独确认。
3. **重大产品变更正在发生**：Splunk UBA 独立产品 **2027-01-31 EOL**（并入 ES Premier）；Sentinel Azure 门户 **2027-03-31 退役**（并入 Defender 门户）；IBM QRadar SaaS 已停止销售且 **2026 年分批 EOL**（迁移方向是 Cortex XSIAM）；AppDynamics 已更名 **Splunk AppDynamics**。选型时必须按 2026 年现状评估，不能依赖旧认知。

## 建议的落地路径（基于案例证据）

| 阶段 | 做什么 | 案例依据 |
|---|---|---|
| 1. 集中化 | 先统一日志/指标/trace 到一个平台（这是所有案例的共同前提） | Domino's、John Lewis、BT（16 工具→1） |
| 2. 规则+统计 | 先上自适应阈值/基线告警与风险评分，压低告警噪音 | Splunk ITSI 自适应阈值、RBA；Datadog Watchdog |
| 3. 无监督 ML | 对用户/实体行为做 UEBA 类检测（内部威胁、失陷账户） | Splunk UBA/ES Premier UEBA；Elastic ML jobs |
| 4. GenAI 层 | 最后叠加 LLM 助手加速调查与报告，而非替代前两层 | Security Copilot（St. Luke's）、Splunk AI Assistant、Bits AI |
| 5. 自动化 | 高置信信号才进入自动 playbook；低置信保持人工确认（"bounded autonomy"） | Johnson Matthey、Louisiana、Charlotte AI Detection Triage |

完整论证、平台对比矩阵、64 个案例数据库与全部来源见：
- `report.md`（主报告，16 章）
- `case-study-matrix.csv`（64 案例矩阵）
- `sources.md`（170 条分级来源）
