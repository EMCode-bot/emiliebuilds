# Phase 1 — Frame the problem

**Question this phase answers:** Is this worth building, and does it need AI at all?

Most AI product failures are framing failures: a capability looking for a problem. This phase is deliberately cheap — a few days of work that can kill a bad idea before it costs a quarter.

## Steps

1. **Write the problem without mentioning AI.** One page: who has the problem, how often, what it costs them, how they solve it today. If the problem only makes sense with "AI" in the sentence, it isn't a problem yet. → [Problem one-pager template](../templates/problem-one-pager.md)
   *(NIST AI RMF: Map — establish context and intended purpose)*

2. **Define success in numbers before choosing a solution.** What user behaviour or business metric changes, by how much, by when? "Users love it" is not a metric.
   *(DORA/Accelerate: outcome measures over output measures)*

3. **Ask the simplest-solution question honestly.** Could this be solved with rules, a form, a lookup table, or better UX? AI earns its place only when the task involves genuine variability — understanding language, judgement at scale, synthesis. Write down why simpler options lose.
   *(Anthropic: find the simplest solution possible; only escalate complexity when it demonstrably improves outcomes)*

4. **Name who could be harmed and how.** Not a full risk assessment yet — a first pass: wrong answers, leaked data, biased treatment, over-reliance. If the harm list includes "someone's health, money, or legal standing", flag the ⚕ overlay now.
   *(NIST AI RMF: Map — identify impacts to individuals, groups, and society)*

5. **⚕ Run the two regulatory screening questions.**
   (a) Could this system fall in the EU AI Act's prohibited or high-risk tiers, or serve EU users?
   (b) Does it diagnose, treat, monitor, or inform clinical decisions — i.e. could it be software-as-a-medical-device under TGA/FDA rules?
   A "maybe" to either means: budget for regulatory advice in Phase 2. Do not silently downgrade a "maybe" to a "no".
   *(EU AI Act: risk-tier classification; TGA/FDA: SaMD boundary)*

6. **Make an explicit go/no-go call with the one-pager in hand.** A "no" here is a success — it cost days, not quarters.

## Exit criteria

- [ ] Problem one-pager exists and a person who *has* the problem has read it and agreed it's real
- [ ] Success metrics are numeric and dated
- [ ] The "why not something simpler?" answer is written down
- [ ] First-pass harm list exists; ⚕ screening questions answered
- [ ] Go/no-go decision recorded, with owner

## Artefact

[Problem one-pager](../templates/problem-one-pager.md)
