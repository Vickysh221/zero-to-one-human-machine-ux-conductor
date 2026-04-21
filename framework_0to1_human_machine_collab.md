# 0→1 人机协作产品构思框架

## 文档目的

这份文档用于沉淀一套 **从 0 到 1 的人机协作产品构思方法**，帮助团队在项目不同阶段系统回答两个问题：

1. **这个方向值不值得做、为什么是现在、第一 wedge 应该切哪里？**
2. **如果方向成立，产品结构应该如何被组织成可协作、可设计、可验证、可进入研发的对象？**

这套框架尤其适用于：

- 人机协作系统
- agent 产品
- agentOS
- 半自动化工作台
- 辅助决策系统
- 车内智能系统
- 辅助驾驶 / 安全关键系统

---

## 这份框架怎么用

这不是一张从头问到尾的单线问卷，而是一个 **双阶段框架**：

- **Target A：方向判别 / Direction Framing**
  - 用于项目早期
  - 目的是判断：该不该做、为什么是现在、从哪里切
- **Target B：结构收束 / Structure Convergence**
  - 用于方向基本成立之后
  - 目的是判断：如果要做，产品结构如何成立

两者之间通过一个明确的交接对象连接：

- **Direction Brief**

只有当 Direction Brief 达到可交接门槛时，才进入结构收束阶段。

---

## 全局原则

1. **先判断方向，再细化结构。**
2. **先定义协作结构，再讨论 surface。**
3. **先定义人机边界，再讨论自动化程度。**
4. **先定义长期关系和不可妥协原则，再允许能力分阶段上线。**
5. **先判断这是不是新协作形态，再判断它是不是 AI 功能升级。**
6. **Evaluation 不是终点，而是触发上游回退和重构的反馈回路。**

---

# Part 1. Target A：方向判别 / Direction Framing

> 目标：把一个模糊想法收束成一个可判断、可交接的方向对象，而不是过早长成完整方案。

---

## A1. Vision / Doctrine

### 要回答的问题

- 产品从第一天起，希望用户形成什么样的人机关系？
- 即使当前版本还做不到完全体，产品已经要把用户带向哪一种稳定协作心智？
- 我们面向的是哪类用户心智，而不是只面向某个抽象用户群？
- 这类用户更接受工程透明语言，还是更克制、舒适、服务化的表达？
- 哪些能力可以延后上线，但不能传递相反的关系心智？
- 哪些原则无论产品如何迭代都不能被打破？

### 建议输出

- directional promise
- relationship vision
- target user orientation
- interface language contract
- non-negotiables

### 典型提醒

- 不可逆动作前必须有明确的人类把关方式
- 长期记忆写回不能默认为无门槛自动发生
- “更智能”不是关系愿景；“人始终保有接管权，系统承担持续推进责任”才是

---

## A2. Why Now / Historical Shift / Capability Fit

### 要回答的问题

- 在这个时间点，原来的工作流先断在哪里？
- 当前到底发生了哪些关键变化？
  - 模型能力
  - 工具调用与执行闭环
  - 端侧与系统级接入能力
  - 车机 / 手机 / PC 的入口与算力变化
  - 传感器、地图、状态可视化、调度等基础能力变化
- 这些变化第一次让系统可以进入问题解决链条中的哪几段？
- 用户当下最痛的不是“效率低”本身，而是理解、控制、协调、责任，还是信任？
- 为什么值得做的不是一个更好的 feature / workflow / integration，而是一种新的人机协作形态？
- 如果不用 agent，只做更好的规则、编排、UI 或系统集成，这个问题能不能先解决 70%？

### 建议输出

- why-now memo
- technology shift map
- capability-to-demand map
- paradigm fit judgment
- workflow-first alternative check

### 典型提醒

- “AI 变强了”不是答案
- 关键是：**变化进入了哪一段链条，满足了哪类真实诉求**

---

## A3. Problem Framing

### 要回答的问题

- 用户问题是什么，而不是用户提出的方案是什么？
- 第一用户是谁？谁只是受影响角色？
- 业务目标、用户目标、交付目标、非目标分别是什么？
- MVP 版本明确不做什么？
- 成功标准是什么，什么只是锦上添花？

### 建议输出

- problem statement
- primary user / role map
- goals
- non-goals
- MVP boundary
- success criteria

### 典型提醒

