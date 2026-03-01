# Domain Profile

## Field

**Primary:** Political Economy
**Adjacent subfields:** Public Finance, Urban Economics, Development Economics, Institutional Economics

---

## Target Journals (ranked by tier)

| Tier | Journals |
|------|----------|
| Top-5 | AER, Econometrica, JPE, QJE, REStud |
| Top field | AEJ: Economic Policy, AEJ: Applied, Journal of Public Economics, JDE |
| Strong field | Journal of Urban Economics, Journal of Political Economy Micro, Economic Journal, Journal of the European Economic Association |
| Specialty | Journal of Public Finance and Public Choice, Public Choice, National Tax Journal, Journal of Economic Geography |

---

## Research Focus

**Core question:** Does politicians' personal wealth being tied to their local jurisdiction (district/municipality) affect economic and taxation outcomes?

**Specific angle:** Brazilian mayors whose wealth (real estate, land, businesses) is concentrated in the municipality they govern — how does this local wealth stake shape tax policy, public goods provision, and fiscal outcomes?

**Key mechanisms to explore:**
- Skin-in-the-game: mayors with local wealth internalize tax/spending consequences
- Self-dealing: mayors may set policy to benefit their own assets (e.g., low property taxes)
- Information: local wealth implies local knowledge about tax base
- Political selection: wealthier candidates may differ on observable/unobservable dimensions

---

## Common Data Sources

<!-- Fill in as you identify data sources for this project -->

| Dataset | Type | Access | Notes |
|---------|------|--------|-------|
| TSE Candidatos | Administrative | Public (TSE) | Candidate asset declarations, election results |
| FINBRA / SICONFI | Administrative | Public (STN) | Municipal fiscal data (revenues, expenditures) |
| IBGE Census / PNAD | Survey | Public (IBGE) | Municipal socioeconomic characteristics |
| RAIS / CAGED | Administrative | Restricted (MTE) | Formal labor market data |
| Cadastro IPTU | Administrative | Varies by municipality | Property tax rolls |
| TBD | -- | -- | To be determined during data exploration phase |

---

## Common Identification Strategies

| Strategy | Typical Application | Key Assumption to Defend |
|----------|-------------------|------------------------|
| Difference-in-Differences | Policy reforms affecting local taxation | Parallel trends in outcomes across treated/control jurisdictions |
| Regression Discontinuity | Close elections — comparing municipalities where wealthy-local mayors barely won vs barely lost | Continuity of potential outcomes at the 50% vote-share cutoff |
| Instrumental Variables | Historical or geographic instruments for wealth/taxation | Exclusion restriction — instrument affects outcome only through endogenous variable |
| Shift-share / Bartik | Local economic shocks affecting mayor's personal wealth | Exogeneity of shares or shocks |
| Event study | Tax reform adoption timing | No anticipation, parallel pre-trends |

---

## Field Conventions

- Clustering at the jurisdiction level for jurisdiction-level policy variation
- Report both OLS and IV estimates when using instrumental variables
- Present event-study plots for DiD designs to assess pre-trends
- Discuss political economy mechanisms (voting, lobbying, sorting) alongside fiscal effects
- Welfare analysis or distributional implications expected for top-5 submissions
- Robustness to alternative geographic boundaries and spatial spillovers

---

## Notation Conventions

<!-- Fill in as notation decisions are made during drafting -->

| Symbol | Meaning | Anti-pattern |
|--------|---------|-------------|
| $Y_{it}$ | Outcome for jurisdiction $i$ at time $t$ | Don't use $y$ without subscripts |
| $\tau_{it}$ | Tax rate for jurisdiction $i$ at time $t$ | Don't use $t$ for both tax and time |
| $W_{it}$ | Wealth measure for jurisdiction $i$ at time $t$ | Distinguish from $w$ (wages) |

---

## Seminal References

<!-- Add key references as literature review progresses -->

| Paper | Why It Matters |
|-------|---------------|
| TBD | To be populated during literature review |

---

## Field-Specific Referee Concerns

- "Sorting/Tiebout" — households sort across jurisdictions in response to tax differences; must address endogeneity
- "Tax competition" — neighboring jurisdictions' policies are not independent; account for strategic interaction
- "Capitalization" — wealth measures may reflect tax policy through property values; direction of causality
- "Political economy channel" — referees expect discussion of why local governments choose observed tax policies
- "External validity" — results from one country/institutional context may not generalize
- "Wealth measurement" — Brazilian asset declarations (TSE) may be noisy or strategically reported; need validation
- "Selection into politics" — wealthier individuals self-select into mayoral races; disentangle selection from causal effect
- "Local vs non-local wealth" — must clearly define and measure geographic concentration of assets

---

## Quality Tolerance Thresholds

| Quantity | Tolerance | Rationale |
|----------|-----------|-----------|
| Point estimates | 1e-6 | Numerical precision |
| Standard errors | 1e-4 | Clustering variability |
| Coverage rates | +/- 0.01 | Bootstrap/simulation variability |
