# Privacy-Friendly Payments

> Open Privacy · v0.1 · July 2026 · Poorvith M P  
> Category ID: `25-payments-privacy`  
> Replaces: Putting one card/identity on every site and subscription

---

## Primary recommendation

| Field | Value |
|---|---|
| **Name** | Cash + minimize stored cards (with privacy cards where available) |
| **Website** | N/A (practice) + regional privacy card providers where legal |
| **Source / repo** | N/A — operational practice; tools vary by country |
| **Open source?** | **Practice** — supporting tools may be proprietary |
| **Local / self-host?** | **Yes** for cash/local transfers; cards are external |
| **Target audience** | Everyday users reducing payment-data exhaust |
| **Platforms** | Real world · banking apps · optional virtual card services |
| **Pricing** | Free practice; card services may charge |
| **Payment notes** | Prefer cash/UPI QR for local commerce when sensible; avoid saving cards on random sites |

### Why this is the one pick
1. Most “payment privacy” is behavior, not an app install.
2. Cash and direct bank transfers leave less marketing graph than every-site card vaults.
3. Works in India-friendly daily life (cash/UPI) without forcing a US-only product.
4. Scales from low-tech to advanced (virtual cards/crypto) as needed.
5. Avoids recommending a single global fintech as if it fits everyone.

### What it does not do
- Does not make you anonymous to your bank.
- UPI/bank rails still identify you to financial institutions.
- Not legal/tax advice.

---

## Install guide (primary)

### Download hubs
- No single download — configure habits + optional tools below

### Windows
1. Remove saved cards from browsers (browser settings → payment methods).
2. Use bank official apps/sites only; enable 2FA.
3. For online subscriptions, prefer one dedicated card/virtual card—not your primary savings card.

### macOS
1. Clear Safari/Chrome/Brave saved cards you do not need.
2. Disable autofill of payment methods where possible.
3. Same dedicated-card strategy for subscriptions.

### Linux
1. Clear browser payment autofill.
2. Prefer direct bank transfers/UPI from official apps over random card gateways when available.
3. Keep financial CSV exports offline/encrypted if stored.

### Android
1. Use official banking/UPI apps from trusted stores.
2. Disable screenshot/notifications content for banking apps if supported.
3. Avoid giving payment apps contacts/SMS permissions unless required.

### iOS
1. Review Wallet/saved cards; remove unused cards.
2. Use official bank apps.
3. Prefer Face ID/strong device passcode for finance apps.

### First-run checklist
1. Stop saving cards on e-commerce sites by default.
2. Use unique emails/aliases per merchant (see `04-email-aliasing`).
3. Monitor statements monthly for mystery subscriptions.

---

## Catches of the primary → one alternative each

| Catch | Why it bites | Alternative (one) | Open source? | Platforms | When not to switch |
|---|---|---|---|---|---|
| Need virtual cards that mask PAN from merchants (where available) | Cash/UPI doesn’t cover all online foreign SaaS | **Privacy.com** (US-focused) or local bank virtual cards | No | Web · apps | Don’t use if unavailable in your country—use bank virtual cards instead |
| Need stronger payment unlinkability and accept crypto complexity | Banks always know fiat identity | **Monero (Cake Wallet)** | Wallet OSS varies | Mobile · desktop | Not for everyday regulated bills; legal compliance required |
| Need private-ish online checkout inside Proton/browser stack | Ecosystem preference | **Mask card via bank + Proton Pass card form fill carefully** | Partial | Apps | Still avoid storing CVV in random sites |

### Alternative installs

#### Privacy.com / bank virtual cards
- Only from official provider sites/apps in supported regions
- India: check whether your bank offers virtual/temporary card numbers

#### Cake Wallet (Monero)
- https://cakewallet.com — install official apps only; learn wallet backup seed offline

#### Bank virtual cards
- Use your bank’s official app documentation for virtual card creation

---

## Local open-source path

| Field | Value |
|---|---|
| **Name** | Cash accounting offline + optional FOSS finance tracker (e.g. GnuCash / AppManager exports) |
| **Repo** | https://www.gnucash.org (optional ledger) |
| **What local means** | Spending records not in a consumer data-broker budget app |
| **Who it’s for** | Users tracking money without fintech upsell apps |
| **Ops burden** | Low–Medium |
| **When primary still wins** | Primary is already a local-first practice |

### Local install
- Optional: install GnuCash from https://www.gnucash.org/download.phtml on Windows/macOS/Linux
- Keep backups encrypted

---

## Quick decision box

```text
Default payment privacy              →  Cash/UPI + no saved cards everywhere
Virtual cards (if available)         →  Bank virtual card / Privacy.com
Crypto unlinkability (advanced)      →  Monero (Cake Wallet)
Local bookkeeping                    →  GnuCash
```
