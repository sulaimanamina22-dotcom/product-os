# Product OS

A three-agent AI system that **validates a product idea, builds it, and takes it to market**. It has judged 80+ ideas so far: most were killed at the validation gate, and the ones that passed were built and smoke-tested with real landing pages.

## The agents

| Agent | Job | Method | Files |
|---|---|---|---|
| 1. Idea Originator & Validator | Decides PASS or KILL on an idea using real evidence of demand, novelty and a wedge into the market | Research gate with an evidence schema and a self-suggestion guard | `agents/idea-originator-validator.md`, `workflows/validate-idea.md` |
| 2. Build & Protect | Designs and builds the product | Seven-lens review panel (UX, engineering, security, reliability and more), then implementation and checks | `agents/build-and-protect.md`, `workflows/scope-build.md` |
| 3. Go to Market | Finds customers | Stage / market / awareness diagnostic, positioning, channels and measurement | `agents/go-to-market.md`, `workflows/go-to-market.md` |

A shared **demand test** workflow (`workflows/test-demand.md`) uses all three: Agent 1 owns the evidence, Agent 2 the experience, Agent 3 the offer and channel.

## How it works

```
Idea  ->  Validate (PASS / KILL)  ->  Scope & build  ->  Demand test  ->  Go to market
```

- **Read first, write back.** Every run starts by reading `memory/principles.md` (the operating law) and the project's state, decisions and open questions, then updates them at the end.
- **Per-project memory.** Each product gets its own `state.md`, `decisions.md` and `questions.md` (see `memory/projects/_TEMPLATE/`).
- **Honest records.** Planned, built, verified, deployed and observed results are recorded separately, so the system never claims more than it did.

## Run it

```bash
cd product-os
claude
```

Then say "Assess this idea", "Design and build this", "Prepare a smoke test" or "Get this product customers".

It also works as a Project in Claude, ChatGPT, Gemini, Kimi or DeepSeek: load `CLAUDE.md`, `agents/` and `workflows/` as project files.

## Related

- [Idea OS](https://github.com/sulaimanamina22-dotcom/idea-os) generates the ideas this OS validates.
- [FringeBoard](https://www.fringeboard.com/) is a live SaaS built with the same approach.

*Project records, outputs and test sites are kept private and not included.*
