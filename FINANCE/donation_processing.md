# Donation Processing — Substrate CIC

## UK Donations (Gift Aid eligible)

### Flow

```
Donor → Stripe/Gocardless (Substrate CIC merchant) → CIC bank account
         ↓
    Gift Aid declaration collected (name, address, postcode, "I am a UK taxpayer")
         ↓
    Substrate submits Gift Aid claim to HMRC quarterly via fiscal host
         ↓
    HMRC pays 25% top-up → CIC bank account
```

### Fiscal Host for Gift Aid

Substrate CIC is **not** a registered charity. Gift Aid requires charitable status.

**Approach:** Partner with a registered UK charity (e.g., food bank network, homelessness charity) that acts as fiscal host for Gift Aid.

- Donor gives to Substrate
- Substrate passes donation to fiscal host
- Fiscal host claims Gift Aid, takes small admin fee (3-5%)
- Fiscal host grants net + Gift Aid to Substrate as restricted grant

**Template:** `FINANCE/fiscal_host_mou.md` (to be drafted)

### Donor data required for Gift Aid

- Full name
- Home address (including postcode)
- Declaration: "I confirm I am a UK Income Tax or Capital Gains Tax payer..."
- Date of declaration

*No other donor data is required or retained.*

---

## International Donations (Non-Gift Aid)

### US Donors

- Route via US fiscal sponsor (e.g., **Fractured Atlas**, **Open Collective Foundation**, **The Giving Block**) for 501c3 tax deductibility
- Substrate operates as a "project" under their umbrella
- Fiscal sponsor takes 5-8% fee; donor gets US tax receipt
- Substrate receives grant payments from fiscal sponsor

### EU/Rest of World

- Direct donation to Substrate CIC Stripe/Gocardless (no tax benefit for donor)
- Or route through local fiscal sponsor if available

### Cryptocurrency

- Accepted via **The Giving Block** (handles UK/US/International, issues tax receipts)
- Fee: 3.95% + gas
- Auto-converts to GBP to CIC bank account

---

## Bank Account

**Requirements:**
- CIC-friendly (Starling, Monzo Business, Tide, Metro Bank)
- API access (for automated reconciliation → bookkeeping)
- Multi-currency (for US/EU donor receipts)
- Separate from personal accounts

**Setup:** Within 2 weeks of CIC incorporation (certificate of incorporation + CIC36 filed)

---

## Reconciliation

- Monthly: export Stripe/Gocardless/fiscal sponsor CSV → import to accounting software (QuickBooks/Xero/FreeAgent)
- Quarterly: Gift Aid claim to HMRC via fiscal host
- Annually: accounts prepared for CIC34 filing + Companies House

---

## Transparency

Published quarterly (see `OPERATIONS/data_handling.md`):
- Total donations received (by channel)
- Gross amount, fees, net to programme
- Gift Aid claimed / received
- Programme spend % of total donations