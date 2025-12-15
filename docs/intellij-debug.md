# IntelliJ IDEA 调试入门

## 1) 打断点

- 在代码行号左侧点击 → 红点
- 以 Debug 方式运行（小虫子图标）

## 2) 常用按钮

- Step Over（F8）：执行下一行（不进入方法）
- Step Into（F7）：进入方法内部
- Step Out（Shift+F8）：跳出当前方法
- Resume（F9）：继续运行到下一个断点

## 3) 变量与表达式

- Variables：查看局部变量、字段
- Evaluate Expression（Alt+F8）：运行一段表达式（比如 `list.size()`）

## 4) 调试习惯（建议）

- 先用断点确认“输入是什么、关键变量是什么、分支走哪条”
- 遇到集合问题：重点看 size、元素内容、是否为空
- 遇到 Map 问题：重点看 key 是否一致（trim/大小写）
