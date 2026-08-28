# Task Plan — Substrate Phase 1

## Overview

Phase 1 decomposes the success criteria into discrete, trackable tasks. Each task is completable in a single focused session. Dependencies are sequential where they must be; parallel where they can be.

---

## Task Dependency Graph

```
T-pre02: Seek CIC filing guidance from support contacts (review prior rejection)
T01: Choose CIC registered office address
T02: File Companies House CIC (depends on T-pre02 + T01)
T03: Open business bank account (depends on T02)
T04: Identify first partner organisation
T05: Negotiate and sign MOU (depends on T04)
T06: Request supplier quotes for Core 5 ingredients (depends on T05)
T07: Negotiate supplier terms / CoA requirements (depends on T06)
T08: Place order for Core 5 sachets (depends on T07)
T09: Pack and label pilot kits (depends on T08)
T10: Conduct partner training session (depends on T09)
T11: Execute first distribution week (depends on T10)
T12: Collect uptake data and AE reports (depends on T11)
T13: Write pilot results (depends on T12)
T14: Decide Phase 2 scope (depends on T13)
```

---

## Pre-Filing Guidance Task

### T-pre02: Seek CIC filing guidance from support contacts

**Background:** A previous CIC application was rejected. Before re-submitting, get external review of the CIC36 and articles to identify and fix the rejection cause.

**Contacts to approach:**

| Contact | Type | Details | Best for |
|---------|------|---------|----------|
| **CIC Regulator** | Government regulator | Email: `cicregulator@companieshouse.gov.uk` / Phone: `029 2150 7420` | Pre-submission review of CIC36 + articles; asking why a prior application was rejected |
| **Companies House Business Support** | Government helpline | Phone: `0303 123 4500` | Step-by-step guidance on the online filing form; not legal advice, but can confirm form correctness |
| **Norfolk Citizens Advice** | Free local advice | Website: `ncab.org.uk` / Office: 83-87 Pottergate, Norwich | Free confidential advice on business/legal matters; may have CIC formation experience |
| **New Anglia Growth Hub** | Local business support | Norfolk/Suffolk business support | Free/low-cost CIC workshops or signposting to local social-enterprise advisors |
| **Low-cost formation agent** | Paid service | Coddan / 1stchoice-formations / Rapid Formations (~£100-£200) | Full handling of filing; knows exact format the Regulator expects |

**Recommended approach:**
1. Contact CIC Regulator first — email them explaining you previously had a CIC application rejected and ask for guidance on what to fix before re-submitting.
2. If no response within 5 working days, call Companies House Business Support.
3. If still unresolved, contact Norfolk Citizens Advice for free local guidance.
4. As a fallback, engage a low-cost formation agent to handle filing and ensure format compliance.

**Acceptance:** Either (a) prior rejection cause identified and fixed in docs, or (b) filing delegated to formation agent with confirmation they've reviewed the application.
**Verify:** Email/notes from CIC Regulator, or formation agent confirmation, or Citizens Advice case reference.
**Files:** `GOVERNANCE/CIC36_objects_clause.md`, `GOVERNANCE/articles_clauses.md` (updated if rejection cause requires changes)
**Dependencies:** T01 (registered office must be confirmed before filing guidance, as it appears in the docs)

---

## Task List

### T01: Choose CIC registered office address

- **Acceptance:** Physical address decided; email and phone for Companies House filing
- **Verify:** Address confirmed by user
- **Files:** (none)

### T02: File Companies House CIC

**Process (online Companies House filing):**
1. Go to `https://www.tax.service.gov.uk/register-your-company/setting-up-new-limited-company`
2. Complete IN01 online form: company name "Substrate CIC", type (limited by guarantee), registered office (42a High Street, Downham Market, PE38 9HH)
3. Upload CIC36 as PDF — text from `GOVERNANCE/CIC36_objects_clause.md`
4. Upload Articles of Association as PDF — text from `GOVERNANCE/articles_clauses.md`
5. Pay £115 filing fee (card)
6. Complete identity verification ( Companies House requires this for new filings)
7. Verify on Companies House public register

