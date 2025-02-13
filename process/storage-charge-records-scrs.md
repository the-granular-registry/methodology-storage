# Storage Charge Records (SCRs)

## **Introduction**

Storage Charge Records (**SCRs**) are digital records created within the registry to track the charging of energy storage systems. Each SCR corresponds to a **specific time interval** in which a storage device absorbs energy from the grid or a production source. This process ensures that the attributes of the charged energy are properly recorded and available for later discharge.

To maintain consistency and accuracy, the **same data-splitting process used for hourly generation meter data** (as described in the [Generation Methodology](https://docs.gc-registry.com/gc-registry/methodology/process/split-meter-data)) will be applied to storage charging events.

***

## **Step-by-Step Process for Creating SCRs**

### **Step 1: Receive Storage Meter Data**

* The system receives **interval-based metering data** from the storage facility’s charge meter.
* The data includes:
  * **Timestamp of energy charging (UTC)**
  * **Energy volume charged (Wh)**
  * **Meter ID and storage asset details**
  * **Charging source identifier (grid, renewable source, etc.)**

### **Step 2: Split Storage Meter Data into Hourly Intervals**

* The registry **splits the raw metering data** into **hourly intervals** using the same approach as the generation methodology:
  1. If the charge event occurs **within a single hour**, the total charge is assigned to that hourly interval.
  2. If the charge event **spans multiple hours**, the system **distributes** the charge proportionally across the hours based on the power profile.
  3. Any **partial-hour charging** at the start or end of an interval is allocated proportionally to ensure correct attribution.

### **Step 3: Assign Charge Attributes to the SCR**

* The SCR is created with the following attributes:
  * **Storage Asset ID** (Unique registry identifier)
  * **Timestamp** (Start and end of charging interval)
  * **Charged Energy Volume (Wh)**
  * **Charging Source** (GC-backed renewable source or grid import)
  * **Reference to Original GCs** (if applicable)
  * **Round-trip efficiency placeholder** (for future discharge tracking)

### **Step 4: Store and Display SCR in the Registry**

* The SCR is **saved in the registry ledger** and linked to the corresponding storage asset.
* The record is displayed in the **Storage Projects Page**, where GC users can view available storage charge records for potential allocation.
* SCRs remain **pending until linked to a corresponding Storage Discharge Record (SDR).**

***

## **Compliance and Data Integrity**

* The registry **validates all incoming meter data** to ensure accuracy before creating an SCR.
* If discrepancies arise, the system **flags and logs anomalies** for manual review.
* The SCR creation process aligns with the **EnergyTag Granular Certificate Standard** to maintain compliance and avoid double counting.

***

## **Summary of SCR Creation Steps**

| Step | Action                            | Registry Interaction                                         |
| ---- | --------------------------------- | ------------------------------------------------------------ |
| 1    | Receive storage charge meter data | System ingests data from storage facility                    |
| 2    | Split into hourly intervals       | Data is allocated across time intervals                      |
| 3    | Create SCR with charge attributes | Energy volume, timestamp, source, and asset ID recorded      |
| 4    | Store and display SCR in registry | SCR appears in **Storage Projects Page** for user visibility |
