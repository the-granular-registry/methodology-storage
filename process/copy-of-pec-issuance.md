---
hidden: true
---

# Copy of PEC Issuance

## Process Overview

After the successful verification of the Project Impact Report and the issuance of the Power Emissions Proof (PEP), the PEC Registry proceeds to generate Power Emissions Certificates (PECs) for the energy discharged from the storage system. This section details how PECs are issued post-verification, focusing on the calculation of discharge avoided emissions and the assignment of net emissions to the issued PECs.

### How PECs are Generated Post-Verification for Storage Discharge Energy

The issuance process involves the following steps:

1. **Assess the Gross Discharge Avoided Emissions for Each Hour**
2. **Subtract the Remaining Induced Emissions from the PEP Report Across All Hours**
3. **Issue PECs for All Discharged Energy Using the Hourly Net Emissions Calculated**

This methodology ensures accurate carbon accounting and fair distribution of remaining induced emissions, preventing bias in PEC issuance.

#### **Step 1: Assess the Gross Discharge Avoided Emissions for Each Hour**

Calculate the gross avoided emissions for each hour of discharge by applying the Marginal Emissions Rates (MER) to the amount of energy discharged during that hour.

* **Hourly Discharge Data**:
  * Use the hourly meter readings of energy discharged (in MWh) from the storage system.
* **Corresponding MER**:
  * Retrieve the MER (in tCO₂/MWh) for each hour of discharge from the selected emissions data provider.
* **Calculate Hourly Gross Avoided Emissions**:

$$
GrossAvoided Emissions_{hour}=Discharging Energy_{hour}×MER_{hour}
$$

* **Example Calculation**:
  * Discharging Energy at Hour 1: $$50 MWh$$
  * MER at Hour 1: $$0.45 tCO₂/MWh$$
  * Avoided Emissions at Hour $$h$$:

$$
50 MWh×0.45 tCO₂/MWh=22.5 tCO₂
$$

#### **Step 2: Subtract the Remaining Induced Emissions from the PEP Report Across All Hours**

Allocate the total remaining induced emissions uniformly across all discharge hours to calculate the net avoided emissions for each hour.

* **Total Remaining Induced Emissions**:
  * Obtain the total remaining induced emissions from the PEP report. This represents the portion of induced emissions from charging that were not neutralized by retired PECs.
  * **Example**:
    * Total Remaining Induced Emissions: $$100 tCO₂$$
* **Total Number of Discharge Hours**:
  * Count the total number of hours during which the storage system discharged energy.
  * **Example**:
    * Total Discharge Hours: $$100 hours$$
* **Allocate Remaining Induced Emissions Uniformly**:

$$
Remaining Induced Emissions (per Hour)=\frac{Total Remaining Induced Emissions}{Total Discharge Hours}
$$

* **Example Calculation**:
* **Calculate Hourly Net Avoided Emissions**:

$$
Net Avoided Emissions_{hour}=Gross Avoided Emissions_{hour}−Remaining Induced Emissions per Hour
$$

* **Example Calculation**:
  * Gross Avoided Emissions at Hour $$h$$: $$22.5 tCO₂$$
  * Remaining Induced Emissions per Hour: $$1 tCO₂/hour$$
  *   Net Avoided Emissions at Hour $$h$$: $$22.5 tCO₂−1 tCO₂=21.5 tCO₂$$


* **Handling Negative Net Avoided Emissions**:
  * If the net avoided emissions for any hour are zero or negative, no PECs will be issued for that hour.

#### **Step 3: Issue PECs for All Discharged Energy Using the Hourly Net Emissions Calculated**

Issue PECs for each hour of discharged energy where the net avoided emissions are positive, assigning the calculated net emissions to the PECs.

* **Eligibility for PEC Issuance**:
  * **Positive Net Avoided Emissions**: PECs are issued only for discharge hours where the net avoided emissions are greater than zero.