**Fee:** £115 online (not £35 — that's for annual CIC report filing)
**Timeline:** 2-5 working days online, up to 15 working days by post

**Acceptance:** Companies House public record shows Substrate CIC, status "Active", CIC36 objects clause and articles filed
**Dependencies:** T01

### T03: Open business bank account

- **Acceptance:** Bank provides account number; Sort Code; SWIFT/BIC
- **Verify:** Can receive and transfer funds
- **Files:** (none)
- **Dependencies:** T02

### T04: Identify first partner organisation

- **Acceptance:** Name, location, and contact person confirmed; partner meets eligibility criteria
- **Verify:** Partner confirms interest; MOU signed within 2 weeks
- **Files:** `PARTNERSHIPS/partner_registry.yaml` (to be created)
- **Dependencies:** (none)

### T05: Negotiate and sign MOU

- **Acceptance:** Signed MOU returned; partner agrees to 12-month term, data terms, AE reporting
- **Verify:** Signed PDF in repo or partner confirmation email
- **Files:** `PARTNERSHIPS/` MOU files
- **Dependencies:** T04

### T06: Request supplier quotes for Core 5 ingredients

- **Acceptance:** Quotes received for 5 Core 5 ingredients at stated bulk volumes
- **Verify:** Minimum 3 quotes per ingredient; all within cost targets
- **Files:** `PROCUREMENT/` (directory to be created)
- **Dependencies:** T05

### T07: Negotiate supplier terms / CoA requirements

- **Acceptance:** Supplier confirms CoA per batch; shelf life >60 days on receipt; bulk pricing locked
- **Verify:** Written supplier agreement or email confirmation
- **Files:** `PROCUREMENT/`
- **Dependencies:** T06

### T08: Place order for Core 5 sachets

- **Acceptance:** Purchase order placed; invoice received; per-unit cost confirmed within target
- **Verify:** Invoice shows actual per-unit cost < target for each ingredient
- **Files:** `FINANCE/accounts/`
- **Dependencies:** T07

### T09: Pack and label pilot kits

- **Acceptance:** 100 monthly kits packed; each with 30 daily sachets; labels printed; batch codes and expiry visible
- **Verify:** Physical inspection; photo documentation
- **Files:** `PILOT/`
- **Dependencies:** T08

### T10: Conduct partner training session

- **Acceptance:** Training log completed (date, who attended, topics covered)
- **Verify:** Training log signed by partner staff
- **Files:** `PILOT/` training log
- **Dependencies:** T09

### T11: Execute first distribution week

- **Acceptance:** First distribution week completed; tally sheets returned; any AE incidents logged
- **Verify:** Tally sheets in repo; AE register entry (or zero-events confirmation)
- **Files:** `PILOT/` pilot log
- **Dependencies:** T10

### T12: Collect uptake data and AE reports

- **Acceptance:** All monthly data collected; AE register updated; partner de-brief conducted
- **Verify:** Data completeness check; partner sign-off on data return
- **Files:** `PILOT/` pilot log; `OPERATIONS/` AE register
- **Dependencies:** T11

### T13: Write pilot results

- **Acceptance:** `PILOT/pilot_results.md` written and committed; includes uptake rates, AE summary, cost per person, partner feedback
- **Verify:** File exists in repo; content covers all success criteria
- **Files:** `PILOT/pilot_results.md`
- **Dependencies:** T12

### T14: Decide Phase 2 scope

- **Acceptance:** Decision made: proceed to 3-month / 3-site Phase 2, or pause for iteration
- **Verify:** Board decision recorded (minutes or email)
- **Files:** `PILOT/`
- **Dependencies:** T13

---

## Task Status

| Task | Title | Status |
|------|-------|--------|
| T01 | Choose CIC registered office address | [ALERT] Not started |
| T02 | File Companies House CIC36 | Not started |
| T03 | Open business bank account | Not started |
| T04 | Identify first partner organisation | Not started |
| T05 | Negotiate and sign MOU | Not started |
| T06 | Request supplier quotes for Core 5 | Not started |
| T07 | Negotiate supplier terms / CoA | Not started |
| T08 | Place order for Core 5 sachets | Not started |
| T09 | Pack and label pilot kits | Not started |
| T10 | Conduct partner training session | Not started |
| T11 | Execute first distribution week | Not started |
| T12 | Collect uptake data and AE reports | Not started |
| T13 | Write pilot results | Not started |
| T14 | Decide Phase 2 scope | Not started |

---

## Parallelism Notes

- T01–T03 are sequential (formation dependencies)
- T04–T05 can run in parallel with T01–T03 (partnership is independent of CIC formation)
- T06–T08 are sequential (quotes → negotiate → order)
- T09–T11 are sequential (pack → train → distribute)
- T12–T14 are sequential (collect → write → decide)
- T04/T05 and T01/T02/T03 can proceed in parallel

---

## Definition of Done (per task)

Each task is complete when:
1. All acceptance criteria are met
2. Relevant files are updated or created in the repo
3. The task status is moved to [OK] in this table
4. No blocking issues remain for dependent tasks
