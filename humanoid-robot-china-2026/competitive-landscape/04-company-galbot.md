# 银河通用机器人 (Galbot) — 公司深度研究报告

**报告日期：** 2026年3月20日 | **研究视角：** 投资人 / 投资决策

---

## 1. 公司概况

| 项目 | 内容 |
|------|------|
| 法定名称 | 北京银河通用机器人有限公司 |
| 英文名称 | Galaxy General Robotics / Galbot |
| 总部 | 北京 |
| 成立时间 | 2023年5月 |
| 员工人数 | 未披露 |
| 所有制 | 私有 |
| 累计融资 | 约13亿元人民币（约1.8亿美元） |
| 主要投资方 | 美团、CATL（宁德时代）、中国发展银行、国家集成电路产业投资基金 |
| 核心差异化 | 具身大模型优先策略，轮式人形机器人，零售/药房商业化 |

---

## 2. 创立历史

银河通用机器人由王鹤（He Wang）于2023年5月在北京创立。王鹤是北京大学前沿计算研究中心（CFCS）助理教授，其学术实验室EPIC Lab（具身感知与交互实验室）是公司技术的重要来源。公司成立后迅速获得独角兽级别融资，并于2026年2月获得习近平视察Galbot G1机器人的高度政治背书。

**发展里程碑：**
- **2023年5月**：创立，王鹤担任创始人兼CTO
- **2023年**：完成天使轮融资
- **2024年**：推出Galbot G1轮式人形机器人
- **2024年**：在北京近10家药房部署无人值守机器人，24/7运营
- **2025年**：累计融资达13亿元人民币，投资方包括CATL、中国发展银行
- **2025年**：预计营收接近1亿元人民币（零售部署）
- **2025年**：王鹤入选MIT《技术评论》"35岁以下创新者"、《财富》"中国40位40岁以下商界领袖"
- **2026年2月**：习近平视察Galbot G1机器人，并与王鹤会面

