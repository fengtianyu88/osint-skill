# OSINT工具与资源清单

> 整合自多篇专业文章、学术论文、安全厂商推荐
> 分类整理，覆盖基础→进阶→专家级工具链
> 标注工具用途、适用场景、推荐等级

---

## 一、核心原则与合规红线

### 基本原则
- **公开性**：仅使用公开可访问的数据源，严禁突破访问权限
- **客观性**：多源交叉验证，避免单一数据源片面性
- **目的性**：先明确情报目标，再选择工具与数据源

### 合规红线（中国场景）
- 严格遵守《网络安全法》《个人信息保护法》《数据安全法》
- 禁止非法收集、泄露、出售个人敏感信息
- 禁止使用OSINT工具实施DDoS攻击、端口扫描等主动入侵行为
- 工具仅用于"被动情报收集"

### 隐私保护
- 使用无痕浏览模式、代理服务器或VPN隐藏自身IP
- 避免使用个人社交账号、邮箱注册OSINT工具
- 分析结果仅用于合法场景

---

## 二、搜索引擎与Dorking

### 基础搜索工具

| 工具 | 用途 | 链接 | 推荐度 |
|------|------|------|--------|
| **Google** | 通用搜索+高级语法 | google.com | ⭐⭐⭐⭐⭐ |
| **Bing** | 补充搜索、微软系内容 | bing.com | ⭐⭐⭐⭐ |
| **百度** | 中文内容搜索 | baidu.com | ⭐⭐⭐⭐ |
| **Yandex** | 图片搜索强、俄语内容 | yandex.com | ⭐⭐⭐ |

### Google Dorking 高级语法

#### 文件类型搜索
```
filetype:pdf "confidential"
filetype:xls "budget"
filetype:doc "resume"
filetype:sql "insert into"
```

#### 站点限定
```
site:linkedin.com/in/ "data scientist"
site:github.com "password"
site:target-company.com filetype:pdf
```

#### 时间范围
```
after:2024-01-01
before:2024-12-31
```

#### 组合查询
```
site:.gov filetype:xls "tender" OR "procurement"
intitle:"government gazette" filetype:pdf
site:s3.amazonaws.com "target-company"
```

### 专业搜索引擎

| 工具 | 用途 | 链接 |
|------|------|------|
| **Shodan** | 联网设备搜索引擎 | shodan.io |
| **Censys** | SSL证书、网络资产 | censys.io |
| **ZoomEye** | 中国网络空间测绘 | zoomeye.org |
| **FOFA** | 中国网络空间测绘 | fofa.info |
| **Hunter** | 邮箱地址搜索 | hunter.io |
| **Google Dataset Search** | 结构化数据集搜索 | datasetsearch.research.google.com |

---

## 三、域名与IP侦察

### Whois查询

| 工具 | 特点 | 链接 |
|------|------|------|
| **Whois.ch** | 简洁快速 | whois.ch |
| **DomainTools** | 深度分析、历史记录 | domaintools.com |
| **阿里云Whois** | 中文界面 | whois.aliyun.com |
| **WhoisXMLAPI** | API批量查询 | whoisxmlapi.com |

### DNS查询

| 工具 | 用途 |
|------|------|
| **DNSdumpster** | DNS记录、邮件服务器 |
| **SecurityTrails** | 历史DNS记录 |
| **ViewDNS.info** | 多维度DNS工具集合 |

### 子域名枚举

| 工具 | 特点 | 推荐度 |
|------|------|--------|
| **Amass** | OWASP开源、多源枚举 | ⭐⭐⭐⭐⭐ |
| **Subfinder** | 被动枚举、快速 | ⭐⭐⭐⭐ |
| **KnockPy** | 暴力破解模式 | ⭐⭐⭐ |
| **dnsenum** | 综合DNS枚举 | ⭐⭐⭐ |

### SSL证书分析

| 工具 | 用途 |
|------|------|
| **CertGraph** | 证书关系图谱 |
| **Crt.sh** | 证书搜索 |
| **SSL Labs** | SSL配置审计 |

---

## 四、社交媒体情报（SOCMINT）

### 平台特定工具

| 平台 | 工具 | 用途 |
|------|------|------|
| **Twitter/X** | Social Links | 社交网络分析 |
| **LinkedIn** | Sales Navigator | 专业人脉分析 |
| **Facebook** | Graph Search | 关系图谱查询 |
| **Instagram** | Picasso | 图片分析 |

### 跨平台工具

| 工具 | 特点 | 推荐度 |
|------|------|--------|
| **Sherlock** | 用户名跨平台追踪 | ⭐⭐⭐⭐⭐ |
| **Maigret** | 更全面的用户名搜索 | ⭐⭐⭐⭐⭐ |
| **Social Links** | 商业级SOCMINT | ⭐⭐⭐⭐ |
| **Whatsmyname** | 社交账号枚举 | ⭐⭐⭐⭐ |
| **Sherlock** | GitHub开源 | ⭐⭐⭐⭐ |

