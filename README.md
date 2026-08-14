# DSH Plugins

Community-maintained plugins and tools for [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) (`dsh`).

This is an independent catalog maintained by [Wanbinyu](https://github.com/Wanbinyu). It is not an official DeepSeek distribution. Check each project README for compatibility, installation details, and support scope.

## Projects

| Project | Type | What it provides | Install / use |
| --- | --- | --- | --- |
| [dsh-billing](https://github.com/Wanbinyu/dsh-billing) | Host + UI plugin | Per-model cost accounting, session quota progress, currency-aware pricing, and an optional composer cost strip. | Clone the repository and install `packages/dsh-billing` and `packages/dsh-client-ui-billing` into the profile. |
| [dsh-mcp-lens](https://github.com/labmimors/dsh-mcp-lens) | Host plugin | Shrinks large MCP catalogs to two model-facing tools, reducing standing schema bytes and input-heavy request cost for long-tail tool sets. | `dsh plugin --profile web add https://github.com/labmimors/dsh-mcp-lens/releases/download/v0.1.0-rc.6/dsh-mcp-lens-0.1.0-rc.6.tgz` |
| [dsh-plugin-git-inspect](https://github.com/Wanbinyu/dsh-plugin-git-inspect) | Host plugin | Read-only `git_status`, `git_diff`, and `git_log` tools for agent workflows. | `npm install github:Wanbinyu/dsh-plugin-git-inspect` |
| [dsh-launcher](https://github.com/Wanbinyu/dsh-launcher) | Windows CLI wrapper | Short `dsh` and `deepseek` commands that start the Harness Web profile and open the browser. | Clone the repository and run `install.ps1`. |

## Compatibility

| Project | Current target |
| --- | --- |
| `dsh-billing` | DeepSeek Harness `0.1.0-rc.x`; built package version `0.2.0` |
| `dsh-mcp-lens` | DeepSeek Harness `0.1.0-rc.6`; release `v0.1.0-rc.6`; Node.js `^22.19.0` or `>=24.0.0` |
| `dsh-plugin-git-inspect` | DeepSeek Harness `0.1.0-rc.x`; Node.js `>=22.19.0` |
| `dsh-launcher` | Windows PowerShell 5.1+; Node.js/npm or a Harness source checkout |

The catalog is also available as machine-readable data in [`plugins.json`](plugins.json).

## Discoverability

Search for the [`dsh-plugin`](https://github.com/topics/dsh-plugin) topic on GitHub. Individual projects own their release notes, issue trackers, and support policies.

## Contributing

Add a project only when it has a public README, a clear compatibility statement, an explicit license, and a reproducible installation path. Keep project-specific bugs and feature requests in the linked project repository.

DeepSeek Harness is in developer preview. The official project currently does not accept external pull requests; community plugins should remain independent and can be shared through [GitHub Discussions](https://github.com/deepseek-ai/deepseek-harness/discussions) and the [DeepSeek Harness Discord](https://discord.gg/Ycq5dCaS4).

## License

The catalog is released under the MIT License. Each listed project keeps its own license.
