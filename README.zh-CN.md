# DSH Plugins

[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)（`dsh`）社区插件与工具目录。

本目录由 [Wanbinyu](https://github.com/Wanbinyu) 独立维护，不代表 DeepSeek 官方。使用前请阅读各项目 README 中的兼容版本、安装方式和支持范围。

## 项目

| 项目 | 类型 | 功能 | 安装 / 使用 |
| --- | --- | --- | --- |
| [dsh-billing](https://github.com/Wanbinyu/dsh-billing) | Host + UI 插件 | 按模型统计费用、显示会话额度进度、支持货币定价，并在输入区显示费用条。 | 克隆仓库后，将 `packages/dsh-billing` 和 `packages/dsh-client-ui-billing` 安装到 profile。 |
| [dsh-mcp-lens](https://github.com/labmimors/dsh-mcp-lens) | Host 插件 | 把大型 MCP 工具库收缩成两个模型可见工具，适合长尾工具多、输入成本高的 Harness 场景。 | `dsh plugin --profile web add https://github.com/labmimors/dsh-mcp-lens/releases/download/v0.1.0-rc.6/dsh-mcp-lens-0.1.0-rc.6.tgz` |
| [dsh-plugin-git-inspect](https://github.com/Wanbinyu/dsh-plugin-git-inspect) | Host 插件 | 为 Agent 提供只读的 `git_status`、`git_diff` 和 `git_log` 工具。 | `npm install github:Wanbinyu/dsh-plugin-git-inspect` |
| [dsh-launcher](https://github.com/Wanbinyu/dsh-launcher) | Windows CLI 封装 | 用简短的 `dsh` 或 `deepseek` 命令启动 Harness Web profile 并打开浏览器。 | 克隆仓库后运行 `install.ps1`。 |

## 兼容性

| 项目 | 当前目标 |
| --- | --- |
| `dsh-billing` | DeepSeek Harness `0.1.0-rc.x`；构建包版本 `0.2.0` |
| `dsh-mcp-lens` | DeepSeek Harness `0.1.0-rc.6`；release `v0.1.0-rc.6`；Node.js `^22.19.0` 或 `>=24.0.0` |
| `dsh-plugin-git-inspect` | DeepSeek Harness `0.1.0-rc.x`；Node.js `>=22.19.0` |
| `dsh-launcher` | Windows PowerShell 5.1+；Node.js/npm 或 Harness 源码目录 |

机器可读目录见 [`plugins.json`](plugins.json)。

## 找到更多项目

可以在 GitHub 搜索 [`dsh-plugin`](https://github.com/topics/dsh-plugin) 话题。每个项目的版本发布、Issue 和支持范围以各自仓库为准。

## 贡献

收录项目应当具备公开 README、明确的兼容版本、开源许可证和可复现的安装方式。项目自身的问题和功能建议请提交到对应项目仓库。

DeepSeek Harness 目前处于开发预览阶段，官方暂不接受外部 Pull Request。社区插件可以通过 [GitHub Discussions](https://github.com/deepseek-ai/deepseek-harness/discussions) 和 [DeepSeek Harness Discord](https://discord.gg/Ycq5dCaS4) 分享。

## 许可证

本目录采用 MIT 许可证；收录项目分别遵循各自的许可证。
