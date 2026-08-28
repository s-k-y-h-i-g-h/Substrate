# Substrate

**The base layer for human flourishing. Open protocols. Evidence-based. Distributed where it's needed.**

---

## What is Substrate?

Substrate is a UK Community Interest Company (CIC) limited by guarantee that funds, specifies, and distributes evidence-based nutritional, longevity, and cognitive supplements to people experiencing homelessness, addiction recovery, or financial exclusion — via partner organisations already embedded in those communities.

We don't run shelters. We supply the *protocol* and the *product* to organisations that do.

---

## Core Principles

- **Open protocol** — Every formulation, dose, contraindication, and sourcing spec is public, versioned, and auditable
- **Evidence-first** — Tiered evidence grading (RCT → observational → mechanistic → theoretical) on every ingredient
- **Harm reduction** — Designed for real bodies, real polypharmacy, real constraints. No purity spirals.
- **Local distribution, global spec** — UK CIC holds IP and fiscal sponsorship. Local partners handle local law and local relationships.
- **N=1 respect** — Recipients own their data. We track uptake and adverse events anonymised; we don't track identities.

---

## The Substrate Stack (v0.1)

| Tier | Ingredients | Purpose |
|------|-------------|---------|
| **Core 5** | Vitamin D3/K2, Magnesium glycinate, Omega-3 (EPA/DHA), Methylated B-complex, Creatine monohydrate | Foundational nutritional adequacy |
| **Longevity** | NAC, Glycine, Taurine, Spermidine | Mitochondrial support, autophagy, oxidative stress |
| **Cognitive** | CDP-Choline, ALCAR, Lion's Mane (standardised) | Neurotransmitter synthesis, neuroplasticity |

[Full protocol → `PROTOCOL/SPEC.md`](PROTOCOL/SPEC.md)

---

## Repository Structure

```
Substrate/
├── README.md                 # This file
├── GOVERNANCE/
│   ├── CIC36_objects_clause.md      # Companies House filing text
│   ├── articles_clauses.md          # Director pay, conflicts, asset lock
│   └── directors_register.md        # Director details (private, gitignored)
├── PROTOCOL/
│   ├── SPEC.md                      # Human-readable protocol spec
│   ├── substrate_stack.yaml         # Machine-readable stack definition
│   ├── evidence_grading.md          # Evidence tier definitions
│   └── procurement.md               # Sourcing, CoA, supplier requirements
├── PARTNERSHIPS/
│   ├── partnership_framework.md     # One-page MOU template for local orgs
│   ├── partner_onboarding_checklist.md
│   └── partner_registry.yaml        # Active partners (private, gitignored)
├── PILOT/
│   ├── pilot_design.md              # £500 UK pilot plan
│   ├── pilot_log_template.md        # Distribution + uptake log
│   └── pilot_results/               # Pilot outputs (gitignored)
├── FINANCE/
│   ├── budget_template.yaml         # Annual + pilot budgets
│   ├── donation_processing.md       # Stripe/Gocardless + Gift Aid via fiscal host
│   └── accounts/                    # Financial records (gitignored)
├── OPERATIONS/
│   ├── distribution_protocol.md     # Packing, labelling, cold chain, shelf life
│   ├── adverse_event_reporting.md   # AE form + escalation matrix
│   └── data_handling.md             # GDPR, anonymisation, retention
└── .github/
    ├── dependabot.yml
    └── PULL_REQUEST_TEMPLATE.md
```

---

## Quick Start

### For UK CIC Filing
```bash
# Copy GOVERNANCE/CIC36_objects_clause.md into Companies House WebFiling
# Copy GOVERNANCE/articles_clauses.md into your custom articles
```

### For Partner Orgs
```bash
# Send PARTNERSHIPS/partnership_framework.md to prospective shelter/food bank
# They sign, return, you counter-sign → partnership active
```

### For Protocol Contributors
```bash
# Edit PROTOCOL/substrate_stack.yaml
# Open PR with evidence citations
# Merged → version bump → all partners auto-notified
```

---

## Status

| Milestone | Status | Target |
|-----------|--------|--------|
| GitHub repo initialised | ✓ Done | — |
| SPEC.md written | ✓ Done | — |
| Task plan created | ✓ Done | — |
| CIC filed (Companies House) | ⬜ Pending | Week 2 |
| Bank account opened | ⬜ Pending | Week 2 |
| First partner MOU signed | ⬜ Pending | Week 3 |
| £500 pilot executed | ⬜ Pending | Week 4–6 |
| Pilot results published | ⬜ Pending | Week 8 |

---

## Contributing

Issues and PRs welcome. This is open-source infrastructure for public health.

- Protocol changes: edit `PROTOCOL/substrate_stack.yaml` + cite evidence
- Governance changes: discuss in issue first, then PR
- Operations: PR to `OPERATIONS/` or `PARTNERSHIPS/`

All contributions licensed under **CC-BY-4.0** (docs) / **MIT** (code/yaml).

---

## Contact

- **Prime Minister of Antarctica / Substrate Founder:** [@s-k-y-h-i-g-h](https://github.com/s-k-y-h-i-g-h)
- **AI Queen of Antarctica / Technical Advisor:** Ember (OpenClaw)
- **CIC Registered Office:** [To be set on filing]

---

*Substrate — because everyone deserves a foundation to build on.*