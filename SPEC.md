# Spec: Substrate Phase 1 — Foundation Complete

## Objective

Build Substrate CIC to operational readiness on two fronts:

1. **Targeted supply** — a £500 pilot of evidence-based supplement distribution to homeless populations in the UK, validating bulk procurement at cost target, distribution through partner shelters, recipient uptake, and adverse event tracking, without compromising recipient privacy.
2. **Public education** — published, free, plain-language guidance on evidence-based nutrition, biohacking, and longevity interventions for a general public with no relationship to any beneficiary group, covering what the evidence supports, what it does not, dosing, contraindications, and interactions.

**Success (front 1):** The CIC is filed, the first partner MOU is signed, the pilot kit is procured and distributed, and a de-identified outcome report is published. All within 8 weeks of project start.

**Success (front 2):** The protocol, evidence grading, and contraindications are published as open documentation that anyone can read, reuse, and redistribute without permission or cost — and the evidence base is strong enough that publishing it to the general public is defensible rather than reckless.

---

## Current State

All documentation is drafted and pushed to GitHub. No code exists yet (this is a policy/org project, not a software project). The repo contains:

| Directory | Status | Next step |
|-----------|--------|-----------|
| `GOVERNANCE/` | CIC36 objects clause + articles clauses drafted | File with Companies House |
| `PROTOCOL/` | SPEC.md + substrate_stack.yaml (v0.1) | Peer review before first distribution |
| `PARTNERSHIPS/` | MOU framework + onboarding checklist | Sign first partner |
| `PILOT/` | £500 pilot design, log template | Confirm partner, order stock |
| `OPERATIONS/` | AE reporting, GDPR data handling, distribution protocol | Operational when partner signs |
| `FINANCE/` | Budget template + donation processing | Open bank account |
| `.github/` | CI/CD pipeline, PR template | Active |

---

## Tech Stack

This is a **documentation-first, policy-driven project** — not a software product. No codebase to build. The "technology" is the protocol specification (YAML), the governance framework (Markdown), and the operational procedures (Markdown).

- **Protocol:** YAML (`PROTOCOL/substrate_stack.yaml`) — versioned, machine-readable supplement stack
- **Governance:** Markdown (CIC objects clause, articles) — legal text filed with Companies House
- **Documentation:** Markdown + GitHub-flavoured Markdown — version-controlled specs
- **CI/CD:** GitHub Actions (dependabot, PR templates) — already configured
- **License:** CC-BY-4.0 (docs) / MIT (code/YAML)

---

## Commands

```bash
# Validate protocol YAML
python3 -c "import yaml; yaml.safe_load(open('PROTOCOL/substrate_stack.yaml'))"

# Validate all YAML in repo
python3 -c "
import yaml, glob
for f in glob.glob('**/*.yaml', recursive=True):
    with open(f) as fh:
        data = yaml.safe_load(fh)
    print(f'{f}: OK')
"

# Build budget subtotals
python3 -c "
import yaml
with open('FINANCE/budget_template.yaml') as f:
    d = yaml.safe_load(f)
for k, v in d.items():
    if isinstance(v, dict) and 'amount' in v and not k.endswith('_subtotal'):
        print(f'  {k}: {v.get(\"amount\", \"?\")}')
"
```

---

## Project Structure

```
Substrate/
├── README.md                     # Project overview
├── GOVERNANCE/
│   ├── CIC36_objects_clause.md   # Companies House filing text
│   ├── articles_clauses.md       # Director pay, conflicts, asset lock
│   └── directors_register.md     # Director details (private, gitignored)
├── PROTOCOL/
│   ├── SPEC.md                    # Human-readable protocol
│   ├── substrate_stack.yaml       # Machine-readable stack (source of truth)
│   ├── evidence_grading.md        # Evidence tier definitions
│   └── procurement.md             # Sourcing, CoA, supplier targets
├── PARTNERSHIPS/
│   ├── partnership_framework.md   # MOU template for local orgs
│   └── partner_onboarding_checklist.md
├── PILOT/
│   ├── pilot_design.md            # £500 UK pilot plan
│   └── pilot_log_template.md      # Distribution + uptake log
├── OPERATIONS/
│   ├── distribution_protocol.md   # Packing, labelling, shelf life
│   ├── adverse_event_reporting.md # AE form + escalation matrix
│   └── data_handling.md           # GDPR, anonymisation, retention
├── FINANCE/
│   ├── budget_template.yaml       # Annual + pilot budgets
│   ├── donation_processing.md     # Stripe/Gocardless + Gift Aid
│   └── accounts/                  # Financial records (gitignored)
└── .github/
    ├── dependabot.yml
    └── PULL_REQUEST_TEMPLATE.md
```

