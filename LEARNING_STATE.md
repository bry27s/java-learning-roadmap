# LEARNING_STATE.md (SSOT)

> **AI 使用说明（必须先读）**
>
> - AI 每次协助前，先读取：**1. Current Focus / 3. Progress Log / 7. Risks & Blockers / 9. Next Actions**，再决定今天推进什么。
> - AI 给建议必须落到：**今天能完成的 1–3 个具体动作**（包含命令/文件/验收标准）。
> - AI 写阶段性评语必须写进：**8. AI Coach Notes (Append Only)**，并引用证据（commit/PR/issues 链接或“已完成的功能说明”）。
> - 若 AI 建议调整学习计划，必须在：**2. Roadmap (Editable) → Change Log** 里**追加**一条变更记录（含日期/原因/影响）。

---

## 0. Profile（个人与目标）

| Item | Value |
|---|---|
| GitHub | [bry27s](https://github.com/bry27s) |
| 学历状态 | 研二 |
| 求职目标 | 研二下学期 **3–4 月找实习**；**7–8 月秋招冲刺** |
| 学习方式 | 项目驱动（就业导向），形成清晰 GitHub 学习轨迹（commit 历史清晰） |
| 每天学习时间 | 3–4 小时 |
| 当前基础（自评） | Java：继承/多态（已学）；集合/Map/Stream（不熟） |
| 工具基础（自评） | Git/IDEA 调试/Maven：不熟（需要纳入计划与训练） |
| 目标岗位画像（简版） | Java 后端实习：能做 Spring Boot CRUD + 基础数据库 + 有测试/工程习惯 |

**使用方式（你自己如何维护本文件）**

- 每天学习完：在 **3. Progress Log (Append Only)** 里**追加**一条记录（不改历史）。
- 每周一次：更新 **5. Skill Matrix** 的掌握程度与证据链接。
- 每完成一个里程碑：要求 AI 在 **8. AI Coach Notes (Append Only)** 写一条“就业导向评语”。

---

## 1. Current Focus（当前聚焦：我正在做什么）

| Focus Window | Current Goal | Definition of Done (DoD) |
|---|---|---|
| 本周（Week 01） | 完成 JavaSE 学生管理系统 v1.0 并建立学习节奏 | 能 `mvnd clean test` 通过；能 `mvnd exec:java` 运行；每天有 commit；完成 Week1 文档与复盘 |

**Today (可改)**

- 当前任务：
  - [ ] 跑通控制台程序并手动走一遍全流程（新增/查询/更新/删除/排序/筛选）
  - [ ] 读懂 repository 的 List+Map 一致性设计（能用 5 句话讲出来）
  - [ ] 写一条学习日志（追加到 3）

---

## 2. Roadmap (Editable)（可调整的 12 周路线，包含版本号与调整记录）

**Roadmap Version**: `v0.1`  
**Last Updated**: `2025-12-15`

### Plan (Weeks 1–12)

| Week Range | Theme | Deliverables (硬产出) | Evidence |
|---|---|---|---|
| Week 1–4 | JavaSE 项目（学生管理系统）+ Git + IDEA 调试 + Maven + JUnit + 集合/Map/Stream | `java-student-management`：从 v1.0 → v2.0（CSV 持久化/更强测试/更清晰的项目表达）；每周 1 份周报 | [repo](https://github.com/bry27s/java-student-management), [week logs](weekly-log/) |
| Week 5–9 | Spring Boot + MySQL 项目（REST API）+ Swagger + 分层 + 统一异常/校验 | Spring Boot CRUD 项目（可部署/可演示）；接口文档；测试（至少 service/controller 基础覆盖） | [TBD](#) |
| Week 10–12 | 项目增强（Redis/权限/性能）+ 面试冲刺（Java/数据库/Spring） | 项目增强点（缓存/权限/性能指标）；面试题库与项目追问清单 | [TBD](#) |

### Change Log (Append Only)

> 规则：这里**只追加**。任何调整必须记录：日期 / 变更点 / 原因 / 影响。

| Date | Change | Reason | Impact |
|---|---|---|---|
| 2025-12-15 | Create initial roadmap v0.1 | 初始化 SSOT | 形成固定节奏与可追踪路线 |

---

## 3. Progress Log (Append Only)（只追加的日志：每天/每周记录）

> **Append Only 规则（强制）**：本章节只允许**追加新记录**，不允许删改历史条目。
>
> 每条至少包含：Date / Time Spent / What I Built / What I Learned / Problems / Tomorrow Plan / Links

### Daily / Weekly Entries

| Date | Time Spent | What I Built | What I Learned | Problems | Tomorrow Plan | Links |
|---|---:|---|---|---|---|---|
| 2025-12-15 (Example) | 3h | 跑通 `java-student-management`；理解 ui→service→repo 分层 | List+Map 为什么同时维护；JUnit5 基本断言 | Maven 依赖下载慢（已用代理解决） | 手动走一遍菜单；补 1 个边界测试（非法 age/score） | [commit aa8083a](https://github.com/bry27s/java-student-management/commit/aa8083a) |

---

## 4. Project Portfolio（项目清单：每个项目的状态、链接、亮点、可讲点）

| Project | Status | Repo | What It Proves | Highlights (可讲点) | Next Upgrade |
|---|---|---|---|---|---|
| Java Student Management (Console) | Active | [java-student-management](https://github.com/bry27s/java-student-management) | 分层、接口抽象、异常、单测、集合/Map/Stream | List+Map 索引一致性；自定义异常；service 层单测；可扩展到 CSV/DB | CSV 持久化；更丰富筛选；更强测试覆盖；演进到 Spring Boot |
| Java Learning Roadmap (Docs) | Active | [java-learning-roadmap](https://github.com/bry27s/java-learning-roadmap) | 学习过程可复盘、可追踪 | 周报/路线/环境文档；commit 规范 | 持续更新 weekly-log 与技能矩阵 |

---

## 5. Skill Matrix（技能矩阵：掌握程度 + 证据链接）

> 级别建议：`0=不了解` / `1=能跟着写` / `2=能独立实现` / `3=能解释+排查问题` / `4=能优化/权衡`

| Skill | Level | Evidence (links) | Notes |
|---|---:|---|---|
| Java OOP（继承/多态/接口） | 2 | [StudentService interface](https://github.com/bry27s/java-student-management/blob/main/src/main/java/com/javalearn/studentmanagement/service/StudentService.java) | 能读懂并写简单接口实现 |
| Java Exceptions（自定义异常） | 2 | [exceptions](https://github.com/bry27s/java-student-management/tree/main/src/main/java/com/javalearn/studentmanagement/exception) | ui 层统一捕获并提示 |
| Collections（List/Map） | 1 | [InMemoryStudentRepository](https://github.com/bry27s/java-student-management/blob/main/src/main/java/com/javalearn/studentmanagement/repository/InMemoryStudentRepository.java) | 需要加强复杂度与一致性理解 |
| Stream/Comparator | 1 | [sort/filter in service](https://github.com/bry27s/java-student-management/blob/main/src/main/java/com/javalearn/studentmanagement/service/StudentServiceImpl.java) | 先能看懂，再自己手写一遍 |
| JUnit5 | 1 | [service tests](https://github.com/bry27s/java-student-management/blob/main/src/test/java/com/javalearn/studentmanagement/service/StudentServiceImplTest.java) | 需要练：边界测试/异常测试 |
| Maven（生命周期/依赖/插件） | 1 | [pom.xml](https://github.com/bry27s/java-student-management/blob/main/pom.xml) | 需要能解释 clean/test/package/exec |
| Git（分支/PR/日志） | 1 | [commit history](https://github.com/bry27s/java-student-management/commits/main) | 需要练分支与 PR 流程 |
| IDEA Debug | 1 | [debug notes](docs/intellij-debug.md) | 需要实践：断点、step into/out |

---

## 6. Interview Readiness（面试准备度：八股/项目追问/手撕）

| Area | Readiness | Evidence | Next |
|---|---:|---|---|
| 八股（Java 基础） | 1/5 | [interview notes](https://github.com/bry27s/java-student-management/blob/main/docs/interview-notes.md) | 以项目为锚：集合/Map/equals&hashCode/多态 |
| 项目讲述（3 分钟版本） | 1/5 | [Project Portfolio](#4-project-portfolio项目清单每个项目的状态链接亮点可讲点) | 练“问题→设计→实现→验证→可扩展”结构 |
| 手撕（基础算法/代码能力） | 0/5 | [TBD](#) | 每周 2 题：数组/字符串/哈希 |
| SQL/数据库 | 0/5 | [TBD](#) | Week 5+ 开始 |
| Spring | 0/5 | [TBD](#) | Week 5+ 开始 |

---

## 7. Risks & Blockers（风险与卡点：AI 要优先帮助解决）

| Risk/Blocker | Severity | Symptoms | Root Cause Hypothesis | Mitigation (Next) |
|---|---:|---|---|---|
| 集合/Map/Stream 不熟导致项目“能跑但讲不清” | High | 看懂但写不快；面试表达断裂 | 缺少刻意练习与复盘 | 每天 30min：手写 2 个小练习 + 写 5 句总结 |
| 工具链不熟（Maven/Git/Debug）影响效率 | High | 跑不通/卡认证/不会调试 | 缺少标准流程与模板 | 固化：`mvnd test` → debug → commit → push；每次写日志记录一次工具点 |
| commit 过大导致轨迹不清晰 | Medium | 1 个 commit 改太多 | 没拆任务/缺验收 | 以“可回滚的小步”为单位，1 commit = 1 事 |

---

## 8. AI Coach Notes (Append Only)（AI 教练评语：阶段性评价，只追加不覆盖）

> **Append Only 规则（强制）**：本章节只允许**追加新评语**，不允许删改历史条目。
> 
> 每当完成里程碑（例如：v1.0 可运行 + 关键测试通过），AI 必须新增一条评语并引用证据。

### Milestone Reviews

| Date | Milestone | Evidence |
|---|---|---|
| 2025-12-15 (Example) | 环境打通 + JavaSE 项目 v1.0 骨架可测 | [BUILD SUCCESS proof](#) / [repo](https://github.com/bry27s/java-student-management) |

#### 2025-12-15 (Example) — Milestone Review

| Field | Content |
|---|---|
| Summary | 完成两仓库初始化；学生管理系统实现分层 + CRUD + 基础排序/筛选 + 5 个 service 单测；能通过 `mvnd clean test` |
| Hireability Signal | 有可运行、可测试的工程；commit 轨迹开始形成；能把“分层/异常/测试/集合”落到代码 |
| Gaps | 对 List/Map 一致性、复杂度、Stream/Comparator 的表达还不顺；对 Maven 生命周期/插件不熟 |
| Next Upgrade Tasks | (1) 手写一遍 List+Map 索引一致性逻辑并解释；(2) 补 2 个边界单测；(3) 用 IDEA Debug 跟一次 `addStudent` → `save` 流程 |
| Resume Bullet Draft | - 实现控制台学生管理系统，采用 ui/service/repository 分层与接口抽象；\n- 使用 List+Map 建立 id 索引提升查询效率，并通过自定义异常统一错误处理；\n- 编写 JUnit5 单元测试覆盖核心 CRUD 场景，确保功能可回归 |
| Interview Q&A Prep | Q1：为什么同时用 List 和 Map？A：List 便于遍历排序，Map 提供按 id O(1) 查询，需保持一致性；\nQ2：为什么 service 层写单测？A：业务规则集中、无 UI/IO 依赖；\nQ3：如何演进到 Spring Boot？A：ui→controller；repo→DB；保留 service 逻辑与测试策略 |

---

## 9. Next Actions（下一步行动：可执行 TODO 列表，按优先级）

> 规则：这里允许编辑（完成后勾选/移动/替换），但尽量保持可执行与可验收。

### P0（今天/明天必须做）

- [ ] 跑通控制台菜单全流程，并截图/记录关键输出（写入 3 的日志 Links）
- [ ] 用 IDEA Debug 跟一次 `addStudent` 调用链（ui → service → repository）并记录观察点
- [ ] 新增 1–2 个边界单测（非法 age/score/gender）并确保 `mvnd test` 通过

### P1（本周完成）

- [ ] 补充 `docs/interview-notes.md`：把 List+Map 一致性和复杂度写成 5 句话
- [ ] 每天 1 条 Progress Log（Append Only）
- [ ] 每周周报：在 `weekly-log/week-01.md` 填完并 push

### P2（下周开始）

- [ ] Phase2: 设计 CSV 导入/导出接口（先写 TODO + 设计文档，再实现）
- [ ] 学会 Maven 生命周期：能解释 `clean/test/package/exec` 各阶段做什么
