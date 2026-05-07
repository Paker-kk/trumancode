# TrumanCode

**TrumanCode** is a Codex/Claude skill for forcing AI work out of stale training-data assumptions and into the real world.

It emphasizes always-on reality sync: read the current computer/session date, perform web research when freshness matters, inspect current open-source repositories, check official documentation, and ask rigorous Dario-style project questions before technical decisions are made.

## Why This Exists

Modern AI assistants can sound confident while relying on old knowledge. TrumanCode gives the assistant a repeatable habit:

1. Read the current date instead of hardcoding a year.
2. Look outside the model by default.
3. Check current docs and real repositories.
4. Compare what maintained projects actually do.
5. Challenge weak product and architecture assumptions like a strict Anthropic executive reviewer.
6. Ask for confirmation before pivoting, implementing, shipping, or closing.

The name comes from the "Truman" idea: leave the artificial studio and see the real world.

## What It Is Good For

- current-year framework, model, SDK, and component-library selection
- open-source implementation research
- product and architecture planning
- AI agent/backend/frontend stack decisions
- commercial-use license checks
- comparing current open-source and closed-source options
- reviewing whether a project direction is still valid
- forcing a confirmation gate before major project transitions
- pushing back on vague ideas until they become executable

## Install

Copy this folder into your Codex/Claude skills directory:

```powershell
Copy-Item -Recurse -Force .\trumancode C:\Users\ava\.agents\skills\trumancode
```

The required file is:

```text
trumancode/SKILL.md
```

## Usage Examples

Prompts that should trigger this skill:

```text
帮我选现在最适合做 AI agent 后台的开源框架和组件库，要能商业化。
```

```text
我们别用 React 了，改成 SvelteKit，然后数据库也换一下，你看着办。
```

```text
我想做一个 AI 简历优化 SaaS，帮我直接开始写前端。
```

```text
帮我同步一下现在 GitHub 上主流开源项目都是怎么实现这个功能的。
```

```text
你先别凭记忆回答，开眼看一下真实世界现在怎么做。
```

```text
这个方案今天还成立吗？帮我查最新代码库和官方文档。
```

## Skill Behavior

When triggered, TrumanCode asks the assistant to:

- run multi-pass current research when freshness matters
- read the current computer/session date as the freshness baseline
- trigger broadly for substantive conversations, not only explicit "latest" requests
- inspect official docs and real open-source repositories
- compare ecosystem signals instead of trusting one source
- challenge product, interaction, algorithm, and architecture assumptions with a strict, skeptical reviewer posture
- produce compact project briefs and recommendation summaries
- ask the user to confirm before major transitions

## Repository Layout

```text
trumancode/
├── SKILL.md
├── README.md
├── LICENSE
└── evals/
    └── evals.json
```

## Evaluation Prompts

The `evals/evals.json` file contains starter test prompts for checking whether the skill:

- pauses before vague implementation
- asks for confirmation before completion
- treats stack changes as a direction-change gate
- requires current research for current-year technical choices
- verifies that the assistant does not hardcode 2026 as a permanent rule

## License

MIT