- “做一个 agentOS”不是问题定义
- “让体验更智能”不是成功标准
- 不要把技术能力误当用户问题

---

## A4. Operating Environment / Stakes

### 要回答的问题

- 这个系统的风险等级是什么？
- 结果可逆吗？回滚代价高吗？
- 用户可用注意力有多大？
- 人是否必须持续在环？
- 系统的 actuation boundary 在哪里？
  - observe
  - propose
  - simulate
  - act / commit
- 延迟容忍度是多少？
- 责任归属和审计要求如何？
- 交互带宽是什么？
  - 手机碎片化触达
  - PC 长时工作面
  - 车内语音 + glanceable UI
  - 驾驶中不可凝视、不可过载

### 建议输出

- stakes profile
- reversibility map
- attention constraints
- actuation boundary
- liability / audit requirements

### 为什么必须单独成章

同一个“agent”在手机、车内服务、辅助驾驶和 PC 工作台中，不是同一类问题。
差异首先来自 **风险、可逆性、注意力、权限和时序结构**，而不是界面长得不一样。

---

## A5. Problem-Solving Flow（粗粒度）

### 至少先拆成五段

1. 问题识别
2. 目标定义
3. 计划形成
4. 执行、监控与动态纠偏
5. 结果评估与复盘

### 要回答的问题

- 当前产品覆盖哪几段？
- 当前版本最先切入哪一段，为什么是这一段？
- 哪些段暂时明确不碰？
- 用户是否还需要自己在段与段之间重新拼接流程？
- 这是不是一个必须跨段协作才能成立的问题？

### 建议输出

- coarse flow map
- first wedge
- covered / uncovered stage map
- stage dependency notes

### 典型提醒

- A 阶段只需粗粒度拆段
- 先决定从哪切，不要过早进入每一步的详细状态机

---

## A6. Direction Decision

### 这一页只做一个动作：给出方向判断

结论只允许四种：

- **Go**
- **Go, but narrow**
- **Hold for evidence**
- **Pivot / No**

### 同时必须给出

- first wedge
- top assumptions
- missing evidence
- top risks
- why-now confidence
- whether to enter Target B

### 建议输出

- direction decision
- direction rationale
- evidence gap list
- risk register
- recommended next step

---

# Part 2. A→B Handoff：Direction Brief

只有当 A 阶段达到可交接门槛，才进入结构收束阶段。

---

## 进入 B 的五个门槛

1. 已明确 primary problem，而不是 solution slogan
2. 已通过 why-now / capability fit 判断
3. 已选出 first wedge，且明确不做范围
4. 已识别主要风险、注意力约束与 actuation boundary
5. 已经不再争论“要不要做这个方向”，而是在争论“这个方向怎么成立”

---

## Direction Brief 模板

### 1. Direction Summary
- 当前要解决的问题
- 当前为什么成立
- 当前第一 wedge

### 2. User and Context
- 第一用户
- 核心场景
- 风险 / 注意力 / 权限边界

### 3. Why Now
- 关键变化
- 变化进入链条的哪几段
- 为什么不是简单 feature 升级

### 4. Boundary
- goals
- non-goals
- MVP boundary

### 5. Assumptions and Gaps
- top assumptions
- missing evidence
- unresolved risks

### 6. Handoff Judgment
- 是否进入 Target B
- 进入 B 后最先收束哪部分结构

---

# Part 3. Target B：结构收束 / Structure Convergence

> 目标：把一个基本成立的方向，收束成一套可协作、可设计、可验证、可进入研发的产品结构。

---

## B1. Problem-Solving Flow Decomposition（细化）

### 要回答的问题

- 每一段流程如何流转？
- 执行、监控、动态纠偏、升级与接管如何发生？
- 哪些状态是常态，哪些是异常态？
- 哪些节点会产生 handoff？
- 哪些节点必须允许局部回退、重跑或改约束？

### 建议输出

- detailed flow map
- stage state model
- escalation / correction path
- exception path map

---

## B2. Human-Machine Collaboration Allocation

### 四种基础关系

1. 人主导、机执行
2. 人主导协作
3. 机主导协作
4. 机自治、人治理

### 还要进一步回答

- 在每一段流程里，谁主导？
- 谁知情？
- 谁审批？
- 谁接管？
- 谁拥有解释权和复盘权？
- 是否允许机器默认先行推进？

### 常见人介入模式

