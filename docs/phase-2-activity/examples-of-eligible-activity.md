# Examples of Eligible Activity

Autocap is agnostic to _how_ Filecoin Pay rails are used, as long as they result in eligible FIL burns. Typical examples include (non-exhaustive):

* **Providing storage services via** [**Filecoin Pay**](https://pay.filecoin.cloud/) **and settling payment rails**, resulting in FIL burns&#x20;
* **Storing data through PDP-based storage flows** that rely on Filecoin Pay settlement, e.g. [https://pdp.vxb.ai/calibration ](https://pdp.vxb.ai/calibration)
* **Storing data via DDO-style workflows on testnet**, where Filecoin Pay is used as the settlement layer e.g. [https://github.com/Eastore-project/ddo-client](https://github.com/Eastore-project/ddo-client)
* **Service provisioning workflows** that use Filecoin Pay as a programmable payment and settlement mechanism

In all cases, Autocap measures only the **burned FIL outcome**, not the service type, counterparty, or metadata.
