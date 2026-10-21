# HANDOFF —— 自生长智能体矩阵调研

> 目标：接手"自生长 agent 矩阵"的调研（未执行，已获批检索方案），用集群并行跑检索线并产出索引报告。
> 编制日期：2026-10-22。编制方式：对话压缩，未执行任何搜索。

## 一句话需求

用户（萧逆尘）设想一个**分类体系随新 agent 注册而自我扩张的多智能体矩阵**（总控分类 → L1/L2 路由 → agent 链路执行，像神经网络一样生长、胜任所有工作）；要验证这个设想在学界/开源界的坐标，并得出"今天能拼什么、缺什么自己写"的落地结论。

## 已确立的结论（勿重复推导，可在调研中验证/推翻）

1. 设想 = 学术上的 self-evolving / self-organizing multi-agent systems；最接近的原型：Agentic Neural Networks（agent 当神经元）、Darwin Gödel Machine（自修改+存档）、Voyager（技能库增长）、EvoAgentX（工作流进化）。
2. 没有任何成熟开源项目完整实现"新 agent 注册 → 自动提议类目 → 影子验证 → 晋升 → 版本化"这条流水线；预期线4/5/9 会证实这是空白（空白本身是核心结论）。
3. 原设计两个必须修正的点：全 agent 两两互通（O(n²) 不可观测，应改黑板/产物契约）；四层树压缩了分解树/角色矩阵/执行DAG 三个正交维度。
4. 务实路线：成熟件搭静态骨架（MCP Registry/A2A + semantic-router + LangGraph/Temporal + Langfuse + 版本表），生长做成离线、带验收、可回滚的演化环。
5. 生长成立的三闭环：增生规则（嵌入挂靠/去重合并/分裂）、验收函数（每类目可验证测试）、版本回滚（topology/agent/contract 三元组）。

## 待执行：九条检索线（集群可按此分工）

执行规则：只采一手来源（arXiv 原文、官方 spec、源码），每条 claim 标出处；找不到标「待核」；每线命中 3–5 个高质量一手来源或证实空白即停。顺序：线1 先行（校准关键词），线4/5/7/8/9 互相独立**可直接并行**。

```
线1 学术谱系定位｜"self-evolving agents survey"、"self-organizing LLM agents survey"、open-ended agent systems
线2 结构自生长｜AFlow、EvoAgentX、ADAS、Meta Agent Search、Darwin-Gödel Machine（arXiv+官方仓）
线3 agent 即神经元｜"Agentic Neural Networks"、TextGrad、textual backpropagation
线4 能力注册与动态发现｜MCP Registry 规范、A2A AgentCard、semantic router、capability discovery（官方 spec 一手）
线5 验收与晋升闭环｜shadow evaluation、agent regression benchmark、canary deployment、Voyager 晋升机制
线6 反面证据｜"why multi-agent systems fail"、MASFT、multi-agent failure taxonomy
线7 开源实现打捞｜GitHub: awesome-self-evolving-agents、topic:agentic-workflow、上述项目官方仓（看活跃度/可跑 demo）
线8 可落地骨架件｜MCP/A2A/LangGraph/Temporal/Langfuse 官方文档与 quickstart
线9 缺口确认｜"agent taxonomy auto-generation"、"dynamic agent registration discovery"（预期空白→自研范围）
```

## 产出要求

- 落盘为索引报告（Markdown），建议路径 `/mnt/agents/output/自生长智能体矩阵-索引报告.md`，结构：一句话需求 → 核心结论（已验证）→ 分线索引表（条目 | 关键机制 | 一手来源链接，每节末一句判定）→ 落地路线（P0→P3）→ 待补搜索。
- 索引为主不搬全文；未验证标「待核」；引用必须来自实际检索结果，禁止编造来源。

## 协作约定（用户偏好，集群各节点遵守）

- 中文回复，全角标点；结构化内容用 tree 样式（`├──` / `└──`）。
- 用户要"极简/N 句话"时严格照做；问答轮不动文件，只在交付产物或用户明说时落盘。
- 默认交付 Markdown，未被点名不做 docx/PPT 转换。

## Suggested skills

- `research`（主用：检索策略、索引报告结构、落盘约定均已在该 skill 中定义）
- `ask-matt`（如需判断后续动作该走哪个流程）
- 调研之后若进入设计/搭建阶段：`prototype`（可运行 MVP）、`to-spec`（发布 spec）、`handoff`（再次交接）

## 待决问题（调研结束前需向用户确认）

1. 每个类目的验收标准来源（影视可"人审+一致性打分"，通用行业呢？）
2. 新类目审批：全自动/全人工/分风险分级？
3. 长到数百类目后的整体回归集怎么维护？
