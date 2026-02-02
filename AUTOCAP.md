<!-- AUTOCAP:START:introduction -->
# (WIP) Introducing AutoCap: An Automatic DataCap Allocator Based on On-Chain Activity

At [CryptoEconLab](https://cryptoeconlab.com/), we've built [**AutoCap**](https://filautocap.xyz/), a system that enables Storage Providers to access Filecoin Plus (FIL+) DataCap through a transparent, automated, and activity-based process.

AutoCap allocates DataCap based on **verifiable on-chain economic activity**, removing the need for manual applications or subjective approval processes.
<!-- AUTOCAP:END:introduction -->


<!-- AUTOCAP:START:what-is-autocap -->
## What is AutoCap?

Under the current Filecoin Plus (FIL+) model, DataCap is typically allocated through a **permission-first process**.

A client applies to a DataCap Allocator, the allocator verifies the client’s dataset off-chain, and DataCap is granted upfront. The client then uses that DataCap to make verified storage deals with Storage Providers, who benefit indirectly through the verified deal power multiplier.

AutoCap pivots this logic.

Instead of requesting DataCap in advance, participants **prove real, verifiable economic activity on-chain first**, and DataCap is distributed automatically as a reward.

AutoCap is a **round-based DataCap allocation system** that rewards participants proportionally to their contribution to the Filecoin network, measured by **FIL burned through the settlement of Filecoin Pay rails**.

Each round defines a fixed amount of DataCap to distribute. Participants who generate FIL burns during the round receive a share of that DataCap proportional to their contribution relative to other participants.

Conceptually, AutoCap retains DataCap as the incentive, but changes the proxy for value:
- In the traditional FIL+ flow, value is inferred through **prior verification and approval**
- In AutoCap, value is measured through **observable, on-chain economic contribution**

This results in an **action-first, reward-later** model, where allocation is derived from behavior rather than permission.
<!-- AUTOCAP:END:what-is-autocap -->


<!-- AUTOCAP:START:how-it-works -->
## How Does AutoCap Work?

AutoCap operates in **discrete allocation rounds**. Each round defines a self-contained accounting period during which economic activity is measured and DataCap is distributed.

Each round is parameterized by:
- A fixed **start time** and **end time**
- A **registration fee**, paid in FIL
- A fixed **total DataCap pool** to be allocated at the end of the round

The round lifecycle consists of four phases: registration, activity measurement, allocation calculation, and distribution.
<!-- AUTOCAP:END:how-it-works -->


<!-- AUTOCAP:START:round-structure -->
### Round Structure

Rounds are independent from one another. Activity in one round does not carry over to the next, and participants must explicitly register for each round they wish to participate in.

This design ensures:
- Clear accounting boundaries
- Deterministic allocation outcomes
- No retroactive effects across rounds
<!-- AUTOCAP:END:round-structure -->


<!-- AUTOCAP:START:phase-1-registration -->
### 1. Registration
![Screenshot 2026-01-12 125319](https://hackmd.io/_uploads/Skl0xDGSZe.png)

When a round opens, Storage Providers can register through the AutoCap Dashboard by:

- Connecting a Filecoin-compatible wallet  
  *(this wallet becomes the **Participant Address** tracked for on-chain activity)*  
- Paying the registration fee from that wallet  
- Providing a **DataCap Actor ID** (`f0xxx`) where any allocated DataCap will be sent

Registration establishes the binding between measured on-chain activity and the DataCap recipient for the round.

**Important:** Registration defines two distinct address roles:

- **Participant Address (wallet address)**  
  This is the address from which **on-chain activity is measured**.  
  Only activity originating from this address is counted toward the round.

- **DataCap Actor ID (`f0xxx`)**  
  This is the address that receives the DataCap allocation at the end of the round.  
  It is not used for activity measurement.

Each Participant Address may register **at most once per round**.
<!-- AUTOCAP:END:phase-1-registration -->


<!-- AUTOCAP:START:onchain-activity-definition -->
### What Counts as On-Chain Activity

For the purposes of AutoCap, *on-chain activity* is defined narrowly and precisely.

AutoCap measures **FIL burned by a registered Participant Address as a result of Filecoin Pay rail settlements**, subject to the following conditions:

- The burn originates from a **registered Participant Address**
- The burn results from the **settlement of a Filecoin Pay payment rail**
- The settlement is **denominated in FIL**
- The settlement is **finalized on-chain**
- The settlement occurs **within the start and end time of the round**

Only FIL that is **actually burned as part of settlement** is counted toward a participant’s contribution.

The following do **not** count as on-chain activity for AutoCap:

- Unsettled Filecoin Pay rails
- Payments or transfers that do not result in FIL burn
- Activity originating from non-registered addresses
- Activity occurring outside the round window
- Activity denominated in assets other than FIL

> **Note on Future Refinements**
>
> Future versions of AutoCap may refine this measurement to count only Filecoin Pay settlements that can be **directly linked to sealed storage sectors (PoRep-backed storage deals)**.
<!-- AUTOCAP:END:onchain-activity-definition -->


<!-- AUTOCAP:START:phase-2-activity -->
### 2. Burn FIL Through Filecoin Pay

During an active round, registered participants generate economic contribution by **burning FIL through the settlement of Filecoin Pay payment rails**.

AutoCap does not track generic payments or transfers. It observes **finalized Filecoin Pay settlement events** that result in FIL being burned on-chain and originate from a registered **Participant Address**.
<!-- AUTOCAP:END:phase-2-activity -->


<!-- AUTOCAP:START:phase-3-allocation -->
### 3. Proportional DataCap Allocation

Once the round closes, AutoCap computes DataCap allocations using a deterministic, proportional formula based solely on **eligible FIL burns** recorded during the round.

```
Your DataCap Allocation
= (Your Eligible FIL Burned / Total Eligible FIL Burned in the Round)
× Round’s Total DataCap Pool
```

If no eligible FIL is burned during a round, no DataCap is allocated. Allocations are computed independently per round and are not adjusted retroactively.
<!-- AUTOCAP:END:phase-3-allocation -->


<!-- AUTOCAP:START:monitoring -->
### 4. Monitoring Your Progress

AutoCap provides a real-time dashboard that allows participants to inspect rounds, registrations, eligible FIL burns, and expected allocations.

All Filecoin Pay settlements and burns can be independently verified via public explorers.
<!-- AUTOCAP:END:monitoring -->


<!-- AUTOCAP:START:who-is-it-for -->
## Who is AutoCap For?

AutoCap is designed for **Storage Providers** who provide services via Filecoin Pay and wish to access DataCap through a transparent, rule-based mechanism.

AutoCap is optional and complements existing Filecoin Plus allocation paths.
<!-- AUTOCAP:END:who-is-it-for -->


<!-- AUTOCAP:START:why-fil-burns -->
## Why FIL Burns?

FIL burns provide a protocol-native, verifiable signal of finalized economic activity on the Filecoin network.

### Registration Fees

Registration fees **do not** count toward eligible FIL burns and serve only as an access-control mechanism.
<!-- AUTOCAP:END:why-fil-burns -->


<!-- AUTOCAP:START:usage-in-practice -->
## Usage in Practice

This section describes how Storage Providers typically participate in an AutoCap round, from preparation to allocation.
<!-- AUTOCAP:END:usage-in-practice -->


<!-- AUTOCAP:START:questions -->
## Questions or Feedback

AutoCap is under active development.  
For questions or feedback, please reach out to CryptoEconLab.
<!-- AUTOCAP:END:questions -->