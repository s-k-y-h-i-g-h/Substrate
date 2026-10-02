# Contributing to Substrate

## Welcome

Substrate is open infrastructure for public health. Contributions are welcome from anyone who supports evidence-based, harm-reduction-first approaches to nutritional support.

Two things are true at once, and contributions should respect both:

- **We supply people who need it most** — free-of-charge product and protocol to people experiencing homelessness, addiction recovery, or financial exclusion, through partner organisations.
- **We publish for everyone** — the protocol, evidence grading, contraindications, and reasoning are free and public, for people who will never need a partner organisation and will never meet us.

The second is not a marketing function for the first. It is the same documentation, published to a wider audience, on the belief that a public able to evaluate longevity claims is a public better able to advocate for people who cannot.

**A word of caution for contributors.** Moving from supplying a defined, often nutritionally deficient population to educating a general audience raises the evidence bar rather than lowering it. The same sentence that is responsible in a shelter may be irresponsible in a forum. See `PROTOCOL/evidence_grading.md` for the two-limb grading rule this creates.

---

## Where to contribute

### Public education (`PROTOCOL/`, `EDUCATION/`)

Open an issue first with:
- The claim you want to make, and to which audience (general public, or targeted-supply population)
- Evidence tier claimed (T1–T5) **for that audience specifically**
- Evidence source (Cochrane review DOI, PubMed ID, or similar)
- Plain-language restatement, and a contraindications/interactions warning

Worse evidence claims are reviewed more strictly, not less. A T4 ingredient promoted to a general
audience needs a director + external reviewer sign-off and a monitoring commitment; the same ingredient
in a research note does not.

### Protocol updates (`PROTOCOL/`)

Open an issue first with:
- Proposed change (add / remove / adjust dose / change ingredient form)
- Evidence tier claimed (T1-T5)
- Evidence source (Cochrane review DOI, PubMed ID, or similar)
- Rationale for inclusion in Substrate Stack

A director + an external reviewer must approve before merge.

### Governance (`GOVERNANCE/`)

Discuss in an issue before submitting a PR. Governance changes affect the legal structure — they need careful review.

### Partnerships (`PARTNERSHIPS/`)

Propose MOUs, onboarding checklists, or partner-facing templates. Real partner data must NOT be committed — see `.gitignore`.

### Operations (`OPERATIONS/`)

Distribution protocol, AE process, data handling. PRs welcome, especially from anyone with experience in humanitarian or shelter operations.

### Finance (`FINANCE/`)

Templates and processes. No actual financial data — that lives in gitignored private directories.

### Pilot (`PILOT/`)

Pilot design documents are public. Pilot results that include data on recipients MUST be anonymised (no names, no identifying details).

---

## Style guide

- Markdown for prose, YAML for machine-readable definitions
- ASCII-compatible markers only (use `[OK]`, `[WARN]`, `[INFO]`, etc., not emoji)
- Commit messages: conventional commits format (`feat:`, `fix:`, `docs:`, `chore:`)
- All commits signed (PGP or SSH)

---

## Code of Conduct

Substrate operates on a harm-reduction basis. We:

- Treat recipients as people, not beneficiaries
- Acknowledge lived experience as expertise
- Resist paternalism, medical overconfidence, and wellness gatekeeping
- Disagree on evidence, not identity

Harassment, bigotry, or weapons-grade ignorance about addiction, homelessness, or mental health is not welcome and will be removed.

---

## Licence

By contributing, you agree that your contributions will be licensed under CC-BY-4.0 (documentation) or MIT (code/YAML), matching the existing repo licence.

---

## Contact

Issues: [github.com/s-k-y-h-i-g-h/Substrate/issues](https://github.com/s-k-y-h-i-g-h/Substrate/issues)  
Email: substrate-board@substrate.org.uk (placeholder, to be set on filing)