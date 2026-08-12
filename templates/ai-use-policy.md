# Team AI-use policy

> Written in [Phase 2 of Building product with AI](../playbook-with-ai/02-govern.md). One page. Reviewed quarterly, or when a vendor changes its data terms, whichever comes first.

**Team:** &nbsp;&nbsp; **Policy owner:** &nbsp;&nbsp; **Last reviewed:** &nbsp;&nbsp; **Next review:**

## 1. Approved tools

| Tool | Approved for | Vendor trains on our data? | Notes |
|---|---|---|---|
| | | Yes / No / Unknown | |
| | | | |

*(Unknown means not approved yet. Find out first.)*

## 2. Data rules: green, amber, red

| Tier | What it covers | Rule |
|---|---|---|
| 🟢 Green | Public info, our own code, synthetic/test data | Fine in prompts |
| 🟠 Amber | Internal docs, anonymised customer data | Allowed with care; when unsure, ask the policy owner |
| 🔴 Red | Secrets, credentials, identifiable customer data, anything under NDA, ⚕ regulated data (health, financial records) | Never in a prompt. No exceptions without the owner's written sign-off |

**Our examples of each tier:** *(fill in 2-3 real examples per tier so nobody has to guess)*

## 3. Code rules

- A named human ships every change and owns it. "The AI wrote it" is never an explanation.
- No merging code you don't understand.
- AI-written code goes through the same review, tests and CI as human-written code.
- Security scanning runs on everything.

## 4. Licensing stance

*(Your position on AI-generated code and third-party licences, e.g. "generated code is treated as ours, but anything resembling a known library gets checked before merge." Get advice if your situation is unusual.)*

## 5. When something goes wrong

Pasted red data into a prompt? Tool behaved oddly with sensitive info? Tell the policy owner the same day. Near-misses are how the policy improves. Nobody gets in trouble for reporting one.

---

**Sign-off (policy owner):** &nbsp;&nbsp; **Date:**
