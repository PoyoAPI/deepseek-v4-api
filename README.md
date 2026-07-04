# DeepSeek V4 API Examples for PoYo

[![Model page](https://img.shields.io/badge/Model%20page-deepseek--v4--api-84cc16)](https://poyo.ai/models/deepseek-v4-flash)
[![API docs](https://img.shields.io/badge/API%20docs-docs.poyo.ai-22d3ee)](https://docs.poyo.ai/api-manual/chat-series/chat-completions)
[![License: MIT](https://img.shields.io/badge/License-MIT-111827)](LICENSE)
[![Main examples](https://img.shields.io/badge/Main%20examples-PoyoAPI%2Fpoyo--examples-0f172a?logo=github)](https://github.com/PoyoAPI/poyo-examples)

Focused server-side examples for building with DeepSeek V4 Flash and Pro on PoYo.

DeepSeek V4 is useful when you need cost-aware coding, reasoning, summarization, and assistant workflows with a fast default path and a stronger pro option.

[Model Page](https://poyo.ai/models/deepseek-v4-flash) | [Docs](https://docs.poyo.ai/api-manual/chat-series/chat-completions) | [Get API Key](https://poyo.ai/dashboard/api-key) | [Pricing](https://poyo.ai/pricing) | [Main Examples](https://github.com/PoyoAPI/poyo-examples)

## What This Repo Covers

- Chat completions with `deepseek-v4-flash`
- Upgrade path to `deepseek-v4-pro`
- OpenAI-style `/v1/chat/completions` requests
- Node.js backend example
- Prompt examples and production integration notes

## Quick Start

```bash
cp .env.example .env
export POYO_API_KEY="your-api-key"
```

Run the Node.js example:

```bash
cd node
npm start
```

Keep `POYO_API_KEY` on the server. Do not expose it in browser code, mobile apps, screenshots, or public logs.

## Production Pattern

- Keep `POYO_API_KEY` on the server
- Send a chat completion request
- Log model, latency, and usage for cost tracking
- Add retries around network failures, not around every model response

## Models

This repo uses `deepseek-v4-flash`, `deepseek-v4-pro`.

## Examples

| Path | What it covers |
| --- | --- |
| [`curl/generate.md`](curl/generate.md) | Copy-paste API request. |
| [`node/`](node/) | Native Node.js backend example. |
| [`docs/prompt-examples.md`](docs/prompt-examples.md) | Practical prompts for product workflows and creative tests. |
| [`docs/production-notes.md`](docs/production-notes.md) | Security and reliability notes before launch. |

## Run Checks

```bash
make check
```

On Windows:

```powershell
./scripts/check.ps1
```

## License

MIT
