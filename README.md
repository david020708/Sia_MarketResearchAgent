# Sia — 多智能体市场研究系统

Sia 是一个基于 Claude Code 构建的多智能体协作系统，专为系统化、可溯源的市场研究而设计。系统采用"一个编排者 + 六个专家"的星型架构，能够并行执行全维度市场分析，输出结构化的研究报告。

## 系统架构

```
                        ┌─────────────┐
                        │   用户请求    │
                        └──────┬──────┘
                               │
                        ┌──────▼──────┐
                        │  Sia 编排器  │
                        │  (Opus/粉色) │
                        └──────┬──────┘
                               │
          ┌────────┬───────┬───┴───┬────────┬────────┐
          ▼        ▼       ▼       ▼        ▼        ▼
       市场规模  宏观环境  客户分群  竞争格局  技术创新  渠道/GTM
       (红色)   (紫色)   (绿色)   (橙色)   (青色)    (蓝色)
```

## 智能体一览

| 智能体 | 职责 | 输出目录 |
|--------|------|----------|
| **Sia** (编排器) | 需求澄清、项目创建、任务分发、交付确认 | 项目根目录 |
| **Market Size Estimator** | TAM/SAM/SOM 三角测算 | `market-sizing/` |
| **Macro Environment Analyst** | 政治、经济、监管、进入壁垒 (PERB) 分析 | `macro-environment/` |
| **Customer Segmentation Analyst** | 客户分群、买家画像、JTBD 分析 | `customer-segmentation/` |
| **Competitive Landscape Analyst** | 竞争格局、公司深度画像、市场份额分析 | `competitive-landscape/` |
| **Technology Innovation Analyst** | 技术图谱、学术研究、专利分析、TRL 评估 | `technology-landscape/` |
| **Distribution & GTM Analyst** | 渠道策略、GTM 模式、合作伙伴生态 | `distribution-gtm/` |

## 使用方式

### 前置条件

- 安装 [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code)
- 拥有可用的 Anthropic API 密钥

### 启动研究

1. 在项目目录下启动 Claude Code：
   ```bash
   cd MarketResearch
   claude
   ```

2. 向 Sia 发起研究请求，例如：
   ```
   我想研究中国新能源汽车市场
   ```

3. Sia 会通过结构化提问来明确研究范围：
   - **市场定义**：具体产品/服务边界
   - **地理范围**：目标市场区域
   - **研究视角**：投资者 / 创业者 / 战略规划
   - **研究维度**：选择需要的分析模块（默认全部）
   - **深度与重点**：特别关注的领域

4. 确认研究简报后，Sia 将并行调度所有专家智能体执行研究。

### 输出结构

每个项目会生成如下目录结构：

```
[项目名称]/
├── market-sizing/           # 市场规模测算
├── macro-environment/       # 宏观环境分析
├── customer-segmentation/   # 客户分群分析
├── competitive-landscape/   # 竞争格局分析
│   ├── master-report.md     # 总览报告
│   └── [公司名].md          # 各公司深度画像
├── technology-landscape/    # 技术创新分析
│   ├── master-report.md     # 总览报告
│   └── [技术名].md          # 各技术深度报告
└── distribution-gtm/        # 渠道与GTM分析
    ├── master-report.md     # 总览报告
    └── [渠道名].md          # 各渠道深度报告
```

## 各智能体详细说明

### Sia（编排器）

Sia 是系统的唯一入口。用户无需直接调用任何专家智能体，只需向 Sia 描述研究需求即可。

工作流程分为四个阶段：

1. **需求澄清** — 通过结构化提问确定研究范围，生成研究简报供用户确认
2. **项目初始化** — 创建项目文件夹及各维度子目录
3. **并行调度** — 通过 Task 工具同时启动所有选定的专家智能体
4. **交付确认** — 汇总各智能体输出，确认研究完成

### Market Size Estimator（市场规模测算）

采用三种方法进行交叉验证：

