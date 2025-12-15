# Maven 基础（够你把项目跑起来 + 写测试）

## 1) Maven 解决什么问题？

- 依赖管理：自动下载 jar
- 统一构建：编译、测试、打包
- 约定目录：`src/main/java`、`src/test/java`

## 2) 常用命令

- 运行测试：`mvn test`
- 打包：`mvn package`
- 清理：`mvn clean`
- 清理 + 测试：`mvn clean test`

## 3) 依赖（dependencies）

- 写在 `pom.xml` 里
- 常见 scope：
  - 默认（compile）：编译/运行都需要
  - `test`：只在测试阶段需要（例如 JUnit）

## 4) 生命周期（非常重要的面试点）

- `validate` → `compile` → `test` → `package` → `verify` → `install` → `deploy`

你输入 `mvn test`，Maven 会自动执行它依赖的前置阶段（compile 等）。

## 5) 插件（plugins）

- Surefire：跑单测（JUnit5）
- Exec：运行 main 方法（控制台项目很方便）

## 6) 常见坑

- Java 版本不一致：确保 `maven.compiler.release` 与本机 JDK 一致
- 依赖下载慢：可配置镜像（后续再做）
