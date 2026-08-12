# Phase 3 — Design the solution

**Question this phase answers:** What's the simplest pattern that could work?

The single most expensive design mistake in AI products is over-building: shipping an autonomous agent where a well-crafted prompt would do. Complexity you don't need costs latency, money, and — worst — debuggability.

## Steps

1. **Climb the complexity ladder from the bottom.** In order: single prompt → prompt + retrieved context (RAG) → fixed workflow (chaining, routing, parallel steps) → autonomous agent. Take the *lowest* rung that plausibly solves the problem, and write down what evidence would justify climbing one rung. Agents are for tasks where the steps genuinely can't be predefined.
   *(Anthropic, Building Effective Agents: start with the simplest pattern; add autonomy only when needed)*

2. **Design the eval criteria now — before building.** What does a "good" output look like, concretely? Collect 20–50 real examples of inputs (from support tickets, transcripts, user interviews) and write the grading criteria. If you can't describe a good output, you can't build one. → Start the [eval plan](../templates/eval-plan.md)
   *(Anthropic: evals designed early; NIST AI RMF: Measure — defined methods before deployment)*

3. **Place the human checkpoints.** Decide where a person reviews, approves, or can override — driven by the risk register, not by what's convenient to build. High-severity risks get a human between the model and the consequence.
   *(NIST AI RMF: Govern — human oversight; EU AI Act: human oversight for high-risk systems; Anthropic: checkpoints as design features)*

4. **Design for distrust.** The UI should show sources, signal uncertainty, make correction easy, and never present a guess as a fact. Assume the model will sometimes confabulate — because it will — and make that survivable.
   *(NIST GAI Profile: confabulation, over-reliance; Anthropic: transparency in product design)*

5. **Keep the AI loosely coupled.** Architect so the model, prompts, and provider can change without rewriting the product: prompts in versioned files (not hard-coded), a thin abstraction over the model API, config-driven model selection. This is what makes Phase 7's "the model changed" survivable.
   *(DORA: loosely coupled architecture; ISO 42001: lifecycle change management)*

6. **Prototype against real data — timeboxed.** One or two weeks, real inputs from step 2, throwaway code. The goal is to learn whether the chosen rung of the ladder works, not to build v1. Feed what you learn back into the eval criteria and the risk register.
   *(Anthropic: iterate on real cases; NIST AI RMF: Map — validate context assumptions)*

## Exit criteria

- [ ] Chosen pattern documented, with the "why not simpler?" note
- [ ] Eval plan drafted: real example inputs collected, grading criteria written
- [ ] Human checkpoints mapped to risk-register entries
- [ ] UX handles uncertainty, sources, and correction
- [ ] Prototype tested on real data; learnings recorded
- [ ] Risk register reviewed and updated

## Artefact

[Eval plan](../templates/eval-plan.md) (drafted here, executed in Phase 5)
