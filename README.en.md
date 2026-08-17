# Wanbinyu Harness Toolbox

[简体中文](README.md) | [English](README.en.md)

An independent third-party index of plugins and companion tools for [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) (`dsh`).

> [!IMPORTANT]
> This toolbox is maintained independently by [Wanbinyu](https://github.com/Wanbinyu). It is not an official DeepSeek project and is not supported, certified, or security-reviewed by DeepSeek. Refer to each project's README, release history, and license.

## Plugin Bundles

These projects provide `dsh.bundle.patch` in `package.json` and ship a `cordis.patch.yml`, so they can be installed through a Harness profile's plugin flow:

| Project | What it provides | Compatibility | Install |
| --- | --- | --- | --- |
| [dsh-billing](https://github.com/Wanbinyu/dsh-billing) | Per-provider/model cost accounting, session quota, and a Web cost strip. | Harness `0.1.0-rc.x` | `dsh plugin --profile web add github:Wanbinyu/dsh-billing` |
| [dsh-plugin-git-inspect](https://github.com/Wanbinyu/dsh-plugin-git-inspect) | Read-only Git status, diff, summary, commit, history, and refs tools. | Harness `0.1.0-rc.x`; Node.js `>=22.19.0` | `dsh plugin --profile web add github:Wanbinyu/dsh-plugin-git-inspect` |

## Companion Tools

| Project | Type | What it provides | Use |
| --- | --- | --- | --- |
| [dsh-launcher](https://github.com/Wanbinyu/dsh-launcher) | Windows CLI tool | Short `dsh` and `deepseek` commands for starting the Harness Web profile and opening the browser. | Download and run [`dsh-launcher-setup.exe`](https://github.com/Wanbinyu/dsh-launcher/releases/download/v0.2.0/dsh-launcher-setup.exe). |

The launcher is not a Cordis plugin and does not need `cordis.yml` or `dsh.bundle`. Keeping it separate avoids confusing Harness extensions with tools that help start Harness.

## Inclusion And Verification

The machine-readable catalog is [`plugins.json`](plugins.json). Run `npm run verify` to check public repositories, versions, bundle manifests, patch files, README installation instructions, and launcher Release assets. For projects classified as bundles, the minimum checks are:

- `package.json` contains `dsh.bundle.patch` and points to a patch file shipped in the repository.
- The patch inserts a plugin package actually provided by the repository and documents its configuration.
- The README states Harness compatibility, runtime requirements, installation steps, and project boundaries.
- The installation path is reproducible, with a clear license and issue tracker.

`lastVerified`, `latestVersion`, `releaseUrl`, and `verificationStatus` help clients judge catalog freshness; they are not an official DeepSeek certification.

A regular plugin can also be installed as a host dependency and composed by the user's own `cordis.patch.yml`. Such a project must be labeled as manual composition instead of claiming support for `dsh plugin ... add`.

## Finding More Projects

You can search the GitHub [`dsh-plugin`](https://github.com/topics/dsh-plugin) topic, but a topic is not proof that a repository is a plugin. Check the bundle manifest, installation path, and README instead of relying on a repository name or star count.

Official discussion entry point: [DeepSeek Harness Discussions](https://github.com/deepseek-ai/deepseek-harness/discussions). Catalog showcase: [Discussion #1045](https://github.com/deepseek-ai/deepseek-harness/discussions/1045).

## License

The catalog is released under the MIT License. Each listed project keeps its own license.

## Language

- [简体中文说明](README.md)
