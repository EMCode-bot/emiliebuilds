# Deep-dive: Evals

Evals are the most important habit in AI product development and the least practised. This page goes deeper than [Phase 5](../playbook/05-evaluate.md): what evals actually are, how to build one that means something, and the traps that make teams think they have one when they don't.

## What an eval is, in plain English

An eval is a repeatable test that turns "seems good" into a number. You collect real inputs, define what a good output looks like, run your product against them, and score the results. Same inputs every time, so you can compare: this prompt versus that one, this model versus the next, last month versus today.

A demo shows your product *can* work once. An eval tells you how often it works, and what "often" means. Products meet thousands of users, not one well-rehearsed one.

*(Sources for this page: Anthropic's evaluation guidance, NIST AI RMF: Measure, DORA: test automation.)*

## The test set: where evals live or die

1. **Use real inputs, not invented ones.** Support tickets, transcripts, actual user questions. Inputs you make up are secretly easy: they're phrased the way you think, not the way users type at 11pm on a phone with a toddler on one arm.
2. **Start at 20 to 50 examples.** Small enough to build this week, big enough to catch patterns. Grow it forever: every incident, every complaint, every weird input becomes a test case. A one-year-old eval set with 300 battle-tested cases is a company asset.
3. **Cover five categories, deliberately:**
   - Happy path: the common cases that must work
   - Edge cases: long inputs, odd formats, ambiguity
   - Out-of-scope: things your product should refuse or redirect
   - Adversarial: injection attempts, harmful requests, data fishing
   - Segments: each user group that matters (language, demographic, use case)
4. **Keep a holdout.** If you tune prompts against your whole eval set, you'll overfit to it: scores rise, real quality doesn't. Keep a slice you never look at while tuning and check it last.

## Three ways to grade, and when to use each

| Method | What it is | Use it for | Watch out for |
|---|---|---|---|
| **Code-graded** | A script checks the output: exact match, format, required fields, banned strings | Anything with an objective answer. Cheapest, fastest, run it on every change | Only tests what's checkable. "Valid JSON" is not "good answer" |
| **Human rubric** | A person scores against written criteria | Tone, usefulness, safety judgement calls | Expensive and slow, so sample. Two graders on the same items first, to check the rubric isn't ambiguous |
| **Model-graded** | An AI grades the outputs against your rubric | Scaling judgement-style grading across hundreds of cases | Spot-check it against human grades before trusting it. And never let the same session that wrote the output grade the output |

Most real eval plans use all three: code-graded for the objective layer on every merge, model-graded for scale, humans for the sample that keeps everyone honest.

## Writing criteria that actually grade

- **Binary beats scales.** "Cites at least one source: yes/no" produces consistent grades. "Rate quality 1 to 10" produces noise, because nobody agrees what a 6 is.
- **One criterion, one question.** "Accurate and helpful and well-formatted" is three criteria wearing a trenchcoat. Split them, or a failure tells you nothing about what failed.
- **Write the failure examples too.** The fastest way to sharpen a criterion is one example that passes and one that fails, side by side. If you can't produce the failing example, the criterion is too vague to grade.

## Thresholds: the rule that keeps evals honest

Agree the pass mark *before* you see results. "≥ 95% on correctness, 100% on the safety cases" decided upfront is a standard. The same numbers decided after seeing your results is a rationalisation. Moving a threshold afterwards is allowed exactly one way: as a written decision with the accountable owner's name on it.

And always report the worst segment next to the average. An 85% average that's 95% for one user group and 60% for another isn't an 85% product. It's a product that fails a group of your users, with a flattering summary statistic.

## Evals as infrastructure, not ceremony

- **Wire them into CI.** A prompt tweak that quietly drops quality should fail a check the same day, not surface in a complaint three weeks later. This is the same logic as unit tests, applied to behaviour.
- **Re-run on a schedule, not just on change.** Model providers update models underneath you, and the world changes what a correct answer is. Monthly re-runs against production config catch silent drift.
- **Treat a provider model update as a deploy.** Eval before, eval after, compare. If you can't hold the model version constant, this habit is your only early warning.

## The five classic traps

1. **The demo-as-eval.** Ten hand-picked inputs the team already knows it passes. Comforting, worthless.
2. **Tests that assert nothing.** AI-generated test code sometimes checks that a function runs, not that it's right. A green tick from a hollow test is worse than no test.
3. **The author grading its own homework.** Same model, same session, writing then approving. Break the loop: different grader, fresh context, or a human.
4. **Overfitting to the eval set.** Scores climb for weeks while users notice nothing. That's the holdout's job.
5. **The stale set.** Product changed, users changed, eval set didn't. If no case has been added in a quarter, the set is measuring last quarter's product.

## ⚕ If you're in a regulated domain

Evals become evidence. Clinical or financial accuracy claims need validation against ground truth agreed with regulatory advice, the methodology written down, and results signed by the accountable owner. The habits above still apply; the bar and the paperwork rise.

---

**Use it with:** the [eval plan template](../templates/eval-plan.md) · [Phase 5: Evaluate](../playbook/05-evaluate.md) · [Phase 5 of Building product with AI](../playbook-with-ai/05-evaluate.md)
