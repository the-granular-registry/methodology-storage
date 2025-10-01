# Appendix

## A.1 EnergyTag Alignment Details

The STAR framework is designed for compatibility with the EnergyTag initiative's standards:

●      GC Scheme Standard V2 (March 2024) <sup>12</sup>:

○      GC Definition: STARs operate on GCs compliant with EnergyTag definitions (Chapter 1.2).

○      Storage Definition (1.6.1): Applies to systems where input/output energy carriers are the same (e.g., electricity-to-electricity storage).

○      SCR/SDR Records (1.6.2, 1.6.5): The Granular Registry's SCR and SDR objects fulfill the mandatory recording requirements for charge/discharge intervals and quantities.

○      Loss Accounting (1.6.4, Annex 2): STARs explicitly record round\_trip\_loss\_wh, aligning with the requirement to account for losses based on measurements.

○      Time-Shifting & Attribute Transfer (1.6.5): The STAR mechanism facilitates the time-shifting process described, linking canceled input GCs (via SCR) to discharge events (SDR) and resulting in an SD-GC with updated timestamps and preserved attributes.

○      SD-GC Issuance (1.6.5.ii): The creation of the final SD-GC upon STAR+GC retirement aligns with the concept of issuing a Storage Discharge GC representing the released energy attributes.

○      Allocation Methods (Annex 3): FIFO is a specific, transparent method consistent with the need for a defined allocation logic.

●      EnergyTag Matching Standard <sup>38</sup> & Use Case Guidelines <sup>27</sup>: SD-GCs generated via STAR retirement can be used for temporal matching claims according to the rules defined in these documents. The STAR process provides the necessary verifiable link for storage-involved matching.

●      EnergyTag Diagrams: The conceptual flow aligns with EnergyTag schematics illustrating energy storage interactions within a GC system.<sup>12</sup>

<figure><img src=".gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

## A.2 Glossary

●      24/7 CFE (Carbon-Free Energy): An energy procurement strategy aiming to match electricity consumption with carbon-free energy generation on an hourly basis within the same grid region.

●      AIB (Association of Issuing Bodies): Organization that develops and maintains the European Energy Certificate System (EECS) for Guarantees of Origin.

●      Attribute (Energy Attribute): A characteristic of energy generation, such as fuel source, location, time of production, or emissions profile, tracked via EACs/GCs.

●      Audit Trail: An immutable record of transactions and state changes within a registry, allowing for verification and traceability.

●      Blockchain Anchoring: Periodically recording cryptographic summaries (hashes) of registry data onto a public blockchain to provide tamper evidence.

●      EAC (Energy Attribute Certificate): A generic term for a tradable certificate representing the attributes of a unit of energy (typically 1 MWh). Includes RECs, GOs, etc.

●      EECS (European Energy Certificate System): The standardized system managed by AIB for issuing, trading, and canceling Guarantees of Origin in Europe.

●      Emissionality: An energy procurement strategy focused on maximizing the avoided greenhouse gas emissions by deploying clean energy when and where it displaces the highest-emitting grid resources, often using MER data.

●      EnergyTag: An independent, industry-led initiative developing standards for Granular Certificates (GCs) to enable hourly energy attribute tracking.

●      FIFO (First-In-First-Out): An accounting method used in the STAR system where the energy attributes charged into storage first are considered discharged first.

●      GC (Granular Certificate): An Energy Attribute Certificate with an hourly or sub-hourly timestamp, compliant with EnergyTag standards.

●      Granular Registry: Granular Registry's platform for issuing, tracking, and managing GCs, STARs, and related storage records.

●      JWS (JSON Web Signature): A standard for digitally signing JSON data structures to ensure integrity and authenticity.

●      MER (Marginal Emissions Rate): The rate of greenhouse gas emissions (e.g., kgCO₂e/MWh) associated with the next unit of electricity generation dispatched on the grid at a specific time and location.

●      PPA (Power Purchase Agreement): A long-term contract between an energy buyer and a generator to purchase electricity and/or associated environmental attributes.

●      REC (Renewable Energy Certificate): The common type of EAC used in North America, representing 1 MWh of renewable electricity generation.

●      RTE (Round-Trip Efficiency): The ratio of energy discharged from a storage system to the energy charged into it, expressed as a percentage, accounting for losses.

●      SCR (Storage Charge Record): A registry record documenting the charging of energy (and associated GC attributes) into a storage system during a specific interval.

●      SDR (Storage Discharge Record): A registry record documenting the discharging of energy from a storage system during a specific interval.

●      SD-GC (Storage-Discharge Granular Certificate): A final, non-tradable GC issued upon retirement of a STAR and original GC, representing the time-shifted clean energy attribute with an updated timestamp reflecting the discharge time.

●      STAR (Storage Time Allocation Record): A novel, tradable certificate issued by the Granular Registry representing the verified right to time-shift energy attributes via a registered storage facility, accounting for losses and FIFO allocation.

●      Tolling Agreement (Storage): A contract where a buyer pays a fee to control the charge/discharge operations of a storage facility owned by another party.

●      CFE (Variable Renewable Energy): Renewable energy sources whose output fluctuates based on weather conditions, such as solar and wind power.

●      DID (Decentralized Identifier): A new type of verifiable, decentralized digital identifier controlled by its subject.

●      VC (Verifiable Credential): A standardized format for digital credentials containing claims that are cryptographically secured and verifiable.

## A3. Works cited