- 前置授权
- 持续共驾
- 监督待命
- 例外接管
- 后置复核

### 建议输出

- collaboration allocation map
- default autonomy judgment
- phase-by-phase responsibility map
- human involvement mode map

### 典型提醒

“人机关系”不是一个整体标签，而是 **流程节点上的权力与责任再分配设计**。

---

## B3. Collaboration Prototype & Unit

### 先判断产品当前在解决哪类协作问题

- Clarification
- Co-creation
- Triage
- Supervision
- Orchestration
- Multi-agent Coordination
- Memory Governance

### 再判断真正管理的最小协作单元是什么

- clarification turn
- work cell / artifact section
- case / decision candidate / alert card
- state snapshot / anomaly / intervention point
- run / workflow instance / mission
- thread / coordination bundle
- memory diff / durable record / rule proposal

### 还要补一个二维判断

- **Y 轴：机器主动性**
  - 被动响应
  - 主动建议
  - 主动推进
  - 代理执行
- **X 轴：orchestration 复杂度**
  - 单轮单对象
  - 单线程多步骤
  - 长时状态流
  - 多线程多角色

### 建议输出

- collaboration prototype ladder
- collaboration unit definition
- proactive level judgment
- orchestration complexity judgment
- evolution path

### 典型提醒

- 不要先问 chat / inbox / board / cockpit
- 那些只是协作结构投影到界面的 surface

---

## B4. Interaction Prototypes

### 每种原型都要回答的七个问题

1. 它解决的核心协作矛盾是什么？
2. 用户实际面对的对象是什么？
3. agent 在其中负责什么？
4. 系统必须暴露哪些状态、证据、历史和风险？
5. 用户可插入哪些指令、修改和接管动作？
6. 何时需要升级给人？
7. 常见的界面投影是什么？

### 需要特别保留的提醒

- `Decision Card` 不是全局主角
- 它只是 `Triage` 原型里的典型 handoff object
- 在不同场景里，handoff object 可能是：
  - decision card
  - anomaly object
  - takeover object
  - run checkpoint
  - approval request

### 建议输出

- prototype coverage map
- prototype responsibilities
- handoff object types
- prototype-by-surface mapping

---

## B5. Handoff & Human Intervention

### 先回答两件事

1. 人在什么模式下进入？
2. 被拉回时面对什么对象？

### 五种模式都要分别定义

- 前置授权
- 持续共驾
- 监督待命
- 例外接管
- 后置复核

### 常见高频进入契机

- 目标定义与标准设定
- 敏感 / 不可逆动作前
- 高不确定性或证据不足
- 多 agent 冲突
- 超出授权边界或策略边界
- 长期记忆写回前

### 人进入后可能拥有的动作权

- 批准
- 拒绝
- 改目标
- 改约束
- 暂停
- 接管
- 回滚
- 转派
- 标记待验证
- 要求补证据

### 建议输出

- intervention mode map
- human-entry trigger matrix
- handoff object spec
- approval boundary
- takeover boundary
- recovery / rollback path

---

## B6. Attention Budget & Modality

### 三种通道

- Interrupt
- Batch
- Silent

### 关键不是优先级，而是：

- 为什么在当前介入模式下，人应该以这种方式被带回协作环？
- 为什么是这种强度，而不是另一种强度？

### 还要补一个模态问题

- 文本
- 语音
- glanceable UI
- 触觉 / 声光提醒
- dashboard / queue / digest / audit trail

### 要回答的问题

- 什么应该 interrupt？
- 什么只该进入 batch？
- 什么只应 silent 记录？
- 不同角色看到的通道是否应该不同？
- 用户能否理解“为什么这次打扰了我，而另一次没有”？

### 建议输出

- mode-to-channel map
- wake-up rationale spec
- modality-by-scenario map
- summary cadence
- silent log / audit spec

### 典型提醒

辅助驾驶里的注意力策略，本质是 **安全召回设计**，不是通知设计。

---

## B7. Durable State / Memory Governance

### 为什么不只叫 Writeback / Shared Memory

因为不同形态的长期沉淀物并不相同：

- 手机 agentOS：偏好、上下文、授权窗口
- PC workbench：事实、artifact 历史、run 记录
- 车内 agentOS：偏好、旅程上下文、服务连续状态
- 辅助驾驶：校准、事件轨迹、incident trace、可审计状态

### 要回答的问题

