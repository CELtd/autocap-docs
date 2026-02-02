# 3. Allocation and Distribution

Once the round closes, Autocap computes DC allocations using a deterministic, proportional formula based solely on **eligible FIL burns** recorded during the round:

{% include "../.gitbook/includes/dc-formula.md" %}

Only FIL burned through **finalized Filecoin Pay settlements** originating from registered Participant Addresses and occurring within the round window are included in the calculation.

**Example:**

* Round has 10 TiB of DC to distribute
* Total FIL burned by all participants: 100 FIL
* You burned: 10 FIL (10% of total)
* You receive: 1 TiB (10% of total DC)

This mechanism ensures:

* **Fairness** — allocations are strictly proportional to contribution;
* **Transparency** — all inputs are on-chain and publicly verifiable;
* **Determinism** — the outcome depends only on observed data, not discretion

If no eligible FIL is burned during a round, no DC is allocated.&#x20;

Also, allocations are computed independently for each round and are not adjusted retroactively.
