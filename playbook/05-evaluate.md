# Phase 5 — Evaluate

**Question this phase answers:** How do we know it works — and fails safely?

A demo proves the product *can* work. An eval proves it *usually* works, and tells you what "usually" means as a number. No AI product should meet users on the strength of a demo.

## Steps

1. **Execute the eval plan against agreed thresholds.** Run the full eval set (built in Phase 3, grown during Phase 4). The pass thresholds were agreed *before* seeing results — moving the goalposts after the fact gets recorded as a formal decision with the accountable owner's name on it. → [Eval plan](../templates/eval-plan.md)
   *(NIST AI RMF: Measure — pre-defined metrics and thresholds; Anthropic: graded evals over vibes)*

2. **Grade with the right mix of machine and human.** Automate what's checkable (format, factual fields, refusal correctness); use structured human review for judgement calls (tone, safety, usefulness); if using a model to grade a model, spot-check the grader against human judgement first.
   *(Anthropic: eval guidance, including care with LLM-as-judge)*

3. **Red-team it before strangers do.** Deliberately attack: prompt injection, requests for harmful output, personal-data fishing, out-of-scope questions, adversarial phrasing from real user language. Log every successful break as a risk-register entry with a fix or an accepted-risk decision.
   *(NIST GAI Profile: information security, harmful content; NIST AI RMF: Measure — adversarial testing)*

4. **Check performance across user groups, not just on average.** Slice eval results by the user segments that matter (demographics, language, accent, condition type — whatever applies). An 85% average that's 95% for one group and 60% for another is a fairness failure hiding in a mean.
   *(NIST AI RMF: Measure — harmful bias; ISO 42001: impact assessment follow-through)*

5. **Test the failure modes, not just the happy path.** What does the user see when the model times out, the provider is down, the answer is refused, or confidence is low? Every failure mode gets a designed experience — silence and spinners are not designs.
   *(NIST AI RMF: Manage — response planning; DORA: resilience practices)*

6. **⚕ Run the clinical/regulated validation.** If Phase 2 classified the product as regulated: execute the evidence plan agreed with regulatory counsel — clinical validation against ground truth, accuracy claims substantiated, safety case written and signed by the accountable owner. This step cannot be compressed to fit a launch date.
   *(TGA/FDA: clinical evidence for SaMD; EU AI Act: conformity assessment for high-risk systems)*

## Exit criteria

- [ ] Eval results meet pre-agreed thresholds (or a signed exception exists)
- [ ] Results reviewed by segment; no group materially left behind
- [ ] Red-team findings fixed or formally accepted in the risk register
- [ ] Every known failure mode has a designed user experience
- [ ] ⚕ Regulated validation complete and signed off
- [ ] Risk register reviewed; accountable owner approves proceeding to launch

## Artefact

Completed [eval plan](../templates/eval-plan.md) with results — this becomes launch evidence.

Want more depth on test sets, grading methods and the classic traps? See the [evals deep-dive](../deep-dives/evals.md).
