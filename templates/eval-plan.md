# Eval plan

> Drafted in [Phase 3 — Design](../playbook/03-design.md), grown during Build, executed in [Phase 5 — Evaluate](../playbook/05-evaluate.md). Rule one: thresholds are agreed **before** results are seen.

**Product:** &nbsp;&nbsp; **Version under test:** &nbsp;&nbsp; **Date:**

## 1. Test set

**Source of examples:** *(real tickets / transcripts / user interviews — real inputs, not invented ones)*
**Count:** *(20–50 to start; grow with every incident and every eval failure)*
**Coverage check:** *(happy path ✅ / edge cases ✅ / out-of-scope requests ✅ / adversarial inputs ✅ / each key user segment ✅)*

## 2. Criteria and thresholds (agree these first)

| # | Criterion | How graded | Threshold to pass |
|---|---|---|---|
| 1 | *(e.g. factually correct against source)* | *(automated / human rubric / model-graded + spot-check)* | *(e.g. ≥ 95%)* |
| 2 | *(e.g. correctly refuses out-of-scope)* | | |
| 3 | *(e.g. no personal data in output)* | | |
| 4 | *(e.g. tone appropriate)* | | |

**Segment slices to report separately:** *(e.g. by language, demographic, condition type — an average can hide a group being failed)*

## 3. Results

| Criterion | Overall | Worst segment (which?) | Pass? |
|---|---|---|---|
| | | | |

## 4. Red-team findings

| Attack tried | Result | Risk-register entry | Fixed / Accepted |
|---|---|---|---|
| | | | |

## 5. Verdict

**Meets thresholds:** Yes / No
**Exceptions (threshold moved or waived — why, by whom):**
**Sign-off (accountable owner):** &nbsp;&nbsp; **Date:**
