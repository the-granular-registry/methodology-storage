# Use Case I: Enabling Credible 24/7 Carbon-Free Energy (CFE)

One of the primary drivers for granular energy tracking and storage integration is the pursuit of 24/7 Carbon-Free Energy (CFE). This strategy aims to match electricity consumption with CFE generation on an hourly basis within the same grid region, moving beyond annual accounting to ensure reliance on clean sources around the clock.<sup>1</sup> STARs provide a critical enabling mechanism for achieving credible 24/7 CFE, particularly for organizations utilizing variable renewable energy sources.

## Methodology: Achieving Hourly Matching with STARs

The core challenge in 24/7 CFE is addressing the temporal mismatch between when CFE resources, such as solar and wind, generate power and when an organization consumes electricity.<sup>3</sup> Solar generation peaks midday, while loads may peak in the evening; wind generation might be highest overnight when loads are lower.<sup>89</sup> Energy storage is the key technology for bridging these temporal gaps.<sup>3</sup> STARs provide the standardized accounting framework to make this time-shifting verifiable for attribute claims:

1. **Identify Surpluses and Deficits:** A CFE buyer first analyzes their hourly load profile against the hourly generation profile of their CFE sources (e.g., from PPAs or onsite generation, represented by GCs). This identifies hours with surplus CFE generation (GCs > Load) and hours with deficits (Load > GCs).
2. **Allocate Surplus GCs for Charging:** During surplus hours, the buyer allocates their excess GCs to a registered storage facility via the Granular Registry. This creates SCRs linked to those GCs, effectively earmarking those clean attributes for storage.<sup>12</sup> The storage operator physically charges the battery during this period (the physical energy source for charging is irrelevant to the _attribute_ tracking, which follows the GC).
3. **Procure STARs:** The storage operator generates STARs based on their physical charge/discharge cycles and associated losses, making these STARs available on the market.
4. **Match GCs with STARs:** The CFE buyer purchases the required quantity of STARs from the storage operator (or secondary market) corresponding to the energy needed to cover their deficit hours.
5. **Retire Instruments for Time-Shifted Claims:** The buyer retires the purchased STARs, along with the original surplus GCs (from the charging hour identified in the STAR's lineage), within the Granular Registry.
6. **Receive SD-GCs:** The Registry validates the retirement and issues non-tradable SD-GCs to the buyer. These SD-GCs have timestamps corresponding to the _discharge_ hours (i.e., the buyer's deficit hours) but retain the source attributes of the original GCs.<sup>12</sup>
7. **Substantiate 24/7 CFE Claim:** The buyer utilizes a combination of directly matched GCs (where generation occurred in the same hour as consumption) and newly created SD-GCs (representing verifiably time-shifted CFE) to demonstrate their hourly CFE matching performance for reporting and verification purposes.

This process provides the missing link: a verifiable, registry-based mechanism to connect surplus CFE attributes from one hour to consumption in another hour via storage. It directly addresses concerns about the credibility of time-shifting claims based on less rigorous methods <sup>5</sup>, ensuring that hourly matching is backed by auditable transactions that account for physical constraints like FIFO and RTE.

## Optimizing Renewable Portfolios with Market-Based Time-Shifting

Corporate buyers often enter into long-term Power Purchase Agreements (PPAs) to secure CFE. However, PPAs tied to a single technology, like solar or wind, inevitably lead to hourly mismatches with typical load profiles.<sup>5</sup> Achieving a high percentage of hourly CFE matching traditionally required either procuring a complex portfolio of diverse CFE resources (e.g., solar, wind, hydro, geothermal) or entering into bundled PPA contracts that include dedicated storage, which can be costly and complex.<sup>3</sup>

STARs introduce a more flexible, market-based approach. They allow buyers to:

* **Leverage Existing Assets:** Buyers with existing CFE PPAs can utilize STARs to enhance their hourly match without requiring contract renegotiation or co-investment in physical storage. They can procure the time-shifting service (STARs) separately as needed.
* **Modular Procurement:** Buyers can source GCs (from PPAs, onsite generation, or unbundled purchases) and STARs independently, potentially from different counterparties and markets. This modularity allows optimization for cost and availability for each component (the clean attribute and the time-shifting service).
* **Complementary Strategy:** STARs complement, rather than replace, traditional PPA strategies. A buyer might secure a cost-effective solar PPA and then use the STAR market to procure the necessary time-shifting to align that solar generation with their evening or nighttime load.

This market-based modularity provides buyers with greater strategic options and potentially lower costs compared to being locked into bundled PPA-plus-storage deals, facilitating broader adoption of 24/7 CFE goals.

## Benefits for 24/7 CFE Buyers

Utilizing STARs for 24/7 CFE strategies offers significant advantages for corporate buyers:

* **Enables Credible Hourly CFE Matching:** Provides the mechanism to verifiably shift CFE attributes across time, addressing criticisms of annual matching and substantiating claims of round-the-clock clean energy use.<sup>1</sup>
* **Optimizes REC and PPA Utilization:** Ensures that surplus CFE generated during certain hours is not wasted from an attribute perspective but is verifiably used to cover consumption in deficit hours, maximizing the value of PPA investments.
* **Enhances Credibility of 24/7 Claims:** Offers auditable proof via the Granular Registry that stored energy attributes are correctly allocated, bolstering the integrity of sustainability reporting.<sup>12</sup>
* **Reduces Reliance on Unrelated Offsets:** Provides a direct, physically linked mechanism for meeting hourly energy needs with CFE, reducing the need to rely on potentially less impactful carbon offsets.<sup>5</sup>
* **Increases Flexibility in Energy Procurement:** Decouples the time-shifting service from energy generation contracts, giving buyers more control and options in designing their CFE procurement portfolio.<sup>21</sup>
* **Avoids Tolling Complexity and Risk:** Circumvents the contractual hurdles, operational oversight requirements, and market/performance risks associated with storage tolling agreements.

## Illustrative Scenarios: Addressing Real-World Mismatches

The practical value of STARs becomes clearer when applied to specific market contexts:

* **Scenario 1: CAISO Solar PPA & the "Duck Curve":** A corporate buyer operates a facility (e.g., data center, manufacturing plant) in California and has a large solar PPA. Due to high solar penetration in CAISO, midday energy prices can be very low, and the buyer generates excess solar GCs during these hours. However, their load persists into the evening after sunset when solar generation ceases, and grid prices/emissions often rise (the "duck curve" phenomenon).<sup>89</sup>
  * _**STAR Application:**_ The buyer allocates their surplus midday solar GCs to SCRs via the Granular Registry. They purchase STARs from a CAISO-based battery operator who physically charges during the day and discharges in the evening. The buyer retires the midday GCs and the purchased STARs, receiving SD-GCs timestamped for the evening hours. This allows them to verifiably claim that their solar PPA output, shifted via storage, met their evening load, directly improving their hourly CFE score and addressing the duck curve challenge from an attribute perspective \[Draft Content Example]. Relevant data includes CAISO historical load <sup>95</sup>, solar generation profiles <sup>89</sup>, and potentially PPA output modeled using tools like NREL's System Advisor Model (SAM).<sup>98</sup>
* **Scenario 2: ERCOT Wind PPA & Industrial Load:** An industrial manufacturer in Texas has a wind PPA in ERCOT. Wind generation is often strongest at night, when grid demand and the facility's operational load are typically lower.<sup>90</sup> The manufacturer needs to cover its significant daytime operational energy consumption with CFE.
  * _**STAR Application:**_ The manufacturer allocates surplus nighttime wind GCs to SCRs. They purchase STARs from an ERCOT-based storage operator who charges overnight and discharges during daytime industrial operating hours. By retiring the nighttime GCs and the STARs, the manufacturer receives SD-GCs that are timestamped for their daytime peak load hours, enabling them to claim that their wind power meets their primary operational demand \[Draft Content Example]. ERCOT load data <sup>105</sup> and wind generation data <sup>90</sup> can illustrate these typical patterns.
* **Scenario 3: Data Center Baseload Demand:** A data center operates with a relatively constant, high baseload demand profile 24/7.<sup>105</sup> They procure CFE through a mix of solar and wind PPAs, resulting in variable hourly supply.
  * _**STAR Application:**_ The data center utilizes STARs to mitigate the variability of its CFE supply. They allocate surplus GCs (from both solar and wind) during oversupply hours to SCRs and purchase STARs to cover hours where their combined PPA generation falls short of their constant load. This enables them to achieve a very high hourly CFE score, which is critical for demonstrating sustainability leadership, given their significant energy footprint.<sup>19</sup>

These scenarios demonstrate how STARs provide a practical, market-based tool for diverse buyers in different regions to verifiably align intermittent CFE generation with their specific hourly consumption patterns, making ambitious 24/7 CFE goals attainable and credible.
