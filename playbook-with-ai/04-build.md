# Phase 4 — Build (pair with AI without losing the plot)

**What AI changes here:** everything and nothing. Code appears ten times faster. Every discipline that kept quality up now matters ten times more. This is the phase where DORA's warning lives: individual speed up, team stability down, unless the habits hold.

## Steps

1. **Give the AI context before asking for code.** A short conventions file in the repo: how this codebase is structured, naming patterns, what to avoid, how tests run. Ten minutes of setup, and every AI session starts smart instead of generic.
   *(Anthropic: context and project conventions make AI-assisted coding dramatically better)*

2. **Plan first, then generate.** Ask for a plan before asking for code. Read the plan. Fix the plan. Then let it build. Reviewing a plan takes two minutes; untangling wrong code takes an hour.
   *(Anthropic: plan-then-execute; DORA: small batches start with small intentions)*

3. **Keep batches small, especially now.** AI makes it easy to generate a week of code in an hour. Don't merge a week of code in an hour. Same rule as ever: small changes, merged often, each one reviewed and tested. This is the single habit DORA's data says protects stability as AI speeds you up.
   *(DORA: small batches, continuous integration, AI adoption findings)*

4. **Never merge code you don't understand.** The rule that makes all the others work. If you can't explain a change to a teammate, you can't review it, debug it, or own it in an incident. Ask the AI to explain it until you can, or rewrite it simpler.
   *(Accountability rule from Phase 2; ISO 42001: human accountability)*

5. **Review AI code like a senior reviews a junior.** It's fast, confident, sometimes brilliant, and sometimes confidently wrong in ways a tired human wouldn't be. Watch for: invented functions, subtly wrong edge cases, unnecessary complexity, and copied patterns that don't fit your codebase.
   *(Anthropic: review everything; NIST GAI Profile: confabulation)*

6. **Let CI be the referee.** Tests and checks run on every merge, no exceptions for AI-written code, no exceptions for human-written code. A green build is the shared definition of "probably fine".
   *(DORA: continuous integration and automated testing)*

## Exit criteria

- [ ] CI runs tests on every merge, and main is always in a shippable state
- [ ] Conventions file exists and AI sessions use it
- [ ] No merged change bigger than the team can genuinely review
- [ ] Every merge has a named human who understands and owns it
- [ ] Secrets live in a secret manager, never in code or prompts
