# Index Methodology Guide
**Index Name:** Stable Jurisdiction Quality Gold Minders (SJQGM)
**Version:** 1.0 
**Objective:** To track the performance of global gold mining companies operating strictly in jurisdictions with quantifiably secure property rights, low risk of creeping or outright expropriation, and high operational quality.

---

## 1. Index Rationale & Philosophy
The global gold mining sector is increasingly subject to both outright nationalization (predominantly in emerging markets) and "creeping expropriation" (in historically safe North American markets). Creeping expropriation is defined as the functional erosion of Net Present Value (NPV) through weaponized permitting delays, retroactive permit revocations, unresolved indigenous land claims, and unlegislated windfall taxation. 

The SJQGM Index employs a strictly quantitative, globally applied framework to exclude jurisdictions suffering from property right erosion. While the index scans a global universe, the mathematical rigor of its jurisdictional filters currently naturally excludes Africa, Latin America, the United States, and Canada, typically resulting in an Australasian and Nordic-concentrated portfolio. Furthermore, the index applies a fundamental quality tilt to reward low-cost, long-life assets with strong balance sheets.

---

## 2. Base Universe Eligibility
To be eligible for inclusion in the initial universe, a security must meet the following baseline criteria:
* **Listing:** Listed on a recognized Developed Market exchange (e.g., ASX, TSX, NYSE, NASDAQ, LSE).
* **Sector Classification:** Classified as a Gold Miner (GICS Sub-Industry: Gold).
* **Market Capitalization:** Free-float market capitalization of $\ge$ USD $350 million (approx. AUD $500m / CAD $475m).
* **Liquidity:** 3-month Average Daily Value Traded (ADVT) of $\ge$ USD $1.0 million.

---

## 3. The Jurisdictional Security Filter (Quantitative Property Rights)
Rather than manually excluding countries, the index algorithm evaluates global mining jurisdictions (at the state/provincial level where applicable) against three quantitative property right metrics. 

A jurisdiction is deemed **"Eligible"** only if it passes *all three* of the following tests:

1. **Permitting Efficiency (Time-to-Value):** 
  * *Metric:* The trailing 5-year average permitting lead time from the publication of a Definitive Feasibility Study (DFS) to the receipt of final operating permits/Record of Decision (ROD).
  * *Rule:* Must be **$\le 7.0$ years**. (Data sourced from S&P Global Market Intelligence / regional mining associations).
2. **Land Claim & Regulatory Certainty:**
  * *Metric:* The annual Fraser Institute Survey of Mining Companies.
  * *Rule:* The jurisdiction must score **$\ge 75/100$** (or rank in the global top quartile) on the sub-index for *"Uncertainty concerning disputed land claims."*
3. **Executive Veto / Expropriation Risk:**
  * *Metric:* Frequency of retroactive permit revocations, executive mineral withdrawals, or uncompensated nationalizations of advanced-stage (PFS/DFS or operating) projects.
  * *Rule:* Must be **Zero (0)** in the trailing 5-year period.

*(Note: Applying these rules currently flags Western Australia, South Australia, Northern Territory, New South Wales, Queensland, New Zealand, and Finland as Eligible. British Columbia, Ontario, Alaska, Nevada, and Arizona currently fail on rules 1, 2, or 3).*

---

## 4. Company-Level Exposure Filters
Once the Eligible Jurisdictions list is generated, companies from the Base Universe are evaluated for purity:
* **Revenue Purity:** $\ge 60\%$ of Trailing Twelve Month (TTM) revenue must be derived from gold.
* **Safe-Harbor Production:** $\ge 65\%$ of TTM gold production (in ounces) must be sourced from mines located within *Eligible Jurisdictions*.
  * *Developer Exception:* For pre-production developers, $\ge 65\%$ of their total Proven & Probable (P&P) Reserves must be located within Eligible Jurisdictions.

---

## 5. Quality Scoring & Tilt Mechanism
Eligible constituents are initially weighted by Free-Float Market Capitalization (FFMC). A Quality Multiplier is then applied to tilt weights toward superior operations. 

### 5.1 Quality Factor Definitions & Weighting
Each company receives a Quality Score from 1.0 (Worst) to 5.0 (Best) based on three fundamental metrics:

* **Factor 1: All-In Sustaining Costs (AISC) – 40% Weight**
  * Based on TTM AISC per ounce (USD equivalent). Evaluates margin resilience.
  * *Score 5:* < 1st Quartile of universe average
  * *Score 1:* > 4th Quartile of universe average
* **Factor 2: Reserve Life – 30% Weight**
  * Calculated as Total P&P Reserves $\div$ TTM Production. Evaluates asset longevity.
  * *Score 5:* $\ge 10$ Years
  * *Score 1:* $< 3$ Years
* **Factor 3: Net Debt / EBITDA – 30% Weight**
  * Evaluates balance sheet risk.
  * *Score 5:* Net Cash ( $< 0.0x$ )
  * *Score 1:* $> 2.0x$ (or negative EBITDA)

### 5.2 The "Junior Developer" Carve-Out
Pre-production companies (Developers) lack TTM production and EBITDA. They are scored as follows:
* *AISC & Reserve Life:* Calculated using the life-of-mine estimates from their most recent PFS or DFS. 
* *Net Debt / EBITDA:* Assigned a default neutral score of **3.0** to reflect standard development funding risk without artificially rewarding or penalizing them.

### 5.3 Calculating the Multiplier
The weighted composite score (1.0 to 5.0) is mapped linearly to a multiplier ranging from $0.85x$ ($-15\%$ penalty) to $1.15x$ ($+15\%$ premium).
$$ Multiplier = 0.85 + [(Composite\ Score - 1) \times 0.075] $$

---

## 6. Weight Calculation & Single-Stock Capping
1. **Pre-Tilt Weight:** Calculate standard FFMC weights for all eligible constituents.
2. **Apply Tilt:** Multiply each company's FFMC weight by its individual Quality Multiplier. 
3. **Normalization:** Re-sum the tilted weights and divide each by the new total so the index sum equals 100%.
4. **Capping:** Any single constituent weight exceeding **30.00%** is hard-capped at 30.00%. 
5. **Redistribution:** The excess weight from capped constituents is redistributed proportionally among the remaining uncapped constituents. This process is applied iteratively until no stock exceeds 30.00%.

---

## 7. Index Maintenance & Rebalancing
* **Rebalancing Frequency:** Semi-Annually, occurring on the third Friday of June and December. 
* **Data Cutoff:** Fundamental data, market capitalization, and jurisdiction risk metrics are captured on the last business day of May and November, respectively.
* **Fraser Institute Updates:** The Jurisdictional Security Filter is updated during the June rebalance to incorporate the latest annual data from the Fraser Institute Survey (typically published in Q1).
* **Corporate Actions:** Spin-offs, M&A, and delistings are handled ad-hoc. If an index constituent is acquired by a non-eligible company (e.g., an operator in an ineligible jurisdiction), it is removed from the index immediately upon deal closure, and weights are proportionally redistributed.

