# Phase 1 — Frame the problem (with AI's help)

**What AI changes here:** research that took a week takes a day. What doesn't change: the go/no-go call is yours.

## Steps

1. **Use AI to synthesise, not to invent.** Feed it real inputs: interview notes, support tickets, survey answers. Ask it to cluster themes, surface contradictions, and pull representative quotes. Do not ask it what users want. It doesn't know your users. It knows your notes.
   *(NIST GAI Profile: confabulation risk. Synthesis of real data is safe ground; generation of "insights" from nothing is not.)*

2. **Check the data rules before pasting anything.** Customer interviews and tickets often contain names, health details, account numbers. If your Phase 2 AI-use policy doesn't exist yet, follow its two default rules now: no identifiable customer data in prompts, no secrets ever.
   *(ISO 42001: data handling. ⚕ In regulated domains this is a legal line, not a guideline.)*

3. **Draft with AI, decide without it.** Let AI draft the problem one-pager from your inputs. Then close the laptop and ask the human questions: do I believe this? Has someone with this problem confirmed it's real? AI is persuasive even when it's wrong, and a well-formatted one-pager can look more validated than it is.
   *(NIST GAI Profile: over-reliance; Anthropic: human checkpoints where stakes are high)*

4. **Use AI to argue against you.** Before the go/no-go, ask it to make the strongest case for "no". Cheap red-teaming for your thinking. Bring the counter-case to the decision.
   *(Anthropic: use the tool to pressure-test, not just to produce)*

## Exit criteria

Same as the [core playbook Phase 1](../playbook/01-frame.md), plus:

- [ ] Every AI-synthesised claim in the one-pager traces to a real input you can point at
- [ ] No identifiable customer data went into any prompt (or your policy explicitly allowed it)