- **自上而下**：从宏观数据逐层筛选
- **自下而上**：单位经济模型 × 买家数量
- **供给侧/价值链**：汇总行业参与者收入

输出包含 TAM/SAM/SOM（含乐观/基准/悲观区间）、CAGR 及驱动因素、置信度评估。

### Macro Environment Analyst（宏观环境分析）

执行 PERB 框架分析：

- **Political（政治）**：政府稳定性、地缘政治、制裁风险
- **Economic（经济）**：GDP、通胀、汇率、FDI、基础设施
- **Regulatory（监管）**：牌照要求、外资限制、行业法规、知识产权
- **Barriers（壁垒）**：资本门槛、规模经济、监管壁垒、国企优势

输出包含环境评分卡（1-5 分制）、Top 3 风险与机会。

### Customer Segmentation Analyst（客户分群分析）

支持 B2C 和 B2B 两种分群框架：

- **B2C**：人口统计、心理特征、行为、地理
- **B2B**：企业特征、技术栈、行为、需求

输出包含分群地图（含规模）、买家画像（11 维结构）、JTBD 分析、优先级矩阵。

### Competitive Landscape Analyst（竞争格局分析）

竞争者分类覆盖：直接竞争者、间接竞争者、替代品、潜在进入者、新兴玩家。

输出包含竞争定位图、波特五力分析、各公司 SWOT、威胁评估矩阵，以及每家公司的 13 节深度画像。

### Technology Innovation Analyst（技术创新分析）

综合运用多种评估框架：

- Gartner 技术成熟度曲线
- McKinsey 技术趋势展望
- 地平线分类（H1/H2/H3）
- NASA TRL 量表（1-9 级）

覆盖学术论文检索（arXiv、Semantic Scholar 等）和专利分析（Google Patents、WIPO 等）。

### Distribution & GTM Analyst（渠道与 GTM 分析）

分析渠道架构（零级到三级）和 GTM 模式（现场销售、内部销售、PLG、渠道销售、平台/市场、社区驱动、ABM）。

输出包含渠道经济学分析（利润率堆栈、CAC、LTV:CAC）、合作伙伴生态图谱、渠道冲突评估。

## 设计原则

### 数据溯源

所有智能体遵循同一核心原则：每一个论断、统计数据和数据点都必须标注来源 URL。禁止编造或虚构数据。

### 不确定性标注

- 推理性结论标注为 `[REASONED INFERENCE — NOT SOURCED DATA]`
- 估算数据标注为 `[PROXY ESTIMATE]` 或 `[TRIANGULATED ESTIMATE]`
- 每个维度附带置信度评级（高/中/低）
- 明确记录数据缺口

### 交叉验证

关键数据要求多源验证：
- 市场规模：三种方法交叉测算
- 竞争分析：多来源收入/份额验证
- 渠道分析：至少两个独立来源

### 中国市场专项能力

五个智能体内置中国市场研究模块，覆盖：
- 中国特色数据源（CNKI、天眼查、艾瑞咨询、QuestMobile 等）
- 监管机构映射及官方门户
- 官方数据与独立来源交叉比对
- 城市分级与代际分群分析

## 文件结构

```
MarketResearch/
└── .claude/
    ├── settings.local.json          # 权限配置（允许的网络域名）
    └── agents/
        ├── sia.md                   # 编排器
        ├── market-size-estimator.md # 市场规模
        ├── macro-environment-analyst.md    # 宏观环境
        ├── customer-segmentation-analyst.md # 客户分群
        ├── competitive-landscape-analyst.md # 竞争格局
        ├── technology-innovation-analyst.md # 技术创新
        └── distribution-gtm-analyst.md     # 渠道/GTM
```

## 适用场景

- 投资尽调：为投资决策提供全维度市场情报
- 创业立项：验证市场机会、评估竞争态势
- 战略规划：支撑企业进入新市场的决策
- 行业研究：系统化的行业分析与趋势洞察

## 许可

本项目为内部工具，仅供授权用户使用。
