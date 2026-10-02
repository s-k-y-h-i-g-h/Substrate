# Evidence Grading Criteria — Substrate Protocol

## Tier Definitions

| Tier | Criteria | Required evidence |
|------|----------|-------------------|
| **T1** | Published RCT in the population the claim is made to | Full-text RCT, peer-reviewed, n>30 |
| **T2** | RCT in general adult population + consistent observational support | ≥2 independent RCTs or 1 large RCT + meta-analysis |
| **T3** | Strong mechanistic rationale + human data | RCT in specific condition OR large observational study |
| **T4** | Mechanistic in vitro/animal OR traditional use | Animal model OR traditional medicine use OR human case series |
| **T5** | Anecdotal / theoretical | No controlled human data; mechanistic only |

**On "the population the claim is made to."** Substrate makes claims to two populations, and the
higher grade is taken against whichever claim is being made:

- For the **poverty-relief** limb (objects clause (a)), a claim needs T1 evidence in homeless,
  addiction-recovery, or financially excluded populations specifically.
- For the **public-education** limb (objects clause (b)), a claim is addressed to the general public,
  so T1 means an RCT in a general adult population.

A T2 grade against the general population may support a public-education claim but does **not** support
the same claim made to a population with elevated deficiency risk. Substrate does not let one grade
launder the other.

**Conflict rule.** Where an ingredient is graded on the basis of general-population evidence but the
targeted-supply population is likely to differ (nutritional status, polypharmacy, organ function), the
lower of the two available grades applies to any distribution under limb (a), and the discrepancy is
recorded in the ingredient's spec entry.

## Application rules

- **Core 5 ingredients must be T2 or better** at time of inclusion.
- **Longevity tier ingredients must be T2 or T3.** T4 ingredients require a 12-month review cycle commitment.
- **Cognitive tier ingredients may be T3 or T4**, but T4 ingredients must carry an explicit monitoring commitment: "Substrate will track adverse events and review evidence every 12 months; formulation will be suspended if no T3+ evidence emerges within 24 months."
- **No T5 ingredients.** Anecdote does not meet the bar.

## Evidence review cycle

- Annual protocol review by at least one director + one external reviewer (clinical or pharmacological).
- Evidence downgrade triggers: new safety signal in any population, RCT showing null effect, regulatory warning from MHRA/EMA/FDA.
- Evidence upgrade triggers: new RCT in target population, meta-analysis confirming effect size.

## Sources considered authoritative

Priority order:
1. Cochrane reviews
2. Systematic reviews / meta-analyses (PRISMA-compliant)
3. Individual RCTs (registered, published)
4. Observational studies (prospective, controlled)
5. Mechanistic studies (human, in vivo)
6. In vitro / animal studies

Sources below these may be cited for rationale only, never as primary support:
- Examine.com (aggregator — trace to primary sources)
- Medscape (review articles — trace to sources)
- Vendor product pages — never accepted as primary evidence

For substance safety: Trust is TripSit, PsychonautWiki, PubChem, FDA labels, DailyMed, EMA EPARs — in that order.

**Maintained as part of PROTOCOL/SPEC.md governance.**