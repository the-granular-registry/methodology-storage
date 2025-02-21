---
hidden: true
---

# Granular Registry Methodology for Time-Shifting Granular Certificates Using Storage Transfer Records

**1. Introduction**

This document outlines the methodology for time-shifting **Granular Certificates (GCs)** using **Storage Transfer Records (STRs)** within the **Granular Registry**. This approach enables clean energy buyers to **align energy storage discharge with specific GCs**, ensuring transparent and auditable claims of **24/7 Carbon-Free Energy (CFE)**.

This methodology applies to all **market participants**, including:

* **Renewable energy generators** being issued GCs
* **Battery storage operators** sharing data with the Granular Registry
* **CFE offtakers** seeking to procure and time-shift GCs
* **REC Registry administrators** ensuring no double-counting

***

#### **2. Key Concepts and Definitions**

**2.1. Granular Certificate (GC)**

A certificate representing **Carbon-Free Energy (CFE)** is generated hourly. Issued in compliance with the **EnergyTag Standard**.

**2.2. Storage Transfer Record (STR)**

A record representing a **battery storage event** that can be matched with a GC to enable time-shifting. Each STR consists of:

* **Storage Charge Record (SCR)** – Logs when a battery **charges** with renewable energy.
* **Storage Loss Record (SLR)** – Tracks energy losses incurred during the storage process.
* **Storage Discharge Record (SDR)** – Logs when the stored energy is **discharged** for use.

**2.3. Storage Loss Record (SLR)**

An SLR quantifies **energy lost** in storage due to inefficiencies. It is calculated as:\
SLRperiod=∑SCRperiod×TotalLossesTotalChargedEnergySLR\_{period} = \sum\_{SCR\_{period\}} \times \frac{TotalLosses}{TotalChargedEnergy}\
where:

* **TotalLosses** is the cumulative energy lost over an audit period.
* **TotalChargedEnergy** is the sum of all SCRs over the same period.
* **SLRs are proportionally distributed across all SCRs** within the audit period.
* **Alternative Approach:** Losses may instead be recorded as an attribute within SCRs.

**2.4. First In, First Out (FIFO) Method**

A **time-based allocation rule** ensuring that the **oldest stored energy is discharged first** when issuing STRs.

**2.5. Storage Discharge Granular Certificate (SD-GC)**

A new GC issued upon the **successful matching of an STR and a GC** in the registry, verifying that the clean energy has been time-shifted.

***

#### **3. Workflow Overview**

The following steps outline the process for **time-shifting GCs** using STRs.

***

#### **Step 1: Storage Operator Submits Dispatch Data**

* The **storage operator** submits **hourly dispatch data** to the **Granular Registry**.
* The registry issues **Storage Transfer Records (STRs)** based on the submitted charge/discharge events.

***

#### **Step 2: Selecting & Purchasing STRs**

* A **corporate buyer** matches STRs to the GCs they want to shift.
* They **purchase STRs** directly from storage operators, brokers, or marketplaces (similar to buying unbundled RECs).

***

#### **Step 3: STR Transfer to the Buyer’s GC Account**

* Upon purchase, the STR is **transferred** from the storage operator’s **registry account** to the buyer’s **GC account**.
* The **Granular Registry** verifies:
  * **STR validity** (ensuring it was issued by an approved storage operator).
  * **No double allocation** (each STR can only be used once).

***

#### **Step 4: Matching STRs to GCs**

* The buyer selects **STRs and GCs** from their account to be processed.
* The **Granular Registry performs timestamp validation** to ensure:
  * The **GC timestamp (original renewable generation)** matches the **STR discharge timestamp**.
  * The **FIFO method** was followed (oldest stored energy is discharged first).
* If timestamps **match**:
  * The **original GC and STR are canceled**.
  * A new **Storage Discharge GC (SD-GC)** is issued **directly to the buyer’s GC account**.

***

#### **Step 5: Buyer Claims 24/7 Carbon-Free Energy**

* The buyer **retires SD-GCs** to be claimed for corporate sustainability reporting.
* They can also **sell excess SD-GCs** on the market (if not needed).

***

#### **4. Compliance and Verification**

**4.1. GC Registry Compliance Checks**

* The registry **validates timestamps** for each GC-STR match.
* Ensures **STRs are not reused** across multiple transactions.
* Verifies **SD-GCs adhere to EnergyTag hourly matching rules**.

**4.2. Double Counting Prevention**

* The **original GC and STR are both canceled** to prevent duplicate claims.
* The **SD-GC inherits all attributes** of the original GC **plus the storage discharge timestamp**.

**4.3. ERCOT-Specific Considerations**

* **All transactions comply** with ERCOT’s existing **REC tracking system**.
* **Battery operators must report hourly metering data** for SCRs, SLRs, and SDRs.
* The **FIFO allocation rule is mandatory** for STR issuance.

***

#### **5. Conclusion**

This methodology **streamlines time-shifting of renewable energy** by introducing a **structured, market-driven, and transparent** STR-GC matching process. The inclusion of **Storage Loss Records (SLRs)** enhances auditability and ensures accurate energy tracking. By leveraging **Granular Certificates**, ERCOT market participants can **enhance 24/7 clean energy procurement**, improve **storage asset monetization**, and **unlock new revenue streams** for flexible clean energy solutions.

This framework will be periodically updated to reflect **evolving regulatory requirements and market developments**.
