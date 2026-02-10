# Examples of Eligible Contribution Paths

AutoCap is **agnostic to how Filecoin Pay payment rails are used**, provided that their settlement results in **eligible FIL burns** that meet the contribution criteria defined in the previous page.

The following are **non-exhaustive examples** of workflows that may generate eligible contributions:

* **Providing storage services via** [**Filecoin Pay**](https://pay.filecoin.cloud/) **and settling payment rails** denominated in FIL, resulting in FIL burns&#x20;
* **Storing data through PDP-based storage flows** that rely on Filecoin Pay settlement in FIL, e.g. [https://pdp.vxb.ai/calibration ](https://pdp.vxb.ai/calibration)
* **Storing data via DDO-style workflows on testnet**, where Filecoin Pay is used as the settlement layer e.g. [https://github.com/Eastore-project/ddo-client](https://github.com/Eastore-project/ddo-client)
* **Service provisioning workflows** that use Filecoin Pay as a programmable payment and settlement mechanism

In all cases, AutoCap measures **only the burned FIL outcome** of settlement events.\
The underlying service type, counterparty, deal structure, or associated metadata are **not** considered in contribution accounting.