来源：[KR Asia — Galbot商业模式](https://www.kr-asia.com/galbots-humanoid-robots-do-the-boring-stuff-and-thats-the-point)、[MIT Innovators Under 35 — 王鹤](https://www.innovatorsunder35.com/the-list/he-wang/)、[The Wire China — 王鹤](https://www.thewirechina.com/whos_who/wang-he-%E7%8E%8B%E9%B9%A4/)

---

## 3. 创始团队背景

### 王鹤（创始人兼CTO）

- **出生**：1992年
- **教育**：斯坦福大学电气工程博士
- **学术职位**：北京大学前沿计算研究中心（CFCS）助理教授；EPIC Lab（具身感知与交互实验室）主任；北京人工智能研究院具身AI中心主任；工信部具身AI分委会副主任
- **研究方向**：具身AI、灵巧操作、视觉-语言-动作模型、3D感知
- **主要学术成果**：
  - GraspVLA：全球首个端到端具身抓取基础模型
  - DexGraspNet：百万级灵巧手抓取数据集（合成数据效率提升50倍）
  - UniDexGrasp++：跨千种物体的通用抓取算法
  - NavFoM：跨机型导航基础模型
- **荣誉**：2025年世界互联网大会领先科技奖、MIT《技术评论》"35岁以下创新者"、ICCV 2023最佳论文提名、ICRA 2023杰出操作论文提名
- **政治资本**：2026年2月习近平视察Galbot G1机器人并与王鹤会面

来源：[王鹤个人主页](http://hughw19.github.io/)、[MIT Innovators Under 35](https://www.innovatorsunder35.com/the-list/he-wang/)、[The Wire China](https://www.thewirechina.com/whos_who/wang-he-%E7%8E%8B%E9%B9%A4/)

---

## 4. 管理团队

- **王鹤**：创始人兼CTO，北大教授背景
- 其他高管信息未公开披露 [SINGLE-SOURCE — VERIFY INDEPENDENTLY]

**主要投资方（战略价值）：**
- **美团**：零售/配送场景资源，是Galbot药房部署的重要战略支持方
- **CATL（宁德时代）**：电池技术支持，长续航优势
- **中国发展银行**：国家级背书，政府资源
- **国家集成电路产业投资基金**：芯片/算力资源

来源：[Technode — 银河通用融资](https://cn.technode.com/post/tag/%E9%93%B6%E6%B2%B3%E9%80%9A%E7%94%A8%E6%9C%BA%E5%99%A8%E4%BA%BA/)

---

## 5. 产品组合

### Galbot G1（核心产品）

| 参数 | 数值 |
|------|------|
| 身高 | 173cm（站立） |
| 体重 | 85kg（含电池） |
| 臂展 | 190cm |
| 最大触及高度 | 240cm（躯干升降65cm） |
| 自由度 | 25 DOF |
| 最大速度 | 1.4 m/s |
| 续航时间 | 600分钟（10小时） |
| 负载能力 | 5kg |
| 底盘类型 | 轮式（非双足行走） |
| AI算力 | NVIDIA Jetson Thor，2070 FP4 TFLOPS，128GB内存 |
| 连接方式 | WiFi（2.4/5GHz）、以太网、USB、云端 |

**核心能力：**
- 双臂灵巧操作（拣选、放置）
- 语音指令识别和自然语言处理
- 自适应学习（AI算法）
- 多模态传感器融合
- 安全人机协作

来源：[Aparobot — Galbot G1规格](https://www.aparobot.com/robots/galbot-g1)、[Robozaps — Galbot G1评测](https://blog.robozaps.com/b/galbot-g1-review)

### AI模型产品线

| 模型 | 功能 |
|------|------|
| GraspVLA | 全球首个端到端具身抓取基础模型，核心竞争力 |
| TrackVLA | 跨机型导航基础模型 |
| DexNDM | 灵巧手神经动力学模型 |

**产品哲学：** 王鹤明确表示，银河通用的核心竞争力是**具身大模型**，而非硬件本身。公司将大部分资源投入AI模型研发，而非推出多款硬件产品。

---

## 6. 财务概况

### 融资历史

| 轮次 | 时间 | 金额 | 主要投资方 |
|------|------|------|-----------|
| 天使轮 | 2023年 | 未披露 | 未披露 |
| A轮及后续 | 2023-2025年 | 累计约13亿元 | 美团、CATL、中国发展银行、国家集成电路基金等 |

来源：[MIT Innovators Under 35](https://www.innovatorsunder35.com/the-list/he-wang/)（"累计融资13亿元"）、[The Wire China](https://www.thewirechina.com/whos_who/wang-he-%E7%8E%8B%E9%B9%A4/)（"超3.35亿美元"）

### 收入预测

[TRIANGULATED ESTIMATE — NOT DISCLOSED]：
- 2025年预计营收接近1亿元人民币（来自零售/药房部署）
- 主要收入来源：机器人硬件销售 + 具身AI模型授权
- 公司未公开财务数据

来源：[KR Asia](https://www.kr-asia.com/galbots-humanoid-robots-do-the-boring-stuff-and-thats-the-point)

### 估值

- 已达独角兽级别（具体估值未披露）[SINGLE-SOURCE — VERIFY INDEPENDENTLY]

---

## 7. 市场拓展

**已商业化场景：**
- **北京药房**：近10家无人值守药房，24/7运营，机器人负责药品分拣和配送
- **计划扩张**：2025年底前扩展至北京、上海、深圳100个药房网点

**试点合作：**
- 梅赛德斯-奔驰（Mercedes-Benz）：汽车制造概念验证
- 极氪（Zeekr）：汽车制造概念验证
- 宇树科技：GraspVLA模型部署合作

**市场定位（王鹤）：**
> "我们不做'迎宾表演'机器人，我们专注于不那么炫酷但真正必要的任务：移动、拣选、放置。"

---

## 8. 技术与知识产权

**核心技术壁垒：**

1. **合成数据生成**：自研基础设施，融合图形学、物理仿真、运动合成流水线，大幅降低真实数据采集成本
2. **GraspVLA**：全球首个端到端具身抓取基础模型，基于10亿视觉-语言-动作帧对训练
3. **跨机型泛化**：模型可跨不同机器人平台迁移，降低部署成本
4. **汽车级可靠性**：面向24/7连续运营设计，而非演示级产品

**王鹤的技术哲学：**
> "合成数据在银河通用当前成就中发挥了非常重要的作用。"
> "从零到一的泛化能力需要5-10年，但我们已经在正确的路上。"

**与学术界的协同：**
- 北京大学Galbot机器人实验室（王鹤学术与创业双轨并行）
- CFCS前沿计算研究中心资源共享

---

## 9. 竞争定位

| 维度 | 银河通用 | 智元机器人 | 宇树科技 |
|------|---------|-----------|---------|
| 底盘类型 | 轮式 | 双足 | 双足 |
| 核心战略 | AI模型优先 | 量产+AI | 性价比+开放 |
| 商业化场景 | 零售/药房（已落地） | 汽车制造 | 研究/工业 |
| 产品价格 | 高端（数十万元） | $10-19万 | $1.35万起 |
| 创始人背景 | 学术（北大/斯坦福） | 工业（华为） | 工程（自学） |
| 习近平视察 | ✓（2026年2月） | ✗ | ✗ |

**核心竞争优势：**
1. **最强学术背景**：王鹤斯坦福博士+北大教授，GraspVLA技术领先
2. **已有真实商业化案例**：北京药房24/7运营，非演示级
3. **顶级战略投资方**：CATL、美团提供场景资源
4. **习近平视察背书**：最高级别政治认可

**主要风险：**
- 轮式底盘限制应用场景（无法上下楼梯）
- 单一产品线，硬件迭代速度慢
- 规模化量产能力尚未验证

---

## 10. 战略方向

1. **零售/药房规模化**：从北京10家扩展至三大城市100家
2. **汽车制造进入**：奔驰、极氪概念验证转化为正式合同
3. **AI模型商业化**：GraspVLA授权给其他机器人公司（已与宇树合作）
4. **IPO筹备**：估值已达独角兽级别，IPO时间表未披露
5. **学术-产业双轨**：持续通过北大实验室输出前沿研究成果

---

## 11. SWOT分析

### 优势（Strengths）
- GraspVLA技术领先，全球首个端到端具身抓取基础模型 [MIT Innovators Under 35](https://www.innovatorsunder35.com/the-list/he-wang/)
- 北京药房已有真实商业化案例，非演示级
- 习近平视察，最高级别政治背书
- CATL、美团等战略投资方提供场景和技术资源

### 劣势（Weaknesses）
- 轮式底盘限制应用场景
- 单一产品线，硬件迭代速度慢于竞争对手
- 规模化量产能力尚未验证
- 营收规模相对较小（预计约1亿元）

### 机会（Opportunities）
- 零售/药房自动化市场规模巨大
- AI模型授权商业模式可轻资产扩张
- 汽车制造场景进入（奔驰、极氪试点）
- 学术资源持续输出前沿技术

### 威胁（Threats）
- 智元、宇树在工业场景竞争激烈
- 双足机器人技术成熟后，轮式底盘优势减弱
- 学术创始人商业化执行能力存疑

---

## 12. 数据可信度评级

**总体评级：中**

| 数据类型 | 可信度 | 说明 |
|---------|--------|------|
| 创始人背景 | 高 | 北大官网、MIT等多源验证 |
| 技术能力 | 高 | 学术论文、官方发布 |
| 融资数据 | 中 | 媒体报道，部分数字存在差异 |
| 商业化案例 | 中 | KR Asia单一来源 |
| 营收预测 | 低 | 单一来源，未官方确认 |
| 估值 | 低 | 未官方披露 |

---

## 13. 来源列表

1. [KR Asia — Galbot商业模式深度报道](https://www.kr-asia.com/galbots-humanoid-robots-do-the-boring-stuff-and-thats-the-point)
2. [MIT Innovators Under 35 — 王鹤](https://www.innovatorsunder35.com/the-list/he-wang/)
3. [The Wire China — 王鹤档案](https://www.thewirechina.com/whos_who/wang-he-%E7%8E%8B%E9%B9%A4/)
4. [王鹤个人主页 — EPIC Lab](http://hughw19.github.io/)
5. [Aparobot — Galbot G1规格](https://www.aparobot.com/robots/galbot-g1)
6. [Robozaps — Galbot G1评测](https://blog.robozaps.com/b/galbot-g1-review)
7. [Aparobot — Galbot G1零售应用](https://www.aparobot.com/articles/galbot-g1-the-humanoid-robot-revolutionizing-retail-with-award-winning-precision)
8. [Humanoid.guide — Galbot产品页](https://humanoid.guide/product/galbot/)
9. [Technode — 银河通用融资列表](https://cn.technode.com/post/tag/%E9%93%B6%E6%B2%B3%E9%80%9A%E7%94%A8%E6%9C%BA%E5%99%A8%E4%BA%BA/)
10. [36Kr — 银河通用战略报道](https://eu.36kr.com/en/p/3350684885707399)
11. [Roboticgizmos — Galbot G1 NVIDIA Jetson Thor](https://www.roboticgizmos.com/gal/)
