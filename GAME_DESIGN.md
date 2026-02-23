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

## 20) Time System (Infinite + Month-Skippable)

The game runs in continuous years, but all operations are processed by month so players can skip time in realistic increments.

### 20.1 Calendar Model

- 1 year = 12 months
- You can advance by: **1 month**, **3 months (quarter)**, **6 months**, or **12 months**
- Long skips auto-run intermediate checks (injury, staffing, cash burn, contracts, pregnancies, auctions)

### 20.2 Monthly Tick (Auto-Processed)

Each month resolves in this order:

1. Payroll and fixed farm overhead
2. Feed/farrier/vet routine accrual
3. Training progress and fatigue updates
4. Competition entries/results in scheduled months
5. Breeding/pregnancy checks when in breeding windows
6. Auctions and receivable settlements
7. Random monthly events (light events)
8. Cash + debt interest update

### 20.3 Time Skip Safeguards

When skipping multiple months:

- Contract expiries still trigger on exact month
- Horses cannot exceed welfare-safe competition frequency
- If liquidity falls below 10% assets, bank pressure warning is injected immediately
- If negative cash occurs, bankruptcy counter updates by year-end status

### 20.4 Seasonal Structure

- Indoor season (typically winter)
- Outdoor season (spring/summer)
- Championship months

This supports realistic planning for training and show timing.

---

## 21) Year Loop (Infinite Engine)

Repeat forever:

1. Run 12 monthly ticks (or player-selected month skips)
2. Roll annual market state
3. Roll annual major event
4. Set annual breeding strategy
5. Set annual training and competition plan
6. Open/manage auctions (Actions tab, max 30 listings)
7. Settle annual receivables/payables and taxes (if enabled)
8. Recompute staff morale, loyalty, and retention risk
9. Update reputation and global brand rank
10. Revalue assets and compute net worth
11. Run compliance checks (sale cap, development minimums, breeding age rules)
12. Check bankruptcy condition and advance year

---

## 22) Staff Hiring System (Full Depth)

Every staff member has tracked attributes:

| Attribute | Range | Affects |
|---|---|---|
| Skill Level | 1–10 | Performance quality |
| Experience | Years | Salary expectation and consistency |
| Loyalty | 1–10 | Leaving/poaching risk |
| Reputation | 1–10 | Client attraction and premium confidence |
| Work Ethic | 1–10 | Horse development speed |
| Demandingness | 1–10 | Salary growth pressure |

### 22.1 Staff Roles

#### Stable Worker

- Salary: **€22,000–€35,000/year**
- Required ratio: **1 per 8 horses**
- Effect: lowers injury probability and supports soundness retention
- Understaffing penalty: **+5% injury risk per missing worker**

#### Professional Rider

- Salary: **€40,000–€120,000/year**
- Training Gain Modifier: `1 + (Skill / 20)`
- Example: Skill 8 => 1.40x training growth
- If rider reputation 8+: horses they campaign gain **+5% sale price**

#### Breeding Manager

- Salary: **€45,000–€90,000/year**
- Effects:
  - +10–25% fertility boost
  - -50% foal mortality risk
  - +1 foal stat reroll per year

#### Sales & Marketing Director

- Salary: **€35,000–€80,000/year**
- Effects:
  - Faster reputation growth
  - +10–30% sale speed
  - +5–15% sale price multiplier

#### On-Site Vet (Elite Farms)

- Salary: **€70,000–€150,000/year**
- Effects:
  - -60% emergency vet costs
  - -70% mortality risk
  - +2 yearly soundness retention (capped by horse max)

### 22.2 Staff Development and Morale

- Skill progression: +1 skill every 3 years when morale is strong
- Morale formula:

`Morale = (Loyalty + WorkConditions + SalarySatisfaction) / 3`

- If morale < 5: 30% annual quit chance
- If farm reputation > 400: high-skill applicant pool unlocked

### 22.3 Contract System

Contract options:

- 1-year (flexible, low commitment)
- 3-year (loyalty bonus)
- 5-year (salary lock)

Rules:

- Early termination penalty = 50% of remaining salary
- High reputation can trigger poaching events for top riders

### 22.4 Strategy Trade-Off

- Lean team = lower costs, higher operational risk
- Heavy team = better horse outcomes, higher burn rate

---

## 23) International Expansion System

Unlock requirements:

- Reputation > 300
- Net worth > €1,000,000

### 23.1 Expansion Regions

