# SJQGM — Stable Jurisdiction Quality Gold Miners Index

A rules-based equity index that tracks gold mining companies operating exclusively in jurisdictions with quantifiably secure property rights, zero expropriation history, and high operational quality.

---

## The Problem with Classical Gold Miner Indices

Traditional gold miner indices (GDX, GDXJ, XGD, GDM) weight constituents by market capitalization without regard for **where** a company mines. This exposes investors to a category of risk that is poorly priced and nearly impossible to hedge: **jurisdictional destruction of shareholder value**.

This destruction takes two forms:

1. **Outright expropriation** — nationalization, permit revocation, or uncompensated seizure of operating mines (e.g., Didipio in the Philippines, various African jurisdictions).
2. **Creeping expropriation** — the slow-motion erosion of Net Present Value through weaponized permitting delays, retroactive regulatory changes, unresolved indigenous land claims, and unlegislated windfall taxation. This is increasingly prevalent in historically "safe" jurisdictions like Canada and the United States.

Classical indices treat a mine in Western Australia and a mine in Mali as carrying equivalent jurisdictional risk. They don't.

---

## What SJQGM Does Differently

SJQGM applies a **strictly quantitative jurisdictional filter** before any company enters the index. Every mining jurisdiction worldwide is evaluated against three measurable tests:

| Filter | Metric | Threshold |
|--------|--------|-----------|
| **Permitting Efficiency** | 5-year avg. time from DFS to final operating permits | &le; 7 years |
| **Land Claim Certainty** | Fraser Institute survey score on disputed land claims | &ge; 75/100 |
| **Expropriation History** | Retroactive revocations, executive withdrawals, or nationalizations | Zero in trailing 5 years |

A jurisdiction must pass **all three** tests. The framework is globally applied and country-agnostic — it does not manually blacklist or whitelist any nation. The math currently qualifies Western Australia, South Australia, Northern Territory, New South Wales, Queensland, New Zealand, and Finland. It currently disqualifies British Columbia, Ontario, Alaska, Nevada, and Arizona on one or more criteria.

After jurisdictional screening, companies must derive **&ge; 65% of production** from eligible jurisdictions and **&ge; 60% of revenue** from gold. A **quality tilt** (AISC, reserve life, balance sheet strength) then adjusts weights by up to &plusmn;15% around a free-float market cap baseline, rewarding low-cost, long-life, conservatively financed operations.

---

## When SJQGM Is the Superior Approach

| Scenario | Why SJQGM Outperforms |
|----------|----------------------|
| **Rising political/regulatory risk cycles** | Classical indices carry dead weight from companies whose NPV is being destroyed by permitting gridlock or hostile regulation. SJQGM has zero exposure. |
| **Gold bull markets** | In sustained rallies, governments in weaker jurisdictions historically increase royalty/tax demands or impose windfall levies. SJQGM constituents operate where the fiscal regime is stable and predictable. |
| **Portfolio risk budgeting** | Investors who want gold exposure without adding sovereign/political risk to their book get a cleaner instrument. The jurisdictional filter eliminates a tail risk that market-cap weighting ignores entirely. |
| **Long-duration capital allocation** | Mine development is a 5-15 year endeavor. Jurisdictional stability over that horizon matters more than spot AISC. SJQGM's permitting-efficiency filter directly measures time-to-value. |
| **ESG/governance mandates** | The index naturally excludes jurisdictions with weak rule of law, contested indigenous rights frameworks, and opaque regulatory processes — without relying on subjective ESG scores. |

SJQGM is **not** designed for investors seeking maximum diversification across geographies or exposure to frontier/emerging-market gold plays. It is deliberately concentrated and deliberately opinionated: the thesis is that **where** you mine matters as much as **how well** you mine.

---

## Current Composition (March 2026)

11 constituents | ~A$97B total market cap | 98.2% Australia, 1.8% Finland

| Company | Ticker | Weight | Primary Jurisdictions |
|---------|--------|--------|-----------------------|
| Evolution Mining | ASX: EVN | 27.09% | NSW, QLD, WA |
| Northern Star Resources | ASX: NST | 26.71% | WA |
| Ramelius Resources | ASX: RMS | 8.35% | WA |
| Greatland Resources | ASX: GGP | 7.26% | WA |
| Capricorn Metals | ASX: CMM | 7.04% | WA |
| Genesis Minerals | ASX: GMD | 6.46% | WA |
| Westgold Resources | ASX: WGX | 4.80% | WA |
| Regis Resources | ASX: RRL | 4.26% | WA |
| Vault Minerals | ASX: VAU | 4.03% | WA |
| Bellevue Gold | ASX: BGL | 2.21% | WA |
| Rupert Resources | TSX: RUP | 1.78% | Finland |

Rebalanced semi-annually (June & December). Single-stock cap: 30%.

---

## Repository Structure

| File | Description |
|------|-------------|
| `index-methodology.md` | Full index methodology — eligibility rules, jurisdictional filters, quality scoring, weighting, and rebalancing |
| `index-constituents.md` | Current constituent list with detailed quality scores, weight waterfall, and company profiles |
| `research-data.md` | Source data log — per-company financials, reserves, AISC, balance sheets, and excluded company rationale |
| `sjqgm_basket.csv` | Index basket export |
| `main.py` | Index tooling |

---

## Key Index Characteristics

| Metric | Value |
|--------|-------|
| Wtd. Avg. AISC (A$/oz) | ~2,264 |
| Wtd. Avg. Reserve Life | ~12.8 years |
| Total Index Production | ~3,970 koz/yr |
| Effective Number of Stocks | ~6.4 |
| Net Cash Constituents | 9 of 11 |

---

## Methodology at a Glance

```
Global Gold Miner Universe
        │
        ▼
┌─────────────────────────┐
│  Base Universe Filter    │  Market cap ≥ US$350M, ADVT ≥ US$1M,
│                          │  listed on developed market exchange
└───────────┬─────────────┘
            ▼
┌─────────────────────────┐
│  Jurisdictional Filter   │  Permitting ≤ 7yr, Fraser ≥ 75,
│  (Property Rights)       │  Zero expropriation events
└───────────┬─────────────┘
            ▼
┌─────────────────────────┐
│  Company Exposure Filter │  ≥ 65% production in eligible jurisdictions,
│                          │  ≥ 60% revenue from gold
└───────────┬─────────────┘
            ▼
┌─────────────────────────┐
│  Quality Tilt            │  AISC (40%) + Reserve Life (30%) +
│  (±15% weight adjustment)│  Net Debt/EBITDA (30%)
└───────────┬─────────────┘
            ▼
┌─────────────────────────┐
│  FFMC Weighting + Cap    │  Free-float market cap weights,
│  (30% single-stock max)  │  quality-tilted, 30% hard cap
└─────────────────────────┘
```

---

## License

This index methodology and research data are provided for informational and educational purposes. This is not financial advice.
