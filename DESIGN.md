## Problem Statement

Endowment insurance policies combine life cover with a maturity benefit.
However, the long-term cashflow structure of these policies is often
difficult for policyholders to evaluate, especially when premiums are
paid periodically and benefits are realized many years later.

This system provides a mathematical analysis of endowment insurance
policy cashflows by modeling premiums paid, maturity benefits, and
optional bonus assumptions. The output includes cashflow schedules,
internal rate of return (XIRR), and breakeven analysis.

The system is designed to improve transparency by presenting numerical
outcomes based on user-provided inputs. It does not provide financial
advice or make recommendations.

## Inputs (V1) (Baseline)

Mandatory:
- start_date
- maturity_date
- premium_paying_term_years
- premium_amount
- premium_frequency (yearly / half-yearly / quarterly / monthly)
- sum_assured

Deferred:
- installments_paid

Optional:
- assumed_bonus_rate


## Output Metrics (V1)

- Cashflow schedule (date, amount)
- Total premiums paid
- Maturity value (guaranteed + assumed bonus scenario)
- Internal Rate of Return (XIRR)
- Breakeven year

## Theoretical Policy Return Logic (Baseline)

This version assumes the policy is held from inception to maturity
and all premiums are paid as scheduled.

1. Determine total number of premium installments based on:
   - premium_paying_term_years
   - premium_frequency

2. Generate premium payment dates starting from start_date
   at intervals defined by premium_frequency.

3. For each premium payment date:
   - Add a negative cashflow equal to premium_amount.

4. On maturity_date:
   - Add a positive cashflow equal to sum_assured.
   - If assumed_bonus_rate is provided:
       add bonus amount to maturity cashflow.
   -Bonus is assumed to be applied at maturity only and is not guaranteed.


5. Compute XIRR using all generated cashflows.

