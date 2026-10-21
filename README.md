# self-growing-agent-matrix-research

自生长智能体矩阵调研 —— 索引报告

> 一个「分类体系随新 agent 注册而自我扩张的多智能体矩阵」设想的学术 / 开源坐标调研：总控分类 → L1/L2 路由 → agent 链路执行，像神经网络一样生长、胜任所有工作。

## 仓库内容

```
├── docs/自生长智能体矩阵-索引报告.md —— 主交付物：九条检索线 × 一手来源索引 + P0→P3 落地路线
└── docs/HANDOFF-自生长智能体矩阵调研.md —— 调研任务交接文档（检索方案与协作约定）
```

## 核心结论速览

1. 学术坐标：self-evolving agents 综述框架下的「架构级演化」× open-endedness 持续扩张交叉点。
2. 核心空白确认：未发现任何一手工作完整实现「新 agent 注册 → 自动提议类目 → 影子验证 → 晋升 → 分类体系版本化」流水线——空白即自研范围。
3. 静态骨架可由现成件拼出：MCP Registry + A2A v1.0 + semantic-router + LangGraph + Temporal + Langfuse。
4. 演化引擎可直接复用：EvoAgentX（活跃维护、pip 可装、内置 AFlow/TextGrad）；ADAS / DGM 的 archive 是最接近的版本化雏形。

## 方法

编制日期：2026-10-22。多 agent 集群并行检索（1 前台校准 + 8 后台并行）；只采一手来源（arXiv 原文、官方 spec / 文档、官方 GitHub 仓），逐条标注出处，未验证标「待核」。
