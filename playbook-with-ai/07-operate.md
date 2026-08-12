# Phase 7 — Operate and improve (AI triages, humans decide)

**What AI changes here:** the 2am incident gets less lonely and the toil shrinks. The judgement calls, and the accountability for them, don't move.

## Steps

1. **Use AI as first responder, not decision maker.** Summarising logs, correlating alerts, drafting a timeline: AI does this well and fast. Deciding severity, deciding to roll back, deciding to wake someone: humans, per the incident plan. Write that split into the runbook so nobody debates it during an outage.
   *(NIST AI RMF: Manage; DORA: fast recovery needs clear roles)*

2. **Draft postmortems with AI, run them with people.** AI turns a messy incident channel into a clean timeline in minutes. The blameless discussion of "what should the system do differently" is the entire point of a postmortem, and it only works with humans in a room.
   *(DORA: blameless postmortems, generative culture)*

3. **Measure whether AI is actually helping.** The DORA four don't lie: deployment frequency, lead time, change failure rate, recovery time. If six months of AI-assisted building shows faster lead time but a climbing change failure rate, Phase 4's discipline is slipping. Look at review quality first.
   *(DORA: four key metrics, AI adoption findings)*

4. **Watch for skill drift.** If nobody on the team can debug the payment flow without AI anymore, that's a fragility, not a productivity win. Rotate people through the hard parts. Understanding is an operational dependency.
   *(NIST GAI Profile: over-reliance, applied to teams)*

5. **Re-review the AI-use policy quarterly.** Tools change, vendor terms change, and what the team pastes into prompts drifts over time. Quarterly: is the tool list current, did any vendor change data terms, any near-misses with red data?
   *(ISO 42001: continual improvement, third-party monitoring)*

## The health check

- [ ] Incident runbook says what AI does and what humans decide
- [ ] DORA metrics reviewed with AI adoption in mind
- [ ] No single system only the AI understands
- [ ] AI-use policy reviewed within the last quarter
