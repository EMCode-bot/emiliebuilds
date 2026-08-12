# Phase 6 — Launch

**Question this phase answers:** How do we go live without betting everything on day one?

Launch is not an event, it's a dial. The DORA evidence says the safest way to ship is gradually and reversibly — and for AI products, whose failure modes are probabilistic, that goes double.

## Steps

1. **Complete the launch checklist — sign it, don't skim it.** One page, walked through by the accountable owner with the team. Anything unchecked either blocks launch or gets a written, named exception. → [Launch checklist](../templates/launch-checklist.md)
   *(ISO 42001: operational planning and control; NIST AI RMF: Manage)*

2. **Turn on monitoring before turning on users.** Dashboards and alerts live *before* first traffic: error rates, latency, cost per interaction, refusal rates, and a feedback channel in the product. If launch day breaks something, you should learn it from an alert, not a tweet.
   *(DORA: monitoring and observability; NIST AI RMF: Manage — post-deployment monitoring)*

3. **Roll out progressively.** Internal users → a small cohort or percentage → everyone, with defined promotion criteria between stages (e.g. "48 hours at <1% error and no severity-1 feedback"). Every stage must be rollback-able in minutes, and rollback rehearsed once before launch.
   *(DORA: progressive delivery, small batches, fast recovery)*

4. **Tell users what they're talking to.** Users know it's AI, know what it can't do, know how their data is used, and know how to reach a human. This is UX *and*, for EU users and transparency-tier systems, law.
   *(EU AI Act: transparency obligations; ISO 42001: information for interested parties; NIST GAI Profile: over-reliance)*

5. **Arm the incident response plan.** One page, printed into the team's heads: severity levels, who gets paged, the kill-switch decision (who may turn the product off, and how fast it takes effect), and the user-communication template. Written *now*, calmly — not during the incident.
   *(NIST AI RMF: Manage — incident response; DORA: failed-deployment recovery)*

6. **⚕ Confirm clearance before first real user.** Regulatory clearance/registration is done, claims in marketing match the validated claims exactly, and adverse-event reporting obligations are wired into the incident process. Marketing "we diagnose X" when validation said "we assist with X" is how regulated launches end careers.
   *(TGA/FDA: clearance and post-market obligations; EU AI Act: high-risk registration)*

## Exit criteria

- [ ] Launch checklist signed by the accountable owner
- [ ] Monitoring and alerts verified live (test-fire an alert)
- [ ] Progressive rollout stages and promotion criteria written down
- [ ] Rollback rehearsed successfully at least once
- [ ] User transparency copy shipped in-product
- [ ] Incident plan exists; on-call and kill-switch owner named
- [ ] ⚕ Clearance confirmed; marketing claims match validated claims

## Artefact

Signed [launch checklist](../templates/launch-checklist.md)
