# 来源总表（sources.md）

> 调研日期：2026-09-24。证据分级：① 厂商官方文档/官方案例 ② 厂商工程博客/新闻稿/专利 ③ 第三方（Gartner/Forrester/IDC、媒体、分析师）④ 学术论文。
> 所有来源均经研究 agent 直接抓取核验或经多源交叉确认；核验失败/受限的条目已注明。
> 标注 `⚠` 的为厂商自报/厂商委托数据，引用时需注明口径。

## 1. Splunk 官方文档 / 博客 / 新闻稿 / 案例

1. Splunk ES RBA 工作原理（官方文档，2025-07-14 更新，已直接核验，页面无 ML 表述）— https://help.splunk.com/en/splunk-enterprise-security-7/risk-based-alerting/7.2/introduction/how-risk-based-alerting-works-in-splunk-enterprise-security
2. Splunk RBA 特性简介（50–90% 告警量下降声明 ⚠）— https://www.splunk.com/en_us/resources/risk-based-alerting-feature-brief.html
3. Splunk UBA 模型概述（无监督 ML、流式/批处理、peer groups，2025-09-02，已直接核验）— https://help.splunk.com/en/security-offerings/splunk-user-behavior-analytics/use-splunk-user-behavior-analytics/5.4.1/splunk-uba-models/splunk-uba-models-overview
4. Splunk UBA EOL 公告（独立产品 EOL 2027-01-31，2026-04-22，已直接核验）— https://help.splunk.com/en/security-offerings/splunk-user-behavior-analytics/plan-and-scale/5.4.5/plan-and-scale-your-splunk-uba-deployment/about-splunk-user-behavior-analytics
5. Splunk UBA 误报抑制模型博客（自监督深度学习、向量化）— https://www.splunk.com/en_us/blog/security/reduce-false-alerts-automatically.html
6. Splunk MLTK/AITK 算法清单（scikit-learn 封装、statsmodels/ARIMA，2025-10-08）— https://help.splunk.com/en/splunk-cloud-platform/alert-and-respond/apply-machine-learning/use-ai-toolkit/5.6.1/algorithms-and-scoring-metrics-in-mltk/algorithms-in-the-splunk-machine-learning-toolkit
7. Splunk MLTK 速查表（80+ scikit-learn 内置、PSC 扩展 300+）— https://www.splunk.com/en_us/pdfs/training/splunk-machine-learning-toolkit-app-cheat-sheet.pdf
8. Splunk DSDL（原 DLTK）Splunkbase 页面（v5.2.4，2026-05-22，TensorFlow/PyTorch，已直接核验）— https://splunkbase.splunk.com/app/4607
9. Splunk AI Assistant Responsible AI 页（Splunk 托管 LLM，基座未公开，已直接核验）— https://www.splunk.com/en_us/about-splunk/splunk-data-security-and-privacy/responsible-ai-for-ai-assistant.html
10. Splunk AI Assistant for SPL 1.4 博客（Agentic AI + Azure OpenAI 可选，2025-11-21，已直接核验）— https://www.splunk.com/en_us/blog/artificial-intelligence/splunk-ai-assistant-for-spl-1-4.html
11. Cisco 安全微调模型博客（Foundation-Sec-8B-1.1-Instruct，替代 Llama-3.1-70B）— https://blogs.cisco.com/security/accelerate-security-operations-with-ciscos-new-security-tuned-model
12. Splunk .conf24 新闻稿（2024-06-19：AI Assistant、ITSI AI 功能，已直接核验）— https://www.splunk.com/zh_cn/newsroom/press-releases/2024/conf24-splunk-introduces-advanced-ai-enhancements-for-observability-security-and-it-service-intelligence.html
13. SDxCentral：.conf25 发布 ES Essentials/Premier、TSFM 开源计划（2025-09）— https://www.sdxcentral.com/news/cisco-officially-ordains-splunk-with-ai-splurge/
14. SiliconANGLE：ES 8.2 与 agentic AI 清单（2025-09-09）— https://siliconangle.com/2025/09/09/cisco-endows-splunk-agentic-ai-security-observability/
15. Splunk ITSI 自适应阈值文档（标准差/分位数/区间/百分比，7 天训练窗口，2026-06-30，已直接核验）— https://help.splunk.com/en/splunk-it-service-intelligence/splunk-it-service-intelligence/visualize-and-assess-service-health/5.0/advanced-thresholding/create-adaptive-kpi-thresholds-in-itsi
16. Splunk ITSI 旧异常检测弃用迁移指引（4.20 起）— https://help.splunk.com/en/splunk-it-service-intelligence/splunk-it-service-intelligence/visualize-and-assess-service-health/5.0/advanced-thresholding/migrate-anomaly-detection-to-adaptive-thresholding-in-itsi
17. Splunk Observability AI 排障代理文档（2026-02-11）— https://help.splunk.com/en/splunk-observability-cloud/create-alerts-detectors-and-service-level-objectives/troubleshoot-with-ai-automated-alerts/ai-troubleshooting-agent-and-remediation-plan-in-splunk-observability-cloud
18. Splunk Tag Spotlight 文档（2026-05-12）— https://help.splunk.com/en/splunk-observability-cloud/monitor-application-performance/analyze-services-with-span-tags-and-metricsets/analyze-service-performance-with-tag-spotlight
19. Splunk Attack Analyzer 专利（autoencoder + 品牌分类 + allow/deny 名单，2025 公开）— https://www.freepatentsonline.com/y2025/0337777.html
20. Splunk TruSTAR 收购公告（2021-05-18）— https://www.splunk.com/en_us/newsroom/press-releases/2021/splunk-announces-intent-to-acquire-trustar.html
21. WSJ：Cisco 完成 280 亿美元收购 Splunk（2024-03-18）— https://www.wsj.com/articles/cisco-closes-28-billion-acquisition-of-splunk-betting-big-on-ai-836b6560
22. Cisco IT 用 Splunk 减重大事故博客（2026-05-18，已直接核验：事故 -25%、零重大中断）— https://www.splunk.com/en_us/blog/platform/cisco-uses-splunk-to-mitigate-major-incidents-network-outages.html
23. Network World：Cisco IT 可观测成本 -86%（2026，第三方转述 ⚠）— https://www.networkworld.com/article/4181727/how-cisco-it-cut-observability-costs-by-86-and-eliminated-major-network-outages.html
24. TransUnion 案例（ITSI+ML，已直接核验）— https://www.splunk.com/en_us/customers/success-stories/transunion.html
25. McLaren Racing 案例 — https://www.splunk.com/en_us/customers/success-stories/mclaren-racing.html
26. Johnson Matthey 案例（调查 -83%、61% 自动关闭 ⚠）— https://www.splunk.com/en_us/pdfs/customer-success-stories/johnson-matthey.pdf
27. Splunk 自身 SOC 案例（处置快 90% ⚠）— https://www.splunk.com/en_us/pdfs/customer-success-stories/splunk-soc.pdf
28. Lenovo 案例（MTTR 30→<5 分钟 ⚠，2021）— https://www.splunk.com/en_us/pdfs/customer-success-stories/lenovo-case-study.pdf
29. Honda Manufacturing of Alabama 案例（MTTR +70% ⚠）— https://www.splunk.com/en_us/pdfs/customer-success-stories/honda-case-study.pdf
30. Heartland Jiffy Lube 新闻稿（ES+UBA，MTTR +60%，2017-11）— https://www.splunk.com/en_us/newsroom/press-releases/2017/heartland-jiffy-lube-speeds-up-detection-of-unknown-threats-with-splunk-user-behavior-analytics.html
31. Carnival 新闻稿（ES+ITSI，MTTR 最高 -98% ⚠，2023-07-18，已直接核验）— https://www.splunk.com/en_us/newsroom/press-releases/2023/carnival-leverages-splunk-to-deliver-a-seamless-guest-experience-through-enhanced-digital-resilience.html
32. Fannie Mae 案例（已直接核验）— https://www.splunk.com/en_us/customers/success-stories/fannie-mae.html
33. 匿名医疗软件公司案例（ARI）— https://www.splunk.com/en_us/customers/success-stories/healthcare-software-company.html
34. John Lewis 案例（2013 数据）— https://www.splunk.com/en_us/pdfs/customer-success-stories/splunk-at-john-lewis.pdf
35. Domino's 案例（2013-2014）— https://www.splunk.com/en_us/customers/success-stories/revealing-the-secret-sauce.html
36. Zillow 案例（约 2016）— https://www.splunk.com/en_us/pdfs/customer-success-stories/splunk-at-zillow.pdf
37. City of Los Angeles 案例 — https://www.splunk.com/en_us/pdfs/customer-success-stories/splunk-at-city-of-los-angeles.pdf
38. StateTech Magazine：LA 用 Splunk 做漏洞优先级（2024-08）— https://statetechmagazine.com/article/2024/08/los-angeles-identifies-and-targets-critical-vulnerabilities-splunk

