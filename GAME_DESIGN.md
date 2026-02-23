# European Warmblood Dynasty (Infinite Codex Edition)

An infinite-year, data-driven stud farm simulation for Codex play.

## 1) Core Concept

You run a European warmblood breeding operation with no fixed end date. You balance:

- Cash flow and debt
- Breeding quality and fertility risk
- Development vs early sales
- Reputation and client trust
- Market cycles and yearly random shocks

The game is intentionally pressure-heavy in early years and rewards long-term strategy.

---

## 2) Win/Loss States

Because the game is infinite, there is no final "victory screen." Instead:

### Legacy Milestones (optional achievements)

- **Foundation Stable**: Net worth €500,000+
- **Serious Breeder**: 8+ broodmares
- **Sport Credibility**: 1 horse actively competing 1.40m+
- **Financial Stability**: Positive annual profit for 3 consecutive years
- **Elite Brand**: Reputation 400+
- **Global Prestige**: Reputation 900+

### Failure State

- **Forced liquidation** if cash is negative for **2 consecutive years**.

---

## 3) Custom Setup (Flexible Starting Cash)

Pick one preset or set any custom starting capital:

| Start Mode | Cash | Loan Access | Starting Reputation |
|---|---:|---|---:|
| Survival | €25,000 | Small loan only | 5 |
| Small Breeder | €100,000 | Medium loan | 10 |
| Investor Backed | €300,000 | Large loan | 20 |
| Dynasty | €750,000 | Premium banking | 35 |
| Custom | Any € | Collateral-based | Background-based |

### Region Modifier

| Region | Feed/Labor/Land Cost Pressure | Sale Price Modifier |
|---|---|---:|
| Eastern EU | Low | x0.90 |
| Central EU | Medium | x1.00 |
| Western EU | High | x1.20 |

---

## 4) Infrastructure System

You may lease or buy facilities.

| Facility | Cost | Capacity/Effect |
|---|---:|---|
| Basic Stable | €60,000 | 8 stalls |
| Professional Stable | €140,000 | 16 stalls |
| Elite Stable | €300,000 | 32 stalls |
| Indoor Arena | €120,000 | Enables reliable winter training |
| Breeding Wing | €50,000 | +10% fertility chance |
| Vet Station | €40,000 | -20% emergency vet event costs |

- **Annual maintenance** = 3% of total building value.

---

## 5) Horse Attribute Model

Each horse has permanent attributes (1–10):

- Conformation
- Movement
- Scope
- Rideability
- Temperament
- Soundness
- Bloodline Prestige

### Discipline Quality Score

Use one of:

- **Jumping quality** = (Conformation + Scope + Rideability) / 3
- **Dressage quality** = (Conformation + Movement + Rideability) / 3

### Injury Risk

- Annual injury risk baseline: `(10 - Soundness) x 2%`

---

## 6) Breeding Mechanics

### Broodmare Rules

- Breedable age: **3 to 18** years only
- Fertility range: **50%–90%**
- Complication risk: **5%–20%**

### Stud Tiers

| Tier | Typical Fee | Stat Quality |
|---|---:|---|
| Local | €1,500 | 5–6 |
| Approved | €8,000 | 7–8 |
| Elite Licensed | €20,000+ | 9–10 |

### Pregnancy Roll

Roll 1–100 each breeding attempt:

- Pregnant if `roll <= effective fertility`

Where:

`effective fertility = mare fertility + breeding wing bonus + event modifiers`

### Foal Quality

1. Start from average of mare and stud discipline stats.
2. Add random variation **-2 to +2**.
3. Add bloodline modifier (typically -1 to +1).
4. Add reputation influence (small, usually 0 to +1 for elite farms).
5. 2% mutation chance: +2 to one random key stat.

### Foal Mortality

- Base 3% mortality risk
- Reduced by Vet Station

---

## 7) Development & Training

### Life Stages

- 0–1: Foal
- 2–3: Youngstock
- 3–4: Backing
- 5–7: Competition development
- 8+: Peak performance

### Training Investment (per horse/year)

| Level | Cost | Improvement Chance |
|---|---:|---|
| Basic | €3,000 | Small |
| Professional | €8,000 | Medium |
| Elite Rider Program | €20,000 | High |