*   **Assign Net Avoided Emissions per PEC**:

    Net Avoided Emissions per PEChour=Net Avoided EmissionshourDischarged Energyhour\text{Net Avoided Emissions per PEC}\_{\text{hour\}} = \frac{\text{Net Avoided Emissions}\_{\text{hour\}}}{\text{Discharged Energy}\_{\text{hour\}}}Net Avoided Emissions per PEChour​=Discharged Energyhour​Net Avoided Emissionshour​​

    * **Example Calculation**:
      * Net Avoided Emissions at Hour hhh: 21.5 tCO₂
      * Discharged Energy at Hour hhh: 50 MWh
      *   Net Avoided Emissions per PEC:

          21.5 tCO₂50 MWh=0.43 tCO₂/MWh\frac{21.5 \text{ tCO₂\}}{50 \text{ MWh\}} = 0.43 \text{ tCO₂/MWh}50 MWh21.5 tCO₂​=0.43 tCO₂/MWh
* **Issue PECs with Assigned Net Emissions**:
  * Each PEC represents 1 MWh of discharged energy with an associated net avoided emissions of 0.43 tCO₂.
*

**SSSSStep 3: Sum Total Avoided Emissions**

* **Formula**:

$$
Total Avoided Emissions=∑_{hour=1}^nAvoided Emissions_{hour}
$$

* **Example**:
  * If the storage system discharged over 100 hours, sum the avoided emissions for each hour:

$$
Total Avoided Emissions=Emissions_1+Emissions_2+⋯+Emissions_{100}
$$

#### **Documentation**

* Record all calculations, including hourly discharging energies, MER values, and resulting avoided emissions.
* Maintain transparency by providing detailed logs for verification.

## **Assigning Net Emissions to Issued PECs**

After calculating the total avoided emissions during discharge, the net emissions reduction is determined by accounting for any remaining induced emissions from the charging phase that were not neutralized by retired PECs. This net emissions reduction is then assigned to the PECs issued for the discharged energy.

### **Steps for Assigning Net Emissions:**

**Step 1: Calculate Net Emissions Reduction**

* **Formula**:

$$
Net Emissions Reduction=Total Avoided Emissions−Remaining Induced Emissions
$$

* **Example**:
  * Total Avoided Emissions: $$1,912.5 tCO₂$$
  * Remaining Induced Emissions: $$100 tCO₂$$
  * Net Emissions Reduction: $$1,912.5 tCO₂−100 tCO₂=1,812.5 tCO₂$$

**Step 2: Assign Net Emissions to PECs**

* **Total PECs to be Issued**: Equal to the total energy discharged (in MWh).
  * Example:
    * Total Discharged Energy: $$4,250 MWh$$
    * PECs Issued: $$4,250$$
* **Net Emissions per PEC**:
  * **Formula**:

$$
PEC AvoidedEmissions (tCO₂)=\frac{Net Emissions Reduction}{Total Discharged Energy (MWh)}
$$

\text{Net Emissions per PEC (tCO₂/MWh)} = \frac{\text{Net Emissions Reduction\}}{\text{Total Discharged Energy (MWh)\}}Net Emissions per PEC (tCO₂/MWh)=Total Discharged Energy (MWh)Net Emissions Reduction​

*   **Example**:

    1,812.5 tCO₂4,250 MWh=0.426 tCO₂/MWh\frac{1,812.5 \text{ tCO₂\}}{4,250 \text{ MWh\}} = 0.426 \text{ tCO₂/MWh}4,250 MWh1,812.5 tCO₂​=0.426 tCO₂/MWh
* **Issuance of PECs**:
  * Each PEC represents 1 MWh of discharged energy with an associated net emissions reduction of 0.426 tCO₂.

1. **Incorporate Traceability**
   * **Link to Power Emissions Proof (PEP)**: Each issued PEC references the PEP, ensuring traceability back to the verification of neutralized charging impact.
   * **Underlying Retired PECs**: Documentation of the retired PECs used for neutralizing charging emissions is associated with the issued PECs.
2. **Documentation and Records**
   * **PEC Registry Entry**: Record all issued PECs in the registry, including serial numbers, timestamps, net emissions reductions, and traceability links.
   * **Transparency**: Provide access to relevant stakeholders for auditing and verification purposes.

#### Benefits of Assigning Net Emissions to Issued PECs

* **Accurate Carbon Accounting**: Assigning net emissions to PECs allows for precise tracking of the environmental benefits associated with each unit of discharged energy.
* **Enhanced Market Value**: PECs with higher net emissions reductions may have greater value in the marketplace, incentivizing optimal storage operations.
* **Facilitates Corporate Reporting**: Corporations purchasing PECs can accurately report Scope 2 emissions reductions in line with the GHGP, enhancing sustainability reporting.
