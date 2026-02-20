# Sia — 多智能体市场研究系统

Sia 是一个基于 Claude Code 构建的多智能体协作系统，专为系统化、可溯源的市场研究而设计。系统采用「主编排者 + 六个专家」的星型架构，通过 **Agent Team** 功能并行执行全维度市场分析，输出结构化的研究报告。

## 系统架构

```
                       ┌─────────────┐
                       │   用户请求    │
                       └──────┬──────┘
                              │
                       ┌──────▼──────┐
                       │  Sia 编排器  │  ← 主 Agent（通过 CLAUDE.md 定义）
                       │  创建 Agent Team │
                       └──────┬──────┘
                              │  TeamCreate + 并行 Task
          ┌────────┬───────┬──┴────┬────────┬────────┐
          ▼        ▼       ▼       ▼        ▼        ▼
       市场规模  宏观环境  客户分群  竞争格局  技术创新  渠道/GTM
       (Sub-Agent Team 成员，并行运行)
```

Sia 是主 Agent，通过 `CLAUDE.md` 定义，打开项目即生效。六个专家 Agent 定义在 `.claude/agents/`，由 Sia 通过 Agent Team 功能并行调度。

---

## 安装 Claude Code

### 1. 安装 Node.js

Claude Code 需要 Node.js 18 或以上版本。

```bash
# macOS（推荐用 Homebrew）
brew install node

# 验证版本
node --version  # 应显示 v18.x.x 或更高
```

### 2. 安装 Claude Code CLI

```bash
npm install -g @anthropic-ai/claude-code
```

### 3. 配置 API Key

```bash
# 方式一：环境变量（推荐）
export ANTHROPIC_API_KEY="sk-ant-..."

# 方式二：写入 shell 配置文件（永久生效）
echo 'export ANTHROPIC_API_KEY="sk-ant-..."' >> ~/.zshrc
source ~/.zshrc
```

API Key 在 [console.anthropic.com](https://console.anthropic.com) 获取。

### 4. 验证安装

```bash
claude --version
```

---

## 快速开始

### 启动 Sia（推荐方式）

进入本项目目录，使用 `--dangerously-skip-permissions` 跳过所有权限确认弹窗：

```bash
cd /path/to/MarketResearch
claude --dangerously-skip-permissions
```

> 本项目只做研究（网络访问、文件读写），不修改代码，跳过权限确认是安全的。
> `.claude/settings.local.json` 已预配置全局工具权限，无需逐个确认。

### 发起研究请求

Claude Code 启动后，直接用自然语言描述研究需求：

```
我想研究中国新能源汽车充电市场
```

```
帮我做一份东南亚 B2B SaaS 市场的完整研究报告
```

Sia 会通过结构化提问确认研究范围，然后自动启动 Agent Team 并行执行所有分析。

---

## Agent Team 工作原理

Sia 确认研究目标后，会执行以下步骤：

### 1. 创建 Agent Team
```
TeamCreate(team_name: "项目名称", description: "研究任务描述")
```
这会在 `~/.claude/teams/` 下创建团队配置，所有成员共享一个任务列表。

### 2. 创建任务清单
为每个研究维度在团队任务列表里创建任务（`TaskCreate`），方便追踪进度。

### 3. 并行启动所有专家 Agent
**在单条消息里**同时发出所有 Task 调用——这是并行的关键：

```
Task(subagent_type: "market-size-estimator",        team_name: "项目名", mode: "bypassPermissions", ...)
Task(subagent_type: "macro-environment-analyst",     team_name: "项目名", mode: "bypassPermissions", ...)
Task(subagent_type: "customer-segmentation-analyst", team_name: "项目名", mode: "bypassPermissions", ...)
Task(subagent_type: "competitive-landscape-analyst", team_name: "项目名", mode: "bypassPermissions", ...)
Task(subagent_type: "technology-innovation-analyst", team_name: "项目名", mode: "bypassPermissions", ...)
Task(subagent_type: "distribution-gtm-analyst",      team_name: "项目名", mode: "bypassPermissions", ...)
```

### 4. 监控与协调
- 各 Agent 完成任务后自动发消息给 Sia
- Sia 通过 `TaskList` 监控整体进度
- 所有任务完成后，Sia 关闭团队并向用户汇报

> **注意**：Agent 在两次操作之间会进入 idle 状态，这是正常现象，不代表出错。

---

## 智能体一览

| 智能体 | 职责 | 输出目录 |
|--------|------|----------|
| **Sia**（主 Agent） | 需求澄清、项目创建、Agent Team 调度、交付确认 | 项目根目录 |
| **market-size-estimator** | TAM/SAM/SOM 三角测算 | `market-sizing/` |
| **macro-environment-analyst** | 政治、经济、监管、进入壁垒 (PERB) 分析 | `macro-environment/` |
| **customer-segmentation-analyst** | 客户分群、买家画像、JTBD 分析 | `customer-segmentation/` |
| **competitive-landscape-analyst** | 竞争格局、公司深度画像、市场份额分析 | `competitive-landscape/` |
| **technology-innovation-analyst** | 技术图谱、学术研究、专利分析、TRL 评估 | `technology-landscape/` |
| **distribution-gtm-analyst** | 渠道策略、GTM 模式、合作伙伴生态 | `distribution-gtm/` |

---

## 输出结构

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

---

## 各智能体详细说明

### Sia（主编排器）

Sia 通过 `CLAUDE.md` 定义为主 Agent，打开项目即生效，无需额外调用。

工作流程分为五个阶段：

1. **需求澄清** — 通过结构化提问确定研究范围，生成研究简报供用户确认
2. **项目初始化** — 创建项目文件夹及各维度子目录
3. **启动 Agent Team** — `TeamCreate` 建团队 → `TaskCreate` 建任务 → 单条消息并行 dispatch 所有专家 Agent
4. **监控协调** — 等待各 Agent 消息，处理阻塞，追踪进度
5. **交付确认** — 关闭团队，汇总输出，向用户报告

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

---

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

---

## 文件结构

```
MarketResearch/
├── CLAUDE.md                            # Sia 主 Agent 提示词（打开项目即生效）
└── .claude/
    ├── settings.local.json              # 权限配置（全局工具权限，无需逐个确认）
    └── agents/
        ├── market-size-estimator.md     # 市场规模 Sub-Agent
        ├── macro-environment-analyst.md # 宏观环境 Sub-Agent
        ├── customer-segmentation-analyst.md  # 客户分群 Sub-Agent
        ├── competitive-landscape-analyst.md  # 竞争格局 Sub-Agent
        ├── technology-innovation-analyst.md  # 技术创新 Sub-Agent
        └── distribution-gtm-analyst.md       # 渠道/GTM Sub-Agent
```

---

## 适用场景

- **投资尽调**：为投资决策提供全维度市场情报
- **创业立项**：验证市场机会、评估竞争态势
- **战略规划**：支撑企业进入新市场的决策
- **行业研究**：系统化的行业分析与趋势洞察

---

## 许可

本项目为内部工具，仅供授权用户使用。