Stat gain roll (1–10):

- 1–3: no gain
- 4–7: +1 primary stat
- 8–10: +1 primary and +1 secondary stat

---

## 8) Sales Valuation Engine

### Base Value

- Foal: `Quality x €4,000`
- 3yo: `Quality x €10,000`
- 5yo with results: `Quality x €18,000`

### Adders

- +€5,000 per competition win
- +€15,000 if actively jumping 1.40m+
- +€25,000 if FEI level

### Multipliers

- Reputation multiplier: `1 + (reputation / 150)`
- Region multiplier: from setup table
- Market multiplier: yearly market roll

### Sale Price Formula

`Final Sale = (Base + Adders) x Reputation x Region x Market`

---

## 9) Reputation System (0–1000)

Start based on setup mode.

### Positive

- High-quality sales
- Verified competition outcomes
- Approved breeding stock
- International repeat buyers

### Negative

- Selling unsound horses
- Disease or welfare scandals
- Contract defaults
- Bankruptcy-related distress sales

### Reputation Gates

| Reputation | Unlock |
|---:|---|
| 200+ | Elite stallion access |
| 400+ | Investor partnerships |
| 700+ | National team rider interest |
| 900+ | Global prestige tier |

---

## 10) Global Market (Yearly Roll)

Roll 1–6 each year:

| Roll | Market State | Effect |
|---:|---|---:|
| 1 | Recession | -25% sale value |
| 2 | Weak | -10% sale value |
| 3–4 | Stable | No modifier |
| 5 | Growth | +15% sale value |
| 6 | Luxury Demand | +30% for elite horses |

---

## 11) Random Event Engine (Yearly Roll 1–20)

Examples:

- Colic emergency (€12,000)
- Mare infertility year
- Rich foreign buyer
- Sponsor offer
- Land tax increase
- Disease quarantine
- Government subsidy
- Olympic spotlight demand boost

Recommended: keep event table in a dedicated data tab so you can add custom events infinitely.

---

## 12) Finance & Debt

- Loan interest: 4–9% depending on reputation/risk.
- Liquidity ratio target: cash >= 10% of total assets.
- If debt > 70% of assets, trigger bank pressure events.
- Negative cash for 2 consecutive years => forced liquidation.

---

## 13) Expansion Paths (Infinite Loop)

Optional business lines:

- Boarding stable
- Sales agency
- Young horse training center
- Stallion station
- International branch
- Sponsored rider team
- National training hub

No cap on years: this is a perpetual management cycle.

---

## 14) Realistic Difficulty Rules

- Can sell max 50% of total stock per year.
- Must keep at least 2 young horses in development.
- No breeding mares younger than 3 or older than 18.
- Optional hardcore: VAT/tax, welfare audits, insurance mandates, import restrictions.

---

## 15) Required Tracking Tabs (Spreadsheet/Data Model)

1. Cash Flow (monthly)
2. Horses
3. Breeding Records
4. Sales
5. Reputation
6. Market Conditions
7. Challenges Log
8. Training Log
9. Competition Results
10. Asset Valuation
11. Debt & Liabilities
12. **Actions** (new command center tab)

---

## 16) Actions Tab (Auction Module, up to 30 Horses)

This tab is the interactive command center where you list horses for NPC bidding.

### 16.1 Listing Rules

- Max **30 active auction listings** at a time.
- Must still obey annual stock sale limit (max 50% stock/year).
- Unsoundness disclosure required (soundness < 6 must be flagged).

### 16.2 Actions Tab Columns

| Field | Description |
|---|---|
| Auction ID | Unique ID |
| Horse ID | Linked horse from Horses tab |
| Age | Auto-pulled |
| Discipline | Jumping/Dressage/Eventing |
| Quality Score | Auto-calculated |
| Temperament | Auto-pulled |
| Soundness | Auto-pulled |
| Competition Record | Wins / level |
| Reputation Tier | Farm rep bracket |
| Reserve Price € | Minimum accepted |
| Start Price € | Opening bid |
| Bid Increment € | Minimum raise |
| Auction Length (days) | 3 / 5 / 7 / 10 |
| NPC Interest Score | Derived demand score |
| Total Bids | Count |
| Highest Bid € | Live top bid |
| Winner NPC | Buyer profile |
| Final Sale € | Settled price |
| Status | Draft / Live / Sold / Unsold |

