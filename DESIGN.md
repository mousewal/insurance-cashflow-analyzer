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

## Inputs (V1)

Mandatory:
- start_date
- maturity_date
- premium_paying_term_years
- premium_amount
- premium_frequency (yearly / half-yearly / quarterly / monthly)
- sum_assured
- installments_paid

Optional:
- assumed_bonus_rate


