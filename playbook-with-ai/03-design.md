# Phase 3 — Design the solution (prototype like it's free)

**What AI changes here:** a prototype that cost a sprint now costs an afternoon. That changes how many ideas you can afford to test. It does not change who makes the design call.

## Steps

1. **Spike two or three approaches, not one.** When prototypes are cheap, comparing beats guessing. Ask AI to build rough versions of competing approaches and put them in front of a real user or a teammate. Keep them deliberately ugly so nobody mistakes them for the product.
   *(DORA: small experiments over big bets; Anthropic: iterate on real cases)*

2. **Throw the prototypes away. Actually away.** Prototype code skips the review, tests and security care that production code gets. The moment a prototype "just gets cleaned up a bit" and shipped, you've smuggled unreviewed code into production. Rebuild properly in Phase 4.
   *(DORA: the delivery discipline exists for a reason; NIST AI RMF: Manage)*

3. **Make AI attack your design.** Before committing: "here's my design, list the ways it fails at 10x load, with a confused user, with malicious input." It will find real holes and some silly ones. The real ones go in the risk register.
   *(Anthropic: pressure-testing; NIST AI RMF: Map)*

4. **Write the design decision down yourself.** A short note: what we chose, what we rejected, why. AI can draft it from your discussion, but a human signs it, because in six months someone will ask "why did we do it this way?" and "the AI suggested it" is not an answer.
   *(ISO 42001: lifecycle documentation)*

## Exit criteria

Same as the [core playbook Phase 3](../playbook/03-design.md), plus:

- [ ] At least two approaches were spiked before choosing
- [ ] Prototype code is deleted or clearly quarantined from production
- [ ] Design decision note exists, signed by a human
