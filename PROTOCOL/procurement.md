# Procurement Specification — Substrate Stack

## Supplier Requirements

All suppliers must satisfy ALL of the following before any order is placed.

### Mandatory

| Requirement | Standard |
|-------------|----------|
| Certificate of Analysis (CoA) | Per batch, from ISO 17025 or GMP-certified lab. Not a vendor self-certificate. |
| Manufacturing standard | GMP (UK/EU) or equivalent. MHRA-licensed facility preferred for UK supply. |
| Shelf life on delivery | Minimum 12 months remaining |
| Allergen declaration | Per batch; major allergens stated on COA |
| Heavy metals testing | Arsenic, cadmium, lead, mercury — each below USP <232> limits or equivalent |
| Oxidation testing | For oils: peroxide value <5 meq/kg; TOTOX <26 (IFOS or equivalent) |
| Identity testing | FTIR or HPLC fingerprint confirming raw material identity |
| Batch traceability | Full batch record: supplier, manufacturer, expiry, lot number |

### Preferred

| Requirement | Notes |
|-------------|-------|
| IFOS 5-star | For Omega-3 products |
| Creapure certification | For creatine |
| Vegan/vegetarian variant | Available for all Core 5 items |
| UK fulfilment | To avoid import delays and suspend import VAT |

---

## Sourcing strategy

### Primary: UK bulk supplement wholesalers

Targets:
- **Bulk Powders** / **SWISS Service GmbH** (Germany, ships UK) — broad range, GMP, per-batch CoA available on request
- **Thorne** / **Pure Encapsulations** UK distribution — higher price, highest quality assurance; suitable for first small run
- **Healthfloor** (UK) — NIC-approved, MHRA-adjacent, good for B-complex and D3
- **Direct manufacturer** — for costs above £5k order: approach Jarrow, Life Extension, NOW Foods direct UK

### Secondary: EU wholesale (Brexit-adjusted)

- EU suppliers viable for orders <£2000 with DDP (Delivered Duty Paid) terms
- Expect customs paperwork; hold 2-3 weeks longer lead time
- Post-Brexit: supplement import requires UKCA marking or MHRA notification for novel food ingredients (check EAC list)

---

## Cost targets at scale

| Ingredient | Unit £ (100-unit) | Unit £ (10,000-unit bulk) | Current supplier |
|------------|-------------------|--------------------------|-----------------|
| D3+K2 | ~£0.25 | ~£0.08 | Healthfloor (est.) |
| Mg glycinate | ~£0.20 | ~£0.06 | Bulk Powders |
| Omega-3 | ~£0.60 | ~£0.18 | IFOS-certified source |
| B-complex methyl | ~£0.40 | ~£0.10 | Thorne/Pure Encaps |
| Creatine | ~£0.15 | ~£0.05 | Creapure direct |
| NAC | ~£0.20 | ~£0.06 | Bulk Powders |
| Glycine | ~£0.15 | ~£0.04 | Bulk Powders |
| Taurine | ~£0.10 | ~£0.03 | Bulk Powders |
| Spermidine | ~£0.60 | ~£0.35 | Wheat germ extract (specialist) |
| CDP-Choline | ~£0.40 | ~£0.12 | Bulk Powders |
| ALCAR | ~£0.30 | ~£0.08 | Bulk Powders |
| Lion's Mane | ~£0.50 | ~£0.18 | Bulk Powders |

**Core 5 unit cost (10k bulk): ~£0.47/day** (vs ~£1.20/day via retail)  
**12-month pilot (100 people, 365 days): ~£17,200** (ingredients only; packaging + logistics +0% margin on top)

### ⚠️ Unreconciled: two cost tables disagree

`PROTOCOL/SPEC.md` states Core 5 unit-cost **targets** that sum to **£0.70/daily unit**. The table above
estimates **£0.47**. Neither is confirmed by an actual supplier quote. Until T07 produces real quotes,
**treat £0.47 as unverified and budget against £0.70.**

This matters more than it looks: the difference between the two tables is ~£690 over a 3,000-unit pilot,
and the MOQ floor below means the true minimum spend is ~£6,550 regardless of cohort size. Any budget
built on the £0.47 figure before quotes exist is not safe.

**Resolution:** T07 must record, per ingredient: quoted price, MOQ, achieved unit cost, and whether the
quote was per-kilo or per-unit. Re-run the pilot budget from those numbers, not from this table.

### Minimum order quantity is the binding constraint

| Ingredient | MOQ | Cost at MOQ |
|------------|-----|-------------|
| D3+K2 | 10,000 | ~£800–1,200 |
| Mg glycinate | 10,000 | ~£600–1,000 |
| Omega-3 | 5,000 | ~£900–1,250 |
| B-complex methyl | 10,000 | ~£1,000–1,500 |
| Creatine | 20,000 | ~£1,000–1,600 |
| **Total** | | **~£4,300–6,550** |

A pilot cannot be sized below the MOQ. Cohort size does not change the purchase price; it only changes
consumption rate. This is why `PILOT/pilot_design.md` is restructured around supplier samples.

---

## Sample and pilot-pricing requests

**Try this before any purchase.** GMP suppliers and raw-material distributors routinely donate or
discount sample quantities to legitimate new programmes, especially where the applicant brings:

- A written protocol with ingredient, dose, and contraindication per unit
- Published, graded evidence with an external review commitment
- A named partner distribution channel
- A defined pilot design with uptake and AE tracking

Substrate meets all four. Sample requests cost nothing and are the normal first step for a first pilot.

Record every response — granted, declined, or price quoted — in the pilot log. A supplier who declines
free samples may offer pilot pricing; that is the fallback path, and it should be in the budget from
the start rather than discovered at T08.

**Never distribute any sample or purchased lot without its matching Certificate of Analysis on file.**

---

## Ordering workflow

1. Director approves order (written, tabled in meeting or signed email)
2. Product list exported from `PROTOCOL/substrate_stack.yaml` version matching current protocol
3. Request RFQ from 2-3 approved suppliers; compare CoA quality + unit cost.
   **Also request pilot pricing or free samples at this step** — see "Sample and pilot-pricing
   requests" above. Record the response either way.
4. Reconcile quotes against both cost tables in this file and `PROTOCOL/SPEC.md`, and update
   `PILOT/pilot_design.md` from the real numbers before committing spend
5. Place order; supplier acknowledges batch number and estimated delivery date
6. On receipt: verify CoA, check expiry, inspect packaging. No lot ships to a partner without its CoA filed
7. Stock logged to inventory (paper log acceptable at pilot stage; spreadsheet or inventory system for scale)

---

## Prohibited suppliers

- No Direct-from-Alibaba/Amazon unbranded products without ISO-lab CoA
- No supplier who cannot provide batch traceability
- No ingredient with Novel Food status in UK without FSA notification review

---

**Maintained by:** Operations team  
**Review date:** 2027-02-27