# 1. Registration

![](https://hackmd.io/_uploads/Skl0xDGSZe.png)

When a round opens, participants register through the [AutoCap Dashboard](https://filautocap.xyz/) by:

* **Connecting** a Filecoin-compatible wallet\
  &#xNAN;_(this wallet becomes the **Participant Address** tracked for on-chain activity)_
* **Paying** the **registration fee** from that wallet
* **Providing** a **DataCap Actor ID** (`f0xxx`) where any allocated DataCap will be sent\
  &#xNAN;_(this is the address that will receive DC at the end of the round)_

Registration establishes a binding between measured on-chain activity of the _**Participant Address**_ and the _**DataCap Actor ID**_, meaning the DC receipient, for the duration of the round.

#### Address Roles

Registration defines two distinct address roles:

* **Participant Address (wallet address)**\
  This is the address from which on-chain economic activity is measured.\
  Only activity originating from this address is counted toward the round.
* **DataCap Actor ID (`f0xxx`)**\
  This is the address that receives the DataCap allocation at the end of the round.\
  It is not used for activity measurement.

These roles are independent: activity is always attributed to the Participant Address, while DataCap is always issued to the specified DataCap Actor ID.

#### Constraints

* Each Participant Address may register **at most once per round**.
* Registration applies only to the active round and does not carry over to future rounds.
