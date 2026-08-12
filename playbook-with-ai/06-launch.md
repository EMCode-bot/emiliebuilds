# Phase 6 — Launch (same discipline, less paperwork pain)

**What AI changes here:** honestly, not the important parts. Progressive rollout, rehearsed rollback and live monitoring are exactly as they were. What AI does change: the writing around a launch stops being a chore.

## Steps

1. **Run the launch checklist unchanged.** AI-assisted development doesn't earn a shortcut past the [core playbook's launch discipline](../playbook/06-launch.md). Staged rollout, monitoring on before users arrive, rollback rehearsed. All of it.
   *(DORA: progressive delivery, fast recovery)*

2. **Let AI draft the launch paperwork.** Release notes from the merged changes. Runbook drafts from the architecture. Rollback steps from the deploy config. Internal announcement from the release notes. Each one drafted in minutes, then checked by the person who owns it, because a runbook with one wrong command is worse than no runbook.
   *(Anthropic: AI for drafts, humans for accuracy; ISO 42001: operational documentation)*

3. **Double-check AI-drafted user-facing text.** Anything users see (release notes, in-app copy, help pages) gets a human read for accuracy and tone. AI drafts overpromise cheerfully.
   *(NIST GAI Profile: information integrity)*

4. **Log what shipped and how it was built.** If big parts of the release were AI-assisted, note it in the release record. Not as a confession: as engineering information. When something breaks in three months, knowing how the code came to be speeds up the fix.
   *(ISO 42001: lifecycle records)*

## Exit criteria

Same as the [core playbook Phase 6](../playbook/06-launch.md), plus:

- [ ] All AI-drafted launch documents checked and signed by their human owner
- [ ] Release record notes the AI-assisted parts
