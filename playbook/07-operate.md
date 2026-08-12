# Phase 7 — Operate and improve

**Question this phase answers:** How do we keep it good after launch?

AI products degrade in ways ordinary software doesn't: the world changes, user behaviour drifts, and the model under you gets updated or deprecated by someone else. Operation isn't maintenance — it's the phase where the product earns its keep or quietly rots.

## Steps

1. **Track the four DORA metrics plus the AI four.** Delivery health: deployment frequency, lead time, change failure rate, recovery time. AI health: output quality (eval scores over time), cost per interaction, refusal/fallback rate, and user-reported issues. Review both sets at a regular cadence with the accountable owner present.
   *(DORA: four key metrics; NIST AI RMF: Manage — ongoing monitoring)*

2. **Re-run the evals on a schedule, not just on change.** Model providers update models under you; the world changes what "correct" means. A monthly eval re-run against the live configuration catches silent drift. Any provider model-version change is treated as a deploy: eval before, eval after.
   *(NIST GAI Profile: model instability; Anthropic: continuous evaluation; DORA: treat every change as a change)*

3. **Work the incidents, then feed them back.** Every incident gets a blameless review: what happened, what the system (not the person) should do differently, which risk-register entry it maps to — creating one if it was unforeseen. ⚕ In regulated domains, check each incident against adverse-event reporting obligations.
   *(NIST AI RMF: Manage — incident response and improvement; DORA: generative culture, blameless postmortems)*

4. **Close the loop from users to backlog.** In-product feedback, support tickets, and eval failures flow into one triaged backlog. Improvements ship as small batches through the same Phase 4–6 pipeline — no "quick prompt fix" straight to production outside CI and evals.
   *(DORA: small batches; Plan–Do–Check–Act as the operating rhythm — ISO 42001)*

5. **Review the risk register and impact assessment quarterly.** Are the mitigations still working? Have new risks appeared (new user groups, new data, new regulation)? Has the product drifted from its assessed intended use? An impact assessment that's 18 months stale describes a product that no longer exists.
   *(ISO 42001: performance evaluation, continual improvement; NIST AI RMF: Govern/Map refresh)*

6. **Keep the exit plans current.** Two of them: the *vendor* exit (provider changes terms or deprecates the model — can you switch within your risk appetite?) and the *product* exit (usage, quality, or economics no longer justify it — what are the criteria for switching it off, and what happens to users and their data?). Deciding to retire a system deliberately is a management function, not a failure.
   *(ISO 42001: third-party controls, lifecycle including retirement; NIST AI RMF: Manage — deactivation and disengagement)*

## Exit criteria

This phase doesn't exit — it cycles. The health check is:

- [ ] Metrics reviewed at cadence, with the accountable owner
- [ ] Evals re-run on schedule; last run within the window
- [ ] No incident without a completed blameless review
- [ ] Risk register and impact assessment reviewed within the last quarter
- [ ] Vendor and product exit plans reviewed within the last two quarters

When a review triggers significant change, re-enter the loop at [Phase 3 — Design](03-design.md).
