### 3. Proportional DataCap Allocation

Once the round closes, AutoCap computes DataCap allocations using a deterministic, proportional formula based solely on **eligible FIL burns** recorded during the round.

```
Your DataCap Allocation
= (Your Eligible FIL Burned / Total Eligible FIL Burned in the Round)
× Round's Total DataCap Pool
```

If no eligible FIL is burned during a round, no DataCap is allocated. Allocations are computed independently per round and are not adjusted retroactively.
