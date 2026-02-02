# How Does Autocap Work?

Autocap operates in **discrete allocation rounds**. Each round defines a self-contained accounting period during which economic activity is measured, and Datacap is distributed.

Each round is parameterized by:

* A fixed **start time** and **end time**
* A **registration fee**, paid in FIL
* A fixed **total DC pool** to be allocated at the end of the round

### Rounds

The round lifecycle consists of **three** protocol **phases**:

1. **Registration ;**
2. **Contribution;**
3. **Allocation** and **Distribution.**

Throughout the round, Autocap provides continuous, real-time observability into contributions and provisional allocations via the dashboard.

Rounds are independent from one another. Activity in one round does not carry over to the next, and participants must explicitly register for each round they wish to participate in.

This design ensures:

* Clear accounting boundaries
* Deterministic allocation outcomes
* No retroactive effects across rounds
