# OSINT 开源情报分析技能

[![Skill Version](https://img.shields.io/badge/version-1.3.0-blue.svg)](https://xiaping.coze.site/skill/d8a6461c-d9f6-40c8-80a9-8be85179d2fa)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-OpenClaw-orange.svg)](https://github.com/openclaw)

> 整合国际标准OSINT情报方法论和工具链的开源情报分析技能，覆盖商业、安全、调查、鉴定等15大应用场景。

## 📖 简介

本技能基于Cambridge、IEEE、Springer等学术研究，整合了完整的OSINT开源情报方法论和100+工具，帮助AI Agent高效完成情报收集与分析任务。

## 🎯 应用场景

| 场景 | 说明 |
|------|------|
| 商业竞争情报 | 竞品分析、市场调研、企业追踪 |
| 地缘政治分析 | 国际事件追踪、冲突分析 |
| 学术情报追踪 | 研究动态、学者网络、技术趋势 |
| 舆情监控 | 品牌舆情、危机预警、传播分析 |
| 供应链情报 | 供应商分析、风险评估 |
| 网络安全威胁情报 | 攻击溯源、APT关联、IOC分析 |
| 反欺诈调查 | 保险欺诈、金融欺诈、证据收集 |
| 知识产权保护 | 侵权监测、维权取证 |
| 招聘背景调查 | 学历核实、工作经历验证 |
| 新闻事实核查 | 多源验证、信源评估 |
| 网络诈骗追踪 | 诈骗溯源、资金追踪 |
| 艺术品鉴定 | 真伪验证、来源追溯 |

## 📚 核心方法论

### 信源评估体系（NATO Admiralty Code）
- **A级**：多源交叉验证 → 直接采信
- **B级**：官方单源 → 可采信，标注单源
- **C级**：权威媒体 → 需追溯原始来源
- **D级**：社交媒体 → 仅作线索，需验证

### R2C2筛选原则
- **R**elevant（相关性）
- **R**eliable（可靠性）
- **C**redible（可信度）
- **C**orroborated（佐证）

### Three Confirms验证规则
- 1源 = 好奇（线索追踪）
- 2源 = 前景（深入调查）
- 3独立源 = 工作级事实（可采信）

### ACH竞争假设分析法
CIA标准方法，用证据证伪假设，对抗认知偏差。

## 🛠️ 工具体系

包含100+工具，覆盖13大类：

- 信息搜索（Google、DuckDuckGo、Yandex）
- 网络空间测绘（Shodan、Censys、ZoomEye）
- 企业信息（天眼查、Crunchbase、LinkedIn）
- 专利与学术（CNIPA、USPTO、arXiv、Semantic Scholar）
- 威胁情报（VirusTotal、CVE、AlienVault OTX）
- 历史存档（Wayback Machine、Archive.today）
- 图片与视频（Google Images、TinEye、InVID）
- 社交媒体情报（Sherlock、Maigret）
- 舆情监控（Google Alerts、百度指数）
- 地理空间情报（Google Earth Pro、Sentinel Hub）
- 法律与公共记录（裁判文书网、PACER）
- 自动化工具（Maltego、SpiderFoot）
- 情报分析工具（Gephi、Neo4j）

## 📋 实战案例

包含15个完整实战案例：

1. 友商电池算法技术追踪
2. 企业技术专利布局分析
3. 信息真伪验证
4. 地缘政治情报分析（美国-伊朗冲突）
5. 商业尽职调查
6. 学术情报追踪
7. 舆情监控与预警
8. 供应链情报分析
9. 网络安全威胁情报
10. 反欺诈调查
11. 知识产权侵权追踪
12. 招聘背景调查
13. 新闻调查与事实核查
14. 网络诈骗追踪
15. 艺术品溯源与鉴定

## 🚀 安装使用

### 方式一：虾评Skill平台（推荐）
访问 [虾评Skill](https://xiaping.coze.site/skill/d8a6461c-d9f6-40c8-80a9-8be85179d2fa) 直接下载安装。

### 方式二：ClawHub
```bash
npx clawhub@latest install ./skill_osint --registry=https://cn.clawhub-mirror.com
```

### 方式三：手动安装
1. 下载本仓库
2. 解压到你的技能目录
3. 在Agent中加载SKILL.md

## 📁 文件结构

```
skill_osint/
├── SKILL.md              # 技能主文件
├── README.md             # 本文件
├── PUBLISH_GUIDE.md      # 发布指南
├── references/
│   ├── methodology.md    # 方法论详细文档
│   └── tools.md          # 工具清单详细文档
└── templates/
    └── report_template.md # 情报报告模板
```

## 📖 参考文献

1. Van Puyvelde, D., & Tabárez Rienzi, F. (2025). The rise of open-source intelligence. *European Journal of International Security*.
2. Coulthart, S., & Nussbaum, J. (2025). OSINT Definition Systematic Review. *Intelligence and National Security*.
3. Heuer, R. J. (1999). *Psychology of Intelligence Analysis*. CIA Center for the Study of Intelligence.
4. Govardhan, D., et al. (2023). Key Challenges and Limitations of the OSINT Framework in Cybersecurity. *IEEE ICECAA*.
5. Springer. (2025). *Open-Source Intelligence (OSINT) for Researchers and Practitioners*.

## 📜 版本历史

### v1.3.0 (2026-04-13)
- 新增7个实战案例（网络安全威胁情报、反欺诈调查、知识产权保护、招聘背调、新闻核查、诈骗追踪、艺术品鉴定）
- 应用场景从6类扩展到15类
- 总计15个完整实战案例

### v1.2.0 (2026-04-13)
- 新增5个实战案例（地缘政治、商业尽职调查、学术情报、舆情监控、供应链情报）
- 工具推荐从7类扩展到13类共100+工具

### v1.1.0 (2026-04-12)
- 新增ACH竞争假设分析法
- 新增反例校验步骤
- 新增踩坑清单模块

### v1.0.0 (2026-04-10)
- 初始版本发布

## 📄 许可证

MIT License

## 🔗 链接

- [虾评Skill主页](https://xiaping.coze.site/skill/d8a6461c-d9f6-40c8-80a9-8be85179d2fa)
- [InStreet社区](https://instreet.coze.site)
- [问题反馈](https://github.com/fengtianyu88/osint-skill/issues)

---

**⚠️ 免责声明**：本技能仅供合法合规的情报分析使用，禁止用于任何非法活动。使用本技能进行的任何操作，由使用者自行承担法律责任。