| Tier | Setup Cost | Operating Cost | Sale Multiplier |
|---|---:|---|---:|
| Eastern Europe | €150,000 | Low | x0.90 |
| Central Europe | €300,000 | Medium | x1.00 |
| Western Europe | €600,000 | High | x1.25 |
| Elite Hub | €1,200,000 | Very High | x1.50 |

Typical targets: Germany, Netherlands, Belgium.

Elite hub grants:

- Premium buyer access
- Higher show and media exposure

### 23.2 Multi-Barn Management

Every branch tracks:

- Staff roster
- Horse count
- Local reputation
- Operating cost
- Specialization (breeding/sales/competition)

Global reputation formula:

`Global Reputation = (HQ Reputation x 0.7) + (Branch Average x 0.3)`

### 23.3 Export/Import

- Export logistics cost: €5,000 per horse
- Transport injury risk: 2% base (reduced with vet coverage)
- International sale value bonus: +10–20%

### 23.4 Global Brand Milestones

- Reputation 500: sponsor offers
- Reputation 700: international investors
- Reputation 900: Olympic spotlight year chance

### 23.5 Expansion Risks

Each additional branch adds:

- +10% management complexity
- Increased administrative cost
- Audit/legal exposure

Potential events: tax audits, local outbreaks, political instability, land crashes, investor lawsuits.

---

## 24) Competition System (Global Performance Ladder)

Compatible with breeding, staffing, and international mechanics.

### 24.1 Disciplines

- Dressage (movement, rideability, temperament)
- Show Jumping (scope, reflexes/scope proxy, soundness)
- Eventing (dressage + jumping + stamina proxy + soundness)

### 24.2 Competition Levels

| Level | Typical Age | Use Case |
|---|---:|---|
| Training Shows | 3–4 | Local preparation |
| Young Horse Classes | 4–6 | Development and branding |
| National | 5+ | Core competitive proving |
| International | 6+ | High-performance exposure |
| Elite / Grand Prix | 8+ | Top-tier commercial/sport value |

### 24.3 Entry Cost Model

| Tier | Entry Fee |
|---|---:|
| Local | €200 |
| National | €500 |
| International | €2,000 |
| Elite | €5,000+ |

Travel cost per show: €1,000–€10,000 by distance class.

### 24.4 Performance Score

`Performance Score = (HorseDisciplineStat x 2) + RiderSkill + TrainingModifier + RandomFactor`

Random factor engine (1–20 roll):

- 1–3: underperformance
- 4–16: normal
- 17–19: strong round
- 20: breakthrough round

### 24.5 Placements

Use score percentile versus field difficulty:

- Top 10%: Win
- Top 25%: Placing
- Mid: Average
- Low: Poor
- Very low: Elimination

### 24.6 Reputation and Value Effects

- International win: +20 reputation
- Top 3: +10
- Placing: +5
- Elimination: -5

Performance multipliers for horse value:

| Result Profile | Value Multiplier |
|---|---:|
| No show record | x1.0 |
| National placing | x1.2 |
| International win | x1.5 |
| Elite win | x2.0+ |

### 24.7 Fatigue and Recovery

- Each show adds fatigue and can reduce soundness by 1–2
- If fatigue > 8: apply performance penalty
- Mandatory 1-month rest after elite competition

### 24.8 Elite Pathway

For 1.50m+/Grand Prix track, horse should have:

- Discipline stat 8+
- Soundness 7+
- Temperament 7+
- At least 2 successful seasons

### 24.9 Prize Money

| Level | Prize Pool |
|---|---:|
| National | €1,000–€5,000 |
| International | €5,000–€50,000 |
| Elite | €50,000–€500,000 |

---

## 25) Required Additional Sheets

Add these tabs to support advanced systems:

- Staff Database
- Contracts Log
- Barn Branch Sheet
- International Sales Sheet
- Sponsor & Investor Log
- Competition Calendar
- Horse Performance Log
- Prize Money Tracker
- Fatigue Tracker
- Discipline Ranking Sheet
- International Points Table

---

## 26) Codex Play Mode (Recommended)

For each year (with month-level drilldown), Codex should output:

- Updated tables (all tabs)
- Event and market roll details
- Cash flow summary (income/expense/profit)
- Balance sheet snapshot (assets/debt/net worth)
- Compliance checks (sale cap, young horse minimum, breeding ages)
- Strategic recommendation for next year

This structure supports infinite simulation with transparent, auditable numbers.
