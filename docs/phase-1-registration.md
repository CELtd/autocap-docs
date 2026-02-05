# 1. Registration

When a round opens, participants register through the [AutoCap Dashboard](https://filautocap.xyz/) by:

* **Connecting** a Filecoin-compatible wallet in the _**Participant Burn Address —** this wallet is tracked for on-chain activity;_
* **Paying** the **registration fee** from that wallet;
* **Providing** a **Participant DataCap Address** (`f0xxx`) — _this is the address that will receive DC at the end of the round._

Registration establishes a binding between measured on-chain activity of the _**Participant Burn Address**_ and the _**Participant DataCap Address**_, meaning the DC receipient, for the duration of the round.

#### Address Roles

Registration defines two distinct address roles:

* **Participant Burn Address**\
  This is the address from which on-chain economic activity is measured.\
  Only FIL burns originating from this addressare counted toward the round.
* **Participant DataCap Address (`f0xxx`)**\
  This is the address that receives the DataCap allocation at the end of the round.\
  It is not used for activity measurement.

These roles are independent: activity is always attributed to the Participant Address, while DataCap is always issued to the specified DataCap Actor ID.

#### Constraints

* Each Participant Address may register **at most once per round**.
* Registration applies only to the active round and does not carry over to future rounds.