### 地理定位工具

| 工具 | 用途 |
|------|------|
| **Geofeedia** | 地理围栏社交搜索 |
| **Echosec** | 地理空间情报 |
| **Geosocialfootprint** | Twitter地理分析 |

---

## 五、自动化侦察框架

### 综合框架

| 工具 | 特点 | 适用场景 | 推荐度 |
|------|------|----------|--------|
| **SpiderFoot** | 集成100+数据源 | 企业暴露面自查 | ⭐⭐⭐⭐⭐ |
| **Recon-ng** | 模块化框架 | 批量侦察 | ⭐⭐⭐⭐ |
| **Maltego** | 关系图谱可视化 | 复杂关联分析 | ⭐⭐⭐⭐⭐ |
| **Datasploit** | 多平台自动聚合 | 快速全貌视图 | ⭐⭐⭐ |
| **OSINT Framework** | 工具导航集合 | 工具查找 | ⭐⭐⭐⭐⭐ |

### SpiderFoot 实战流程
```
输入目标域名 → 选择数据源 → 启动扫描 → 生成HTML报告
报告内容：子域名、邮箱、关联IP、社交账号、漏洞信息
```

### Maltego 实战流程
```
输入目标邮箱 → 关联域名 → 关联社交账号 → IP地址 → 威胁情报
输出：交互式关系图谱
```

---

## 六、文件元数据提取

| 工具 | 特点 | 支持格式 |
|------|------|----------|
| **FOCA** | 自动抓取网站文档分析 | PDF、DOCX、XLSX、PPT |
| **ExifTool** | 深度元数据提取 | 图片、视频、文档 |
| **Metagoofil** | Google文档收割机 | PDF、DOC、XLS |
| **Cancan** | 文档指纹分析 | 多种格式 |

**提取信息**：用户名、路径、软件版本、创建时间、GPS坐标

---

## 七、历史存档与溯源

### Wayback Machine家族

| 工具 | 用途 |
|------|------|
| **Wayback Machine** | 网页历史版本 |
| **Wayback Compare** | 版本对比 |
| **Web.archive.org** | API访问 |

**应用场景**：
- 查找已删除内容
- 发现隐性修改
- 追踪网站演变

---

## 八、图片与视频分析

### 反向图片搜索

| 工具 | 特点 | 链接 |
|------|------|------|
| **Google Images** | 通用搜索 | images.google.com |
| **TinEye** | 精确匹配 | tineye.com |
| **Yandex Images** | 面部识别强 | yandex.com/images |
| **Bing Visual Search** | 综合搜索 | bing.com/visualsearch |

### 图像取证

| 工具 | 用途 |
|------|------|
| **ExifTool** | EXIF元数据提取 |
| **FotoForensics** | ELA分析、错误级别分析 |
| **ImageMagick** | 图片处理、对比 |
| **InVID** | 视频验证插件 |

### 深度伪造检测

| 工具 | 用途 |
|------|------|
| **Reality Defender** | AI生成内容检测 |
| **SITU Research** | 虚假信息溯源 |
| **Deepware** | 深度伪造扫描 |

---

## 九、威胁情报平台

### 聚合平台

| 平台 | 特点 | 免费额度 |
|------|------|----------|
| **VirusTotal** | 多引擎扫描、URL分析 | 有限免费 |
| **AlienVault OTX** | 社区情报、脉冲 | 免费 |
| **IBM X-Force** | 企业级情报 | 有限免费 |
| **ThreatConnect** | 威胁情报管理 | 试用 |

### CVE漏洞数据库

| 数据库 | 链接 |
|--------|------|
| **CVE** | cve.mitre.org |
| **NVD** | nvd.nist.gov |
| **CNVD** | cnvd.org.cn |
| **CNNVD** | cnnvd.org.cn |

### STIX/TAXII标准

- **STIX**：结构化威胁信息表达
- **TAXII**：可信自动交换指标
- **MISP**：开源威胁情报平台

---

## 十、人员身份追踪

### 核心工具链

| 工具 | 用途 |
|------|------|
| **Pipl** | 深度人员搜索 |
| **Spokeo** | 人物数据库 |
| **PhoneInfoga** | 电话号码情报 |
| **GHunt** | Google账户分析 |
| **Epios** | OSINT人员搜索 |

### 工作流程
```
1. 提取核心标识（用户名/邮箱/手机）
2. 跨平台身份关联（Sherlock/Maigret）
3. 指纹比对（头像、签名、发帖风格）
4. 真实身份溯源（邮箱反查、关联信息）
5. 交叉验证
```

---

## 十一、监控与告警

### 持续监控工具

| 工具 | 用途 |
|------|------|
| **Google Alerts** | 关键词监控（可设Dork） |
| **Talkwalker** | 社交媒体监控 |
| **Mention** | 品牌监控 |
| **Hunchly** | 自动网页捕获 |
| **onWatch** | 目标持续追踪 |

