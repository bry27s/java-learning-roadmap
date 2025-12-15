# java-learning-roadmap

目标：用「项目驱动」方式完成 Java 就业导向学习，并且把学习轨迹沉淀成可复盘的文档 + 清晰的 commit 历史。

## 学习目标

- 3-4 月：能胜任实习的 Java 后端基础（JavaSE + Maven + JUnit + Git + 基础工程习惯）
- 7-8 月：秋招面试准备（Spring Boot + MySQL + Redis + 常见八股/项目表达）

## 学习方式（项目驱动）

- 以仓库 [java-student-management] 的迭代为主线：从控制台 JavaSE → 文件持久化 → Spring Boot REST → 数据库
- 每周固定节奏：
  - 周一：定目标
  - 周二~周五：推进任务 + 小步提交
  - 周末：复盘总结 + 补缺

## 仓库内容

- docs/：路线、Git/Maven/调试入门
- weekly-log/：每周周报模板（week-01.md 等）

## 如何使用

1. 先阅读路线：docs/roadmap-12-weeks.md
2. 每周复制一份模板：weekly-log/week-01.md → week-02.md ...
3. 每次学习结束写 3~10 行复盘（遇到的坑、学到的点、下次要做的事）

## Commit 规范建议

建议使用：
- `feat: ...` 新增学习内容/新增模块
- `fix: ...` 修正文档错误/修复代码
- `docs: ...` 文档
- `refactor: ...` 重构
- `test: ...` 测试
- `chore: ...` 杂项（初始化、脚本等）

示例：
- `docs: add week-01 learning log`
- `docs: summarize maven lifecycle and commands`
- `docs: add 12-week roadmap`