- 什么可以进入 durable state？
- 什么只是 working hypothesis？
- 多 agent 冲突时，保留的是结论、分歧还是待验证状态？
- 写回需要什么证据等级？
- 错写后如何撤销、降级和修复污染？

### 建议输出

- durable state policy
- memory write policy
- promotion / demotion rules
- provenance requirements
- rollback / contamination control

---

## B8. Surface System / UX

### 这一章不再问“chat 还是 inbox”
而是回答：

> 前面的原型、介入模式、注意力通道和 durable state 该如何共同映射成一套 surface system？

### 通常至少包含四类面

1. **Primary Work Surface**
   - 用户平时真正工作的主面
2. **Re-entry Surface**
   - 被重新拉回协作环时首先进入的面
3. **State Visibility Surface**
   - 理解当前状态、风险、进度与线程关系的面
4. **Memory / Audit Surface**
   - 回看、复核、写回、回滚和审计的面

### 要回答的问题

- 主工作面是什么，为什么？
- 哪些原型只应作为辅助面存在，哪些必须独立成面？
- Interrupt / Batch / Silent 分别会把人导向哪个面？
- 用户如何在主工作面、状态面、接管面和审计面之间切换，而不丢对象连续性？
- 哪些对象必须跨 surface 保持同一个 ID，而不是被重新包装？

### 建议输出

- surface system map
- prototype-to-surface mapping
- re-entry flow
- wake-up path by mode
- state visibility model
- memory / audit model
- object continuity rules

---

## B9. Evaluation

### 至少拆成四类

#### 1. Adoption
- 用户敢不敢把真实任务放进来？
- 真实任务迁入率如何？

#### 2. Control
- 用户是否知道系统当前状态？
- 是否知道何时介入、如何接管、如何纠错？

#### 3. Quality / Safety
- 结果质量如何？
- 误触发、误升级、误执行、漏升级的代价如何？

#### 4. Learning
- 系统是否在变得更稳，而不是更复杂？
- 团队是否在积累能被下一轮 rollout 利用的知识？

### 建议输出

- metrics tree
- adoption metrics
- control metrics
- quality / safety metrics
- learning metrics
- review cadence

---

## B10. Rollout Ladder

### 不同 autonomy 级别应分阶段放开

- Suggest-only
- Supervised execution
- Bounded autonomy
- Default execution within bounds
- Human governance over autonomous loops

### 要回答的问题

- 当前阶段适合哪一级 rollout？
- 哪些信号允许升级？
- 哪些失败信号必须降级？
- 哪些功能必须先在 shadow mode 里跑？

### 建议输出

- rollout ladder
- promotion criteria
- demotion criteria
- shadow mode plan

---

## B11. Iteration / Learning Loop

### Evaluation 之后不应结束
而要明确：

- 哪些信号触发回到 Vision / Doctrine？
- 哪些信号触发重做 Problem Framing？
- 哪些信号说明 collaboration allocation 错了？
- 哪些信号说明不是 UX 问题，而是 capability fit 根本不成立？
- 哪些信号说明需要降低 autonomy，而不是增加功能？

### 建议输出

- learning loop
- trigger-to-revisit map
- iteration priorities

---

# Part 4. 不同产品形态的分叉重点

> 这不是四套不同方法，而是同一框架在不同环境约束下的分支。
> `Target A` 仍然是方向判别，`Target B` 仍然是结构收束；下面的分支只是在不同环境里强调不同的判断重点与收束重点，而不是重定义 A / B。

---

## 1. 手机 agentOS

### A 阶段更该判断
- 问题是不是跨 app 连续性与 re-entry friction
- 是不是系统级入口而不是单 app feature
- 是否需要长期偏好与上下文延续
- 是否真的需要 agent，而不是更好的集成和自动化

### B 阶段更该收束
- orchestration / triage / personal context thread
- 通知洪水下的 attention policy
- 权限、授权窗口、re-entry surface
- durable state 的边界与回滚

### 典型协作单元
- intent
- task run
- pending approval
- personal context thread

---

## 2. PC / Workbench

### A 阶段更该判断
- 痛点是不是长任务推进、多工具碎片化、审查成本过高
- 更适合 co-creation、triage 还是 orchestration

### B 阶段更该收束
- work item / run / decision object / artifact section
- review burden 与 evidence traceability
- 主工作面、审计面、run view 的关系

