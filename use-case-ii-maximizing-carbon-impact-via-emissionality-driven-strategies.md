# Use Case II: Maximizing Carbon Impact via Emissionality-Driven Strategies

Beyond achieving hour-for-hour CFE matching, a growing number of organizations are focusing on maximizing the _decarbonization impact_ of their clean energy procurement. This "emissionality" or "impact accounting" approach seeks to deploy clean energy resources in a manner that displaces the maximum amount of greenhouse gas emissions from the electricity grid.<sup>1</sup> Energy storage, facilitated by STARs, plays a crucial role in enabling these strategies by shifting clean energy into the highest-impact periods.

## Methodology: Quantifying Avoided Emissions with Marginal Emissions Rates (MERs)

The core principle of emissionality is that not all MWh of clean energy has the same impact on grid emissions. Injecting clean energy when the grid is already saturated with renewable energy sources might displace other clean sources or have a minimal effect. However, injecting clean energy when the grid is reliant on high-emitting fossil fuel "peaker" plants to meet demand can result in significant avoided emissions.<sup>16</sup>

The key metric for quantifying this impact is the Marginal Emissions Rate (MER), typically expressed in kilograms or metric tons of CO₂ equivalent per megawatt-hour (kg CO₂-e/MWh or t CO₂-e/MWh). The MER represents the emissions intensity of the power plant(s) that would ramp up or down to meet the next increment (or decrement) of electricity demand at a specific location and time.<sup>28</sup> MERs fluctuate constantly based on the real-time grid generation mix, demand levels, transmission constraints, and fuel prices. Data providers like REsurety, WattTime offer real-time and forecasted MER data for various grid regions.<sup>30</sup>

Energy storage enables emissionality strategies by facilitating carbon arbitrage:

* **Charging:** Store energy (ideally represented by zero-emission GCs) during periods when the grid's MER is low (e.g., high CFE output, low demand).
* **Discharging:** Releasing the stored energy back to the grid during periods when the MER is high (e.g., when peak demand is met by gas peakers or low CFE output).

STARs provide the essential tracking mechanism for this process. By recording the precise timestamps of the charging event (via the SCR) and the discharging event (via the SDR), STARs enable the association of MER data with each end of the storage cycle. This allows for quantifying the _net carbon impact_ achieved by the time-shifting operation.

## The STAR Carbon Impact Calculation

The Granular Registry, using the temporal data embedded in the STAR and integrating external MER data feeds, can calculate the estimated carbon impact of the time shift. This whitepaper proposes a net impact calculation:

$$
Net\ Impact\ =\ ({MWh}_{discharged}\ \ast\ {MER}_{discharge_time})\ -\ ({MWh\ }_{charged}\ \ast\ {MER}_{charge_time})
$$

Where:

●      _MWh\_discharged​_ is the energy discharged (already accounting for losses, i.e., MWh\_discharged​=MWhCharged​×RTE).

●      _MER\_discharge\_tim&#x65;_&#x200B; is the marginal emissions rate at the location during the discharge hour(s).

●      _MWh\_charge&#x64;_&#x200B; is the energy charged.

●      _MER\_charge\_tim&#x65;_&#x200B; is the marginal emissions rate at the location during the charging hour(s).

The STAR carries a "carbon uplift" potential based on the net impact. This uplift is applied to the final SD-GC when the STAR is retired with the original GC. The impact recorded on the SD-GC could then be represented as:

$$
{SD-GC}_{Impact}\ ={Original\ GC}_{Impact}\ +{STAR}_{Impact}
$$

The process requires access to reliable, granular (hourly or sub-hourly), and location-specific MER data for both charge and discharge periods.<sup>26</sup> Transparency regarding the MER data source and calculation methodology is crucial for the credibility of any impact claims derived from STARs.

## Optimizing Storage Dispatch for Grid Decarbonization

