# 12 周 Java 学习路线（就业导向）

原则：项目驱动 + 复盘驱动。每周产出：
- 1 次小项目迭代（能跑、能测）
- 1 份周报（weekly-log）
- 1~2 个面试表达点（可复用）

## Week 01：JavaSE 项目起步（控制台 + 分层）

- 目标：能写出分层清晰、可测试的控制台项目
- 关键词：类/接口、多态、异常、List/Map 基础
- 输出：`java-student-management` v1.0（CRUD + 排序/筛选 + JUnit）

## Week 02：集合与泛型、Stream 入门

- 目标：熟练 List/Map/Set + 泛型常见写法
- 输出：在项目里增加 2~3 个高级筛选（按名称模糊、按分数段）
- 补充：学习 `Comparator`、`stream().map/filter/sorted/collect`

## Week 03：IO 与持久化（CSV）

- 目标：掌握 BufferedReader/Writer、文件路径、异常处理
- 输出：实现 CSV 导入/导出（StudentCsvRepository）+ 单测

## Week 04：Maven 深入 + 测试完善

- 目标：熟悉依赖、生命周期、插件、测试分层
- 输出：更多 service 测试、增加边界条件覆盖

## Week 05：Spring Boot 入门（REST）

- 目标：控制台 → HTTP API，理解 Controller/Service/Repository
- 输出：把学生管理系统升级为 Spring Boot（只做最小 CRUD）

## Week 06：MySQL + JDBC/JPA 选一条路

- 目标：掌握表设计、CRUD、事务基础
- 输出：把 repository 换成数据库实现

## Week 07：Redis 入门

- 目标：理解缓存、过期、常用数据结构
- 输出：为“按 id 查询”加缓存（并说明一致性策略）

## Week 08：并发与线程池（结合场景）

- 目标：理解线程安全、锁、线程池
- 输出：在项目里做一个“批量导入”或“并发查询”实验并记录结论

## Week 09：Web 基础与常见中间件概念

- 目标：HTTP/JSON、日志、配置、分层、异常处理
- 输出：统一异常响应结构、日志规范（仅最小实现）

## Week 10：面试准备（核心八股 + 项目表达）

- 目标：整理集合/IO/并发/事务/缓存等面试表达
- 输出：每个主题 1 页 notes + 项目中的例子

## Week 11：系统设计小题（入门）

- 目标：会画基本架构图，能讲清楚缓存/一致性/扩展性
- 输出：对学生管理系统给出“演进路线图”

## Week 12：查漏补缺 + 模拟面试

- 目标：把“项目讲述”打磨到 3 分钟版本
- 输出：一份最终简历项目描述 + 常见追问清单
