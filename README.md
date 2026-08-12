# EmilieBuilds — AI Product Playbooks

Two rigorous, framework-mapped playbooks for startup and scale-up product teams:

1. **[Building an AI product](playbook/00-overview.md)** — taking an AI-powered product from problem to live to well-operated. AI is in the thing you ship.
2. **[Building product with AI](playbook-with-ai/00-overview.md)** — how a team works when AI tools help you research, design, code and operate. AI is in how you build.

Every step in both is traceable to a recognised source. When someone asks *"says who?"*, the answer is on the page.

## The sources

| Source | What it is | What we take from it |
|---|---|---|
| **NIST AI Risk Management Framework** (+ Generative AI Profile) | US government framework for managing AI risk; the most widely cited AI governance reference globally. Free. | The four functions — Govern, Map, Measure, Manage — as the risk backbone of every phase. |
| **ISO/IEC 42001:2023** | The international, certifiable standard for AI management systems (Anthropic is certified against it). | Leadership accountability, AI impact assessment, lifecycle documentation, continual improvement. |
| **DORA / *Accelerate*** | The largest evidence-based research program on what makes software teams perform. | The four delivery metrics, small batches, CI/CD, and the finding that speed and stability rise together. |
| **Anthropic's published guidance** | Practitioner guidance from a frontier AI lab: *Building Effective Agents*, prompt engineering docs, eval guidance. Vendor-neutral in this playbook — the principles apply to any model provider. | Start with the simplest pattern that works; design evals before you build; treat prompts and tools as engineered artefacts. |
| **Regulation (overlay)** | EU AI Act; TGA (Australia) and FDA (US) software-as-a-medical-device rules. | Checkpoints marked **⚕ Regulated overlay** — only relevant if your product touches a regulated domain like health. |

See [frameworks.md](frameworks.md) for a plain-English breakdown of each source's key points.

## The lifecycle (shared by both playbooks)

Both playbooks use the same seven phases. The middle column maps them to standard product lifecycle language.

| Phase | In standard terms | Question it answers |
|---|---|---|
| 1. Frame the problem | Define | Is this worth building, and does it need AI at all? |
| 2. Govern before you build | Plan | Who is accountable, and what are the rules? |
| 3. Design the solution | Design | What's the simplest approach that could work? |
| 4. Build | Build | How do we ship small and often? |
| 5. Evaluate | Verify / Test | How do we know it works, and fails safely? |
| 6. Launch | Release | How do we go live without betting everything on day one? |
| 7. Operate and improve | Operate / Run | How do we keep it good after launch? |

Start with each playbook's overview: [Building an AI product](playbook/00-overview.md) · [Building product with AI](playbook-with-ai/00-overview.md)

## Templates

Fill-in artefacts, used at the phase where they earn their place:

- [Problem one-pager](templates/problem-one-pager.md) — Phase 1
- [Risk register](templates/risk-register.md) — Phase 2 onwards
- [Team AI-use policy](templates/ai-use-policy.md) — Phase 2 of *Building product with AI*
- [Eval plan](templates/eval-plan.md) — Phases 3–5
- [Launch checklist](templates/launch-checklist.md) — Phase 6

## How to use this

1. Read the [overview](playbook/00-overview.md) (5 minutes).
2. Run Phase 1 on a real problem this week — don't read the whole playbook first.
3. Skip what doesn't apply, but write down *why* you skipped it. That note is your audit trail.

**A note on the ⚕ Regulated overlay:** if your product gives clinical, financial, or legal advice — or your users are in the EU — the marked overlay steps are not optional. Get regulatory advice early; this playbook tells you *when* to ask, not *what the answer is*.

---

*Maintained by EmilieBuilds. This playbook maps to the named frameworks; it does not reproduce their text. It is not legal or regulatory advice.*