### 16.3 Reserve Price Guidance (Realistic)

Set reserve from estimated fair value:

`reserve = fair market value x [0.85 to 1.05]`

- Young/unproven: 0.85–0.95
- Reliable amateur horse: 0.95–1.00
- Elite sport horse: 1.00–1.05

### 16.4 NPC Buyer Types

| NPC Type | Budget | Preference |
|---|---:|---|
| Amateur Rider | €8k–€45k | Temperament 7+, safe horses |
| Junior Ambition Family | €20k–€90k | Rideability + bloodline |
| Professional Yard | €50k–€250k | Scope, results, resale margin |
| Investor Syndicate | €80k–€500k | Elite upside, pedigree |
| International Dealer | €30k–€300k | Margin + market timing |

### 16.5 NPC Interest Score

Use 0–100 score before each auction:

`Interest = Quality*4 + Temperament*2 + Soundness*2 + RecordScore + ReputationBand + MarketBand - OverpricingPenalty`

Suggested components:

- RecordScore: 0 to 20
- ReputationBand: 0 to 15
- MarketBand: -15 to +15
- OverpricingPenalty: 0 to 25

### 16.6 Bid Generation Logic (per auction day)

1. Determine active NPC pool from horse profile.
2. For each NPC, roll participation chance from Interest Score.
3. If they bid, bid amount = `current bid + increment x aggression factor`.
4. Stop when:
   - no NPC can exceed current bid, or
   - budget ceilings reached, or
   - auction timer ends.

Aggression factor guideline:

- Conservative NPC: 1.0x–1.5x increment
- Neutral NPC: 1.5x–3.0x increment
- Competitive NPC: 3.0x–6.0x increment

### 16.7 Anti-Unrealistic Pricing Safeguards

- Hard cap bid at 130% of model fair value unless horse is FEI/1.40m+.
- If reserve > 120% of fair value, reduce bidder participation heavily.
- If horse has hidden risk (low soundness), chance of post-sale dispute event.

### 16.8 Auction Outcomes

- If highest bid >= reserve: Sold.
- If highest bid < reserve: Unsold (option to relist with lower reserve).
- Rich client event can add +20% top bid ceiling for one auction.

### 16.9 Payout Timing

- 10% deposit immediately
- Remaining 90% clears in 7–21 days
- 2% transaction fee deducted
- Optional failed-payment risk (1–3%) on weak-market years

---

## 17) Core Horse Table Template

| ID | Name | Age | Sex | Breed | Conformation | Movement | Scope | Rideability | Temperament | Soundness | Bloodline | Discipline | Quality | Value € |
|---|---|---:|---|---|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|

---

## 18) Core Broodmare Table Template

| Mare | Age | Quality | Bloodline Score | Fertility % | Stud Used | Stud Fee € | Pregnant? | Foal Quality | Complication? |
|---|---:|---:|---:|---:|---|---:|---|---:|---|

---

## 19) Core Expense Table Template

Per horse per year baseline:

| Expense | Cost |
|---|---:|
| Feed | €3,000 |
| Farrier | €1,200 |
| Vet Routine | €1,500 |
| Insurance | €1,000 |
| Training (optional base) | €6,000 |

Additional:

- Broodmare with foal: +€1,000
- Stable worker: €28,000/year
- Professional rider: €45,000/year

---

## 20) Year Loop (Infinite Engine)

Repeat forever:

1. Roll market
2. Roll event
3. Decide breeding plan
4. Decide training investment
5. Run competitions
6. Open auctions (Actions tab, max 30 listings)
7. Settle sales & receivables
8. Pay yearly costs, debt, maintenance
9. Update reputation
10. Revalue assets and compute net worth
11. Check bankruptcy condition
12. Advance year

---

## 21) Codex Play Mode (Recommended)

For each year, Codex should output:

- Updated tables (all tabs)
- Event and market roll details
- Cash flow summary (income/expense/profit)
- Balance sheet snapshot (assets/debt/net worth)
- Compliance checks (sale cap, young horse minimum, breeding ages)
- Strategic recommendation for next year

This structure supports infinite simulation with transparent, auditable numbers.
