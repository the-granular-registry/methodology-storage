# Market Adoption and Implementation Roadmap for STARs

Introducing a novel instrument like STARs requires not only a sound technical foundation but also a clear value proposition for market participants and a strategic roadmap for adoption. This section outlines the benefits STARs offer to key stakeholders, the relevant policy context, a phased approach to market integration, and potential barriers to overcome.

### Stakeholder Value Proposition

STARs are designed to create value across the energy ecosystem:

* **Corporate Buyers (24/7 CFE & Emissionality):** Gain a simplified, low-risk, auditable method to achieve credible hourly CFE matching or maximize carbon impact using storage. STARs provide flexibility in portfolio construction and optimize the utilization of existing PPA assets, avoiding the complexities and risks of tolling agreements.<sup>21</sup>
* **Storage Operators & Developers:** Unlock a new revenue stream by monetizing the time-shifting attribute of their assets, separate from energy arbitrage or ancillary services. The potential for premium pricing on high-impact (high ΔMER) STARs creates incentives for carbon-optimizing dispatch. Clear market signals from STAR pricing can improve project bankability and inform deployment strategies.<sup>42</sup>
* **Utilities & Energy Suppliers:** Enable the creation of differentiated green tariffs offering verified hourly-matched CFE to customers. STARs provide a mechanism to integrate utility-controlled or third-party storage into supply portfolios for balancing and meeting potential regulatory mandates.<sup>21</sup>
* **Grid Operators & Policymakers:** Introduce a market-based tool to incentivize storage deployment and operation in ways that support grid reliability (CFE integration, peak shaving) and accelerate decarbonization. STARs enhance transparency in tracking CFE flows and impacts, supporting policy goals and grid planning.<sup>7</sup>
* **Registry Providers:** Opportunity to offer innovative, value-added products (STARs) within the evolving EAC/GC landscape, meeting emerging market demands for granularity and storage tracking.<sup>14</sup>

Articulating these distinct benefits is crucial for building the broad stakeholder support necessary for successful market adoption. Demonstrating how STARs address specific pain points or create new opportunities for each group encourages participation and fosters a collaborative ecosystem.

## Navigating the Evolving Policy Landscape

Regulatory and policy developments are creating significant tailwinds for granular tracking and storage solutions like STARs:

* **US Clean Hydrogen Production Tax Credit (PTC) - Section 45V:** The final Treasury regulations mandate hourly matching of EACs for grid-connected electrolytic hydrogen production starting January 1, 2030.<sup>138</sup> Crucially, the rules explicitly allow for this matching to occur via energy storage, provided the EACs meet the "three pillars" (incrementality, hourly temporal matching, deliverability) and the storage process (including losses) is tracked by a qualified registry.<sup>142</sup> STARs and SD-GCs issued through the Granular Registry, which is designed to handle hourly tracking, storage losses, and FIFO, appear well-suited to meet these compliance requirements, creating a strong potential market driver.<sup>146</sup>
* **European Union Regulations (RED III, Fit for 55):** The EU's updated Renewable Energy Directive (RED III) encourages Member States to issue granular (time-stamped) Guarantees of Origin (GOs).<sup>149</sup> Furthermore, EU rules for defining renewable hydrogen will also require hourly matching between electricity consumption and renewable generation by 2030.<sup>24</sup> These developments, part of the broader 'Fit for 55' package aiming for ambitious 2030 climate targets <sup>154</sup>, signal a clear regulatory shift towards granularity where STAR-like mechanisms could play a role in the future, especially given EnergyTag's influence on European standards.<sup>131</sup>
* **GHG Protocol Scope 2 Revisions:** The ongoing updates to the influential GHG Protocol Scope 2 guidance are considering stricter requirements for the market-based method, potentially emphasizing temporal and geographical correlation between consumption and CFE procurement.<sup>14</sup> A move towards favoring or requiring hourly matching would significantly boost demand for GCs and associated time-shifting instruments like STARs.
* **State-Level Initiatives:** Numerous US states have ambitious clean energy goals, RPS mandates, and specific energy storage targets or procurement requirements.<sup>7</sup> As these policies mature, the need for verifiable tracking of storage contributions, potentially through instruments like STARs, is likely to increase.<sup>163</sup>

These regulatory trends, particularly the explicit requirement for hourly matching in significant compliance markets like the 45V tax credit, serve as powerful accelerators. They transform granular tracking and verifiable storage solutions from voluntary enhancements into essential compliance tools, strengthening the business case for STARs and the Granular Registry.

## A Phased Approach to Market Integration

The introduction and scaling of STARs require a structured, phased approach to build market confidence, refine operational processes, and ensure alignment with the broader energy ecosystem . Granular Registry proposes the following roadmap:

#### Phase 1: Pilot Programs & Early Adoption (0-1 Years):

