# Building product with AI: overview

The companion to [Building an AI product](../playbook/00-overview.md). That playbook is about what you ship. This one is about how the team works when AI tools help you research, design, code and operate.

Same seven phases. Same sources. One golden rule throughout:

> **AI accelerates the typing. You still own the thinking, and a human is always accountable for what ships.**

## The evidence worth knowing first

DORA's research on AI-assisted development found something uncomfortable: AI makes individuals faster, but team delivery can get *less* stable at the same time. The cause is not the AI. It's that fast code generation tempts teams into big batches and thin review. The fix is the boring stuff: small changes, real review, strong CI. This playbook is mostly that fix, phase by phase.

## The phases

| Phase | In standard terms | What AI changes here |
|---|---|---|
| [1. Frame the problem](01-frame.md) | Define | Research gets faster. Judgement stays human. |
| [2. Govern before you build](02-govern.md) | Plan | You need an AI-use policy before the first prompt. |
| [3. Design the solution](03-design.md) | Design | Prototypes get almost free. Try more of them. |
| [4. Build](04-build.md) | Build | The big one. Pair with AI without losing the plot. |
| [5. Evaluate](05-evaluate.md) | Verify / Test | AI can write tests and review code. It cannot own quality. |
| [6. Launch](06-launch.md) | Release | Discipline unchanged. AI does the paperwork. |
| [7. Operate and improve](07-operate.md) | Operate / Run | AI triages. Humans decide. Measure if it's actually helping. |

## Sources, same four plus the same overlay

- **DORA / Accelerate**: the four delivery metrics, small batches, and the recent findings on AI adoption.
- **Anthropic's published guidance**: practical AI-assisted engineering habits (give the tool context, plan before code, review everything). Vendor-neutral here, as always.
- **NIST AI RMF**: the risks of *using* AI at work: confabulation, data leakage, over-reliance.
- **ISO/IEC 42001**: acceptable-use policy, accountability, and reviewing how AI is used as the tools change.
- **⚕ Regulated overlay**: if your codebase or data is regulated (health records, financial data), the data rules in Phase 2 are not optional.

## One template

[Team AI-use policy](../templates/ai-use-policy.md). One page. Written in Phase 2, reviewed quarterly. Most teams skip this and regret it the first time customer data ends up in a prompt.
