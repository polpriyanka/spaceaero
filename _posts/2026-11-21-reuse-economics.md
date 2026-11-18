---
layout: article
title: "Landing Saves the Rocket — but Does It Save Money?"
summary: "A simple, reproducible cost model of when reusing a rocket's first stage becomes cheaper per kilogram than discarding it — and when more flights can't help."
---

*How payload capacity and refurbishment affect the economics of rocket reuse.*

## Abstract

Recovering a rocket booster allows expensive hardware to be used again. However, recovery also creates costs. Equipment and propellant needed for landing can reduce payload capacity, and the booster must be recovered, inspected, and prepared for another flight. This study uses a hypothetical cost model to examine when reusing a first-stage booster becomes cheaper per kilogram delivered to orbit than replacing it after every launch. In the baseline scenario, the average cost per kilogram across three flights first falls below the expendable alternative. A sensitivity analysis varies payload reduction from 10% to 40% and refurbishment costs from $1 million to $10 million between flights. Across these assumptions, the first cost advantage ranges from two flights to no advantage within twenty flights. These results illustrate how engineering performance affects recurring transportation costs. They do not estimate the actual costs or profitability of a particular launch company.

## Introduction

Landing a rocket booster is an impressive engineering achievement. Whether landing it saves money is a separate question.

An expendable booster is used once. A reusable booster can spread its manufacturing cost across several launches, but bringing it home requires additional equipment, reserved propellant, and recovery operations. Preparing it for another flight also costs money.

This creates a tradeoff: a reusable rocket may cost less to operate per launch while carrying less payload. Comparing launch costs alone can therefore give an incomplete answer.

This study asks: after how many flights does a reusable first-stage booster become cheaper per kilogram delivered to orbit than an expendable alternative?

Previous research has examined reusable-launch economics, including how payload capacity and different cost categories affect the comparison. This study uses a simplified, transparent model to explore those relationships at a manageable scale.

### What this study contributes

Webb discusses how financial measures and operating conditions affect the economics of reuse. Kang and colleagues model launch costs across different payload capacities. This study isolates payload reduction and refurbishment cost in a simpler, reproducible comparison. Its purpose is to explain how those factors interact and why some combinations never become economical through repeated use alone. The model leaves out development cost, fixed annual overhead, financing, vehicle reliability, and detailed vehicle performance. Its contribution is educational: an explanation that readers can check by hand, rather than a cost estimate for a real vehicle.

## Engineering background

### Why recovery affects payload

Payload is the useful cargo a rocket delivers, such as satellites or scientific instruments.

Recovering a booster requires hardware and, for a powered landing, propellant that cannot all be consumed during ascent. These requirements can reduce payload capacity.

However, one kilogram of recovery equipment does not necessarily remove exactly one kilogram of payload capacity. Recovery equipment stays with the first stage, while the payload continues toward orbit with the upper stage. The relationship depends on the vehicle and flight profile.

The ideal rocket equation helps explain why mass matters:

Δv = vₑ · ln( m₀ / m_f )

Here, Δv is the ideal change in velocity, vₑ is exhaust velocity, m₀ is starting mass, and m_f is mass remaining after the burn.

For a fixed starting mass and exhaust velocity, leaving more mass at the end of a burn reduces the velocity gained. Propellant reserved for recovery remains aboard during the ascent burn.

The rocket equation explains this mechanism, but it does not by itself determine a real vehicle's payload reduction. This study therefore treats the reduction as an input:

P_R = P_E (1 − p)

where P_E is expendable payload capacity, P_R is reusable payload capacity, and p is the fractional payload reduction.

## Methods

### Scope and assumptions

The model compares hypothetical expendable and reusable launch systems delivering payload to the same destination orbit.

All launches are assumed to succeed and carry their full payload capacity. Only the first-stage booster is reused. Other launch expenses, including the upper stage, remain recurring costs.

The numerical inputs are illustrative assumptions, not measured costs from a launch provider. They were selected to make the tradeoffs visible and the calculations reproducible.

