# Drug R&D Skill Suite (CN)

这是一套面向“计算与数字化药物研发”的 ChatGPT Skills 组合包。设计原则是：

1. **DrugClaw 直接覆盖的阶段**，优先用 DrugClaw 的任务边界来做 skill；
2. **DrugClaw 不直接覆盖的阶段**，用 GitHub 上仍活跃、社区可见度较高的开源项目做替代性 skill 设计；
3. 每个 skill 都是“给另一个 ChatGPT 使用的说明书”，重点是触发条件、输入输出、判断逻辑、交付模板，而不是把第三方项目代码直接打包进去。

## DrugClaw 适合覆盖的阶段

- 靶点发现与验证
- 机制与证据综合
- 药物重定位 / 适应症扩展
- ADR / DDI / PGx / Label / Clinical evidence 风险综合

## 用外部热门项目补齐的阶段

- 结构预测与结构准备：OpenFold, PaddleHelix
- 虚拟筛选与 docking runbook：DockM8, EasyDock, QVina
- ADMET / 分子性质建模：Chemprop, DeepChem, TorchDrug
- de novo 分子生成：DrugGEN
- 临床采集与 CDM：OpenClinica
- 实验记录与知识沉淀：eLabFTW, AI4Green

## Skill 清单

| 阶段 | Skill | 主要来源 |
|---|---|---|
| 靶点发现 / 验证 | target-evidence-triage | DrugClaw |
| 重定位 / 适应症扩展 | repurposing-hypothesis-screen | DrugClaw |
| 安全性 / PGx / 标签 | safety-pgx-brief | DrugClaw |
| 结构建模 | structure-folding-planner | OpenFold, PaddleHelix |
| 虚拟筛选 / 命中发现 | virtual-screening-orchestrator | DockM8, EasyDock, QVina |
| Lead 优化 / ADMET | admet-property-modeler | Chemprop, DeepChem, TorchDrug |
| 从头生成 | de-novo-molecule-generator | DrugGEN |
| 临床数据运营 | clinical-study-ops | OpenClinica |
| 实验记录 / 知识沉淀 | lab-knowledge-capture | eLabFTW, AI4Green |

## 怎么用

### 方式 1：单独上传某个 skill
每个 skill 子目录都已经单独打成了 `skill.zip`，可直接选择你想要的那个上传。

### 方式 2：先读说明，再挑 skill
先看每个 skill 目录下的 `SKILL.md` 和来源说明，确认它适合你的团队当前阶段，再上传。

## 推荐组合

- **早研策略组合**：target-evidence-triage + repurposing-hypothesis-screen + safety-pgx-brief
- **结构药设组合**：structure-folding-planner + virtual-screening-orchestrator + admet-property-modeler
- **生成式设计组合**：de-novo-molecule-generator + virtual-screening-orchestrator + admet-property-modeler
- **转化与执行组合**：clinical-study-ops + lab-knowledge-capture

## 明确边界

本套 skill 更偏向：
- 计算生物学
- 药物知识检索与证据综合
- 虚拟筛选 / 设计 / 建模
- 临床数据流程和实验知识沉淀

本次**没有单独生成** CMC / 制剂工艺 / GMP 生产 / eCTD 申报写作 skill。原因不是不能写，而是这些阶段更依赖企业 SOP、法规模板、QMS 与私有系统，单靠当前这一轮 GitHub 热门项目检索，不足以稳定地产生一个高可信的“通用技能包”。