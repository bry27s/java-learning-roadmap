# Java 学习环境配置指南（Windows）

本文档记录 bry27s 的 Java 学习环境完整配置步骤，方便在新电脑上快速复现开发环境。

---

## 环境清单

| 工具 | 版本 | 用途 |
|------|------|------|
| JDK | 17+ (当前使用 25) | Java 运行时 |
| Git | 2.52+ | 版本控制 |
| Maven Daemon (mvnd) | 1.0.3+ | 构建工具（Maven 加速版） |
| VS Code (可选) | 最新版 | 代码编辑器 |

---

## 1. 安装 JDK

### 1.1 下载安装
- **推荐**：Oracle JDK 17 或 OpenJDK (Temurin)
  - Oracle JDK: https://www.oracle.com/java/technologies/downloads/#java17
  - Temurin (推荐): https://adoptium.net/temurin/releases/?version=17
- 安装时**勾选"添加到 PATH"**，或安装后手动配置环境变量

### 1.2 配置环境变量（如果未自动添加）
1. 右键"此电脑" → 属性 → 高级系统设置 → 环境变量
2. 新建系统变量：
   - 变量名：`JAVA_HOME`
   - 变量值：JDK 安装路径（例如 `C:\Program Files\Java\jdk-17`）
3. 编辑系统变量 `Path`，新增：`%JAVA_HOME%\bin`

### 1.3 验证安装
```powershell
java -version
```
应输出类似：
```
java version "17.0.x" ...
```

---

## 2. 安装 Git

### 2.1 下载安装
- 官网：https://git-scm.com/download/win
- 安装过程：
  - 选择"Git from the command line and also from 3rd-party software"
  - 其他选项保持默认即可

### 2.2 配置 Git 用户身份（必须）
```powershell
git config --global user.name "bry"
git config --global user.email "1740444512@qq.com"
```

### 2.3 配置代理（如果网络受限）
```powershell
# 替换端口为你的代理端口（例如 Clash 默认 7890）
git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890
```

**取消代理**（切换网络后）：
```powershell
git config --global --unset http.proxy
git config --global --unset https.proxy
```

### 2.4 配置 HTTP/1.1（避免某些网络环境下连接重置）
```powershell
git config --global http.version HTTP/1.1
```

### 2.5 验证安装
```powershell
git --version
git config --list
```

---

## 3. 安装 Maven Daemon (mvnd)

### 3.1 下载
- 官网：https://github.com/apache/maven-mvnd/releases
- 下载：`maven-mvnd-1.0.3-windows-amd64.zip`（或更新版本）

### 3.2 解压并配置 PATH
1. 解压到任意目录（例如 `D:\Download\maven-mvnd-1.0.3-windows-amd64`）
2. 添加环境变量（PowerShell 执行）：
   ```powershell
   $mvndPath = "D:\Download\maven-mvnd-1.0.3-windows-amd64\bin"
   $currentPath = [Environment]::GetEnvironmentVariable("Path", "User")
   [Environment]::SetEnvironmentVariable("Path", "$currentPath;$mvndPath", "User")
   ```
3. 重启 PowerShell 或 VS Code

### 3.3 配置 JAVA_HOME（可选，避免每次自动查找）
```powershell
# 设置系统环境变量 JAVA_HOME（如果第 1 步没做）
[Environment]::SetEnvironmentVariable("JAVA_HOME", "C:\Program Files\Java\jdk-17", "User")
```

### 3.4 验证安装
```powershell
mvnd -v
```
应输出类似：
```
Apache Maven Daemon (mvnd) 1.0.3 ...
Apache Maven 3.9.x
Java version: 17.0.x
```

---

## 4. 克隆项目到本地

### 4.1 创建工作目录
```powershell
# 建议统一放在一个目录下
mkdir D:\Desktop\Javalearn
cd D:\Desktop\Javalearn
```

### 4.2 克隆两个仓库
```powershell
# 克隆学生管理系统（代码项目）
git clone https://github.com/bry27s/java-student-management.git

# 克隆学习路线（笔记文档）
git clone https://github.com/bry27s/java-learning-roadmap.git
```

