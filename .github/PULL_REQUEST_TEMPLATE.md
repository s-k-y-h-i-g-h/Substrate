# Pull Request Template — Substrate

## Description

Brief summary of the change and why it's needed.

---

## Type of Change

- [ ] Protocol update (ingredient, dose, evidence tier) — requires PROTOCOL/SPEC.md + substrate_stack.yaml sync
- [ ] Governance change (articles, CIC filing, director details)
- [ ] Partnership update (MOU template, onboarding, partner registry)
- [ ] Operations (distribution, AE, data handling)
- [ ] Finance (budget, donation processing, accounts)
- [ ] Pilot (design, results, lessons learned)
- [ ] Documentation (README, CONTRIBUTING, etc.)
- [ ] Infrastructure (GitHub, CI, tooling)

---

## Evidence / Rationale

- **Protocol changes:** Cite evidence tier and source (RCT DOI, Cochrane review, etc.)
- **Governance changes:** Reference CIC Regulator guidance or legal advice
- **Operations:** Reference partner feedback or incident log
- **Finance:** Reference bank statement / invoice / grant agreement

---

## Checklist

- [ ] All markdown renders correctly on GitHub
- [ ] YAML files are valid (run `yamllint` or equivalent)
- [ ] Protocol version bumped in `PROTOCOL/substrate_stack.yaml` + `PROTOCOL/SPEC.md` if ingredients/doses changed
- [ ] Changelog entry added to relevant SPEC.md
- [ ] No personal data (names, addresses, NHS numbers) in this PR
- [ ] No private keys, API tokens, or bank details
- [ ] If protocol change: reviewed by at least one director + one external reviewer (name in PR description)

---

## Reviewers

@[director] (required for protocol, governance, finance)  
@[external-reviewer] (required for protocol)

---

## Notes for Maintainers

- This repo is the single source of truth for Substrate governance and protocol.
- Private data (partner contacts, AE details, accounts) lives in gitignored directories and is NOT committed.
- All public-facing documents are CC-BY-4.0; code/YAML is MIT.