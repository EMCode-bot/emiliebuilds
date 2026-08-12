# Phase 6 — Launch (same discipline, less paperwork pain)

**What AI changes here:** honestly, not the important parts. Progressive rollout, rehearsed rollback and live monitoring are exactly as they were. What AI does change: the writing around a launch stops being a chore.

## Steps

1. **Keep the full launch discipline. AI-assisted building doesn't earn a shortcut.** The non-negotiables:
   - Monitoring and alerts are live **before** the first user arrives, and you've test-fired an alert. If launch breaks something, you should learn it from an alert, not a tweet.
   - Roll out in stages: your own team, then a small group, then everyone. Write down what has to be true before each promotion (for example "48 hours with under 1% errors").
   - Rehearse the rollback once before launch. Reversing a bad release should take minutes, not meetings.
   - Have a one-page incident plan: severity levels, who gets called, who can pull the product, and a draft of what you'd tell users.

   *(DORA: progressive delivery, monitoring, fast recovery)*

2. **Let AI draft the launch paperwork.** Release notes from the merged changes. Runbook drafts from the architecture. Rollback steps from the deploy config. Internal announcement from the release notes. Each one drafted in minutes, then checked by the person who owns it, because a runbook with one wrong command is worse than no runbook.
   *(Anthropic: AI for drafts, humans for accuracy; ISO 42001: operational documentation)*

3. **Double-check AI-drafted user-facing text.** Anything users see (release notes, in-app copy, help pages) gets a human read for accuracy and tone. AI drafts overpromise cheerfully.
   *(NIST GAI Profile: information integrity)*

4. **Log what shipped and how it was built.** If big parts of the release were AI-assisted, note it in the release record. Not as a confession: as engineering information. When something breaks in three months, knowing how the code came to be speeds up the fix.
   *(ISO 42001: lifecycle records)*

## Exit criteria

- [ ] Monitoring live and an alert test-fired before launch
- [ ] Rollout stages and promotion criteria written down
- [ ] Rollback rehearsed successfully at least once
- [ ] Incident plan exists, with named decision-makers
- [ ] All AI-drafted launch documents checked and signed by their human owner
- [ ] Release record notes the AI-assisted parts

Shipping an AI product too? Its launch has extra obligations (user transparency, regulated clearance). See the companion playbook: [Building an AI product, Phase 6](../playbook/06-launch.md).