1\.     Home • EnergyTag, accessed April 21, 2025, [https://energytag.org/](https://energytag.org/)

2\.     The Granular Registry: Introduction, accessed April 21, 2025, [https://docs.granular-foundation.org/](https://docs.granular-foundation.org/)

3\.     24/7 Carbon-free energy: What it is and why it can help cities to eliminate fossil fuels from their grid - C40 Knowledge Hub, accessed April 21, 2025, [https://www.c40knowledgehub.org/s/article/24-7-Carbon-free-energy-What-it-is-and-why-it-can-help-cities-to-eliminate-fossil-fuels-from-their-grid?language=en\_US](https://www.c40knowledgehub.org/s/article/24-7-Carbon-free-energy-What-it-is-and-why-it-can-help-cities-to-eliminate-fossil-fuels-from-their-grid?language=en_US)

4\.     The State of 24/7 Carbon-free Energy: Recent Progress and What to Watch, accessed April 21, 2025, [https://www.wri.org/insights/247-carbon-free-energy-progress](https://www.wri.org/insights/247-carbon-free-energy-progress)

5\.     We must move on from RECs - DCD - Data Center Dynamics, accessed April 21, 2025, [https://www.datacenterdynamics.com/en/opinions/we-must-move-on-from-recs/](https://www.datacenterdynamics.com/en/opinions/we-must-move-on-from-recs/)

6\.     How should hybrid resources (renewable+battery) be issued RECs? : r/energy - Reddit, accessed April 21, 2025, [https://www.reddit.com/r/energy/comments/1amdie6/how\_should\_hybrid\_resources\_renewablebattery\_be/](https://www.reddit.com/r/energy/comments/1amdie6/how_should_hybrid_resources_renewablebattery_be/)

7\.     DOES ENERGY STORAGE FIT IN AN RPS?, accessed April 21, 2025, [https://www.cesa.org/wp-content/uploads/Energy-Storage-and-RPS-Holt.pdf](https://www.cesa.org/wp-content/uploads/Energy-Storage-and-RPS-Holt.pdf)

8\.     24/7 Hourly Matching of Electricity | US EPA, accessed April 21, 2025, [https://www.epa.gov/green-power-markets/247-hourly-matching-electricity](https://www.epa.gov/green-power-markets/247-hourly-matching-electricity)

9\.     What You Need to Know about BESS Tolling Agreements - Green Dealflow, accessed April 21, 2025, [https://greendealflow.com/what-you-need-to-know-about-bess-tolling-agreements](https://greendealflow.com/what-you-need-to-know-about-bess-tolling-agreements)

10\.  Tolling agreements and floor pricing for BESS - enspired, accessed April 21, 2025, [https://hub.enspired-trading.com/blog/tolling-agreements-and-floor-pricing-for-bess](https://hub.enspired-trading.com/blog/tolling-agreements-and-floor-pricing-for-bess)

11\.  CRU Review of Large Energy Users connection policy (EnergyTag Response, accessed April 21, 2025, [https://consult.cru.ie/en/system/files/materials/200/CRU202504u%20-%20EnergyTag\_1.pdf](https://consult.cru.ie/en/system/files/materials/200/CRU202504u%20-%20EnergyTag_1.pdf)

12\.  Granular Certificate Scheme Standard | EnergyTag, accessed April 21, 2025, [https://energytag.org/wp-content/uploads/2024/12/EnergyTag\_Granular-Certificate-Scheme-Standard-V2.pdf](https://energytag.org/wp-content/uploads/2024/12/EnergyTag_Granular-Certificate-Scheme-Standard-V2.pdf)

13\.  Locational Matching of Granular Certificates - Energy Track & Trace, accessed April 21, 2025, [https://energytrackandtrace.com/wp-content/uploads/2023/11/2022-09-Paper-Locational-Matching-of-Granular-Certificates.pdf](https://energytrackandtrace.com/wp-content/uploads/2023/11/2022-09-Paper-Locational-Matching-of-Granular-Certificates.pdf)

14\.  Announcing the Granular Registry: A New Era for Granular Certificates, accessed April 21, 2025, [https://www.granular-foundation.org/post/announcing-the-granular-registry-a-new-era-for-granular-certificates](https://www.granular-foundation.org/post/announcing-the-granular-registry-a-new-era-for-granular-certificates)

15\.  What is the GHG Protocol: Scope 2 Guidance - Becour, accessed April 21, 2025, [https://becour.com/renewable-energy/news/how-to-follow-the-ghg-protocol-scope-2-guidance-2/](https://becour.com/renewable-energy/news/how-to-follow-the-ghg-protocol-scope-2-guidance-2/)

16\.  Briefing: 24/7 renewable electricity matching is a far more credible approach for the GHG Protocol and the SBTi than the Emissions First Partnership proposal | NewClimate Institute, accessed April 21, 2025, [https://newclimate.org/news/briefing-247-renewable-electricity-matching-is-a-far-more-credible-approach-for-the-ghg](https://newclimate.org/news/briefing-247-renewable-electricity-matching-is-a-far-more-credible-approach-for-the-ghg)

17\.  The future of energy certificates: Putting a precise timestamp on green power - Statkraft, accessed April 21, 2025, [https://www.statkraft.com/newsroom/explained/the-future-of-energy-certificates-putting-a-precise-timestamp-on-green-power/](https://www.statkraft.com/newsroom/explained/the-future-of-energy-certificates-putting-a-precise-timestamp-on-green-power/)

18\.  MAKING '24/7 CARBON-FREE ENERGY' A REALITY, accessed April 21, 2025, [https://www.seforall.org/system/files/2023-05/rm-case-study\_carbon-free-energy.pdf](https://www.seforall.org/system/files/2023-05/rm-case-study_carbon-free-energy.pdf)

19\.  Case Studies - EnergyTag, accessed April 21, 2025, [https://energytag.org/case\_studies/](https://energytag.org/case_studies/)

20\.  Iron Mountain decarbonizing with Google Cloud CFE Suite, accessed April 21, 2025, [https://cloud.google.com/blog/topics/sustainability/iron-mountain-decarbonizing-with-google-cloud-cfe-suite](https://cloud.google.com/blog/topics/sustainability/iron-mountain-decarbonizing-with-google-cloud-cfe-suite)

21\.  Exploring the 24/7 carbon-free energy (CFE) ecosystem - the future of corporate procurement - Eurelectric, accessed April 21, 2025, [https://www.eurelectric.org/in-detail/exploring-the-24-7-carbon-free-energy-cfe-ecosystem-the-future-of-corporate-procurement/](https://www.eurelectric.org/in-detail/exploring-the-24-7-carbon-free-energy-cfe-ecosystem-the-future-of-corporate-procurement/)

22\.  Pursuing 24/7 carbon-free energy is complex. Here's what really matters. | Utility Dive, accessed April 21, 2025, [https://www.utilitydive.com/news/247-carbon-free-energy-investors-power-producers/732419/](https://www.utilitydive.com/news/247-carbon-free-energy-investors-power-producers/732419/)

23\.  What is 24/7 carbon free energy matching? - Eurelectric, accessed April 21, 2025, [https://www.eurelectric.org/in-detail/247-2/](https://www.eurelectric.org/in-detail/247-2/)

24\.  Improve your energy procurement contracts with 24/7 carbon free energy matching, accessed April 21, 2025, [https://www.eurelectric.org/in-detail/energyprocurement/](https://www.eurelectric.org/in-detail/energyprocurement/)

25\.  www.eurelectric.org, accessed April 21, 2025, [https://www.eurelectric.org/in-detail/247-2/#:\~:text=Eurelectric%20Power%20Summit.-,What%20are%20the%20main%20challenges%20to%20adopting%20a%2024%2F7,develop%20this%20enhanced%20procurement%20strategy.](https://www.eurelectric.org/in-detail/247-2/)

26\.  Granular Certificate Scheme Standard | EnergyTag, accessed April 21, 2025, [https://energytag.org/wp-content/uploads/2022/03/20220329-GC-Scheme-Standard.pdf](https://energytag.org/wp-content/uploads/2022/03/20220329-GC-Scheme-Standard.pdf)

27\.  Granular Certificate Use Case Guidelines | EnergyTag, accessed April 21, 2025, [https://www.energytag.org/wp-content/uploads/2022/03/20220329-GC-Use-Case-Guidelines.pdf](https://www.energytag.org/wp-content/uploads/2022/03/20220329-GC-Use-Case-Guidelines.pdf)

28\.  Sustainability Dashboard Methodology - World Resources Institute, accessed April 21, 2025, [https://www.wri.org/sustainability-wri/dashboard/methodology](https://www.wri.org/sustainability-wri/dashboard/methodology)

29\.  Consequential Analysis of the Greenhouse Gas Emissions Impacts of Actions That Influence the Electric Grid - NREL, accessed April 21, 2025, [https://www.nrel.gov/docs/fy25osti/91580.pdf](https://www.nrel.gov/docs/fy25osti/91580.pdf)

30\.  Methodology + Validation - WattTime, accessed April 21, 2025, [https://watttime.org/data-science/methodology-validation/](https://watttime.org/data-science/methodology-validation/)

31\.  Energy Attribute Certificates (EACs) | US EPA, accessed April 21, 2025, [https://www.epa.gov/green-power-markets/energy-attribute-certificates-eacs](https://www.epa.gov/green-power-markets/energy-attribute-certificates-eacs)

32\.  Energy Attribute Certificate FAQs - 3Degrees, accessed April 21, 2025, [https://3degreesinc.com/what-we-do/implement-your-strategy/energy-attribute-certificates/energy-attribute-certificate-faqs/](https://3degreesinc.com/what-we-do/implement-your-strategy/energy-attribute-certificates/energy-attribute-certificate-faqs/)

33\.  A Beginner's Guide to Energy Attribute Certificates (EACs) | Green Project Technologies, accessed April 21, 2025, [https://www.greenprojecttech.com/newsroom/a-beginners-guide-to-energy-attribute-certificates-eacs](https://www.greenprojecttech.com/newsroom/a-beginners-guide-to-energy-attribute-certificates-eacs)

34\.  T-EACs help drive around the clock carbon-free energy | Google Cloud Blog, accessed April 21, 2025, [https://cloud.google.com/blog/topics/sustainability/t-eacs-help-drive-around-the-clock-carbon-free-energy](https://cloud.google.com/blog/topics/sustainability/t-eacs-help-drive-around-the-clock-carbon-free-energy)

35\.  Status and Trends Report on U.S. Energy Attribute Tracking Systems - Environmental Protection Agency (EPA), accessed April 21, 2025, [https://www.epa.gov/system/files/documents/2025-01/status\_and\_trends\_report\_us\_energy\_attribute\_tracking\_systems.pdf](https://www.epa.gov/system/files/documents/2025-01/status_and_trends_report_us_energy_attribute_tracking_systems.pdf)

36\.  Granular Certificate Use Case Guidelines | EnergyTag, accessed April 21, 2025, [https://energytag.org/wp-content/uploads/2023/09/Granular-Certificate-Use-Case-Guidelines-V2.pdf](https://energytag.org/wp-content/uploads/2023/09/Granular-Certificate-Use-Case-Guidelines-V2.pdf)

37\.  What is GHG Accounting? Market-based mistake - Greenhouse Gas Management Institute, accessed April 21, 2025, [https://ghginstitute.org/2024/01/31/what-is-ghg-accounting-market-based-mistake/](https://ghginstitute.org/2024/01/31/what-is-ghg-accounting-market-based-mistake/)

38\.  Granular Certificate Matching Standard | EnergyTag, accessed April 21, 2025, [https://energytag.org/wp-content/uploads/2024/03/Granular-Certificate-Matching-Standard\_V1.pdf](https://energytag.org/wp-content/uploads/2024/03/Granular-Certificate-Matching-Standard_V1.pdf)

39\.  Renewable Energy Storage Facts - The American Clean Power Association (ACP), accessed April 21, 2025, [https://cleanpower.org/facts/clean-energy-storage/](https://cleanpower.org/facts/clean-energy-storage/)

40\.  Hybrid Storage Market Assessment: A JISEA White Paper - NREL, accessed April 21, 2025, [https://www.nrel.gov/docs/fy18osti/70237.pdf](https://www.nrel.gov/docs/fy18osti/70237.pdf)

41\.  Pathways to Commercial Liftoff: Long Duration Energy Storage, accessed April 21, 2025, [https://liftoff.energy.gov/wp-content/uploads/2023/05/Pathways-to-Commercial-Liftoff-LDES-May-5\_UPDATED.pdf](https://liftoff.energy.gov/wp-content/uploads/2023/05/Pathways-to-Commercial-Liftoff-LDES-May-5_UPDATED.pdf)

42\.  System Benefits of Granular Certification - Elering, accessed April 21, 2025, [https://www.elering.ee/sites/default/files/2022-08/ETT\_System%20benefits%20paper\_1\_0.pdf](https://www.elering.ee/sites/default/files/2022-08/ETT_System%20benefits%20paper_1_0.pdf)

43\.  The challenge of truly clean-powered operations - pv magazine USA, accessed April 21, 2025, [https://pv-magazine-usa.com/2025/04/07/the-challenge-of-truly-clean-powered-operations/](https://pv-magazine-usa.com/2025/04/07/the-challenge-of-truly-clean-powered-operations/)

44\.  States Energy Storage Policy, accessed April 21, 2025, [https://www.cesa.org/wp-content/uploads/State-Energy-Storage-Policy-Best-Practices-for-Decarbonization.pdf](https://www.cesa.org/wp-content/uploads/State-Energy-Storage-Policy-Best-Practices-for-Decarbonization.pdf)

45\.  Grid Operational Impacts of Widespread Storage Deployment - NREL, accessed April 21, 2025, [https://www.nrel.gov/docs/fy22osti/80688.pdf](https://www.nrel.gov/docs/fy22osti/80688.pdf)

46\.  Energy Storage 101, accessed April 21, 2025, [https://storagewiki.epri.com/index.php/Energy\_Storage\_101](https://storagewiki.epri.com/index.php/Energy_Storage_101)

47\.  The challenge of truly clean-powered operations - PV Magazine, accessed April 21, 2025, [https://www.pv-magazine.com/2025/04/07/the-challenge-of-truly-clean-powered-operations/](https://www.pv-magazine.com/2025/04/07/the-challenge-of-truly-clean-powered-operations/)

48\.  Draft: White Paper on the Value of Energy Storage to the Future Power System, accessed April 21, 2025, [https://www.nwcouncil.org/sites/default/files/energy-storage-whitepaper-plusappendix-draft-for-release.pdf](https://www.nwcouncil.org/sites/default/files/energy-storage-whitepaper-plusappendix-draft-for-release.pdf)

49\.  Beyond Renewable Integration: The Energy Storage Value Proposition, accessed April 21, 2025, [https://acore.org/wp-content/uploads/2017/12/Beyond-Renewable-Integration\_The-Energy-Storage-Value-Proposition.pdf](https://acore.org/wp-content/uploads/2017/12/Beyond-Renewable-Integration_The-Energy-Storage-Value-Proposition.pdf)

50\.  EXECUTIVE SUMMARY: Energy Storage Systems for Ancillary Services, accessed April 21, 2025, [https://www.ctc-n.org/sites/default/files/resources/asvc-11-executive-summary.pdf](https://www.ctc-n.org/sites/default/files/resources/asvc-11-executive-summary.pdf)

51\.  Elevating the role of energy storage on the electric grid - Deloitte, accessed April 21, 2025, [https://www2.deloitte.com/us/en/insights/industry/power-and-utilities/battery-energy-storage-electric-grid.html](https://www2.deloitte.com/us/en/insights/industry/power-and-utilities/battery-energy-storage-electric-grid.html)

52\.  Fact Sheet | Energy Storage (2019) | White Papers | EESI, accessed April 21, 2025, [https://www.eesi.org/papers/view/energy-storage-2019](https://www.eesi.org/papers/view/energy-storage-2019)

53\.  FINAL SEIA Energizing Battery Storage Manufacturing Whitepaper-Nov 2023, accessed April 21, 2025, [https://seia.org/wp-content/uploads/2023/11/FINAL20SEIA20Energizing20Battery20Storage20Manufacturing20Whitepaper-Nov202023\_0.pdf](https://seia.org/wp-content/uploads/2023/11/FINAL20SEIA20Energizing20Battery20Storage20Manufacturing20Whitepaper-Nov202023_0.pdf)

54\.  energy storage update - Orrick, Herrington & Sutcliffe LLP, accessed April 21, 2025, [https://media.orrick.com/Media%20Library/public/files/o/orrick-energy-storage-update-and-outlook-2024.pdf](https://media.orrick.com/Media%20Library/public/files/o/orrick-energy-storage-update-and-outlook-2024.pdf)

55\.  A 2025 Update on Utility-Scale Energy Storage Procurements - Morgan Lewis, accessed April 21, 2025, [https://www.morganlewis.com/pubs/2025/03/a-2025-update-on-utility-scale-energy-storage-procurements](https://www.morganlewis.com/pubs/2025/03/a-2025-update-on-utility-scale-energy-storage-procurements)

56\.  A 2024 Update on Utility-Scale Energy Storage Procurements - Morgan Lewis, accessed April 21, 2025, [https://www.morganlewis.com/pubs/2024/03/an-update-on-utility-scale-energy-storage-procurements](https://www.morganlewis.com/pubs/2024/03/an-update-on-utility-scale-energy-storage-procurements)

57\.  Maine Energy Storage Program, accessed April 21, 2025, [https://www.maine.gov/energy/sites/maine.gov.energy/files/2024-12/GEO%20Energy%20Storage%20Program%20Recommendations%20Dec%2023%202024.pdf](https://www.maine.gov/energy/sites/maine.gov.energy/files/2024-12/GEO%20Energy%20Storage%20Program%20Recommendations%20Dec%2023%202024.pdf)

58\.  Frequently Asked Questions - M-RETS, accessed April 21, 2025, [https://www.mrets.org/resources/faqs/](https://www.mrets.org/resources/faqs/)

59\.  24/7 Hourly Energy Matching & Tracking - M-RETS, accessed April 21, 2025, [https://www.mrets.org/solutions/hourly-tracking/](https://www.mrets.org/solutions/hourly-tracking/)

60\.  Generation Attribute Tracking System Hourly Certificate - PJM-EIS, accessed April 21, 2025, [https://www.pjm-eis.com/-/media/DotCom/pjm-eis/rec-creation/hourly-certification-info-sheet.pdf](https://www.pjm-eis.com/-/media/DotCom/pjm-eis/rec-creation/hourly-certification-info-sheet.pdf)

61\.  PJM EIS - Home, accessed April 21, 2025, [https://pjm-eis.com/](https://pjm-eis.com/)

62\.  What is the difference between bundled and unbundled EACs? - Ecohz, accessed April 21, 2025, [https://www.ecohz.com/blog/bundled-vs-unbundled-eacs](https://www.ecohz.com/blog/bundled-vs-unbundled-eacs)

63\.  Storage Discharge Granular Certificate (SD-GC) Issuance | The, accessed April 21, 2025, [https://docs.granular-foundation.org/storage-methodology/process/storage-discharge-granular-certificate-sd-gc-issuance](https://docs.granular-foundation.org/storage-methodology/process/storage-discharge-granular-certificate-sd-gc-issuance)

64\.  Energy Storage Systems: Duration and Limitations - Qmerit, accessed April 21, 2025, [https://qmerit.com/blog/energy-storage-systems-understanding-the-duration-and-limitations-of-energy-storage-capacity/](https://qmerit.com/blog/energy-storage-systems-understanding-the-duration-and-limitations-of-energy-storage-capacity/)

65\.  Round Trip Efficiency - energymag, accessed April 21, 2025, [https://energymag.net/round-trip-efficiency/](https://energymag.net/round-trip-efficiency/)

66\.  What are the pros/cons of using JWE or JWS \[closed] - Stack Overflow, accessed April 21, 2025, [https://stackoverflow.com/questions/33589353/what-are-the-pros-cons-of-using-jwe-or-jws](https://stackoverflow.com/questions/33589353/what-are-the-pros-cons-of-using-jwe-or-jws)

67\.  JWS + JWK in a Spring Security OAuth2 Application - Baeldung, accessed April 21, 2025, [https://www.baeldung.com/spring-security-oauth2-jws-jwk](https://www.baeldung.com/spring-security-oauth2-jws-jwk)

68\.  RFC 7515 - JSON Web Signature (JWS) - IETF Datatracker, accessed April 21, 2025, [https://datatracker.ietf.org/doc/html/rfc7515](https://datatracker.ietf.org/doc/html/rfc7515)

69\.  Verifiable Credentials (W3C) - walt.id Docs, accessed April 21, 2025, [https://docs.walt.id/community-stack/concepts/digital-credentials/verifiable-credentials-w3c](https://docs.walt.id/community-stack/concepts/digital-credentials/verifiable-credentials-w3c)

70\.  Decentralized Identifiers (DIDs) v1.1 - W3C, accessed April 21, 2025, [https://www.w3.org/TR/did-1.1/](https://www.w3.org/TR/did-1.1/)

71\.  What is a DID? Definition and uses - BCdiploma, accessed April 21, 2025, [https://www.bcdiploma.com/en/blog/what-is-a-did-definition-and-uses](https://www.bcdiploma.com/en/blog/what-is-a-did-definition-and-uses)

72\.  Decentralized Identifiers (DIDs): The Ultimate Beginner's Guide 2025 - Dock.io, accessed April 21, 2025, [https://www.dock.io/post/decentralized-identifiers](https://www.dock.io/post/decentralized-identifiers)

73\.  A new blockchain investment and energy certificate platform - Taylor & Francis Online, accessed April 21, 2025, [https://www.tandfonline.com/doi/full/10.1080/23311916.2023.2260226](https://www.tandfonline.com/doi/full/10.1080/23311916.2023.2260226)

74\.  Blockchain Integration and Its Impact on Renewable Energy - MDPI, accessed April 21, 2025, [https://www.mdpi.com/2073-431X/13/4/107](https://www.mdpi.com/2073-431X/13/4/107)

75\.  Assessing blockchain's future in transactive energy - Atlantic Council, accessed April 21, 2025, [https://www.atlanticcouncil.org/in-depth-research-reports/report/assessing-blockchains-future-in-transactive-energy/](https://www.atlanticcouncil.org/in-depth-research-reports/report/assessing-blockchains-future-in-transactive-energy/)

76\.  Storage power purchase agreements to enable the deployment of energy storage in Europe - PMC - PubMed Central, accessed April 21, 2025, [https://pmc.ncbi.nlm.nih.gov/articles/PMC9304613/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9304613/)

77\.  Key considerations in battery storage offtake agreements - Renewable Energy World, accessed April 21, 2025, [https://www.renewableenergyworld.com/energy-storage/battery/key-considerations-in-battery-storage-offtake-agreements/](https://www.renewableenergyworld.com/energy-storage/battery/key-considerations-in-battery-storage-offtake-agreements/)

78\.  For whom the BESS tolls | PFI - Project Finance International, accessed April 21, 2025, [https://www.pfie.com/story/4986317/for-whom-the-bess-tolls-jmxfpdm4xh](https://www.pfie.com/story/4986317/for-whom-the-bess-tolls-jmxfpdm4xh)

79\.  PPAs and EACs: An In-depth Comparison - Future Bridge NetZero Events, accessed April 21, 2025, [https://netzero-events.com/ppa-and-eac-an-in-depth-comparison/](https://netzero-events.com/ppa-and-eac-an-in-depth-comparison/)

80\.  Battery Storage Risks & Green Energy Trends - Travelers Insurance, accessed April 21, 2025, [https://www.travelers.com/resources/business-industries/energy/battery-storage-risks-and-green-energy-trends](https://www.travelers.com/resources/business-industries/energy/battery-storage-risks-and-green-energy-trends)

81\.  The Role of Large-Scale Energy Storage Systems: Benefits, Risks, and Comparisons - Santa Cruz Works, accessed April 21, 2025, [https://www.santacruzworks.org/news/the-role-of-large-scale-energy-storage-systems-benefits-risks-and-comparisons](https://www.santacruzworks.org/news/the-role-of-large-scale-energy-storage-systems-benefits-risks-and-comparisons)

82\.  EnergyTag Whitepaper:, accessed April 21, 2025, [https://energytag.org/wp-content/uploads/2023/09/EnergyTag-Whitepaper.pdf](https://energytag.org/wp-content/uploads/2023/09/EnergyTag-Whitepaper.pdf)

83\.  From Annual to Granular: Clean Energy Tracking for Next-Gen Climate Goals, accessed April 21, 2025, [https://www.leveltenenergy.com/post/granular-clean-energy-tracking](https://www.leveltenenergy.com/post/granular-clean-energy-tracking)

84\.  The Granular Certificate Trading Alliance, Led by LevelTen Energy and in Collaboration with AES, Constellation, Google, and Microsoft, Forms to Build a Critical Solution, with ICE, to Decarbonize the Grid, accessed April 21, 2025, [https://www.leveltenenergy.com/post/gctradingalliance-pressrelease](https://www.leveltenenergy.com/post/gctradingalliance-pressrelease)

85\.  About time: How incorporating timestamped energy certificates into electricity markets could accelerate the energy transition - Nord Pool, accessed April 21, 2025, [https://www.nordpoolgroup.com/49b69a/globalassets/download-center/whitepaper/whitepaper-may-2023.pdf](https://www.nordpoolgroup.com/49b69a/globalassets/download-center/whitepaper/whitepaper-may-2023.pdf)

86\.  Scope 2 Guidance | GHG Protocol, accessed April 21, 2025, [https://ghgprotocol.org/scope-2-guidance](https://ghgprotocol.org/scope-2-guidance)

87\.  GHG Protocol Scope 2 Guidance, accessed April 21, 2025, [https://ghgprotocol.org/sites/default/files/2023-03/Scope%202%20Guidance.pdf](https://ghgprotocol.org/sites/default/files/2023-03/Scope%202%20Guidance.pdf)

88\.  Getting to 24/7 carbon-free energy – practical steps for buyers and suppliers, accessed April 21, 2025, [https://247.eurelectric.org/wp-content/uploads/2024/11/EY-x-Eurelecric-247-CFE.pdf](https://247.eurelectric.org/wp-content/uploads/2024/11/EY-x-Eurelecric-247-CFE.pdf)

89\.  New Berkeley Lab Report Documents Trends in System Impacts, Reliability and Market Value of Solar in the United States, accessed April 21, 2025, [https://emp.lbl.gov/news/new-berkeley-lab-report-documents-trends](https://emp.lbl.gov/news/new-berkeley-lab-report-documents-trends)

90\.  Land-Based Wind Market Report: 2023 Edition - Department of Energy, accessed April 21, 2025, [https://www.energy.gov/sites/default/files/2023-08/land-based-wind-market-report-2023-edition.pdf](https://www.energy.gov/sites/default/files/2023-08/land-based-wind-market-report-2023-edition.pdf)

91\.  The Shift to Hourly Matched Green Energy - RE24, accessed April 21, 2025, [https://re24.energy/blog-the-shift-to-hourly-matched-green-energy/](https://re24.energy/blog-the-shift-to-hourly-matched-green-energy/)

92\.  Frequently Asked Questions (FAQ) - CRS - Center for Resource Solutions, accessed April 21, 2025, [https://resource-solutions.org/faq/](https://resource-solutions.org/faq/)

93\.  New Berkeley Lab Report Documents Trends in System Impacts, Reliability and Market Value of Solar in the United States, accessed April 21, 2025, [https://emp.lbl.gov/news/new-berkeley-lab-report-documents](https://emp.lbl.gov/news/new-berkeley-lab-report-documents)

94\.  Solar-to-Grid: Trends in System Impacts, Reliability, and Market Value in the United States with Data Through 2020, accessed April 21, 2025, [https://emp.lbl.gov/publications/solar-grid-trends-system-impacts-0](https://emp.lbl.gov/publications/solar-grid-trends-system-impacts-0)

95\.  Library | Historical EMS hourly load - California ISO, accessed April 21, 2025, [https://www.caiso.com/library/historical-ems-hourly-load](https://www.caiso.com/library/historical-ems-hourly-load)

96\.  Historical EMS Hourly Load Data Updated - California ISO, accessed April 21, 2025, [https://www.caiso.com/documents/historicalemshourlyloaddataupdated.html](https://www.caiso.com/documents/historicalemshourlyloaddataupdated.html)

97\.  Department of Market Monitoring Update - California ISO, accessed April 21, 2025, [https://www.caiso.com/documents/department-of-market-monitoring-update-feb-2025.pdf](https://www.caiso.com/documents/department-of-market-monitoring-update-feb-2025.pdf)

98\.  Weather Data - System Advisor Model - SAM - NREL, accessed April 21, 2025, [https://sam.nrel.gov/weather-data.html](https://sam.nrel.gov/weather-data.html)

99\.  Introduction, accessed April 21, 2025, [https://samrepo.nrelcloud.org/help/index.html](https://samrepo.nrelcloud.org/help/index.html)

100\.  Lifetime hourly and hourly results - SAM Forum - System Advisor Model - NREL, accessed April 21, 2025, [https://sam.nrel.gov/forum/forum-general/3084-lifetime-hourly-and-hourly-results.html](https://sam.nrel.gov/forum/forum-general/3084-lifetime-hourly-and-hourly-results.html)

101\.  Generation - ERCOT.com, accessed April 21, 2025, [https://www.ercot.com/gridinfo/generation](https://www.ercot.com/gridinfo/generation)

102\.  Wind Power Production - Hourly Averaged Actual and Forecasted Values - ERCOT.com, accessed April 21, 2025, [https://www.ercot.com/mp/data-products/data-product-details?id=NP4-732-CD](https://www.ercot.com/mp/data-products/data-product-details?id=NP4-732-CD)

103\.  Hourly System-wide and Regional Wind Forecasts by Model - ERCOT.com, accessed April 21, 2025, [https://www.ercot.com/mp/data-products/data-product-details?id=NP4-442-CD](https://www.ercot.com/mp/data-products/data-product-details?id=NP4-442-CD)

104\.  Combined Wind and Solar - ERCOT.com, accessed April 21, 2025, [https://www.ercot.com/gridmktinfo/dashboards/combinedwindandsolar](https://www.ercot.com/gridmktinfo/dashboards/combinedwindandsolar)

105\.  Report on the Capacity, Demand and Reserves (CDR) in the ERCOT Region, 2025-2029 Revised February 13, 2025, accessed April 21, 2025, [https://www.ercot.com/files/docs/2025/02/12/CapacityDemandandReservesReport\_December2024.pdf](https://www.ercot.com/files/docs/2025/02/12/CapacityDemandandReservesReport_December2024.pdf)

106\.  Load Profiling - ERCOT.com, accessed April 21, 2025, [https://www.ercot.com/mktinfo/loadprofile](https://www.ercot.com/mktinfo/loadprofile)

107\.  Hourly Load Data Archives - ERCOT.com, accessed April 21, 2025, [https://www.ercot.com/gridinfo/load/load\_hist](https://www.ercot.com/gridinfo/load/load_hist)

108\.  Opportunities and Challenges for Data Center Demand Response, accessed April 21, 2025, [https://www.ams.stonybrook.edu/\~zhliu/DCDRsurvey.pdf](https://www.ams.stonybrook.edu/~zhliu/DCDRsurvey.pdf)

109\.  The Era of Flat Power Demand is Over - Grid Strategies, accessed April 21, 2025, [https://gridstrategiesllc.com/wp-content/uploads/2023/12/National-Load-Growth-Report-2023.pdf](https://gridstrategiesllc.com/wp-content/uploads/2023/12/National-Load-Growth-Report-2023.pdf)

110\.  Marginal Emissions Factors for the US Electricity System | WattTime, accessed April 21, 2025, [https://watttime.org/wp-content/uploads/2023/11/Marginal-Emissions-Factors-for-the-US-Electricity-System\_April-2012.pdf](https://watttime.org/wp-content/uploads/2023/11/Marginal-Emissions-Factors-for-the-US-Electricity-System_April-2012.pdf)

111\.  Methodology for Calculation of the Marginal Emission Rates from a Complex Cogeneration Facility compared with that of the co-loc - ScholarSpace, accessed April 21, 2025, [https://scholarspace.manoa.hawaii.edu/bitstreams/b9792797-2335-44fc-a964-e455ddcfc501/download](https://scholarspace.manoa.hawaii.edu/bitstreams/b9792797-2335-44fc-a964-e455ddcfc501/download)

112\.  Scope 2 - Standard Development Plan - 2024.12.20 - GHG Protocol, accessed April 21, 2025, [https://ghgprotocol.org/sites/default/files/2025-01/S2-SDP-20241220.pdf](https://ghgprotocol.org/sites/default/files/2025-01/S2-SDP-20241220.pdf)

113\.  GHG Protocol Scope 2 Guidance, accessed April 21, 2025, [https://ghgprotocol.org/sites/default/files/2022-12/Scope2\_ExecSum\_Final.pdf](https://ghgprotocol.org/sites/default/files/2022-12/Scope2_ExecSum_Final.pdf)

114\.  Choosing the Best Carbon Factor for the Job: Exploring Available Carbon Emissions Factors and the Impact of Factor Selection - NREL, accessed April 21, 2025, [https://www.nrel.gov/docs/fy24osti/86682.pdf](https://www.nrel.gov/docs/fy24osti/86682.pdf)

115\.  Average vs. Marginal Emissions - WattTime, accessed April 21, 2025, [https://watttime.org/data-science/data-signals/average-vs-marginal/](https://watttime.org/data-science/data-signals/average-vs-marginal/)

116\.  Protocols, rates, factors, attribution, accounting, oh my! A survey of U.S. emission accounting resources and what stakeholders should know Phillips - American Council for an Energy-Efficient Economy, accessed April 21, 2025, [https://www.aceee.org/sites/default/files/pdfs/ssi23/3-127-PHILLIPS.pdf](https://www.aceee.org/sites/default/files/pdfs/ssi23/3-127-PHILLIPS.pdf)

117\.  Using Attributional Life Cycle Assessment to Estimate Climate-Change Mitigation Benefits Misleads Policy Makers | Request PDF - ResearchGate, accessed April 21, 2025, [https://www.researchgate.net/publication/258373482\_Using\_Attributional\_Life\_Cycle\_Assessment\_to\_Estimate\_Climate-Change\_Mitigation\_Benefits\_Misleads\_Policy\_Makers](https://www.researchgate.net/publication/258373482_Using_Attributional_Life_Cycle_Assessment_to_Estimate_Climate-Change_Mitigation_Benefits_Misleads_Policy_Makers)

118\.  Relevance of attributional and consequential life cycle assessment for society and decision support - Frontiers, accessed April 21, 2025, [https://www.frontiersin.org/journals/sustainability/articles/10.3389/frsus.2023.1063583/full](https://www.frontiersin.org/journals/sustainability/articles/10.3389/frsus.2023.1063583/full)

119\.  A Conceptual Review on Using Consequential Life Cycle Assessment Methodology for the Energy Sector - MDPI, accessed April 21, 2025, [https://www.mdpi.com/1996-1073/13/12/3076](https://www.mdpi.com/1996-1073/13/12/3076)

120\.  A Review on Consequential Life Cycle Assessment in the Power Sector - IRIS UniPA, accessed April 21, 2025, [https://iris.unipa.it/retrieve/e3ad8924-1719-da0e-e053-3705fe0a2b96/15.08\_02.pdf](https://iris.unipa.it/retrieve/e3ad8924-1719-da0e-e053-3705fe0a2b96/15.08_02.pdf)

121\.  What's Scope 2 good for? | Oxford Open Climate Change, accessed April 21, 2025, [https://academic.oup.com/oocc/article/4/1/kgae011/7715934](https://academic.oup.com/oocc/article/4/1/kgae011/7715934)

122\.  GHG Protocol Scope 2 Update Technical Working Group Discussion Topic Overview, accessed April 21, 2025, [https://ghgprotocol.org/sites/default/files/2024-11/S2-Meeting3-Discussion%20Paper-20241107.pdf](https://ghgprotocol.org/sites/default/files/2024-11/S2-Meeting3-Discussion%20Paper-20241107.pdf)

123\.  Scope 4 Emissions: Everything You Need to Know - Net0, accessed April 21, 2025, [https://net0.com/blog/scope-4](https://net0.com/blog/scope-4)

124\.  Estimating and Reporting Avoided Emissions - GHG Protocol, accessed April 21, 2025, [https://ghgprotocol.org/estimating-and-reporting-avoided-emissions](https://ghgprotocol.org/estimating-and-reporting-avoided-emissions)

125\.  Evaluating GHG Emissions and Renewable Energy Use in the Italian Energy Sector: Monitoring, Reporting, and Objectives - MDPI, accessed April 21, 2025, [https://www.mdpi.com/2076-3298/12/2/55](https://www.mdpi.com/2076-3298/12/2/55)

126\.  Accounting for the climate benefit of temporary carbon storage in nature - PMC, accessed April 21, 2025, [https://pmc.ncbi.nlm.nih.gov/articles/PMC10485027/](https://pmc.ncbi.nlm.nih.gov/articles/PMC10485027/)

127\.  Full article: Methods that equate temporary carbon storage with permanent CO2 emission reductions lead to false claims on temperature alignment, accessed April 21, 2025, [https://www.tandfonline.com/doi/full/10.1080/17583004.2023.2284714](https://www.tandfonline.com/doi/full/10.1080/17583004.2023.2284714)

128\.  Undoing Equivalence: Rethinking Carbon Accounting for Just Carbon Removal - Frontiers, accessed April 21, 2025, [https://www.frontiersin.org/journals/climate/articles/10.3389/fclim.2021.664130/full](https://www.frontiersin.org/journals/climate/articles/10.3389/fclim.2021.664130/full)

129\.  Energy Tracking from Source to Switch with Granular Certificates, accessed April 21, 2025, [https://energytrackandtrace.com/energy-tracking-from-source-to-switch-with-granular-certificates/](https://energytrackandtrace.com/energy-tracking-from-source-to-switch-with-granular-certificates/)

130\.  Readiness for Hourly: U.S. Renewable Energy Tracking Systems - Center for Resource Solutions, accessed April 21, 2025, [https://resource-solutions.org/wp-content/uploads/2023/06/Readiness-for-Hourly-U.S.-Renewable-Energy-Tracking-Systems.pdf](https://resource-solutions.org/wp-content/uploads/2023/06/Readiness-for-Hourly-U.S.-Renewable-Energy-Tracking-Systems.pdf)

131\.  EECS - AIB, accessed April 21, 2025, [https://www.aib-net.org/eecs](https://www.aib-net.org/eecs)

132\.  Decentralized Identifiers (DIDs) v1.0 - W3C, accessed April 21, 2025, [https://www.w3.org/TR/did-1.0/](https://www.w3.org/TR/did-1.0/)

133\.  Verifiable Credentials Data Model v2.0 - W3C, accessed April 21, 2025, [https://www.w3.org/TR/vc-data-model-2.0/](https://www.w3.org/TR/vc-data-model-2.0/)

134\.  Identity and Attestation Management - Blueprint v1.0 - Data Spaces Support Centre, accessed April 21, 2025, [https://dssc.eu/space/BVE/357075352](https://dssc.eu/space/BVE/357075352)

135\.  THIS USER AGREEMENT (this “Agreement”) is entered into and effective as of (insert date) between (insert PJM/PJM Tech name) - PJM-EIS, accessed April 21, 2025, [https://www.pjm-eis.com/-/media/DotCom/pjm-eis/documents/terms-of-use.pdf](https://www.pjm-eis.com/-/media/DotCom/pjm-eis/documents/terms-of-use.pdf)

136\.  As of December 10, 2024, accessed April 21, 2025, [https://www.pjm.com/-/media/DotCom/committees-groups/forums/tech-change/2024/20241210/20241210-item-04---6---product-roadmap---data-miner.pdf](https://www.pjm.com/-/media/DotCom/committees-groups/forums/tech-change/2024/20241210/20241210-item-04---6---product-roadmap---data-miner.pdf)

137\.  Major US energy buyers projected to acquire 17 TWh of hourly renewable energy certificates by 2026: survey | Utility Dive, accessed April 21, 2025, [https://www.utilitydive.com/news/granular-certificate-trading-alliance-survey-levelten/735342/](https://www.utilitydive.com/news/granular-certificate-trading-alliance-survey-levelten/735342/)

138\.  U.S. Department of the Treasury Releases Final Rules for Clean Hydrogen Production Tax Credit, accessed April 21, 2025, [https://home.treasury.gov/news/press-releases/jy2768](https://home.treasury.gov/news/press-releases/jy2768)

139\.  Treasury Department, IRS Release Section 45V Clean Hydrogen PTC Final Regulations | Insights | Holland & Knight, accessed April 21, 2025, [https://www.hklaw.com/en/insights/publications/2025/01/treasury-department-irs-release-section-45v-clean-hydrogen-ptc](https://www.hklaw.com/en/insights/publications/2025/01/treasury-department-irs-release-section-45v-clean-hydrogen-ptc)

140\.  IRS Finalizes Hydrogen Tax Credit Regulations - Latham & Watkins LLP, accessed April 21, 2025, [https://www.lw.com/admin/upload/SiteAttachments/IRS-Finalizes-Hydrogen-Tax-Credit-Regulations.pdf](https://www.lw.com/admin/upload/SiteAttachments/IRS-Finalizes-Hydrogen-Tax-Credit-Regulations.pdf)

141\.  Final Regulations for Clean Hydrogen: Making Tax Credits More Accessible, accessed April 21, 2025, [https://www.whitecase.com/insight-alert/final-regulations-clean-hydrogen-making-tax-credits-more-accessible](https://www.whitecase.com/insight-alert/final-regulations-clean-hydrogen-making-tax-credits-more-accessible)

142\.  Final Regulations for the Hydrogen Production Tax Credit (Section 45V) - Cherry Bekaert, accessed April 21, 2025, [https://www.cbh.com/insights/articles/section-45v-hydrogen-tax-credit-final-rules-released/](https://www.cbh.com/insights/articles/section-45v-hydrogen-tax-credit-final-rules-released/)

143\.  IRS Issues Final Regulations on Clean Hydrogen Tax Credits | Troutman Pepper Locke, accessed April 21, 2025, [https://www.troutman.com/insights/irs-issues-final-regulations-on-clean-hydrogen-tax-credits.html](https://www.troutman.com/insights/irs-issues-final-regulations-on-clean-hydrogen-tax-credits.html)

144\.  A Closer Look at the 45V Final Rule - EnergyTag, accessed April 21, 2025, [https://energytag.org/a-closer-look-at-the-45v-final-rule/](https://energytag.org/a-closer-look-at-the-45v-final-rule/)

145\.  FPOG Stakeholder Engagement Meeting – 45V and 48E Hydrogen Tax Credit Rules, accessed April 21, 2025, [https://lwrs.inl.gov/content/uploads/11/2025/03/09.-Tax-Credit-Sect-45V-Cadogan-FINAL-2.pdf](https://lwrs.inl.gov/content/uploads/11/2025/03/09.-Tax-Credit-Sect-45V-Cadogan-FINAL-2.pdf)

146\.  www.whitecase.com, accessed April 21, 2025, [https://www.whitecase.com/insight-alert/final-regulations-clean-hydrogen-making-tax-credits-more-accessible#:\~:text=Clean%20Hydrogen%20PTC%20and%20ITC\&text=The%20facility%20must%20generally%20be,CO2e%20per%20kilogram%20of%20hydrogen.](https://www.whitecase.com/insight-alert/final-regulations-clean-hydrogen-making-tax-credits-more-accessible)

147\.  Final Rules for the Clean Hydrogen Production Tax Credit | Willkie Farr & Gallagher LLP, accessed April 21, 2025, [https://www.willkie.com/publications/2025/01/final-rules-for-the-clean-hydrogen-production-tax-credit](https://www.willkie.com/publications/2025/01/final-rules-for-the-clean-hydrogen-production-tax-credit)

148\.  Clean Hydrogen Production Tax Credit - Alternative Fuels Data Center, accessed April 21, 2025, [https://afdc.energy.gov/laws/13399](https://afdc.energy.gov/laws/13399)

149\.  How changing EU regulatory frameworks will impact the market for GOs - Renewabl, accessed April 21, 2025, [https://www.renewabl.com/post/how-changing-eu-regulatory-frameworks-will-impact-the-market-for-gos](https://www.renewabl.com/post/how-changing-eu-regulatory-frameworks-will-impact-the-market-for-gos)

150\.  RED III and its impact on PPAs and GOs - Magnus Commodities, accessed April 21, 2025, [https://magnuscmd.com/red-iii-and-its-impact-on-ppas-and-gos/](https://magnuscmd.com/red-iii-and-its-impact-on-ppas-and-gos/)

151\.  Call for Rapid Implementation of Granular Guarantees of Origin in Europe - The European Association for Storage of Energy, accessed April 21, 2025, [https://ease-storage.eu/wp-content/uploads/2024/07/A-Call-for-Granular-Guarantees-of-Origin-FINAL.pdf](https://ease-storage.eu/wp-content/uploads/2024/07/A-Call-for-Granular-Guarantees-of-Origin-FINAL.pdf)

152\.  Understanding Hourly Matching When You're New to the Industry - Granular Energy, accessed April 21, 2025, [https://www.granular-energy.com/insights/hourly-matching-for-industry-newbies](https://www.granular-energy.com/insights/hourly-matching-for-industry-newbies)

153\.  Frequently Asked Questions on EU Requirements for Renewable Hydrogen and its Derivatives. FAQs on the delegated acts 2023/1184 &, accessed April 21, 2025, [https://www.ecologic.eu/sites/default/files/publication/2024/60022-FAQ-EU-requirements-green-hydrogen-and-PtX.pdf](https://www.ecologic.eu/sites/default/files/publication/2024/60022-FAQ-EU-requirements-green-hydrogen-and-PtX.pdf)

154\.  The European Green Deal & Fit for 55 - KPMG International, accessed April 21, 2025, [https://assets.kpmg.com/content/dam/kpmg/xx/pdf/2021/11/green-deal-and-fit-for-55-slip-sheet\_v5\_web.pdf](https://assets.kpmg.com/content/dam/kpmg/xx/pdf/2021/11/green-deal-and-fit-for-55-slip-sheet_v5_web.pdf)

155\.  Revision of the Renewable Energy Directive: Fit for 55 package - European Parliament, accessed April 21, 2025, [https://www.europarl.europa.eu/RegData/etudes/BRIE/2021/698781/EPRS\_BRI(2021)698781\_EN.pdf](https://www.europarl.europa.eu/RegData/etudes/BRIE/2021/698781/EPRS_BRI\(2021\)698781_EN.pdf)

156\.  Renewable Energy Directive, accessed April 21, 2025, [https://energy.ec.europa.eu/topics/renewable-energy/renewable-energy-directive-targets-and-rules/renewable-energy-directive\_en](https://energy.ec.europa.eu/topics/renewable-energy/renewable-energy-directive-targets-and-rules/renewable-energy-directive_en)

157\.  FIT FOR 55% PACKAGE - E3G, accessed April 21, 2025, [https://www.e3g.org/wp-content/uploads/E3G\_Press-Briefing\_Fit\_for\_55-July-2021.pdf](https://www.e3g.org/wp-content/uploads/E3G_Press-Briefing_Fit_for_55-July-2021.pdf)

158\.  'Fit for 55': EU on track for climate goals and sustainable growth - Enel Group, accessed April 21, 2025, [https://www.enel.com/company/stories/articles/2021/08/fit-for-55-europe-energy-transition-goals](https://www.enel.com/company/stories/articles/2021/08/fit-for-55-europe-energy-transition-goals)

159\.  Revision of the Renewable Energy Directive: Fit for 55 package \[EU Legislation in Progress], accessed April 21, 2025, [https://epthinktank.eu/2021/11/15/revision-of-the-renewable-energy-directive-fit-for-55-package-eu-legislation-in-progress/](https://epthinktank.eu/2021/11/15/revision-of-the-renewable-energy-directive-fit-for-55-package-eu-legislation-in-progress/)

160\.  Electron Bank: Powering Europe's Clean Industrial Future - EnergyTag, accessed April 21, 2025, [https://energytag.org/electron-bank/](https://energytag.org/electron-bank/)

161\.  Energy-Storage-Roadmap.pdf - nyserda - NY.gov, accessed April 21, 2025, [https://www.nyserda.ny.gov/-/media/Project/Nyserda/Files/Programs/Energy-Storage/Energy-Storage-Roadmap.pdf](https://www.nyserda.ny.gov/-/media/Project/Nyserda/Files/Programs/Energy-Storage/Energy-Storage-Roadmap.pdf)

162\.  STATE OF NEW YORK PUBLIC SERVICE COMMISSION CASE 18-E-0130 - In the Matter of Energy Storage Deployment Program. ORDER ESTABLISH - nyserda - NY.gov, accessed April 21, 2025, [https://www.nyserda.ny.gov/-/media/Project/Nyserda/Files/Programs/Energy-Storage/2024-06-6GW-Energy-Storage-Order.pdf](https://www.nyserda.ny.gov/-/media/Project/Nyserda/Files/Programs/Energy-Storage/2024-06-6GW-Energy-Storage-Order.pdf)

163\.  Recommendations Regarding the Energy Storage Grand Challenge, accessed April 21, 2025, [https://www.energy.gov/oe/articles/final-eac-recommendations-esgcaug-26](https://www.energy.gov/oe/articles/final-eac-recommendations-esgcaug-26)

164\.  Energy Tag API Specification (2.0), accessed April 21, 2025, [https://energytag.org/api/](https://energytag.org/api/)

165\.  EnergyTag Supplemental Comments on PSD Updated Language - California Energy Commission : e-filing, accessed April 21, 2025, [https://efiling.energy.ca.gov/GetDocument.aspx?tn=260127\&DocumentContentId=96362](https://efiling.energy.ca.gov/GetDocument.aspx?tn=260127\&DocumentContentId=96362)

166\.  LevelTen PPA Price Index, accessed April 21, 2025, [https://www.leveltenenergy.com/ppa?trk=public\_post\_main-feed-card\_reshare-text](https://www.leveltenenergy.com/ppa?trk=public_post_main-feed-card_reshare-text)

167\.  LevelTen Energy Had a Record-Breaking 2024 Powering the Clean Energy Transition, accessed April 21, 2025, [https://www.leveltenenergy.com/post/2024-a-record-breaking-year](https://www.leveltenenergy.com/post/2024-a-record-breaking-year)

168\.  Suggest a better/worse name for M-RETS, accessed April 21, 2025, [https://www.mrets.org/blog/better-worse-rename-mrets/](https://www.mrets.org/blog/better-worse-rename-mrets/)

169\.  What Effect Will 24/7 CFE Have on Renewable Energy Markets? - OPIS, accessed April 21, 2025, [https://www.opisnet.com/blog/247-cfe-effect-on-markets/](https://www.opisnet.com/blog/247-cfe-effect-on-markets/)
