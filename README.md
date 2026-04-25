<p align="center">
  <img src="assets/readme-banner.svg" alt="Repo Context Pack banner" width="100%">
</p>

<h1 align="center">Repo Context Pack</h1>

<p align="center">Create a small, reviewable context pack from README, AGENTS.md, prompts, and package metadata.</p>

<p align="center"><a href="README.zh-CN.md">中文</a> · <a href="#quick-start">Quick Start</a> · <a href="#checks">Checks</a></p>

<p align="center">
  <img alt="Node.js" src="https://img.shields.io/badge/node-%3E%3D18-22C55E">
  <img alt="dependencies" src="https://img.shields.io/badge/dependencies-0-111827">
  <img alt="license" src="https://img.shields.io/badge/license-MIT-2563EB">
</p>

## Why This Exists

AI agent tooling is growing quickly, but many repos still miss tiny checks that can run locally or in CI. This project stays zero-dependency, short-command, and easy to fork.

## Quick Start

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

## Checks

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

## Contributing

Good first PRs: add checks, add fixtures, improve docs, or add GitHub Actions examples.

## License

MIT
