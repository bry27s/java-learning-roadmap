# Git 常用命令与工作流（最常用的那 20%）

## 一、初始化与克隆

- 克隆：`git clone <url>`
- 初始化：`git init`
- 查看状态：`git status`

## 二、提交（最常用）

- 暂存：`git add .` 或 `git add <file>`
- 提交：`git commit -m "feat: ..."`
- 查看历史：`git log --oneline --decorate --graph --all`

## 三、分支

- 查看分支：`git branch`
- 新建并切换：`git checkout -b feature/week1`
- 切换：`git checkout main`
- 合并：`git merge feature/week1`

## 四、远程与推送

- 添加远程：`git remote add origin <url>`
- 查看远程：`git remote -v`
- 推送：`git push -u origin main`
- 拉取：`git pull`

## 五、PR（Pull Request）推荐流程

1. `git checkout -b feat/something`
2. 小步 commit（每个 commit 只做一件事）
3. `git push -u origin feat/something`
4. 在 GitHub 发起 PR → 自检 → 合并

## 六、最常见问题

- 提交信息写错：
  - 还没 push：`git commit --amend`
  - 已 push：建议新提交修正（避免强推）
- 想撤销本地修改：
  - 丢弃未暂存：`git restore <file>`
  - 取消暂存：`git restore --staged <file>`
