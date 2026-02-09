---
description: Register your wallet address
---

# 1. Registration

When a round opens, participants can register through the [AutoCap Dashboard](https://filautocap.xyz/) by:

* **Connecting** a Filecoin-compatible wallet in the _**Burn Address**_ \
  &#x20;_This wallet is tracked for on-chain activity;_
* **Paying** the **registration fee** from that wallet;
* **Providing** a **DataCap Recipient Address** (`f0xxx`)\
  &#xNAN;_&#x54;his is the address that will receive DC at the end of the round._\
  _Participant can either provide the Actor ID of the wallet directly, or the wallet address (0x, f1, f2, ...). The registration form will automatically convert the address in the corresponding Actor ID._

Registration establishes a binding between measured on-chain activity of the _**Burn Address**_ and the _**DataCap Recipient Address**_, meaning the DC recipient, for the duration of the round.

<figure><img src=".gitbook/assets/registration (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The **DataCap Recipient Address** is in the form of **Filecoin's Actor ID** (`f0xxx`). \
However, during the registration for the round, it can be provided as a standard wallet address `f1, f2, f3, f4, 0x` since Autocap automatically derives the correct address. \
You can check your Actor ID at [https://filecoin.blockscout.com/](https://filecoin.blockscout.com/).
{% endhint %}

#### Address Roles

Registration defines two distinct address roles:

* **Participant Burn Address**\
  This is the address from which on-chain economic activity is measured.\
  Only FIL burns originating from this address are counted toward the round.
* **Participant DataCap Recipient Address**\
  This is the address that receives the DataCap allocation at the end of the round.\
  It is not used for activity measurement.

These roles are independent: activity is always attributed to the Burn Address, while DataCap is always issued to the specified DataCap Recipient Address.

#### Constraints

* Each Participant Burn Address may register **at most once per round**.
* Registration applies only to the active round and does not carry over to future rounds.
