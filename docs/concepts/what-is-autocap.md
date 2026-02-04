# What is Autocap?

Autocap is an **automatic DC allocator** based on On-chain economic activity **rather than prior approval.**\
\
In the current [Filecoin Plus (FIL+)](https://fil.org/filecoin-plus) model, DataCap (DC) is typically allocated through a **permission-first process**.

A client applies to a DC Allocator, the allocator verifies the client's dataset off-chain, and DC is granted upfront. The client then uses that DC to make verified storage deals with Storage Providers, who benefit indirectly through the verified deal power multiplier.

Autocap pivots this logic.

Instead of requesting DC in advance, participants **prove real, verifiable economic activity on-chain first**, and DC is distributed automatically as a reward.

In practice: Autocap is a **round-based DC allocation system** that rewards participants proportionally to their contribution to the Filecoin network, measured by **FIL burned through the settlement of Filecoin Pay rails**.

Each round defines a fixed amount of DC to distribute. Participants who generate FIL burns during the round receive a share of that DC proportional to their contribution relative to other participants.

Conceptually, Autocap retains DC as the incentive, but changes the proxy for value:

* In the traditional FIL+ flow, value is inferred through **prior verification and approval**
* In Autocap, value is measured through **observable, on-chain economic contribution**

This results in an **action-first, reward-later** model, where allocation is derived from behavior rather than permission.
