# 1. Registration

![](https://hackmd.io/_uploads/Skl0xDGSZe.png)

When a round opens, participants can register through the [Autocap Dashboard](https://filautocap.xyz/) by:

*   Connecting a Filecoin-compatible wallet;

    _(this wallet becomes the **Participant Address** tracked for on-chain activity)_
* Paying the registration fee from that wallet;
* Providing a **DataCap Actor ID** (`f0xxx`) where any allocated DC will be sent\
  &#xNAN;_(this is the address of the wallet that will receive DC)_

Registration establishes the binding between measured on-chain activity and the DC recipient for the round.

**Important:** Registration defines two distinct address roles:

* **Participant Address (wallet address)** This is the address from which **on-chain activity is measured**. Only activity originating from this address is counted toward the round.
* **DataCap Actor ID (`f0xxx`)** This is the address that receives the DC allocation at the end of the round. It is not used for activity measurement.

Each Participant Address may register **at most once per round**.
