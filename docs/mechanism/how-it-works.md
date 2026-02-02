# How Does AutoCap Work?

AutoCap operates in **discrete allocation rounds**. Each round defines a self-contained accounting period during which economic activity is measured and DataCap is distributed.

Each round is parameterized by:

* A fixed **start time** and **end time**
* A **registration fee**, paid in FIL
* A fixed **total DataCap pool** to be allocated at the end of the round

The round lifecycle consists of four phases:&#x20;

1. Registration,&#x20;
2. Activity measurement,&#x20;
3. Allocation calculation, and distribution.

Rounds are independent from one another. Activity in one round does not carry over to the next, and participants must explicitly register for each round they wish to participate in.

This design ensures:

* Clear accounting boundaries
* Deterministic allocation outcomes
* No retroactive effects across rounds