## 2. 安全平台（Microsoft / Google / CrowdStrike / Palo Alto / IBM / Elastic / Sumo / 其他）

39. Microsoft Sentinel UEBA 文档（TF-IDF peer groups、双评分，2025-12-15，已直接核验）— https://learn.microsoft.com/en-us/azure/sentinel/identify-threats-with-entity-behavior-analytics
40. Microsoft Sentinel Fusion 文档（ML 关联引擎、30 天训练、Defender 门户替代、2027-03-31 Azure 门户退役，2024-11-26）— https://learn.microsoft.com/en-us/azure/sentinel/fusion
41. Microsoft Sentinel 可定制 ML 异常规则文档 — https://learn.microsoft.com/en-us/azure/sentinel/soc-ml-anomalies
42. Microsoft Security Copilot 发布博客（GPT-4 + 安全专用模型，2023-03-28，已直接核验）— https://blogs.microsoft.com/blog/2023/03/28/introducing-microsoft-security-copilot-empowering-defenders-at-the-speed-of-ai/
43. Microsoft Security Copilot What's New（GPT-4.1 GA 2025-07；Sentinel 集成 GA 2025-09；Security Analyst Agent 2026-04）— https://learn.microsoft.com/en-us/copilot/security/whats-new-copilot-security
44. Microsoft 统一 SecOps 平台 GA 博客（50% 更快关联/99% 准确率 ⚠，2024-07-11）— https://www.microsoft.com/en-us/security/blog/2024/07/11/simplified-zero-trust-security-with-the-microsoft-entra-suite-and-unified-security-operations-platform-now-generally-available/
45. ASOS Sentinel 案例（解决时间约减半，2021-11 更新）— https://learn.microsoft.com/en-us/shows/azure-videos/asos-centralizes-security-operations-tackles-cyberthreats-with-azure-sentinel
46. QNET Sentinel+Copilot 案例（效率 +60%，2024-10-07，已直接核验）— https://news.microsoft.com/zh-hk/2024/10/07/qnet-採用-microsoft-網絡安全解決方案-提升事件應對效率-60/
47. St. Luke's 案例（Security Copilot，月省 200 小时，2025-09-25，已直接核验）— https://www.microsoft.com/en/customers/story/25330-st-lukes-university-health-network-microsoft-security-copilot
48. Google SecOps 架构文档（检测引擎漏斗）— https://docs.cloud.google.com/chronicle/docs/secops/secops-architecture
49. Google SecOps curated detections 文档（Precise/Broad、MITRE 映射）— https://docs.cloud.google.com/chronicle/docs/detection/curated-detections
50. Google Cloud RSA 博客（ML 优先化端点告警、Investigation Assistant GA、约 7 倍提效 ⚠，2024-05-07，已直接核验）— https://cloud.google.com/blog/products/identity-security/introducing-google-security-operations-intel-driven-ai-powered-secops-at-rsa
51. Duet AI in SecOps GA 博客（security-specialized LLM，2023-12-13）— https://cloud.google.com/blog/products/ai-machine-learning/duet-ai-for-developers-and-in-security-operations-now-ga
52. Google SecOps Alert Triage and Investigation Agent 公告（Public Preview，Vertex AI Gemini，2025-11-12，已直接核验）— https://security.googlecloudcommunity.com/news-announcements-9/be-one-step-ahead-with-the-google-secops-alert-triage-and-investigation-agent-now-in-public-preview-6244
53. VirusTotal Code Insight 博客（基于 Sec-PaLM，2023-04-24，已直接核验）— https://blog.virustotal.com/2023/04/introducing-virustotal-code-insight.html
54. Jack Henry 与 Google Cloud 扩大合作新闻稿（2026-06-25，已直接核验）— https://www.googlecloudpresscorner.com/2026-06-25-Jack-Henry-and-Google-Cloud-Expand-Collaboration-to-Deliver-AI-Driven-Security-for-Banks-and-Credit-Unions
55. 三菱自动车 Google SecOps 案例 — https://cloud.google.com/customers/intl/ja-jp/mmc
56. Charles Schwab Google SecOps 博客引语（2023-09-19，已直接核验）— https://cloud.google.com/blog/products/identity-security/introducing-the-unified-chronicle-security-operations-platform
57. CrowdStrike 云 ML 工程博客（特征向量、50 万向量/秒、8600 万哈希/天，2022-07-01，已直接核验）— https://www.crowdstrike.com/en-us/blog/how-crowdstrike-machine-learning-model-maximizes-detection-efficacy-using-the-cloud/
58. CrowdStrike AI-powered IOAs 博客（深度学习提取 PowerShell 代码段，2022-08-10）— https://www.crowdstrike.com/en-us/blog/introducing-ai-powered-indicators-of-attack-ioas/
59. CrowdStrike Charlotte AI Detection Triage 新闻稿（98% 准确率 ⚠、周省 40 小时，2025-02-13）— https://www.crowdstrike.com/en-us/press-releases/crowdstrike-delivers-next-breakthrough-in-ai-powered-agentic-cybersecurity-with-charlotte-ai-detection-triage/
60. CrowdStrike–AWS 合作（Charlotte AI 基于 Amazon Bedrock，2023-05-31）— https://ir.crowdstrike.com/node/11631/pdf
61. Charlotte AI AgentWorks 报道（Anthropic/NVIDIA/OpenAI 伙伴，2025-09）— https://www.pipelinepub.com/news/crowdstrike-launches-charlotte-ai-agentworks
62. City of Las Vegas 案例 — https://www.crowdstrike.com/en-us/resources/customer-stories/city-of-las-vegas-video/
63. Mondelez 案例（Forbes，2025-10-14）— https://www.forbes.com/sites/tonybradley/2025/10/14/inside-mondelezs-cloud-sec-overhaul-with-aws-and-crowdstrike/
64. Orica 案例（分诊 4h→10 分钟、A$1.5M 预测）— https://www.crowdstrike.com/en-us/resources/customer-stories/orica/
65. Montage Health 案例（53 秒修复）— https://www.crowdstrike.com/en-au/resources/customer-stories/montage-health-remediation-in-seconds-not-weeks/
66. Berkeley Group 案例（30 秒遏制）— https://www.crowdstrike.com/en-us/resources/customer-stories/berkeley-group/
67. Palo Alto XSIAM 检测规则文档（IOC/BIOC/ABIOC）— https://cortex-docs.paloaltonetworks.com/cortex-xsiam/detect-investigate-and-respond-to-threats/threat-management/detection-rules/what-are-detection-rules.md
68. Palo Alto Precision AI 技术简报（ML + deep learning + GenAI 定义）— https://www.paloaltonetworks.com/apps/pan/public/downloadResource?pagePath=/content/pan/fr_FR/resources/techbriefs/one-platform-any-threat-the-cortex-portfolio
69. Palo Alto "Fight AI with AI" 页面（SmartGrouping 75% 降噪 ⚠、AgentiX 98% MTTR ⚠，2026 更新）— https://www.paloaltonetworks.com/cortex/fight-ai-with-ai
70. Green Bay Packers 案例（MTTR 42 分钟→40 秒，2025-07，已直接核验）— https://www.paloaltonetworks.com/customers/securing-the-green-bay-packers-through-an-ai-driven-platform-approach
71. CBTS 新闻稿（2025-04-28）— https://investors.paloaltonetworks.com/node/19226/pdf
72. Oneida Nation 案例（成本 -20%、MTTR 43 秒）— https://origin-www.paloaltonetworks.in/customers/safeguarding-tradition-in-the-digital-age-oneida-nation-security-transformation
73. NHL 案例 — https://origin-www.paloaltonetworks.in/customers/nhl-stays-ahead-of-the-game-with-palo-alto-networks
74. Konecta 案例（MTTD/MTTR -90%，2025-07，已直接核验）— https://www.paloaltonetworks.com/customers/cortex-xsiam-helps-konecta-drive-secure-agile-global-business-growth
75. Louisiana 案例（86% 自动解决、ROI 300%，2024-12，已直接核验）— https://www.paloaltonetworks.com/customers/louisiana-scales-security-using-ai-driven-cortex-xsiam
76. XSIAM Forrester TEI 研究（厂商委托 ⚠：257% ROI、85% MTTR）— https://www.paloaltonetworks.lat/content/dam/pan/es_LA/assets/pdf/xsiam-ai-driven-secops-platform-goes-beyond-reactive-security-vb-es-la.pdf
77. IBM–Palo Alto 合作新闻稿（2024-05-15，已直接核验：QRadar SaaS 资产、watsonx→XSIAM、免费迁移）— https://newsroom.ibm.com/2024-05-15-Palo-Alto-Networks-and-IBM-to-Jointly-Provide-AI-powered-Security-Offerings-IBM-to-Deliver-Security-Consulting-Services-Across-Palo-Alto-Networks-Security-Platforms
78. Palo Alto cyberpedia：QRadar 收购（完成 2024-08-31、EoS/EoL 生效 2025-04-14、on-prem 不受影响，已直接核验）— https://www.paloaltonetworks.com/cyberpedia/ibm-qradar-acquired-by-palo-alto-networks
79. IBM 云服务下架公告 AD24-0738（2024-09-05：QRadar on Cloud 停止营销，经索引确认）— https://www.ibm.com/docs/en/announcements/cloud-service-withdrawal-access-discontinuance-select-cloud-service-programs-no-replacements?region=US
80. Palo Alto EoS/EoL 数据表（QRadar SaaS EoL 2026-04-14/2026-08-31 两档）— https://www.paloaltonetworks.com/apps/pan/public/downloadResource?pagePath=/content/pan/en_US/resources/datasheets/eos-and-eol-for-threat-management-saas-products
81. IBM QRadar 支持生命周期页（7.6.0 GA 2026-06-30，无 EOS，已直接核验）— https://www.ibm.com/support/pages/node/725959
82. IBM QRadar NTA 文档（"machine learning techniques" 网络基线、outlier 0–100）— https://www.ibm.com/docs/en/qsip/7.6.0?topic=apps-qradar-network-threat-analytics-app
83. Elastic 预置 ML 任务参考（v3_ 系列、auth、dns_tunneling，已直接核验）— https://www.elastic.co/docs/reference/machine-learning/ootb-ml-jobs-siem
84. Elastic ML 算法文档（聚类/时间序列分解/贝叶斯分布建模/相关分析，已直接核验）— https://www.elastic.co/guide/en/machine-learning/current/ml-ad-algorithms.html
85. Elastic ML 入门（95% 置信区间、anomaly score，已直接核验）— https://www.elastic.co/guide/en/machine-learning/current/ml-getting-started.html
86. Elastic 日志分类文档（明确"非 NLP"，已直接核验）— https://www.elastic.co/guide/en/machine-learning/current/ml-configuring-categories.html
87. Elastic ml-cpp GitHub（Elastic License，生产需 license key，已直接核验）— https://github.com/elastic/ml-cpp
88. Elastic Attack Discovery 文档（LLM 告警归并为攻击叙事）— https://www.elastic.co/docs/solutions/security/ai/attack-discovery
89. Elastic Attack Discovery 宣布（2024-05-06 RSA、8.14 Enterprise）— https://ir.elastic.co/news/news-details/2024/Elastic-changes-the-SIEM-game-with-AI-driven-security-analytics/default.aspx
90. Elastic AI Assistant 发布博客（2023-06-13，OpenAI/Azure OpenAI 连接器，已直接核验）— https://www.elastic.co/blog/introducing-elastic-ai-assistant
91. Elastic AIOps 页面（100+ 预置任务、Hexaware -96% 误报 ⚠、PepsiCo -30% MTTR ⚠，已直接核验）— https://www.elastic.co/observability/aiops
92. Elastic 2025 Autumn Edition（Elastic Managed LLM GA 8.18.3/9.0.3，2025-11）— https://info.elastic.co/rs/813-MAM-392/images/2025-autumn-edition-getting-the-most-out-of-elastic-observability-new-features-6036.pdf
93. Elastic Agentic SOC 发布（Attack Discovery 自主 triage agent，2026-07-31）— https://ir.elastic.co/News--Events/news/news-details/2026/Elastic-Advances-the-Agentic-SOC-Bringing-Security-Teams-Closer-to-Alert-Zero/default.aspx
94. TAMUS 案例（月省 100+ 工时 ⚠，已直接核验）— https://www.elastic.co/customers/tamus
95. DoD/USAF 部署博客（600,000+ 端点，2025-11-13，已直接核验）— https://www.elastic.co/blog/defense-and-intelligence-community-endpoint-security
96. Uber ElasticON 2021 演讲（已直接核验）— https://www.elastic.co/elasticon/archive/2021/event/north-america/reinventing-enterprise-defense-with-the-elastic-stack
97. OmniSOC 博客（2018-03-21）— https://www.elastic.co/blog/omnisoc-high-speed-threat-detection-at-the-big-ten
98. Telefónica Germany（Elastic 引 Gartner MQ 口径：RCA -80% ⚠，2025-07）— https://www.nasdaq.com/press-release/elastic-recognized-leader-2025-gartnerr-magic-quadranttm-observability-platforms-2025
99. Sumo Logic Cloud SIEM 产品页（Insight Engine、自适应 Signal clustering，已直接核验）— https://www.sumologic.com/platform/cloud-siem/
100. Sumo Logic AI/ML 文档（LogReduce/Outlier/Insight Trainer/Dojo AI，2025-10-03）— https://d3f0cnhsmnxacx.cloudfront.net/docs/get-started/ai-machine-learning/
101. Sumo Logic Insight Trainer 文档（60 天历史学习、crowd-sourced ML）— https://www.sumologic.com/help/docs/cse/rules/insight-trainer/
102. Sumo Logic Mo Copilot GA 新闻稿（2024-12-02，Amazon Bedrock）— https://www.businesswire.com/news/home/20241202361702/en/
103. Sumo Logic Copilot on Bedrock 技术博客（模型 bakeoff：Claude Instant v1/Claude 2.1.1/GPT-4.1 Turbo，2024-10-31，已直接核验）— https://www.sumologic.com/blog/copilot-amazon-bedrock
104. Sumo Logic OpenPayd 案例（MTTD/MTTR -80%，已直接核验）— https://www.sumologic.com/case-studies/openpayd-fintech
105. Sumo Logic SAP Fieldglass 案例（已直接核验）— https://www.sumologic.com/case-studies/sap
106. Sumo Logic Standard Chartered nexus 案例（已直接核验）— https://www.sumologic.com/case-studies/standard-chartered
107. Sumo Logic SOC Analyst Agent 新闻（2026-03：推荐补救动作、MTTR 最高 -75% ⚠）— https://www.tmcnet.com/usubmit/2026/03/23/10352669.htm
108. SentinelOne Purple AI GA 博客（2024-04-08，已直接核验）— https://www.sentinelone.com/blog/transforming-the-soc-with-purple-ai/
109. SentinelOne–AWS 合作（Purple AI 经 Bedrock、Claude 3.5 Sonnet 可选，2024-10-17）— https://investor.wedbush.com/wedbush/article/bizwire-2024-10-17-sentinelone-expands-strategic-collaboration-with-aws-to-deliver-ai-powered-cybersecurity
110. Securonix EON 发布（Claude 3 via Bedrock，2024-04-30）— https://www.businesswire.com/news/home/20240430073533/en
111. Gurucul UEBA datasheet（5,000+ ML 模型声称 ⚠，仅营销材料）— https://gurucul.com/wp-content/uploads/resources/ds/Gurucul-UEBA-Datasheet.pdf
112. Anvilogic Monte Copilot（$45M Series C 同时发布，2024-04）— https://www.cervinventures.com/news/anvilogic-raises-45m-in-series-c-funding
113. Panther AI（Claude 3.5 Sonnet via Bedrock、告警量 -70% 声称 ⚠）— https://www.anthropic.com/customers/panther

