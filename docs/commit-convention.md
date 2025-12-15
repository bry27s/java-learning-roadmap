# Commit Message 规范（建议）

目标：让 commit 历史成为你的学习轨迹。

## 1) 推荐格式

使用：`type: summary`

- `feat:` 新功能/新知识点落地（代码或文档）
- `fix:` 修 bug
- `docs:` 文档
- `refactor:` 重构（不改变外部行为）
- `test:` 测试
- `chore:` 构建/脚手架/杂项

## 2) 推荐写法

- summary 用动词开头：`add/implement/update/remove`
- 一次 commit 做一件事（粒度小）
- 例子：
  - `feat: implement student update and delete`
  - `test: cover duplicate id and not-found cases`
  - `docs: add week-01 retrospective`

## 3) 学习轨迹建议

- 每天至少 1 个 commit（哪怕只改文档/加一个测试）
- 每次 commit 前先跑：测试/编译（能跑再提交）
- 重要节点打 tag：
  - `git tag v1.0` → `git push --tags`
