<p align="center">
  <img src="assets/readme-banner.svg" alt="Repo Context Pack banner" width="100%">
</p>

<h1 align="center">Repo Context Pack</h1>

<p align="center">从 README、AGENTS.md、prompt 和包元数据生成小而可审阅的仓库上下文包。</p>

<p align="center"><a href="README.md">English</a> · <a href="#快速开始">快速开始</a> · <a href="#检查项">检查项</a></p>

<p align="center">
  <img alt="Node.js" src="https://img.shields.io/badge/node-%3E%3D18-22C55E">
  <img alt="dependencies" src="https://img.shields.io/badge/dependencies-0-111827">
  <img alt="license" src="https://img.shields.io/badge/license-MIT-2563EB">
</p>

<p align="center">
  <img src="assets/cli-preview.svg" alt="Repo Context Pack CLI preview" width="88%">
</p>

## 为什么做这个

AI Agent 工具链正在快速增长，但很多仓库缺少能直接放进 CI 或本地预检的小工具。这个项目保持零依赖、命令短、输出清楚，适合被收藏、fork、二次改造。

## 快速开始

```bash
npx github:aolingge/repo-context-pack --path README.md --markdown
```

Generate Markdown:

```bash
npx github:aolingge/repo-context-pack --path README.md --markdown --markdown > report.md
```

Use a score gate:

```bash
npx github:aolingge/repo-context-pack --path README.md --markdown --min-score 80
```

## 检查项

| Check | What it looks for |
| --- | --- |
| readme | Includes README or quick start material. |
| agents | Includes agent instructions. |
| commands | Includes verification commands. |
| boundaries | Includes privacy boundary. |

## Output

```text
Repo Context Pack score: 100/100
PASS  example-check  Useful signal found
FAIL  missing-check  Add the missing guidance
```

## 参与贡献

Good first PRs: add checks, add fixtures, improve docs, or add GitHub Actions examples.

## License

MIT


## Quality Gate

Use this project as a repeatable gate before an AI agent marks work as done:

- [Quality gate guide](docs/quality-gates.md)
- [Copy-ready GitHub Actions example](examples/github-action.yml)

