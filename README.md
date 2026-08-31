# 🔑 keyvault (金钥匙) — 官方版本发布与下载中心

<p align="center">
  <strong>专为 AI 时代打造的本地凭据保险库与 MCP 代理安全中枢</strong><br>
  <em>AI 用得到、看不到 · 零泄漏风险 · 隐私绝对可控</em>
</p>

<p align="center">
  <a href="https://github.com/tracy115-ops/keyvault-release/releases"><img src="https://img.shields.io/github/v/release/tracy115-ops/keyvault-release?color=7287fd&logo=github&label=最新版本" alt="Latest Release"></a>
  <img src="https://img.shields.io/badge/Platform-Windows%20x64-blue?logo=windows" alt="Platform">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
</p>

---

## 📥 安装包下载 (Downloads)

请前往右侧 👉 **[Releases 官方版本发布页面](https://github.com/tracy115-ops/keyvault-release/releases)** 获取最新版本的安装包：

| 产物名称 | 文件类型 | 适用场景 |
| :--- | :--- | :--- |
| **`keyvault_x.x.x_x64-setup.exe`** | NSIS 安装程序 **(推荐)** | 个人电脑快捷安装，支持桌面快捷方式与系统托盘常驻 |
| **`keyvault_x.x.x_x64_en-US.msi`** | Windows MSI 企业安装包 | 企业批量部署与静默安装 |
| **`keyvault-cli-vx.x.x-windows-x64.zip`** | 独立 CLI 压缩包 | 包含 `kv.exe` 终端命令行工具，适合脚本与服务器环境 |

---

## ✨ 核心特性

- 🔒 **军工级本地加密**：主密码 Argon2id + 硬件钥匙串 (DPAPI / Keychain) + 数据库 AES-256-GCM 强加密。
- 🛡️ **3 层智能脱敏过滤**：
  1. 精确值匹配脱敏；
  2. 60+ 类常见高危 Token/Key 模式扫描；
  3. 统计高熵特征值探测（Shannon Entropy 拦截未知高危密钥）。
- 🛑 **AI 紧急熔断与防御规则**：高危写操作与系统命令拦截，一键开启物理熔断隔绝所有 AI 访问。
- 🔌 **原生 MCP 协议支持**：完美支持 Claude Desktop, Cursor, Zed, Windsurf, Cline 等主流 AI 开发工具。
- 🧰 **开发者安全工具箱**：内置 2FA 动态验证码生成、SSH 密钥对生成 (Ed25519 / RSA)、JWT 离线验签、数据库连接串脱敏、.env 模板生成、Cron 表达式自然语言预测等 9 大实用工具。

---

## 🚀 快速上手

### 1. 桌面端 (GUI)
1. 下载并运行 `keyvault_x.x.x_x64-setup.exe`；
2. 首次启动时设置您的专属主密码（初始化金库）；
3. 在「MCP 服务控制台」一键复制配置代码，粘贴至 Claude 或 Cursor 的配置文件中即可立即开始使用。

### 2. 命令行工具 (CLI)
解压 `keyvault-cli-vx.x.x-windows-x64.zip`，将 `kv.exe` 加入系统环境变量 `PATH`：

```bash
# 查看金库状态
kv status

# 列出凭证
kv list

# 启动 MCP 标准 Stdio 代理
kv mcp serve
```

---

<p align="center">
  <sub>© 2026 keyvault (金钥匙). All rights reserved.</sub>
</p>
