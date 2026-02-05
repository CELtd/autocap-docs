# How Autocap Works?

AutoCap operates through **discrete allocation rounds**. Each round defines a self-contained accounting period during which on-chain economic activity is measured and DataCap is distributed.

Each round is parameterized by:

* A fixed start time and end time
* A registration fee, paid in FIL
* A fixed total DataCap (DC) pool to be allocated at the end of the round

#### Round Lifecycle

Each round progresses through three protocol phases:

1. **Registration**\
   Participants explicitly register for the round by paying the registration fee.
2. **Contribution and On-Chain activity**\
   During the active window of the round, participants generate on-chain economic activity. Contributions are measured through FIL burned via the settlement of Filecoin Pay rails.
3. **Allocation and Distribution**\
   At the end of the round, the total DC pool is distributed proportionally to participants based on their relative contribution during the round.

Throughout the round, AutoCap provides continuous, real-time observability into participant contributions and provisional allocation outcomes via the dashboard.

{% hint style="warning" %}
#### **Only Rails denominated in FIL are eligible for DC allocation via Autocap.**
{% endhint %}

#### Round Independence

Rounds are independent of one another. Activity in one round does not carry over to subsequent rounds, and participants must register separately for each round they wish to join.

This design ensures:

* Clear accounting boundaries
* Deterministic allocation outcomes
* No retroactive effects across rounds
