# Phase 4 — Build

**Question this phase answers:** How do we build so we can ship small and often?

The DORA research finding that matters most here: teams that ship in small, frequent batches are *both* faster and more stable. For AI products, "small batches" covers prompts and model configs, not just code.

## Steps

1. **Set up continuous integration before feature one.** Every change merges to main frequently (no week-old branches), tests run automatically on every merge, and a broken main is everyone's first priority. This is the foundation the DORA metrics stand on.
   *(DORA: continuous integration, trunk-based development)*

2. **Version-control everything that changes behaviour.** Code, prompts, tool definitions, model choice, temperature, system instructions — all in git, all reviewed, all diffable. "Who changed the prompt and when?" must have an answer.
   *(Anthropic: prompts and tools as engineered artefacts; ISO 42001: lifecycle documentation and change control)*

3. **Write prompts like an engineer, not a poet.** Clear role and instructions, concrete examples of good output, explicit handling for "I don't know" cases, structured output formats. Review prompt changes like code changes — they are.
   *(Anthropic: prompt engineering guidance)*

4. **Give tools crisp contracts.** If the model calls tools/functions: precise descriptions, unambiguous parameters, and error messages the model can act on. Most "agent is dumb" bugs are really "tool description is vague" bugs.
   *(Anthropic, Building Effective Agents: the agent-computer interface deserves as much design as the prompt)*

5. **Build the guardrails as features, not patches.** Input filtering (off-topic, injection attempts), output checks (formats, banned content, PII leakage), rate limits, and spend caps per user/day. Cheaper to build now than to retrofit after an incident.
   *(NIST GAI Profile: information security, data privacy; NIST AI RMF: Manage — risk controls)*

6. **Keep secrets and personal data out of the model's reach by default.** API keys in secret managers, personal data minimised or masked before it reaches a prompt, logging that captures behaviour without hoarding sensitive content.
   *(ISO 42001: data controls; privacy law — see Phase 2, step 5)*

7. **Run the evals continuously, not ceremonially.** Wire the Phase 3 eval set into CI so a prompt tweak that quietly breaks quality fails a check the same day, not in a user complaint three weeks later.
   *(Anthropic: eval-driven iteration; DORA: automated testing; NIST AI RMF: Measure)*

## Exit criteria

- [ ] CI runs tests and evals on every merge; main is deployable
- [ ] Prompts, configs, and tool definitions are versioned and reviewed
- [ ] Guardrails implemented and tested (including at least basic injection attempts)
- [ ] Secrets managed properly; personal data flow documented and minimised
- [ ] Feature-complete against the Phase 3 design, or scope change recorded

## Artefact

None new — this phase feeds the [eval plan](../templates/eval-plan.md) and keeps the [risk register](../templates/risk-register.md) current.
