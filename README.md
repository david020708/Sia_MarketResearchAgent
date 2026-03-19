# Sia — AI 市场研究助手

Sia 是一个基于 Claude Code 构建的市场研究系统，通过 **Skill 模块化架构** 执行全维度市场分析，输出结构化的研究报告。Sia 作为主编排器（通过 `CLAUDE.md` 定义），按需调用六个专业 Skill 模块，依次完成市场研究的各个维度。

## 系统架构

```
                       ┌─────────────┐
                       │   用户请求    │
                       └──────┬──────┘
                              │
                       ┌──────▼──────┐
                       │  Sia 编排器  │  ← 通过 CLAUDE.md 定义，打开项目即生效
                       │  调用 Skill  │
                       └──────┬──────┘
                              │  Skill tool 依次调用
          ┌────────┬───────┬──┴────┬────────┬────────┐
          ▼        ▼       ▼       ▼        ▼        ▼
       市场规模  宏观环境  客户分群  竞争格局  技术创新  渠道/GTM
       (.claude/skills/ 下的六个 Skill 模块)
```

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

进入本项目目录，使用 `--dangerously-skip-permissions` 跳过所有权限确认弹窗：

```bash
cd /path/to/MarketResearch
claude --dangerously-skip-permissions
```

> 本项目只做研究（网络访问、文件读写），不修改代码，跳过权限确认是安全的。

直接用自然语言描述研究需求：

```
我想研究中国新能源汽车充电市场
```

```
帮我做一份东南亚 B2B SaaS 市场的完整研究报告
```

Sia 会通过结构化提问确认研究范围，然后依次调用各 Skill 模块执行分析。

---

## Skill 模块一览

| Skill | 职责 | 输出目录 |
|-------|------|----------|
| `market-sizing` | TAM/SAM/SOM 三角测算 | `market-sizing/` |
| `macro-environment` | 政治、经济、监管、进入壁垒 (PERB) 分析 | `macro-environment/` |
| `customer-segmentation` | 客户分群、买家画像、JTBD 分析 | `customer-segmentation/` |
| `competitive-landscape` | 竞争格局、公司深度画像、市场份额分析 | `competitive-landscape/` |
| `technology-landscape` | 技术图谱、学术研究、专利分析、TRL 评估 | `technology-landscape/` |
| `distribution-gtm` | 渠道策略、GTM 模式、合作伙伴生态 | `distribution-gtm/` |

---

## 工作流程

Sia 确认研究目标后，按以下阶段执行：

1. **需求澄清** — 通过结构化提问确定市场定义、地理范围、研究视角、所需维度，生成研究简报供用户确认
2. **项目初始化** — 创建项目文件夹及各维度子目录
3. **执行研究** — 通过 `Skill` tool 依次调用选定的 Skill 模块，每个模块接收完整的研究简报
4. **交付确认** — 汇总所有输出文件，标注数据缺口和低置信度区域，建议后续研究方向
5. **行业瓶颈分析** — 综合所有研究维度，在聊天中直接输出分层的行业发展瓶颈分析（核心瓶颈 / 重要制约 / 次要障碍），识别真正制约行业发展的关键因素
6. **Follow-up 研究回写** — 用户提出后续问题时，Sia 完成补充研究后会将新发现写回对应的报告文件，作为补充章节追加

---

## 输出结构

每个项目会生成如下目录结构：

```
[项目名称]/
├── market-sizing/           # 市场规模测算
├── macro-environment/       # 宏观环境分析
├── customer-segmentation/   # 客户分群分析
├── competitive-landscape/   # 竞争格局分析
├── technology-landscape/    # 技术创新分析
└── distribution-gtm/        # 渠道与GTM分析
```

---

## 各 Skill 模块详细说明

### Market Sizing（市场规模测算）

采用三种方法进行交叉验证：

- **自上而下**：从宏观数据逐层筛选
- **自下而上**：单位经济模型 × 买家数量
- **供给侧/价值链**：汇总行业参与者收入

输出包含 TAM/SAM/SOM（含乐观/基准/悲观区间）、CAGR 及驱动因素、置信度评估。

### Macro Environment（宏观环境分析）

执行 PERB 框架分析：

- **Political（政治）**：政府稳定性、地缘政治、制裁风险
- **Economic（经济）**：GDP、通胀、汇率、FDI、基础设施
- **Regulatory（监管）**：牌照要求、外资限制、行业法规、知识产权
- **Barriers（壁垒）**：资本门槛、规模经济、监管壁垒、国企优势

输出包含环境评分卡（1-5 分制）、Top 3 风险与机会。

### Customer Segmentation（客户分群分析）

支持 B2C 和 B2B 两种分群框架：

- **B2C**：人口统计、心理特征、行为、地理
- **B2B**：企业特征、技术栈、行为、需求

输出包含分群地图（含规模）、买家画像（11 维结构）、JTBD 分析、优先级矩阵。

### Competitive Landscape（竞争格局分析）

竞争者分类覆盖：直接竞争者、间接竞争者、替代品、潜在进入者、新兴玩家。

输出包含竞争定位图、波特五力分析、各公司 SWOT、威胁评估矩阵，以及每家公司的深度画像。

### Technology Landscape（技术创新分析）

综合运用多种评估框架：

- Gartner 技术成熟度曲线
- McKinsey 技术趋势展望
- 地平线分类（H1/H2/H3）
- NASA TRL 量表（1-9 级）

覆盖学术论文检索（arXiv、Semantic Scholar 等）和专利分析（Google Patents、WIPO 等）。

### Distribution & GTM（渠道与 GTM 分析）

分析渠道架构（零级到三级）和 GTM 模式（现场销售、内部销售、PLG、渠道销售、平台/市场、社区驱动、ABM）。

输出包含渠道经济学分析（利润率堆栈、CAC、LTV:CAC）、合作伙伴生态图谱、渠道冲突评估。

---

## 设计原则

### 数据溯源

所有 Skill 模块遵循同一核心原则：每一个论断、统计数据和数据点都必须标注来源 URL。禁止编造或虚构数据。

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

多个 Skill 模块内置中国市场研究能力，覆盖：
- 中国特色数据源（CNKI、天眼查、艾瑞咨询、QuestMobile 等）
- 监管机构映射及官方门户
- 官方数据与独立来源交叉比对
- 城市分级与代际分群分析

---

## 文件结构

```
MarketResearch/
├── CLAUDE.md                            # Sia 主编排器提示词（打开项目即生效）
├── README.md                            # 本文件
└── .claude/
    ├── settings.local.json              # 权限配置
    └── skills/
        ├── market-sizing/SKILL.md       # 市场规模 Skill
        ├── macro-environment/SKILL.md   # 宏观环境 Skill
        ├── customer-segmentation/SKILL.md  # 客户分群 Skill
        ├── competitive-landscape/SKILL.md  # 竞争格局 Skill
        ├── technology-landscape/SKILL.md   # 技术创新 Skill
        └── distribution-gtm/SKILL.md       # 渠道/GTM Skill
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