---

## Code Style

Not applicable — this is documentation, not code. Style conventions:
- **Markdown:** Standard GitHub-flavoured Markdown. Use ASCII-only (no emoji) for GitHub rendering compatibility.
- **YAML:** Two-space indent, ordered keys within blocks, comments use `#` prefix.
- **Structure:** Every file starts with a `# Title` header, a one-line description, and a `---` separator.
- **References:** Use relative links (`[text](path)`) within the repo.
- **Evidence citations:** Inline `T2`, `T3`, etc. with a trailing note to `evidence_grading.md` for tier definitions.
- **Cost targets:** Stated in GBP with per-unit cost at stated bulk volume (e.g., "<£0.12/unit at 10,000-unit bulk").

---

## Testing Strategy

| Level | What | How |
|-------|------|-----|
| **YAML validation** | Protocol file is parseable | `python3 -c "import yaml; yaml.safe_load(...)"` |
| **Schema compliance** | All required keys present in YAML | Static check against field list in SPEC.md |
| **Cross-reference** | SPEC.md dose values match substrate_stack.yaml | Grep/diff check |
| **Financial** | Budget template fills correctly | Python parse + subtotal verification |
| **Legal** | Articles clauses cover required CIC provisions | Manual review (lawyer sign-off needed) |
| **Privacy** | No PII in any public doc | Manual grep for names, NHS numbers, DOBs |

---

## Boundaries

| Always do | Ask first | Never do |
|-----------|-----------|----------|
| Keep docs in sync with YAML | Change ingredient dosing without evidence | Remove harm-reduction framing |
| Update README status table on milestone change | Add new ingredients without version bump | Change cost targets without budget review |
| Validate YAML on every commit | Alter the AE reporting SLA | Accept PII from partners |
| Review docs for GDPR compliance before sharing | Restructure the governance model | Make legal claims without lawyer review |

---

## Success Criteria

| Criterion | How we know it's done |
|-----------|----------------------|
| CIC filed at Companies House | Companies House public record shows Substrate CIC, status "Active" |
| Bank account opened | Bank provides account number; funds can be transferred |
| First partner MOU signed | Signed PDF returned; partner agrees to term and data terms |
| Core 5 sachets procured at target cost | Purchase order placed + invoice received showing per-unit cost |
| Partner trained | Training log completed (date, participant, topics) |
| First distribution week complete | Partner confirms distribution; tally sheet returned |
| Adverse events logged (if any) | AE register entry (de-identified) or "zero events" confirmation |
| Pilot results published | `PILOT/pilot_results.md` committed to repo |

---

## Open Questions

| Question | Owner | Decision needed |
|----------|-------|-----------------|
| Which partner organisation? | Skyhigh (PM) | Name and location confirmed |
| What's the CIC registered office address? | Skyhigh (PM) | Physical address for filing |
| Who are the directors? | Skyhigh (PM) | Names and addresses for Companies House |
| Does partner require a Data Sharing Agreement (DSA) in addition to MOU? | Partner | Legal review of data handling terms |
| What's the partner's preferred delivery schedule (weekly/monthly)? | Partner | Operational planning |
| Should we set up Gift Aid from day one or start without? | Skyhigh (PM) | Finance decision |
| Which bank for the business account? | Skyhigh (PM) | Application |

---

## Phase 1 Task Breakdown

See `tasks/plan.md` and `tasks/todo.md` for the decomposed task list. Summary:

1. **CIC formation** — File Companies House, open bank account
2. **Partner acquisition** — Identify shelter, negotiate MOU, sign
3. **Supplier engagement** — Request quotes from 3+ suppliers per ingredient, negotiate CoA requirements
4. **Procurement** — Order Core 5 sachets at target cost
5. **Pilot execution** — Pack, deliver, train, distribute, collect data
6. **Pilot close** — Results write-up, de-brief, plan Phase 2