## 3. APM / 可观测性平台

114. Dynatrace Davis 根因分析文档（fault-tree、5 分钟合并/90 分钟上限，已直接核验）— https://docs.dynatrace.com/docs/discover-dynatrace/platform/davis-ai/root-cause-analysis/concepts
115. Dynatrace AWS Workshop "How Davis Works"（确定性因果 vs 传统 ML、NASA/FAA 类比）— https://dynatrace.awsworkshop.io/50_operate/20_how_davis_works.html
116. Dynatrace Hypermodal AI 新闻稿（2023-07-25）— https://www.dynatrace.com/news/press-release/dynatrace-expanding-davis-hypermodal-ai/
117. Dynatrace Davis CoPilot GA 博客（2024-10-10，LLM 未具名）— https://www.dynatrace.com/news/blog/announcing-general-availability-of-davis-copilot-your-new-ai-assistant/
118. Dynatrace 预防性运维博客（>99.9% 降噪、MTTR -56% ⚠）— https://www.dynatrace.com/news/blog/advancing-aiops-preventive-operations-powered-by-davis-ai/
119. Dynatrace BT Digital 案例（16 工具→1、MTTI -90%、£28m，已直接核验）— https://www.dynatrace.com/customers/bt-digital-transformation/
120. BT 官方新闻（2025 自愈目标）— https://newsroom.bt.com/bt-doubles-down-on-aiops-with-dynatrace--targets-self-healing-systems-by-2025/
121. Dynatrace Air Canada 案例（MTTR -55%）— https://dt-cdn.net/customers/air-canada/
122. Dynatrace SAP CX 案例（MTTR -50%）— https://assets.dynatrace.com/en/docs/case/7411-SAP-case-study-dynatrace.pdf
123. Dynatrace Kroger 案例（700→7 工单/周，已直接核验）— https://www.dynatrace.com/customers/kroger/
124. Dynatrace Soldo 案例（Log4Shell 数天→数分钟，已直接核验）— https://www.dynatrace.com/customers/soldo/
125. Dynatrace IDC 商业价值研究（厂商委托 ⚠：451% ROI）— https://assets.dynatrace.com/en/infographic/11966-ig-the-business-value-of-dynatrace.pdf
126. Experian 选择 Dynatrace 新闻稿（2018-09-06）— https://www.businesswire.com/news/home/20180906005050/en/Experian-Selects-Dynatrace-Software-Intelligence-Platform-Automate
127. Datadog Watchdog 异常检测文档（三算法、周季节）— https://docs.datadoghq.com/monitors/types/anomaly/
128. Datadog 专利 US 11,256,596（去趋势、Kendall's tau、误差分位数，2022-02-22 授权）— https://www.datadoghq.com/pdf/patents/11256596-systems-and-techniques-for-adaptive-identification-and-prediction-of-data-anomalies-and-forecasting-data-trends-across-high-scale-network-infrastructures.pdf
129. Datadog Watchdog RCA 文档（四类状态变更根因，已直接核验）— https://docs.datadoghq.com/watchdog/rca/
130. Datadog Toto 发布博客（151M 参数时间序列基础模型，2025-05-21）— https://www.datadoghq.com/blog/datadog-time-series-foundation-model/
131. Datadog Bits AI 博客（2023-08-03）— https://www.datadoghq.com/blog/datadog-bits-generative-ai/
132. Datadog Bits AI SRE 新闻稿（GA 2025-12-02）— https://www.datadoghq.com/ko/about/latest-news/press-releases/datadog-launches-bits-ai-sre-agent-to-resolve-incidents-faster/
133. Datadog Peloton 案例（30 天 12 endpoint 3 倍+）— https://www.datadoghq.com/blog/peloton-app-monitoring/
134. Datadog Samsung 案例（AIOps Agent+BEDROCK、约 1 分钟根因 ⚠）— https://www.datadoghq.com/ko/case-studies/samsung/
135. Datadog Mercado Libre 案例（已直接核验）— https://www.datadoghq.com/case-studies/mercado-libre/
136. Datadog Arc XP 案例（2026，已直接核验）— https://www.datadoghq.com/case-studies/arcxp-2026/
137. Datadog Cvent 案例 PDF — https://www.datadoghq.com/pdf/case_study_cvent_210912.pdf
138. New Relic Grok 发布（2023-05-23，OpenAI）— https://newrelic.com/jp/press-release/20230523
139. New Relic 异常检测文档（标准差+季节基线）— https://github.com/newrelic/docs-website/blob/develop/src/content/docs/alerts-applied-intelligence/applied-intelligence/anomaly-detection/anomaly-detection-applied-intelligence.mdx
140. New Relic 专利 US 10,339,457（异常关联/排序）— https://patentimages.storage.googleapis.com/1b/16/d6/23f9c00d3ae9f5/US10339457.pdf
141. New Relic 私有化完成（2023-11-08）— https://newrelic.com/de/press-release/20231108
142. New Relic Chegg 案例（MTTR -87%，已直接核验）— https://newrelic.com/customers/chegg
143. New Relic AB InBev 案例（MTTR -80%，已直接核验）— https://newrelic.com/customers/abinbev
144. InfoQ：Skyscanner 遥测成本 -90%（2025-05）— https://www.infoq.com/news/2025/05/skyscanner-observability/
145. AppDynamics 异常检测文档（EPM/ART、48 小时训练、Automated RCA）— https://docs.appdynamics.com/appd/24.x/24.3/en/cisco-appdynamics-essentials/alert-and-respond/anomaly-detection
146. 週刊 BCN：Splunk AppDynamics 更名（2024-11-28）— https://www.weeklybcn.com/journal/news/detail/20241128_207173.html
147. Grafana 收购 Asserts.ai（2023-11-14）— https://grafana.com/about/press/2023/11/14/grafana-labs-announces-strategic-acquisition-of-asserts.ai-and-new-tools-to-ease-complexity-of-observing-systems-at-annual-observabilitycon/
148. Grafana Cloud ML 文档（Prophet/DBSCAN）— https://grafana.com/docs/grafana-cloud/machine-learning/machine-learning/
149. Grafana AI 文档（Sift、Assistant、LLM Plugin 模型列表）— https://grafana.com/docs/grafana-cloud/machine-learning/intro/
150. Azure Monitor Smart Detection 文档（20 分钟窗口、Xσ、聚类分析，2025-07-09）— https://learn.microsoft.com/en-us/azure/azure-monitor/alerts/proactive-diagnostics
151. Azure Monitor AIOps 文档（Smart Groups、Dynamic thresholds）— https://learn.microsoft.com/en-us/azure/azure-monitor/aiops/aiops-machine-learning
152. Copilot in Azure 监控文档（2025-02-07）— https://learn.microsoft.com/en-us/azure/copilot/get-monitoring-information
153. GCP Cloud Monitoring ForecastOptions API（forecastHorizon 1–60h）— https://documentation.s3ns.fr/ruby/docs/reference/google-cloud-monitoring-v3/1.7.1/Google-Cloud-Monitoring-V3-AlertPolicy-Condition-MetricThreshold-ForecastOptions
154. GCP Gemini Cloud Assist Investigations 文档（RCA：Observations、多假设）— https://docs.cloud.google.com/cloud-assist/investigations
155. Google Cloud Monitoring 经典异常检测文档 404 实测记录（2026-09-24）— cloud.google.com/monitoring/alerts/anomaly-detection → 301 → docs.cloud.google.com 同路径 404
156. ADEO Services GCP 案例（已直接核验）— https://cloud.google.com/customers/adeo-services

