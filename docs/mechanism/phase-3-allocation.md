# 3. Allocation and Distribution

Once a round closes, AutoCap determines DataCap (DC) allocations based on the economic activity observed during that round.

Allocation is driven entirely by **eligible FIL burns**. Only FIL that was burned as a result of finalized Filecoin Pay settlement events, originating from registered Participant Burn Addresses and occurring within the round window, is taken into account. No off-chain inputs, manual adjustments, or discretionary decisions play any role in this process.

Formally, AutoCap applies a **proportional allocation rule**. Each participant’s share of the round’s DataCap pool is equal to their share of the total eligible FIL burned during the round.

#### The Formula

Let:

* _DC_<sub>_pool_</sub> be the total DataCap available for distribution in the round
* _B_<sub>_total​_</sub> be the total eligible FIL burned by all participants during the round
* _B_<sub>_i_</sub><sub>​</sub> be the eligible FIL burned by _i-th_ participant

The DC allocation that the _i-th_ participant receives is given by:

{% include "../.gitbook/includes/dc-formula.md" %}

This formula is applied once, at round close, using the finalized on-chain data recorded during the round.

{% hint style="info" %}
#### Example

* Round has 10 TiB of DC to distribute
* Total FIL burned by all participants: 100 FIL
* Alice burned 10 FIL (10% of total) from the Burn Address
* Alice receives 1 TiB (10% of total DC) in the DataCap Recipient Address
{% endhint %}

{% hint style="warning" %}
#### Minimum Allocation is 1 MiB (1,048,576 bytes)

Only allocation over 1 MiB will be executed by AutoCap.

Any allocation below this threshold will not receive any DC during the round.
{% endhint %}

#### Allocation Properties&#x20;

This mechanism ensures:

* **Fairness:** allocations are strictly proportional to contribution;
* **Transparency:** all inputs are on-chain and publicly verifiable;
* **Determinism:** the outcome depends only on observed data, not discretion

#### Finality and Edge Cases

If no eligible FIL is burned during a round, no DataCap is allocated for that round.

Each round is evaluated independently. Allocation results are final once computed and are never adjusted retroactively based on future activity.

DataCap is issued to the **DataCap Recipient Address** specified by each participant at registration.