### 典型协作单元
- work item
- decision object
- run
- artifact section

---

## 3. 车内 agentOS（非辅助驾驶）

### A 阶段更该判断
- 问题是不是低注意力条件下的服务编排与旅程连续性
- 是不是值得上升为系统级协作形态

### B 阶段更该收束
- supervision + clarification + 轻量 orchestration
- 语音 + glanceable UI
- 低打扰、可中断、可恢复
- 服务 handoff 与 trip state continuity

### 典型协作单元
- trip state
- cabin intent
- service handoff
- route / interruption event

---

## 4. 辅助驾驶 / 安全关键系统

### A 阶段更该判断
- 问题是不是 mode awareness、takeover、trust calibration、risk visibility
- 风险和责任是否允许某种 autonomy

### B 阶段更该收束
- supervision / exception handoff
- deterministic interrupt
- takeover object / anomaly object
- durable state / incident trace
- 安全召回与接管路径

### 典型协作单元
- mode state
- anomaly
- takeover request
- safety boundary event

### 关键提醒
- 这里通常不是 chat-first
- 也不该默认用 decision card 统一表达全部 handoff

---

# Part 5. Project Thinking Canvas

## A. 方向判别画布

### 1. Vision / Doctrine
- 我们要把用户带向什么关系？
- 哪些原则不可妥协？

### 2. Why Now / Capability Fit
- 为什么是现在？
- 为什么不是更简单的 workflow / UI / integration？

### 3. Problem Framing
- 用户问题是什么？
- 第一用户是谁？
- goals / non-goals 是什么？

### 4. Operating Environment / Stakes
- 风险、可逆性、注意力、权限、责任、模态限制是什么？

### 5. Problem-Solving Flow（粗粒度）
- 产品覆盖哪几段？
- first wedge 切哪段？

### 6. Direction Decision
- Go / Go but narrow / Hold / Pivot
- 最大假设、最大风险、最大证据缺口是什么？

---

## B. 结构收束画布

### 1. Flow Decomposition
- 流程如何细化？
- 执行、监控、纠偏、升级如何发生？

### 2. Collaboration Allocation
- 每一段里谁主导、谁知情、谁审批、谁接管？

### 3. Collaboration Prototype & Unit
- 当前是 clarification / co-creation / triage / supervision / orchestration 中的哪种或哪种组合？
- 最小协作单元是什么？

### 4. Interaction Prototypes
- 用户面对什么对象？
- agent 负责什么？
- handoff object 是哪一类？

### 5. Handoff & Human Intervention
- 采用何种人介入模式？
- 触发人进入的机制是什么？

### 6. Attention Budget & Modality
- 什么 interrupt / batch / silent？
- 用何种模态触达？

### 7. Durable State / Memory
- 什么可沉淀？
- 什么只能停留在 working hypothesis？

### 8. Surface System
- 主工作面、re-entry 面、状态面、审计面分别是什么？
- 对象如何跨面保持连续？

### 9. Evaluation & Rollout
- 如何衡量成立？
- autonomy 如何逐步放开？

---

# Part 6. Working Ledger（建议全流程保留）

## 推荐标签

- FACT
- ASSUMPTION
- OPEN QUESTION
- DECISION
- RISK
- CONFLICT
- TODO RESEARCH

## 使用原则

- 事实与假设必须显式分开
- 分歧不能被悄悄抹平
- 每个决策都要保留 rationale
- 每个 durable write 都要带 provenance
- 任何跨层矛盾都要单独成表，不允许“边聊边吞掉”

---

# Part 7. 常见误区

## 1. 太早讨论 surface
还没明确协作结构，就开始争论 chat / inbox / cockpit。

## 2. 把自动化程度当核心问题
真正的问题是：**谁在什么节点拥有哪种权力与责任**。

## 3. 把 AI fit 当成默认成立
很多问题更适合 workflow-first，而不是 agent-first。

## 4. 把 Decision Card 误当全局主角
它只是 Triage 原型里的典型 handoff object。

## 5. 把 Evaluation 写成终点
Evaluation 更重要的作用，是决定该回退到哪一层重构。

---

# 一句话定义

这份框架不是为了把每个项目都做成 agent。

它真正的作用是：

> **帮助团队先判断一个方向是否值得成立，再把成立的方向收束成一套不会自相矛盾的人机协作产品结构。**
