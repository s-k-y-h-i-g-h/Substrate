# Pilot Design — Substrate v0.1 Pilot

## Objective

Validate that the Substrate Core 5 stack can be:  
(a) procured in bulk to cost target,  
(b) distributed through a partner shelter,  
(c) accepted and taken by intended recipients,  
(d) tracked for uptake without compromising privacy.

## Budget

### ⚠️ The original £500 pilot could not be executed

A previous draft budgeted ~£140 for Core 5 stock for 100 people × 30 days. That implies
**£0.047 per daily unit** — roughly one-tenth of the cheapest cost target anywhere in this
repository. The figure appears to have been carried over without checking it against
`PROTOCOL/SPEC.md`.

Two cost tables currently disagree, and **which is correct is unknown until suppliers are actually
quoted** — see `PROTOCOL/procurement.md`.

| Source | Core 5 per daily unit |
|--------|----------------------|
| `PROTOCOL/SPEC.md` (conservative targets) | £0.70 |
| `PROTOCOL/procurement.md` (10k bulk estimates) | £0.47 |

**Minimum order quantity is the binding constraint, not per-unit cost.** Buying to MOQ costs
**~£6,550** whether the pilot serves 10 people or 100, because the MOQs are 10,000 / 10,000 / 5,000 /
10,000 / 20,000 units. A £500 budget cannot buy this stack at any cohort size.

### Revised pilot design: supplier-funded sample run

The pilot is restructured as a **sample-and-validate run**, not a purchased-stock run.

1. **Request supplier samples and pilot pricing first.** GMP suppliers and distributors routinely
   donate or discount sample quantities to legitimate new programmes, especially where the applicant
   brings an open protocol, published evidence grading, and a named research purpose. Substrate has all
   three. This is the normal first step for a first pilot, not a favour to ask for.
2. **If samples are granted**, run the full 100-person × 30-day design at near-zero ingredient cost.
   The rest of the original budget stands.
3. **If samples are refused**, the pilot requires **~£7,000** for stock at MOQ and cannot be a £500
   pilot. It must be funded as a separate, larger round — or narrowed to fewer ingredients, since
   Core 5 at MOQ is what breaks the budget.

### Revised budget

| Line | Sample run | If purchased at MOQ |
|------|-----------|---------------------|
| Core 5 ingredients | £0 (supplier samples) | ~£6,550 |
| Packaging (labels, boxes) | ~£60 | ~£60 |
| Partner coordination | ~£100 | ~£100 |
| AE buffer | ~£100 | ~£100 |
| Contingency / admin | ~£50 | ~£50 |
| **Total** | **~£310** | **~£6,860** |

**Original £450/£500 target:** achievable only on the sample path. Delete it from any funding
conversation that has not confirmed samples in writing.

## Partner

[One UK homeless shelter or day centre. Criteria:  
- Currently conducts nutritional support or food provision  
- Has supervised distribution process (staff on-site)  
- Willing to sign MOU per PARTNERSHIPS/partnership_framework.md  
- Has storage facility (cool, dry)]

**Target: one partner, single site.**

## Kit design

- Individual daily sachets: Core 5 combined
- One month = 30 sachets in labelled sleeve per participant
- Batch code and expiry on every sachet
- "Take with food" reminder on label

## Recipient flow

1. Partner staff introduces program to eligible residents (verbal explanation + written flyer)
2. Eligible person opts in. Staff records: date of first collection only. No name retained.
3. Person collects sachets from designated point — self-serve or supervised
4. Staff marks daily count on tally sheet (paper)
5. End of month: staff returns completed tally + unused sachets

## Data collected (minimum viable)

| Field | Who records | Format | Retention |
|-------|------------|--------|-----------|
| Date | Partner staff | Paper tally | 6 months, then destroyed |
| Sachets distributed that day | Partner staff | Count only | 6 months |
| Uptake estimate | Partner staff | Count returned vs. issued | 6 months |
| Adverse events (any) | Partner staff | AE form | Ongoing; report to Substrate within 24h |

**No names. No NHS numbers. No individual health data.**

## Adverse event procedure

See `OPERATIONS/adverse_event_reporting.md`. Pilot-level escalation:
- Partner calls Substrate director directly (number provided)
- Substrate responds within 24h
- If hospitalisation suspected: partner calls NHS 111 + Substrate simultaneously

## Timeline

| Week | Activity |
|------|----------|
| W1 | Confirm partner MOU; order supplements; print labels |
| W2 | Receive stock; quality check; pack month kits |
| W3 | Partner training session (1 hr, on-site) |
| W4 | Go live — first distribution week |
| W5-7 | Active distribution; weekly check-in call with partner |
| W8 | Collect tally sheets; de-brief partner; write up results |

## Success criteria

- 80%+ of monthly kits collected by at least 30 distinct recipients
- <3 adverse events reported (any severity)
- Partner satisfied enough to agree to Phase 2 (3 months, 3 sites)
- Cost per person per month within 20% of target (£0.70/head/day)

## Outputs

1. `PILOT/pilot_log_template.md` — completed tally (anonymised summary only published)
2. `PILOT/pilot_results.md` — write-up within 2 weeks of pilot close
3. Updated protocol (if ingredients adjusted)
4. Partner testimonial (with consent)

---

**Pilot sponsor:** Substrate CIC board  
**Review date:** 2026-09-30 (after 4-week go-live)