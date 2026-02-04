---
description: Burn FIL Through Filecoin Pay
---

# 2. Contribution and On-Chain Activity

AutoCap defines economic contribution narrowly and precisely.

During an active round, registered participants generate contribution by **burning FIL through the settlement of Filecoin Pay payment rails**.

AutoCap does not track generic payments, transfers, or intermediate obligations. Contribution is observed **only at settlement**, when accumulated payment obligations are finalized on-chain and result in FIL being burned.

#### Valid Contribution Conditions

A FIL burn is counted toward a participant’s contribution **only if all of the following hold**:

* The burn originates from a **registered Participant Address**
* The burn results from the **settlement of a Filecoin Pay payment rail**
* The settlement is **denominated in FIL**
* The settlement is **finalized on-chain**
* The settlement occurs **within the active round window**

Only FIL that is actually burned as part of settlement is included in AutoCap’s accounting.

#### Excluded Activity

The following do **not** count toward contribution:

* Unsettled or partially settled rails
* Pending obligations that have not been finalized
* Reverted or failed settlement transactions
* Payments or transfers that do not result in FIL burn
* Activity originating from non-registered addresses
* Activity occurring outside the round window
* Activity denominated in assets other than FIL

#### Note on Future Refinements

Future versions of AutoCap may further constrain contribution accounting to include only Filecoin Pay settlements that can be directly linked to sealed storage sectors (e.g. PoRep-backed storage deals).

