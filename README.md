# TrumanCode

**TrumanCode** is a Codex/Claude skill for forcing AI work out of stale training-data assumptions and into the real world.

It emphasizes multi-pass web research, current open-source repository inspection, official documentation checks, and rigorous project questioning before technical decisions are made.

## Why This Exists

Modern AI assistants can sound confident while relying on old knowledge. TrumanCode gives the assistant a repeatable habit:

1. Look outside the model.
2. Check current docs and real repositories.
3. Compare what maintained projects actually do.
4. Challenge weak product and architecture assumptions.
5. Ask for confirmation before pivoting, implementing, shipping, or closing.

The name comes from the "Truman" idea: leave the artificial studio and see the real world.

## What It Is Good For

- 2026-era framework, model, SDK, and component-library selection
- open-source implementation research
- product and architecture planning
- AI agent/backend/frontend stack decisions
- commercial-use license checks
- comparing current open-source and closed-source options
- reviewing whether a project direction is still valid
- forcing a confirmation gate before major project transitions

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
帮我选 2026 年最适合做 AI agent 后台的开源框架和组件库，要能商业化。
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

## Skill Behavior

When triggered, TrumanCode asks the assistant to:

- run multi-pass current research when freshness matters
- inspect official docs and real open-source repositories
- compare ecosystem signals instead of trusting one source
- challenge product, interaction, algorithm, and architecture assumptions
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
- requires current research for 2026 technical choices

## License

MIT