### 4.3 验证项目可运行
```powershell
cd D:\Desktop\Javalearn\java-student-management

# 运行单元测试（验证编译通过）
mvnd clean test

# 运行控制台程序（体验功能）
mvnd exec:java
```

如果测试通过，输出：
```
Tests run: 5, Failures: 0, Errors: 0, Skipped: 0
BUILD SUCCESS
```

---

## 5. VS Code 配置（可选但推荐）

### 5.1 安装 VS Code
- 官网：https://code.visualstudio.com/

### 5.2 安装扩展
在 VS Code 中搜索并安装以下扩展：
- **Extension Pack for Java**（微软官方 Java 套件，包含调试、Maven、测试等）
- **GitLens** (可选，增强 Git 功能)

### 5.3 打开项目
```powershell
cd D:\Desktop\Javalearn\java-student-management
code .
```

---

## 6. 常见问题排查

### 6.1 `java` / `git` / `mvnd` 命令找不到
- 确认环境变量 `Path` 中包含对应的 `bin` 目录
- **重启终端或 VS Code**（环境变量修改后需要重启）

### 6.2 Git push 时 `Connection was reset`
- 配置代理（见 2.3）
- 或配置 HTTP/1.1（见 2.4）
- 或切换到手机热点/其他网络

### 6.3 GitHub 登录/认证
- 首次 `git push` 会弹出登录窗口（Git Credential Manager）
- 如果提示输入密码：需要使用 **Personal Access Token (PAT)**，不是 GitHub 账户密码
  - 生成 Token：GitHub → Settings → Developer settings → Personal access tokens → Generate new token (classic)
  - 勾选 `repo` 权限
  - 复制生成的 `ghp_xxx...` 字符串，粘贴到密码位置

### 6.4 Maven 下载依赖慢
- 国内可配置阿里云镜像（在 `~/.m2/settings.xml` 中添加）：
  ```xml
  <mirrors>
    <mirror>
      <id>aliyun</id>
      <mirrorOf>central</mirrorOf>
      <url>https://maven.aliyun.com/repository/public</url>
    </mirror>
  </mirrors>
  ```

---

## 7. 日常开发工作流

### 7.1 拉取最新代码
```powershell
cd D:\Desktop\Javalearn\java-student-management
git pull
```

### 7.2 修改代码后提交
```powershell
# 查看改动
git status

# 添加所有改动
git add .

# 提交（按规范写提交信息）
git commit -m "feat: add age filter validation"

# 推送到 GitHub
git push
```

### 7.3 运行测试
```powershell
mvnd test
```

### 7.4 运行程序
```powershell
mvnd exec:java
```

---

## 8. 快速验证清单（新环境必做）

安装完所有工具后，依次执行以下命令验证：

```powershell
# 1. 验证 Java
java -version

# 2. 验证 Git
git --version
git config --list

# 3. 验证 Maven
mvnd -v

# 4. 克隆项目
cd D:\Desktop\Javalearn
git clone https://github.com/bry27s/java-student-management.git
git clone https://github.com/bry27s/java-learning-roadmap.git

# 5. 验证项目可运行
cd java-student-management
mvnd clean test

# 看到 "BUILD SUCCESS" + "Tests run: 5, Failures: 0" 就 OK 了！
```

---

## 附录：环境变量一览表

| 变量名 | 变量值示例 | 说明 |
|--------|-----------|------|
| `JAVA_HOME` | `C:\Program Files\Java\jdk-17` | JDK 安装目录 |
| `Path` | 追加 `%JAVA_HOME%\bin` | Java 命令行 |
| `Path` | 追加 `D:\Download\maven-mvnd-1.0.3-windows-amd64\bin` | Maven 命令行 |
| `Path` | 追加 `C:\Program Files\Git\cmd` | Git 命令行（通常安装时自动添加） |

---

**配置完成后，建议把本文档 commit 到 `java-learning-roadmap` 仓库，方便随时查阅！**