* _**Objective:**_ Validate the technical feasibility and market value proposition of STARs in controlled environments.
* _**Activities:**_ Collaborate with a select group of forward-looking corporate buyers (potentially those involved in initiatives like the GC Trading Alliance <sup>84</sup>) and storage operators. Onboard pilot storage projects onto the Granular Registry. Issue, trade, and retire initial batches of STARs. Test and refine FIFO logic, loss accounting methods, and registry functionalities based on real-world data and user feedback. Establish robust data standards and API specifications for integration.<sup>164</sup> Conduct targeted stakeholder education workshops and outreach.<sup>21</sup> Gather data from pilots in key markets like CAISO and ERCOT.<sup>19</sup>

#### Phase 2: Market Expansion & Regulatory Alignment (1-3 Years):

* _**Objective:**_ Increase market participation and liquidity, achieve interoperability with major REC/GC registries, and gain formal recognition within key voluntary and compliance frameworks.
* _**Activities:**_ Expand the number of registered storage facilities and increase the number of participating buyers. Enable STAR trading through partnerships with existing certificate trading platforms (e.g., potentially leveraging platforms being developed by LevelTen Energy for GCs <sup>83</sup>). Actively engage with standards bodies (EnergyTag, GHG Protocol) to ensure STAR methodology alignment and recognition. Work with regulators to position STARs as a valid compliance tool (e.g., for 45V hourly matching). Enhance integration of MER data feeds for robust emissionality calculations.<sup>1</sup>

#### Phase 3: Global Scale & Policy Integration (3+ Years):

* _**Objective:**_ Achieve widespread market adoption, integrate STARs into global 24/7 CFE procurement practices, and embed STARs within relevant energy policies and compliance mechanisms.
* _**Activities:**_ Establish full interoperability with major international EAC registries (e.g., AIB/EECS for GOs). Advocate for policy incentives (e.g., tax credits, adders in clean energy programs) that explicitly recognize and reward the use of STARs for time-shifting CFE. Explore the use of automation and AI to optimize STAR creation and matching based on real-time grid conditions and forecasts.<sup>3</sup>

This phased strategy enables iterative learning and adaptation, mitigating the risks associated with launching a new market instrument while systematically building the necessary technical infrastructure, market participation, and regulatory support for long-term success.

## Overcoming Barriers to Adoption

Despite the clear need and potential benefits, the widespread adoption of STARs faces several challenges that must be proactively addressed:

* **Data Standardization and Access:** Implementing STARs requires reliable, high-granularity (hourly or sub-hourly) metering data for both CFE generation and storage charge/discharge cycles. Access to this data can be inconsistent across regions and utilities, and standards for data formats and APIs are still evolving.<sup>4</sup> The Granular Registry's APIs <sup>164</sup> aim to facilitate this, but broader ecosystem coordination is needed.
* **Registry Capabilities and Interoperability:** While some registries like M-RETS are advancing hourly tracking <sup>59</sup> and PJM GATS has added hourly retirement functionality <sup>60</sup>, many legacy systems lack the built-in capability to handle the complex logic required for storage (FIFO, losses, linking multiple certificate types).<sup>8</sup> This necessitates either upgrades to existing systems, reliance on specialized platforms like the Granular Registry, or robust interoperability protocols. Delays in registry upgrades (e.g., WREGIS projected 3-5 years <sup>130</sup>) can slow adoption in certain regions. The evolution of European systems under AIB/EECS also needs monitoring.<sup>131</sup>
* **Market Education and Perceived Complexity:** STARs introduce a new layer to the already complex world of energy attributes. Stakeholders (buyers, sellers, regulators) need clear education on how STARs work, their advantages over tolling, and how they integrate into existing procurement and reporting workflows.<sup>21</sup> Overcoming inertia and perceived complexity requires clear communication and demonstrated ease-of-use through registry platforms.
* **Cost and Price Discovery:** Implementing the necessary metering and registry integration for STAR tracking may involve costs for storage operators. For buyers, the market price of STARs relative to conventional RECs or the all-in cost of tolling agreements is currently unknown . 137 Pilot programs and early trading activities, such as potential GC auctions 137, are crucial for establishing price benchmarks and demonstrating the economic viability of STARs.
* **Regulatory and Standards Uncertainty:** The evolving nature of GHG accounting rules (Scope 2 updates <sup>122</sup>), granular certificate standards (EnergyTag refinement <sup>12</sup>), and clean energy policies creates uncertainty that can make potential adopters hesitant.<sup>43</sup> Finalization of key rules (like the 45V regulations <sup>139</sup>) helps reduce this uncertainty, but ongoing engagement with policymakers and standards bodies is essential.

Addressing these barriers requires a concerted effort from Granular Registry and its partners. This includes advocating for data access and standardization, collaborating with other registries on interoperability, providing clear educational materials and user-friendly platforms, facilitating price discovery through pilots, and actively participating in policy and standard-setting processes.
