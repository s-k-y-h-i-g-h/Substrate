# Pilot Design — Substrate v0.1 Pilot

## Objective

Validate that the Substrate Core 5 stack can be:  
(a) procured in bulk to cost target,  
(b) distributed through a partner shelter,  
(c) accepted and taken by intended recipients,  
(d) tracked for uptake without compromising privacy.

## Budget

| Line | Amount |
|------|--------|
| Core 5 sachets (100 people x 30 days, bulk) | ~£140 |
| Packaging (print sachet labels, boxes) | ~£60 |
| Partner coordination (travel, meeting time) | ~£100 |
| AE buffer (medical contingency) | ~£100 |
| Contingency / admin | ~£50 |
| **Total target** | **~£450** |
| **Slippage buffer** | **Up to £500** |

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