This article is a mathematical teaching study rather than an estimate of a particular vehicle. Payload reductions of 10–40% and refurbishment costs of $1–10 million are illustrative ranges selected to explore how the model behaves. They are not validated operating ranges.

The reusable booster is recovered after every flight, including its final flight. Refurbishment occurs only between flights. A booster completing five flights therefore undergoes five recoveries and four refurbishments. No resale value is assigned at retirement.

| Input | Baseline assumption |
| --- | --- |
| Expendable booster manufacturing cost | $30 million |
| Reusable booster manufacturing cost | $36 million |
| Other recurring costs per launch, either system | $20 million |
| Recovery cost per reusable flight | $1 million |
| Refurbishment between reusable flights | $3 million |
| Expendable payload capacity | 20,000 kg |
| Reusable payload capacity | 15,000 kg |
| Baseline payload reduction | 25% |
| Flights examined per reusable booster | 1–20 |

### Cost model

For the expendable system:

k_E = ( B_E + O ) / P_E

where B_E is booster manufacturing cost, O represents other recurring launch costs, and k_E is cost per kilogram. Using the baseline assumptions:

k_E = ( $30M + $20M ) / 20,000 = $2,500/kg

For the reusable system:

k_R(N) = [ B_R + N(O + R) + (N − 1)F ] / ( N · P_R )

Here, B_R is reusable booster manufacturing cost, R is recovery cost per flight, F is refurbishment cost between flights, and N is the total number of flights. The numerator is total cost across those flights; the denominator is total payload delivered. The first economical flight count is the smallest whole number N for which k_R(N) < k_E.

### Sensitivity analysis

To test how the answer depends on uncertain inputs, the model combines four payload reductions — 10%, 20%, 30%, and 40% — with four refurbishment costs: $1 million, $3 million, $6 million, and $10 million. Each combination is evaluated for one through twenty flights, producing 320 evaluations. All other assumptions remain fixed. These ranges are exploratory; they are not presented as confidence intervals or verified operating ranges for an actual rocket.

## Results

### Baseline comparison

Under the baseline assumptions, the reusable system's total cost across N flights, in millions of dollars, is:

C_R(N) = 36 + 21N + 3(N − 1) = 33 + 24N

The resulting cost comparison is:

| Flights per reusable booster | Expendable cost/kg | Reusable cost/kg | Lower-cost option |
| --- | --- | --- | --- |
| 1 | $2,500 | $3,800 | Expendable |
| 2 | $2,500 | $2,700 | Expendable |
| 3 | $2,500 | $2,333 | Reusable |
| 5 | $2,500 | $2,040 | Reusable |
| 10 | $2,500 | $1,820 | Reusable |
| 20 | $2,500 | $1,710 | Reusable |

Values are rounded to the nearest dollar.

The reusable system first wins at three flights: the average cost per kilogram across the first three flights (one initial flight and two reuses) is lower than the expendable alternative. The per-kilogram figures in the table are averages over N flights, not the cost of the Nth flight alone. At five flights, the reusable system's average cost is 18.4% less per kilogram than the expendable system.

An independent algebraic check gives the same result:

( 33 + 24N ) / ( 15,000 N ) < 50 / 20,000

Solving gives N > 2.44, so the first qualifying whole number is three.

