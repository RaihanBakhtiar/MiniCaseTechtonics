# Financial Model Template

All values need a unit, period, source or **ASSUMPTION**, and named owner. Build the calculations in a spreadsheet when figures are ready; this file is the model specification.

## Core assumptions

| Variable | Base case | Upside | Downside | Unit | Source / rationale | Owner |
|---|---|---|---|---|---|---|
| Downloads |  |  |  | per month |  |  |
| Sign-up rate |  |  |  | % of downloads |  |  |
| Activation rate |  |  |  | % of sign-ups |  |  |
| D30 retention |  |  |  | % of activated users |  |  |
| Premium conversion |  |  |  | % of eligible active users |  |  |
| Monthly price | 25,000 |  |  | IDR / user / month | Casebook starting price |  |
| Gross margin |  |  |  | % |  |  |
| Blended CAC |  |  |  | IDR / acquired user |  |  |
| Monthly churn |  |  |  | % of paid users |  |  |

## Funnel and revenue projection

| Period | Downloads | Sign-ups | Activated | Retained | Paid new | Paid active | Revenue (IDR) | Acquisition cost | Net contribution |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| M1 |  |  |  |  |  |  |  |  |  |

**Formula guide:** sign-ups = downloads × sign-up rate; activated = sign-ups × activation rate; paid new = eligible active users × conversion rate; revenue = paid active × monthly price. State your precise eligibility and churn rules.

## Unit economics checks

| Metric | Formula | Base value | Decision threshold | Notes |
|---|---|---:|---|---|
| CAC | acquisition spend / acquired user |  |  |  |
| ARPPU | revenue / paid active users |  |  |  |
| LTV | ARPPU × gross margin × expected paid lifetime |  |  |  |
| LTV:CAC | LTV / CAC |  |  |  |
| Payback period | CAC / monthly gross contribution per paid user |  |  |  |

## Budget allocation

| Initiative | One-time / recurring | Period | Cost (IDR) | Expected funnel impact | Owner | Assumption / source |
|---|---|---|---:|---|---|---|
|  |  |  |  |  |  |  |
