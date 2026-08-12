# Phase 2 — Govern before you build (the AI-use policy)

**What AI changes here:** you need rules for the tools themselves, agreed before the team is ten prompts deep. This phase produces one page. It might be the highest-value page in this playbook.

## Steps

1. **Write the team AI-use policy.** One page, using the [template](../templates/ai-use-policy.md). It answers five questions: which tools are approved, what data may enter a prompt, who reviews AI-written code, what's our stance on licensing, and who owns this policy.
   *(ISO 42001: acceptable-use policy and assigned responsibility; NIST AI RMF: Govern)*

2. **Sort your data into green, amber, red.** Green goes in prompts freely (public info, your own code, synthetic data). Amber needs care (internal docs, anonymised customer data). Red never goes in (secrets, credentials, identifiable customer data, anything under NDA). Ten minutes of sorting now prevents the incident later.
   *(NIST GAI Profile: data privacy; ⚕ regulated data is red by default, whatever the vendor's terms say)*

3. **Check what your AI vendors do with your prompts.** Do they train on your data? Retain it? For how long? Business plans usually differ from consumer plans. Write the answer into the policy so nobody has to guess.
   *(ISO 42001: third-party controls)*

4. **Decide the accountability rule and say it out loud.** Suggested wording: "AI never merged anything. A named person ships every change and owns it." This kills the "the AI wrote it" excuse on day one.
   *(ISO 42001: leadership and accountability; NIST AI RMF: Govern)*

5. **Set the review date.** AI tools change monthly. The policy gets reviewed quarterly, or when a tool changes its data terms, whichever comes first.
   *(ISO 42001: continual improvement)*

## Exit criteria

- [ ] AI-use policy exists, fits on one page, and every team member has read it
- [ ] Data sorted into green, amber, red, with examples of each
- [ ] Vendor data-handling terms checked and recorded
- [ ] Accountability rule agreed in writing
- [ ] Quarterly review date in the calendar

## Artefact

[Team AI-use policy](../templates/ai-use-policy.md)
