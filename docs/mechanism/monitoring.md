---
description: Real-Time Dashboard
---

# Monitoring and Transparency

<figure><img src="../.gitbook/assets/Screenshot 2026-02-09 121911.png" alt="Snapshot of the dashboard"><figcaption><p>Snapshot of the real-time dashboard</p></figcaption></figure>

Autocap is designed to be fully observable throughout the entire lifecycle of a round. Monitoring is provided through a [**real-time dashboard**](https://filautocap.xyz/) that exposes both participant activity and provisional allocation outcomes as they evolve.

During all phases of a round (registration, contribution, and allocation) participants can use the dashboard to:

* View active, and completed rounds
* See the set of registered participants for each round
* Track finalized on-chain eligible FIL burns as Filecoin Pay settlements
* View expected DataCap allocations, updated continuously as new settlements occur
* Verify registration status and associated addresses

All contribution data displayed in the dashboard is derived directly from on-chain events. For each participant, the dashboard links the associated Participant Burn Address to [**https://pay.filecoin.cloud**](https://pay.filecoin.cloud), where Filecoin Pay settlement transactions and the resulting FIL burns can be independently inspected and verified.

By exposing both inputs (settlement events and burns) and intermediate outputs (provisional allocations) in real time, Autocap enables participants and third parties to independently audit round progress and reproduce final allocation outcomes.