### RSS聚合

| 工具 | 用途 |
|------|------|
| **Feedly** | RSS阅读聚合 |
| **Inoreader** | 高级RSS管理 |
| **RSS Feed生成** | Google Alerts转RSS |

---

## 十二、浏览器插件

### 必备插件

| 插件 | 浏览器 | 功能 |
|------|--------|------|
| **Search by Image** | Chrome/Firefox | 一键反向图片搜索 |
| **BuiltWith** | Chrome | 网站技术栈识别 |
| **Wappalyzer** | Chrome | 技术分析 |
| ** Ghostery** | 多浏览器 | 追踪器分析 |
| **IP Address and Domain Info** | Chrome | 快速查看IP/DNS |

### Maltego浏览器插件

- 一键发送到Maltego进行关联分析

---

## 十三、数据可视化

### 关联分析

| 工具 | 特点 | 适用场景 |
|------|------|----------|
| **Maltego** | 交互式图谱 | 复杂关系挖掘 |
| **Gephi** | 开源图可视化 | 大规模网络分析 |
| **Neo4j** | 图数据库 | 深度关联查询 |
| **Linkurious** | 企业版图分析 | 商业情报 |

### 地理可视化

| 工具 | 用途 |
|------|------|
| **Google Earth** | 地理定位分析 |
| **Google Maps** | 位置关联 |
| **Mapbox** | 自定义地图可视化 |
| **Kepler.gl** | 大规模地理数据 |

---

## 十四、学习资源

### 书籍

| 书名 | 作者 | 内容 |
|------|------|------|
| 《掌握开源情报完整指南》 | 拉金德·库马尔 | OSINT标准教材 |
| 《OSINT Techniques》 | Michael Bazzell | 隐私与OSINT |
| 《Web Reconnaissance》 | Various | 网络侦察技术 |

### 在线资源

| 资源 | 链接 |
|------|------|
| OSINT Framework | osintframework.com |
| Technisette | technisette.com |
| OSINT Dojo | osintdojo.com |
| Sector035 | sector035.nl |

### 认证

| 认证 | 机构 | 用途 |
|------|------|------|
| **CCIA** | 认证网络情报分析师 | 系统化方法 |
| **OSINT Masters** | Various | 专业技能认证 |

---

## 十五、工具速查表

### 场景 → 工具映射

| 调查场景 | 推荐工具组合 |
|----------|--------------|
| **企业暴露面自查** | Amass + Censys + Shodan + SpiderFoot |
| **人员背景调查** | Sherlock + Maigret + Pipl + GHunt |
| **网站历史分析** | Wayback Machine + BuiltWith + Wappalyzer |
| **图片溯源** | Google Images + TinEye + ExifTool |
| **社交媒体分析** | Social Links + Geofeedia + Social Searcher |
| **域名调查** | Whois + DNSdumpster + SecurityTrails |
| **漏洞情报** | CVE + NVD + VirusTotal + OTX |

### 工具选择决策树

```
情报目标
├── 人物调查
│   ├── 已知用户名 → Sherlock/Maigret
│   ├── 已知邮箱 → GHunt/Hunter
│   └── 已知手机 → PhoneInfoga
├── 企业调查
│   ├── 域名分析 → Amass + SecurityTrails
│   ├── 资产发现 → Shodan + Censys
│   └── 关系图谱 → Maltego
├── 内容调查
│   ├── 图片溯源 → Google Images + ExifTool
│   ├── 文档分析 → FOCA + Metagoofil
│   └── 视频验证 → InVID + Forensic
└── 持续监控
    ├── 关键词告警 → Google Alerts
    ├── 域名监控 → SecurityTrails
    └── 社交监控 → Talkwalker
```

---

## 十六、工具分类总览

### 工具类型分布

```
OSINT工具生态
├── 搜索工具（搜索引擎、Dorking）
├── 侦察工具（域名、IP、DNS）
├── 社交工具（SOCMINT）
├── 分析框架（SpiderFoot、Maltego）
├── 取证工具（元数据、图片）
├── 监控工具（告警、RSS）
└── 可视化工具（图谱、地图）
```

### 开源 vs 商业工具

| 类型 | 代表工具 | 适用场景 |
|------|----------|----------|
| **开源免费** | SpiderFoot CE、Maltego CE、Amass、Recon-ng、TheHarvester | 个人学习、中小任务 |
| **商业付费** | Maltego Enterprise、Social Links、Pipl Pro、Recorded Future | 企业级、大规模调查 |

---

## 参考来源

| 来源 | 链接 | 标注 |
|------|------|------|
| GoUpSec OSINT工具盘点 | 77169.net | 2025年最新 |
| ReadMedium Top 10 | readmedium.com | 2024年更新 |
| CSDN开源情报全攻略 | blog.csdn.net | 综合指南 |
| FunInformatique Top 10 | funinformatique.com | 免费工具 |
| YISHUTECH OSINT方法论 | yayskj.cn | 深度指南 |
