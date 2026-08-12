# Phase 5 — Evaluate (AI checks the work, you own the verdict)

**What AI changes here:** tests get cheaper to write and review gets an extra pair of eyes. The trap: letting the same tool that wrote the code decide the code is fine.

## Steps

1. **You write the test criteria. AI writes the tests.** Deciding what "correct" means is the valuable part, and it stays human. Once the criteria are written, AI turns them into test code quickly and thoroughly. Review the tests too: a test that asserts nothing still shows up green.
   *(DORA: test automation; Anthropic: humans own the definition of good)*

2. **Use AI review as an extra pass, never the only pass.** AI code review catches real things: edge cases, security slips, inconsistencies. Run it before human review, so humans spend attention on design and correctness instead of typos. The human pass still decides.
   *(DORA: peer review; NIST AI RMF: Measure)*

3. **Don't let the author grade its own homework.** If AI wrote the code, be suspicious of the same session confirming the code is great. Fresh session, different tool, or a human: anything that breaks the self-agreement loop.
   *(NIST GAI Profile: over-reliance; Anthropic: care with model-graded checks)*

4. **Security-scan generated code every time.** AI-generated code can carry classic vulnerabilities with total confidence: injection risks, weak input handling, outdated patterns from old training data. Automated scanning in CI plus a human eye on anything touching auth, money or personal data.
   *(NIST GAI Profile: information security; DORA: build security in, don't bolt it on)*

5. **⚕ Regulated code paths get the full treatment.** Anything touching health records, payments or legal obligations gets human review regardless of how it was written, and the review is recorded. "An AI reviewed it" satisfies no auditor.
   *(ISO 42001: documented control; regulated-domain obligations)*

## Exit criteria

- [ ] Test criteria written by a human; tests reviewed, not just generated
- [ ] The failure modes were tested, not just the happy path
- [ ] Every change had at least one human review pass
- [ ] Security scanning runs in CI on all code, whoever wrote it
- [ ] ⚕ Regulated paths have recorded human review

Want more depth on test sets, grading methods and the classic traps? See the [evals deep-dive](../deep-dives/evals.md).