## 4. 学术 / 技术验证

157. DeepLog（ACM CCS 2017，LSTM log key 预测）— https://dl.acm.org/doi/10.1145/3133956.3134015
158. LogAnomaly（IJCAI 2019，template2vec）— https://www.ijcai.org/proceedings/2019/658
159. LogBERT（arXiv:2103.04475，2021）— https://arxiv.org/abs/2103.04475
160. LogRobust（ESEC/FSE 2019）— https://dl.acm.org/doi/abs/10.1145/3338906.3338931
161. 日志异常检测 DL 综述（泛化性问题，arXiv:2202.04301）— https://arxiv.org/abs/2202.04301
162. BigPanda 告警关联逻辑文档（规则模式、300 上限）— https://docs.bigpanda.io/en/alert-correlation-logic
163. Moogsoft 相似度文档（shingling、Sørensen–Dice）— https://docs.moogsoft.com/moogsoft-cloud/en/defining-correlations-310847.html
164. Splunk ITSI Event iQ Detect 文档（语义相似度 85%、Jaro-Winkler 90%）— https://help-preview.splunk.com/en/splunk-it-service-intelligence/splunk-it-service-intelligence/detect-and-act-on-notable-events/5.0/event-correlation/automate-event-correlation-with-event-iq-detect-in-itsi
165. 云原生计算：Panther/Anvilogic 之外的第三方评估（PayMongo IT Brief Asia 报道）— https://itbrief.asia/story/paymongo-taps-datadog-to-boost-payments-reliability
166. Forrester XSIAM TEI（257% ROI ⚠，厂商委托）— 见 #76

## 5. 本会话独立事实核查记录（2026-09-24）

167. Splunk UBA EOL 页面直接核验 — 确认 EOL 2027-01-31、无监督 ML 描述（见 #4）
168. Palo Alto cyberpedia 直接核验 — 确认收购完成 2024-08-31、EoS/EoL 2025-04-14、on-prem 不受影响；页面未提 watsonx（watsonx 嵌入 XSIAM 出自 IBM 侧公告 #77）
169. Elastic Attack Discovery 时间线 — 2024-05-06 宣布（RSA）、8.14 技术预览、2024-08-22 支持 Vertex AI/Gemini、2026-07-31 升级为自主 triage agent
170. Sumo Logic Dojo AI/SOC Analyst Agent — Bedrock 构建、MTTR 最高 -75% 为厂商声称（见 #107）

---
**使用说明**：报告中引用以上来源时以编号 [S-x] 或平台+条目方式标注。⚠ 条目为厂商自报或厂商委托研究，横向比较时不可视为独立验证数据。
