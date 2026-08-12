# The frameworks, broken down

Plain-English key points of each source this playbook is built on, and what each one is *for*. None of these replaces the others — they cover different layers: **risk** (NIST), **organisation** (ISO), **delivery** (DORA), **craft** (Anthropic), **law** (regulation).

---

## 1. NIST AI Risk Management Framework (AI RMF)

**What it is:** A voluntary framework from the US National Institute of Standards and Technology (2023) for identifying and managing AI risks, extended in 2024 with a **Generative AI Profile** covering LLM-specific risks. Free to read and cite. The most common shared vocabulary for AI risk worldwide.

**The four functions:**

1. **Govern** *(cross-cutting — runs through everything)* — Build a culture and structure where AI risk is someone's job: policies exist, roles are assigned, accountability is clear, and workers can raise concerns.
2. **Map** — Before building, establish context: what is this system for, who uses it, who could be harmed, what could go wrong? You can't manage a risk you haven't named.
3. **Measure** — Test and track the risks you mapped: evaluate performance, robustness, bias, and safety with defined methods and thresholds — not vibes.
4. **Manage** — Act on what you measured: prioritise risks, mitigate or accept them deliberately, monitor in production, respond to incidents, and know when to switch a system off.

**Generative-AI-specific risks the 2024 profile adds:** confabulation (confident false output), data privacy leakage, harmful bias, information integrity (misuse for misinformation), over-reliance by users, and unstable behaviour when the underlying model changes.

**Use it for:** the risk backbone. Phases 1–2 are Map/Govern, Phase 5 is Measure, Phase 7 is Manage.

---

## 2. ISO/IEC 42001:2023

**What it is:** The first international, *certifiable* standard for an AI Management System (AIMS) — the organisational machinery around AI, not the model itself. Anthropic holds this certification. The standard's text is paywalled; the structure below is what matters practically.

**Key points:**

1. **Leadership owns it** — top management is accountable for AI policy and outcomes; it can't be delegated to an enthusiastic engineer.
2. **Plan–Do–Check–Act** — the whole standard is a continuous improvement loop, not a one-off audit.
3. **AI impact assessment** — formally assess how each AI system could affect individuals, groups, and society *before and during* its life.
4. **Lifecycle documentation** — record design decisions, data provenance, and changes across the system's whole life, including retirement.
5. **Third-party control** — you remain responsible for AI capability you buy in (model APIs, vendors, datasets).
6. **Defined controls** — an annex of concrete controls covering policies, roles, resources, data quality, transparency to users, and responsible use.

**Use it for:** proving the organisation behind the product is sound. Phase 2 is mostly ISO territory; documentation and review habits throughout come from here.

---

## 3. DORA / *Accelerate*

**What it is:** A decade-plus research program (published in the book *Accelerate*, continued as Google Cloud's DORA reports) measuring what actually distinguishes high-performing software teams, with data from tens of thousands of teams. Not AI-specific — it's the delivery engine underneath.

**The four key metrics:**

1. **Deployment frequency** — how often you ship to production.
2. **Lead time for changes** — commit to running-in-production time.
3. **Change failure rate** — what fraction of deploys cause a failure.
4. **Failed-deployment recovery time** — how fast you restore service.

**The headline finding:** speed and stability are **not** a trade-off — elite teams ship more often *and* break less, because small frequent changes are easier to test, review, and roll back than big ones.

**The capabilities that drive those metrics:** continuous integration, trunk-based development (no long-lived branches), automated testing, working in small batches, loosely coupled architecture, and a generative culture where messengers aren't shot.

**Use it for:** Phases 4, 6 and 7 — how to build, ship, and operate. For AI products, "small batches" extends to prompts, evals, and model configs, not just code.

---

## 4. Anthropic's published guidance

**What it is:** Practitioner guidance published by Anthropic — most notably *Building Effective Agents* (2024), plus prompt engineering and evaluation documentation. Written about Claude, but the principles are provider-agnostic and this playbook applies them neutrally.

**Key points:**

1. **Start with the simplest pattern that works.** A single well-crafted prompt beats a workflow; a workflow (fixed steps: chaining, routing, parallelisation) beats an autonomous agent. Add autonomy only when the task genuinely can't be predefined — complexity costs money, latency, and debuggability.
2. **Design evals before (or while) you build, not after.** A small set of real test cases with graded criteria is worth more than a demo that impressed the CEO once.
3. **Prompts and tools are engineered artefacts.** Version them, review them, test them like code. Clear instructions, good examples, and well-documented tools move quality more than model choice usually does.
4. **Keep humans in the loop where stakes are high.** Checkpoints where a person reviews or approves are a design feature, not an admission of failure.
5. **Transparency in the product.** Show your sources, expose uncertainty, make it easy for users to correct the system.

**Use it for:** Phases 3–5 — the craft of designing, building, and evaluating the AI itself.

---

## 5. Regulation (the ⚕ overlay)

**What it is:** Not a framework — law. Included because two things are true: (a) the EU AI Act now applies broadly to systems touching EU users, and (b) health-tech products (clinical scribes, telehealth, diagnostics) can be regulated as **software-as-a-medical-device** by the TGA (Australia) or FDA (US).

**Key points:**

1. **EU AI Act uses risk tiers:** prohibited practices (e.g. social scoring), high-risk (strict obligations: risk management, logging, human oversight, conformity assessment), transparency-tier (users must know they're talking to AI), and minimal risk. Know your tier *before* you build.
2. **"Is it a medical device?" is a legal question, not a product decision.** Software that diagnoses, treats, or informs clinical decisions may need TGA/FDA classification, clinical evidence, and quality-system requirements.
3. **Timing matters:** classification determines your evidence burden, and clinical validation can dwarf the build effort. Finding out at launch is the expensive way.

**Use it for:** the ⚕-marked overlay steps in Phases 1, 2, 5, 6 and 7. This playbook flags *when* to get regulatory advice — it is not that advice.