![Figure 1. Cost per kilogram against flights per reusable booster under the baseline assumptions. The reusable curve falls as the booster's manufacturing cost is spread over more flights, crossing below the flat expendable line between the second and third flight and flattening toward a floor of about $1,600/kg.](/images/reuse-crossover.png)

### Effects of payload reduction and refurbishment

The table below shows the first total flight count at which reuse becomes cheaper per kilogram.

| Payload reduction | $1m refurb. | $3m refurb. | $6m refurb. | $10m refurb. |
| --- | --- | --- | --- | --- |
| 10% | 2 | 2 | 2 | 2 |
| 20% | 2 | 3 | 3 | 3 |
| 30% | 3 | 4 | 4 | 7 |
| 40% | 5 | 6 | 11 | No advantage within 20 flights |

At a 10% payload reduction, every tested refurbishment cost produces an advantage by the second flight. At a 40% reduction, refurbishment costs have a much larger effect: increasing refurbishment from $1 million to $6 million shifts the first advantage from five flights to eleven. This shows that the two variables interact. An expensive refurbishment process is harder to absorb when each flight also carries substantially less cargo.

## Discussion

### A cheaper launch may still be expensive transportation

The key comparison is the cost of delivering useful payload. For example, a $35 million launch carrying 15,000 kg costs approximately $2,333/kg. The same launch cost with only 12,000 kg of payload becomes approximately $2,917/kg. The launch expense has not changed, but the transportation cost per kilogram has increased. This is why payload performance belongs in an economic analysis.

### Why savings flatten out

The baseline reusable cost can also be written as:

k_R(N) = ( 24 + 33/N ) × 1,000,000 / 15,000

As flight count increases, the 33/N term becomes smaller. However, the recurring expenses remain. Under these assumptions, cost approaches $1,600/kg as flight count grows. This is a mathematical limit of the model, not a prediction that a real booster can fly indefinitely. The practical lesson is that reuse spreads manufacturing costs across more flights; it does not eliminate the cost of each launch.

### Some combinations cannot become economical through reuse alone

For the tested case with a 40% payload reduction and $10 million refurbishment cost, reusable cost is:

k_R(N) = ( 31 + 26/N ) × 1,000,000 / 12,000

Even as N grows, the cost approaches approximately $2,583/kg — above the expendable benchmark of $2,500/kg. Therefore, this particular fixed-cost scenario would not become cheaper simply by adding more flights. Payload capacity or recurring expenses would also need to improve.

## Limitations

The model uses hypothetical costs and payload reductions. Its numerical results apply only to the stated assumptions. It assumes full payloads, successful launches, successful recoveries, and constant refurbishment costs. Actual operations could involve partially filled launches, booster losses, or maintenance expenses that increase with age.

Development costs, dedicated infrastructure, annual fixed overhead, financing, and the time required to complete multiple flights are excluded. Consequently, the model compares selected recurring transportation costs, not complete program costs or company profitability. The study also does not calculate payload performance from a detailed flight simulation or compare different rocket sizes.

## Conclusion

Under the hypothetical baseline assumptions, the average cost per kilogram across the first three flights falls below the expendable alternative. Across the sensitivity analysis, the first advantage ranges from two flights to no advantage within the twenty-flight window.

The result depends on both the cost of preparing a booster for another flight and the payload capacity sacrificed for recovery. In some scenarios, repeated use alone cannot overcome high recurring costs per kilogram.

Landing preserves valuable hardware. Whether it saves money depends on how much useful payload the system delivers and what each additional flight costs.

## Data and reproducibility

A spreadsheet supplement accompanies this article. It contains the input assumptions, formulas, the baseline comparison, all 320 sensitivity evaluations, and instructions for reproducing the comparison table and figure. The supplied inputs reproduce the reported results; changing the inputs recalculates the workbook, while the article and its figure remain a record of the stated baseline.

---

**Sources:**

1. Webb, R. (2016). *Is It Worth It? — The Economics of Reusable Space Transportation.* International Cost Estimating and Analysis Association symposium. NASA Technical Reports Server. [ntrs.nasa.gov/citations/20160013370](https://ntrs.nasa.gov/citations/20160013370)
2. Kang, S.-Y., Jo, M.-S., Choi, J.-Y., & Yang, S. S. (2025). Cost effectiveness of reusable launch vehicles depending on the payload capacity. *Aerospace, 12*(5), 364. [doi.org/10.3390/aerospace12050364](https://doi.org/10.3390/aerospace12050364)
3. NASA Glenn Research Center. *Ideal Rocket Equation.* Beginner's Guide to Aeronautics. [www1.grc.nasa.gov/beginners-guide-to-aeronautics/ideal-rocket-equation](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/ideal-rocket-equation)