Currently, most grid-scale batteries are dispatched primarily based on economic signals – maximizing revenue through energy price arbitrage (buy low, sell high) and participation in ancillary service markets.<sup>40</sup> These economic incentives do not always align with maximizing grid decarbonization. A battery might charge using high-MER grid power if prices are low enough, and discharge during lower-MER periods if prices are sufficiently high, potentially leading to a net increase in grid emissions.

STARs offer a mechanism to correct this misalignment by introducing a direct financial incentive tied to carbon impact. Suppose STARs associated with high avoided emissions (i.e., a large positive ΔMER, achieved by discharging during very high MER periods) command a premium price in the market. In that case, storage operators gain a new revenue stream to consider in their dispatch optimization.<sup>1</sup>

Operators could then co-optimize their dispatch strategy considering:

1. Energy arbitrage margins.
2. Ancillary service payments.
3. The potential market value of the STARs generated, based on their calculated carbon impact.

This creates a tangible carbon price signal influencing operational decisions, encouraging operators to shift charging towards low-MER hours and discharging towards high-MER hours, thereby contributing more effectively to grid decarbonization.

### Waterfall Chart Showing GC Carbon Uplift using STARs

<figure><img src=".gitbook/assets/image.png" alt="Waterfall Chart Showing GC Carbon Uplift using STARs"><figcaption></figcaption></figure>

## Benefits for Emissionality Stakeholders

Adopting STARs for emissionality-focused strategies provides several benefits:

* **Targeted Carbon Reduction:** Enables buyers to specifically procure clean energy attributes that are verifiably shifted to maximize CO₂e displacement on the grid.
* **Enhanced Impact Claims:** Provides a quantitative metric (e.g., kgCO₂e avoided per MWh shifted, based on ΔMER) to support more sophisticated and impactful sustainability claims, going beyond simple hourly matching.<sup>28</sup>
* **Market Signal for High-Impact Storage:** Creates explicit market demand and financial value for storage assets deployed in locations and operated during times that offer the greatest potential for displacing fossil fuels.<sup>1</sup>
* **Alignment with Policy Goals:** Supports policy objectives aimed at achieving deeper, faster grid decarbonization by incentivizing the most impactful use of clean resources and flexibility assets.

## Contextualizing within Carbon Accounting Frameworks

Integrating emissionality claims based on STARs and MERs into established corporate carbon accounting frameworks, particularly the GHG Protocol Scope 2 Guidance, requires careful consideration.<sup>86</sup>

* **GHG Protocol Scope 2 (Market-Based Method):** This method allows companies to report emissions based on the attributes of the energy they contractually purchase, typically via EACs.<sup>15</sup> Retiring a GC or an SD-GC representing zero-emission generation (e.g., solar, wind) allows the buyer to claim zero emissions for the corresponding MWh of consumption in that specific hour. This is an _attributional_ approach – attributing the characteristics of the purchased instrument to the consumption.
* **Emissionality (MER-Based Impact):** Calculating avoided emissions using MERs (ΔMER) is fundamentally a _consequential_ approach.<sup>29</sup> It estimates the change in _total grid emissions_ that occurred as a consequence of the decision to shift energy from one time to another.<sup>117</sup>

**Recommended Positioning:** To maintain accounting integrity and avoid conflict with established protocols, the calculated carbon impact (ΔMER or total avoided emissions) associated with a STAR should be treated as supplementary information recorded on the SD-GC, rather than a modification of the core Scope 2 emission factor. This allows:

1. Buyers to use the SD-GC for standard Scope 2 market-based reporting (claiming zero emissions for the MWh consumed in the discharge hour).
2. Buyers focused on emissionality to separately report the _additional estimated grid impact_ (avoided emissions based on ΔMER) facilitated by their use of storage and STARs, using this data for broader impact narratives and potentially influencing future accounting standards.

This approach preserves the integrity of current Scope 2 accounting while still providing the valuable impact quantification enabled by STARs and MER data for organizations pursuing emissionality goals.

