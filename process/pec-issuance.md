---
hidden: true
---

# PEC Issuance

## Process Overview

After the successful verification of the Project Impact Report and the issuance of the Power Emissions Proof (PEP), the PEC Registry proceeds to generate Power Emissions Certificates (PECs) for the energy discharged from the storage system. This section details how PECs are issued post-verification, focusing on the calculation of discharge avoided emissions and the assignment of net emissions to the issued PECs.

## How PECs are Generated Post-Verification for Storage Discharge Energy

The issuance process involves the following steps:

1. **Assess the Gross Discharge Avoided Emissions for Each Hour**
2. **Subtract the Remaining Induced Emissions from the PEP Report Across All Hours**
3. **Issue PECs for All Discharged Energy Using the Hourly Net Emissions Calculated**

This methodology ensures accurate carbon accounting and fair distribution of remaining induced emissions, preventing bias in PEC issuance.

### **Step 1: Assess the Gross Discharge Avoided Emissions for Each Hour**

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

### **Step 2: Subtract the Remaining Induced Emissions from the PEP Report Across All Hours**

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

### **Step 3: Issue PECs for All Discharged Energy Using the Hourly Net Emissions Calculated**

Issue PECs for each hour of discharged energy where the net avoided emissions are positive, assigning the calculated net emissions to the PECs.

* **Eligibility for PEC Issuance**:
  * **Positive Net Avoided Emissions**: PECs are issued only for discharge hours where the net avoided emissions are greater than zero.
* **Assign Net Avoided Emissions per PEC**:
  *   $$\text{Net Avoided Emissions per PEC}_{\text{hour}} = \frac{\text{Net Avoided Emissions}_{\text{hour}}}{\text{Discharged Energy}_{\text{hour}}}$$


  * **Example Calculation**:
    * Net Avoided Emissions at Hour h: $$21.5 tCO₂$$
    * Discharged Energy at Hour h: $$50 MWh$$
    * Net Avoided Emissions per PEC:
      * $$\frac{21.5 \text{ tCO₂}}{50 \text{ MWh}} = 0.43 \text{ tCO₂/MWh}$$
* **Issue PECs with Assigned Net Emissions**:
  * Each PEC represents a volume of discharged energy with an associated net avoided emissions of 0.43 tCO₂.

## Benefits of Assigning Net Emissions to Issued PECs

* **Accurate Carbon Accounting**: Assigning net emissions to PECs allows for precise tracking of the environmental benefits associated with each unit of discharged energy.
* **Enhanced Market Value**: PECs with higher net emissions reductions may have greater value in the marketplace, incentivizing optimal storage operations.
* **Facilitates Corporate Reporting**: Corporations purchasing PECs can accurately report Scope 2 emissions reductions in line with the GHGP, enhancing sustainability reporting.
* **Documentation**:
  * **Record Details for Each PEC**:
    * Serial Number
    * Hourly Timestamp
    * Net Avoided Emissions per PEC
    * Reference to the PEP and underlying retired PECs

### Benefits of This Approach

* **Accurate Carbon Accounting**:
  * By calculating net avoided emissions for each hour, the methodology ensures that PECs accurately reflect the true environmental impact of the energy storage operation.
* **Avoids Bias**:
  * Uniformly allocating the remaining induced emissions across all discharge hours prevents bias that could occur if emissions were unevenly distributed.
* **Incentivizes Optimal Operation**:
  * Encourages energy storage operators to maximize discharging during periods of higher grid emissions intensity, enhancing overall emissions reductions.
* **Transparency and Traceability**:
  * Detailed records and clear calculations provide transparency, building trust among stakeholders and facilitating auditing and verification.

### Handling Situations with Insufficient Net Avoided Emissions

* **Zero or Negative Net Avoided Emissions**:
  * If the net avoided emissions for a particular hour are zero or negative, no PECs are issued for that hour.
  * **Reasoning**:
    * Issuing PECs in such cases would not represent a genuine reduction in emissions, thereby compromising the integrity of the carbon accounting system.
* **Example**:
  * Gross Avoided Emissions at Hour h: 0.8 tCO₂
  * Remaining Induced Emissions per Hour: 1 tCO₂/hour
  * Net Avoided Emissions at Hour h:
    * $$0.8 \text{ tCO₂} - 1 \text{ tCO₂} = -0.2 \text{ tCO₂}$$
  * **Action**:
    * No PECs are issued for this hour.

### Documentation and Records

Maintaining thorough documentation is essential for transparency, traceability, and compliance. The PEC Registry ensures that all records are accurate and accessible for verification.

* **PEC Registry Entry**:
  * **Information Recorded for Each PEC**:
    * Serial Number
    * Hourly Timestamp
    * Discharged Energy (MWh)
    * Net Avoided Emissions per PEC (tCO₂/MWh)
    * Reference to the PEP and Retired PECs
* **Traceability to PEP and Retired PECs**:
  * Each issued PEC is linked to the corresponding PEP, which includes details of the underlying retired PECs used to neutralize charging activity.
* **Data Accessibility**:
  * Records are securely stored and can be accessed by authorized stakeholders for auditing and compliance purposes.
* **Transparency Measures**:
  * Summary reports and aggregated data may be made available to stakeholders, supporting corporate reporting and market transparency.

## Compliance and Integrity

* **Alignment with Standards**:
  * The issuance process aligns with the methodology's principles, the Greenhouse Gas Protocol (GHGP) Scope 2 Guidance, and the EnergyTag Standard.
* **Verification and Auditing**:
  * The PEC Registry conducts periodic reviews to ensure ongoing compliance and integrity of the PEC issuance process.
* **Stakeholder Confidence**:
  * Accurate and transparent PEC issuance fosters trust among corporate buyers, regulators, and other market participants.
