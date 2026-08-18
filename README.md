# Wanbinyu Harness 工具箱

[简体中文](README.md) | [English](README.en.md)

[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（`dsh`）的独立第三方插件与配套工具索引。

> [!IMPORTANT]
> 本工具箱由 [Wanbinyu](https://github.com/Wanbinyu) 独立维护，不是 DeepSeek 官方项目，也不代表 DeepSeek 官方提供支持、认证或安全保证。收录项目请以各自仓库的 README、版本和许可证为准。

## 插件 Bundle

下列项目提供 `package.json` 中的 `dsh.bundle.patch`，并附带 `cordis.patch.yml`，可以通过 Harness profile 的插件流程安装：

| 项目 | 功能 | 兼容性 | 安装 |
| --- | --- | --- | --- |
| [dsh-billing](https://github.com/Wanbinyu/dsh-billing) | 按 provider/model 统计费用、会话额度和 Web 费用条。 | Harness `0.1.0-rc.x` | `dsh plugin --profile web add github:Wanbinyu/dsh-billing` |
| [dsh-plugin-git-inspect](https://github.com/Wanbinyu/dsh-plugin-git-inspect) | 提供只读的 Git 状态、diff、摘要、提交、历史和 refs 工具。 | Harness `0.1.0-rc.x`；Node.js `>=22.19.0` | `dsh plugin --profile web add github:Wanbinyu/dsh-plugin-git-inspect` |

## 配套工具

| 项目 | 类型 | 功能 | 使用 |
| --- | --- | --- | --- |
| [dsh-launcher](https://github.com/Wanbinyu/dsh-launcher) | Windows CLI 工具 | 用 `dsh` 或 `deepseek` 快捷启动 Harness Web profile 并打开浏览器。 | 下载并运行 [`dsh-launcher-setup.exe`](https://github.com/Wanbinyu/dsh-launcher/releases/download/v0.3.4/dsh-launcher-setup.exe)。 |

启动器不是 Cordis 插件，也不需要 `cordis.yml` 或 `dsh.bundle`。把它单列可以避免将“能扩展 Harness 的插件”和“帮助启动 Harness 的工具”混为一谈。

## 收录与核验标准

目录中的 `plugins.json` 提供机器可读数据。可以运行 `npm run verify` 自动检查公开仓库、版本、bundle 清单、patch 文件、README 安装说明和 launcher Release 资产。对于可声明为 bundle 的项目，至少核对以下内容：

- `package.json` 包含 `dsh.bundle.patch`，且指向仓库内的 patch 文件。
- patch 文件能插入仓库实际提供的插件包，并写明所需配置。
- README 写明 Harness 兼容版本、运行时要求、安装方法和项目边界。
- 安装路径可复现，许可证和 Issue 入口清晰。

`lastVerified`、`latestVersion`、`releaseUrl` 和 `verificationStatus` 用于让客户端判断目录信息的新鲜度；它们不是 DeepSeek 官方认证标记。

普通插件也可以由宿主项目安装为依赖，再由用户自己的 `cordis.patch.yml` 手动组合；这种项目应明确标记为手动组合，而不是声称支持 `dsh plugin ... add`。

## 找到更多项目

可以在 GitHub 搜索 [`dsh-plugin`](https://github.com/topics/dsh-plugin) 话题，但话题本身不等于插件资格。收录前请检查 bundle 清单、安装路径和 README，不要只按仓库名称或 star 数判断。

官方讨论入口：[DeepSeek Harness Discussions](https://github.com/deepseek-ai/deepseek-harness/discussions)。本目录的展示帖：[Discussion #1045](https://github.com/deepseek-ai/deepseek-harness/discussions/1045)。

## 许可证

目录采用 MIT 许可证；收录项目分别遵循各自仓库的许可证。

## 语言

- [English README](README.en.md)
