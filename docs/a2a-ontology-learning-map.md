# A2A、本体论与工程化落地学习地图

更新日期：2026-07-16

配套互动教程：[A2A 与本体论互动教程](tutorial/index.html)

这份索引用于快速建立三类能力：

- 理解 **A2A / Agent2Agent**：Agent 之间如何发现、通信、传递任务、处理身份认证和多轮协作。
- 理解 **本体论 / ontology engineering**：如何用对象、关系、约束、规则和语义标准描述业务世界。
- 理解 **本体论如何工程化落地**：如何从概念模型走到数据管道、知识图谱、语义层、Agent 能力发现、治理和可执行动作。

## 1. 推荐阅读顺序

### 第一阶段：先理解 A2A 是什么

1. [A2A Protocol 官方文档](https://a2a-protocol.org/latest/)
   - 类型：官方文档
   - 重点：A2A 的目标、核心概念、协议边界、与 MCP 的关系。
   - 读完要能回答：A2A 解决的是 Agent-to-Agent 通信，不是单个 Agent 内部工具调用。

2. [A2A Protocol Specification](https://a2a-protocol.org/latest/specification/)
   - 类型：官方规范
   - 重点：Agent Card、Message、Task、Artifact、Security、Streaming、Push Notification。
   - 读完要能回答：一个 Agent 如何声明能力，另一个 Agent 如何发起任务并追踪状态。

3. [A2A and MCP](https://a2a-protocol.org/latest/topics/a2a-and-mcp/)
   - 类型：官方说明
   - 重点：A2A 和 MCP 的分工。
   - 读完要能回答：MCP 偏工具/上下文接入，A2A 偏 Agent 之间的任务协作和互操作。

4. [a2aproject/A2A GitHub 仓库](https://github.com/a2aproject/A2A)
   - 类型：官方 GitHub
   - 重点：规范变更、issue、proposal、release notes、SDK 列表。
   - 读完要能回答：当前协议有哪些稳定部分，哪些语义仍在演进。

5. [a2aproject/a2a-samples](https://github.com/a2aproject/a2a-samples)
   - 类型：官方示例
   - 重点：多语言样例、签名校验、多租户、SDK 使用方式。
   - 读完要能回答：A2A 在工程里如何启动服务、暴露 Agent Card、处理消息和任务。

### 第二阶段：理解本体论和语义建模基础

1. [Ontology Development 101: A Guide to Creating Your First Ontology](https://protege.stanford.edu/publications/ontology_development/ontology101.pdf)
   - 类型：经典教程
   - 重点：类、属性、实例、约束、复用、迭代建模。
   - 读完要能回答：为什么 ontology 不是数据库表结构，也不是单纯 taxonomy。

2. [RDF 1.1 Primer](https://www.w3.org/TR/rdf11-primer/)
   - 类型：W3C 标准入门
   - 重点：主语-谓语-宾语三元组、IRI、literal、graph。
   - 读完要能回答：知识图谱里事实如何被表达为机器可处理的语义关系。

3. [OWL 2 Web Ontology Language Primer](https://www.w3.org/TR/owl2-primer/)
   - 类型：W3C 标准入门
   - 重点：类、公理、等价、推理、约束表达能力。
   - 读完要能回答：OWL 相比普通 schema 强在哪里，为什么它适合表达领域知识。

4. [SHACL 官方规范](https://www.w3.org/TR/shacl/)
   - 类型：W3C 标准
   - 重点：Shape、constraint、validation report。
   - 读完要能回答：如何验证知识图谱数据是否满足业务规则和接口契约。

5. [SKOS Primer](https://www.w3.org/TR/skos-primer/)
   - 类型：W3C 标准入门
   - 重点：概念体系、词表、同义词、 broader/narrower 关系。
   - 读完要能回答：如何先用轻量概念词表统一业务语言，再逐步升级为完整 ontology。

6. [SPARQL 1.1 Query Language](https://www.w3.org/TR/sparql11-query/)
   - 类型：W3C 标准
   - 重点：查询 RDF graph、路径查询、过滤、聚合。
   - 读完要能回答：语义图谱如何被查询、验证和集成到应用里。

### 第三阶段：理解“本体论如何变成系统”

1. [Palantir Ontology 官方产品说明](https://www.palantir.com/platforms/foundry/ontology/)
   - 类型：厂商官方
   - 重点：Object、Link、Action、Logic、Operational layer。
   - 读完要能回答：本体不是文档，而是把数据、业务对象、权限和动作连接起来的运行时语义层。

2. [Palantir Ontology SDK](https://www.palantir.com/docs/foundry/ontology-sdk/overview/)
   - 类型：厂商官方文档
   - 重点：用代码访问 ontology 对象、关系、动作和函数。
   - 读完要能回答：业务本体如何被前端、后端和自动化流程调用。

3. [Palantir AIP and Ontology](https://www.palantir.com/platforms/aip/)
   - 类型：厂商官方
   - 重点：LLM/Agent 通过 Ontology 访问业务对象和执行动作。
   - 读完要能回答：企业 Agent 为什么需要语义层和权限边界，而不是直接连数据库。

4. [jingw2/nano-ontoprompt](https://github.com/jingw2/nano-ontoprompt)
   - 类型：GitHub 项目
   - 重点：受 Palantir Foundry 启发的本体工程平台，支持多源数据、关系推断、Logic/Action、图谱可视化。
   - 读完要能回答：一个轻量本体平台最小需要哪些模块。

5. [nano-ontoprompt 中文 README](https://github.com/jingw2/nano-ontoprompt/blob/master/README_zh.md)
   - 类型：GitHub 项目文档
   - 重点：Pipeline Mapping、LLM 提取、关系推断、Graph fallback、安全隔离。
   - 读完要能回答：从文件/结构化数据到业务本体和图谱的工程路径。

## 2. A2A 重点概念与应该关注的问题

### Agent Card

- 资料：[Agent Card 官方说明](https://a2a-protocol.org/latest/specification/#agent-card)
- 要理解的问题：
  - Agent 如何声明身份、能力、接口、认证方式和扩展字段。
  - Agent Card 是否可以承载 ontology URL、skill semantic type、输入输出 shape。
  - 如何避免 Agent 自报能力不可信。

### Task / Message / Artifact

- 资料：[A2A Protocol Specification](https://a2a-protocol.org/latest/specification/)
- 要理解的问题：
  - Message 是交互内容，Task 是可追踪的工作单元，Artifact 是结果产物。
  - 多轮交互、人工确认、长任务、失败恢复需要 Task history 和状态语义。
  - 本体论可以把 Task history 转成可查询、可验证、可审计的事件图。

### Security / Identity / Multi-tenancy

- 资料：[Enterprise-Ready Features](https://a2a-protocol.org/latest/topics/enterprise-ready/)、[Multi-Tenancy and Multi-Agent Routing](https://a2a-protocol.org/latest/topics/multi-tenancy/)、[Agent Discovery](https://a2a-protocol.org/latest/topics/agent-discovery/)
- 要理解的问题：
  - A2A 负责认证声明和通信安全，但业务权限仍要靠领域模型和策略模型落地。
  - 多租户路由不能只靠 URL，需要配合对象级权限、动作权限和审计日志。

### Streaming / Push Notification

- 资料：[Streaming and Asynchronous Operations](https://a2a-protocol.org/latest/topics/streaming-and-async/)
- 要理解的问题：
  - 长任务需要流式状态更新。
  - 本体论可以约束状态转移是否合法、事件字段是否完整、结果是否可复现。

## 3. 本体论工程化重点概念

### Object Type

- 含义：业务世界里的核心对象类型，例如客户、订单、供应商、设备、风险事件、Agent、Skill、Task。
- 工程落点：数据库表、API DTO、图谱节点、权限对象、搜索索引、前端详情页都应能映射回 Object Type。
- 常见错误：把每个源系统表直接当 Object Type，导致本体变成数据库镜像。

### Link Type

- 含义：对象之间有业务含义的关系，例如客户拥有账户、订单来自供应商、Agent 执行 Skill。
- 工程落点：图谱边、外键、事件关联、血缘关系、权限传播路径。
- 常见错误：只保存 ID 关联，不命名关系语义，导致 Agent 无法理解关系含义。

### Logic

- 含义：派生状态、校验规则、风险规则、推理规则。
- 工程落点：SQL view、规则引擎、SHACL shape、后端 service、stream job。
- 常见错误：规则散落在前端、ETL、API 和报表里，没人知道哪个是准的。

### Action

- 含义：可对业务对象执行的动作，例如审批、派单、冻结账户、发起采购、通知负责人。
- 工程落点：API endpoint、workflow、queue job、权限校验、审计日志。
- 常见错误：本体只做“看图谱”，没有把动作纳入模型，Agent 只能问答不能执行。

### Shape / Constraint

- 含义：对象和关系必须满足的结构、字段、枚举、基数、范围、权限约束。
- 工程落点：SHACL、JSON Schema、OpenAPI schema、数据库 constraint、CI 校验。
- 常见错误：只有自然语言说明，没有机器可验证约束。

## 4. 本体论落地方案对比

| 方案 | 适合场景 | 技术形态 | 优点 | 风险 |
| --- | --- | --- | --- | --- |
| 轻量业务词表 | 团队刚开始统一语言 | Markdown + SKOS + glossary | 成本低，容易启动 | 推理和校验能力弱 |
| RDF/OWL/SHACL 本体 | 需要标准化语义互操作 | RDF store + OWL + SHACL + SPARQL | 标准成熟，适合跨系统 | 学习成本高，工程工具链复杂 |
| Property Graph 知识图谱 | 重点是关系查询和可视化 | Neo4j / TigerGraph / Neptune | 工程友好，查询直观 | 语义标准化弱于 RDF/OWL |
| Palantir 风格 Ontology | 需要对象、权限、动作、运营闭环 | Object/Link/Logic/Action + SDK | 能把数据和业务动作连起来 | 需要强治理和平台投入 |
| GraphRAG / Semantic RAG | 重点是 LLM 检索和问答 | 文档抽取 + 图谱 + 向量索引 | 见效快，适合知识助理 | 容易停留在检索，不进入业务执行 |
| Agent Semantic Layer | 多 Agent 需要能力发现和互操作 | A2A Agent Card + ontology profile + SHACL | 适合 Agent 生态治理 | 标准还在形成，需要自定义扩展 |

## 5. 工程化参考项目与平台

### 图谱与语义标准

- [Apache Jena](https://jena.apache.org/)
  - RDF、SPARQL、reasoning、SHACL，适合 Java 生态和标准语义栈。
- [Eclipse RDF4J](https://rdf4j.org/)
  - RDF 数据管理、SPARQL、repository API，适合 Java 语义应用。
- [TopBraid EDG / SHACL 资料](https://www.topquadrant.com/technology/shacl/)
  - SHACL 与企业语义建模资料较丰富，适合理解约束验证落地。
- [Ontotext GraphDB](https://graphdb.ontotext.com/)
  - 企业 RDF graph database，适合 RDF/OWL/SPARQL 方向。
- [Stardog](https://www.stardog.com/)
  - Enterprise knowledge graph / semantic layer，适合看“语义层 + 企业数据”产品化路径。

### Property Graph / GraphRAG

- [Neo4j GraphRAG Python](https://github.com/neo4j/neo4j-graphrag-python)
  - Neo4j 官方 GraphRAG Python 库，适合理解图谱和 LLM 检索的工程接口。
- [Microsoft GraphRAG](https://github.com/microsoft/graphrag)
  - GraphRAG 的端到端 pipeline 参考，适合理解文档到图谱、社区摘要、检索的流程。
- [LlamaIndex Knowledge Graph / Property Graph 文档](https://docs.llamaindex.ai/en/stable/module_guides/indexing/lpg_index_guide/)
  - 适合快速构建 LLM + property graph 的实验。
- [LangChain Knowledge Graph 相关文档](https://python.langchain.com/docs/integrations/graphs/)
  - 适合了解 LLM 应用框架如何接图数据库。
- [cognee](https://github.com/topoteretes/cognee)
  - AI memory / graph pipeline 项目，适合观察 agentic memory 的工程化方向。

### 本体建模工具

- [Protégé](https://protege.stanford.edu/)
  - 经典 ontology 编辑器，适合学习 OWL、本体类层次、属性、公理。
- [WebVOWL](https://service.tib.eu/webvowl/)
  - OWL 本体可视化，适合检查 ontology 是否可理解。
- [VocBench](https://vocbench.uniroma2.it/)
  - 词表、SKOS、OWL 协作管理工具。
- [PoolParty Semantic Suite](https://www.poolparty.biz/)
  - 企业级 taxonomy / ontology / semantic layer 平台，可参考产品化能力。

## 6. A2A × 本体论落地架构

### 目标

让 Agent 不只是“互相发消息”，而是能用共同语义完成发现、选择、授权、执行、审计。

### 最小可行架构

```text
业务数据源
  -> 数据接入 / 映射
  -> Object / Link / Logic / Action 本体层
  -> RDF/Graph/SQL 混合存储
  -> Semantic Profile 导出
  -> A2A Agent Card metadata / extension
  -> Agent 发现、能力匹配、任务派发
  -> Task history / Artifact / Action audit
```

### 关键设计

1. **Agent Card 不承载完整 ontology，只承载入口。**
   - `ontologyProfileUrl`
   - `skillSemanticType`
   - `inputShapeUrl`
   - `outputShapeUrl`
   - `actionPolicyUrl`

2. **用 SHACL 或 JSON Schema 验证 Agent 输入输出。**
   - 请求前验证：调用方是否给足字段、类型、权限上下文。
   - 返回后验证：结果是否满足业务约束。
   - CI 验证：Agent Card 与 semantic profile 是否同步。

3. **把 Task history 变成事件图。**
   - TaskCreated
   - MessageReceived
   - SkillSelected
   - ActionInvoked
   - ArtifactProduced
   - HumanApproved
   - TaskCompleted / TaskFailed

4. **把权限建模到对象和动作。**
   - 谁能看什么 Object Type。
   - 谁能沿哪些 Link Type 查询。
   - 谁能执行哪些 Action。
   - 哪些 Action 需要人工确认。

5. **能力声明需要证据。**
   - 不只写“我会采购分析”。
   - 需要示例任务、输入输出 shape、评测结果、支持范围、失败边界、版本。

## 7. 可以直接做的 PoC

### PoC 1：A2A Agent Card 语义扩展

目标：给一个 A2A Agent Card 增加 ontology 入口。

产物：

- `agent-card.json`
- `semantic-profile.jsonld`
- `input-shape.ttl`
- `output-shape.ttl`

验证点：

- Agent Card 可以被普通 A2A client 读取。
- 支持语义扩展的 client 可以进一步读取 profile。
- 输入输出可以通过 SHACL/JSON Schema 校验。

### PoC 2：nano-ontoprompt 到 Agent Skill Profile

目标：从 nano-ontoprompt 的 Object/Link/Logic/Action 导出 Agent skill 描述。

产物：

- Object Type 到 Agent 能力领域的映射。
- Action 到 A2A skill 的映射。
- Logic 到 precondition/postcondition 的映射。

验证点：

- 一个 Agent 能根据 profile 判断另一个 Agent 是否能处理某类任务。
- 错误任务能在调用前被 schema 或 shape 拦截。

### PoC 3：A2A Task History 语义审计

目标：把 A2A task/message/artifact/status update 记录成事件图。

产物：

- `TaskEvent` ontology。
- `TaskEventShape`。
- SPARQL 或 graph query 示例。

验证点：

- 能查询某个业务对象被哪些 Agent 处理过。
- 能查询某个 Action 是谁触发、基于哪些输入、产出哪些 Artifact。
- 能识别缺少审批、缺少 provenance、状态跳转非法的任务。

## 8. 论文与深度资料

- [FOI-O: Formal Ontology of Inquiry](https://arxiv.org/abs/2607.02947)
  - 重点：OWL/RDF/SHACL 用于流程、规则和验证。
  - 适合：理解本体如何约束流程和审计边界。

- [A Semantic Framework for Reproducible Variational Quantum Algorithm Execution Records](https://arxiv.org/abs/2607.03982)
  - 重点：用 OWL、SHACL、SPARQL 表达执行记录和完整性验证。
  - 适合：迁移到 Agent task history / execution record。

- [Memory-Orchestrated Semantic System](https://arxiv.org/abs/2607.04391)
  - 重点：用结构化数据库、概念词表和可审计日志构造 agentic memory。
  - 适合：反思纯向量记忆的不足。

- [Capability Advertisement as a Market for Lemons](https://arxiv.org/abs/2606.03034)
  - 重点：Agent 能力声明可能不可信，需要验证和声誉机制。
  - 适合：设计 Agent Card capability proof。

- [Knowledge Graphs for Explainable Artificial Intelligence: Foundations, Applications and Challenges](https://arxiv.org/abs/2302.01954)
  - 重点：知识图谱如何支持可解释 AI。
  - 适合：理解 KG 对 Agent 决策解释和治理的价值。

## 9. 判断一篇资料是否值得读

优先读满足以下条件的资料：

- 有官方规范、代码、schema、release note 或可复现实验。
- 明确说明对象、关系、约束、动作、权限、审计中的至少两项。
- 能回答“如何接入现有系统”，而不是只讲概念。
- 能说明 A2A、MCP、RAG、KG、Ontology 的边界。
- 能给出失败案例、限制和迁移成本。

谨慎对待以下资料：

- 把 A2A 当成任意“两个 AI 聊天”的泛称。
- 把 ontology 等同于 prompt 模板或简单标签体系。
- 只有图谱可视化，没有约束、权限、动作和审计。
- 只讲 GraphRAG 效果，不讲实体解析、关系质量、版本治理和数据血缘。
- 声称“自动生成企业本体”，但没有人工治理和验证机制。

## 10. 下一步建议

1. 先读 A2A 官方文档、spec、A2A and MCP、a2a-samples。
2. 同时读 Ontology 101、RDF Primer、OWL Primer、SHACL。
3. 用 nano-ontoprompt 跑一个小数据集，观察 Object/Link/Logic/Action 如何出现。
4. 设计一个最小 `semantic-profile.jsonld`，挂到 A2A Agent Card metadata。
5. 用 SHACL 或 JSON Schema 验证一个 A2A skill 的输入输出。
6. 把一次 A2A task 执行记录导出成事件图，验证是否能审计。
