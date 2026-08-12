# Phase 2 — Govern before you build

**Question this phase answers:** Who is accountable, and what are the rules?

This is the phase teams skip because it feels like bureaucracy — and it's the phase that certification bodies, enterprise customers, and regulators check first. Done right it's a week, not a quarter, and most of it is reusable across every product you build.

## Steps

1. **Name one accountable owner.** A person, not a committee — accountable for the product's behaviour in the world, with authority to stop a launch. Leadership signs off on the name.
   *(ISO 42001: leadership commitment and assigned responsibilities; NIST AI RMF: Govern — accountability structures)*

2. **Write (or reuse) the AI policy — one page.** What data may and may not be sent to models, which providers are approved, what requires human review, how users are told they're interacting with AI. If the org already has one, check this product fits it.
   *(ISO 42001: AI policy; NIST AI RMF: Govern — policies and procedures)*

3. **Open the risk register.** Convert Phase 1's harm list into named risks with severity, likelihood, owner, and mitigation status. It stays open for the product's life and gets reviewed at every phase gate. → [Risk register template](../templates/risk-register.md)
   *(NIST AI RMF: Govern/Manage; ISO 42001: risk management)*

4. **Run an AI impact assessment.** Beyond risks-to-the-business: how could this system affect individuals and groups — fairness across user demographics, accessibility, what happens to people the model gets wrong? Keep it short, keep it honest, file it.
   *(ISO 42001: AI system impact assessment; NIST AI RMF: Map — impacts)*

5. **Check the data before promising the product.** Where does training/context data come from, who owns it, did users consent to this use, does it contain personal or health information, and under which privacy law (e.g. Australian Privacy Act, GDPR) is it handled? Data surprises found here cost days; found in Phase 5 they cost the roadmap.
   *(ISO 42001: data quality and provenance controls; NIST GAI Profile: data privacy)*

6. **Assess third-party dependencies.** For each model provider or AI vendor: data-use terms (do they train on your data?), uptime history, deprecation policy, and an exit plan if the provider changes terms or shuts the model down. You stay responsible for what you buy in.
   *(ISO 42001: third-party and supplier controls)*

7. **⚕ Get the regulatory classification in writing.** If Phase 1 screening said "maybe": engage regulatory counsel now, get the classification (EU AI Act tier; TGA/FDA device class or exemption) documented, and add its evidence requirements to the plan. This step gates the budget — clinical evidence requirements can exceed the build cost.
   *(EU AI Act: high-risk obligations; TGA/FDA: SaMD classification)*

## Exit criteria

- [ ] Accountable owner named and accepted, in writing
- [ ] AI policy exists (or product's fit with existing policy confirmed)
- [ ] Risk register opened with Phase 1 harms converted to entries
- [ ] Impact assessment done and filed
- [ ] Data provenance and privacy basis documented
- [ ] Vendor terms reviewed; exit plan sketched
- [ ] ⚕ Regulatory classification documented (or confirmed not applicable)

## Artefact

[Risk register](../templates/risk-register.md)
