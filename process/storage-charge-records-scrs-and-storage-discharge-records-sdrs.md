# Storage Charge Records (SCRs) and Storage Discharge Records (SDRs)

## **Introduction**

The issuance of **Storage Charge Records (SCRs) and Storage Discharge Records (SDRs)** is a fundamental process in the registry that ensures accurate tracking of energy entering and exiting a storage system. These records serve as the foundation for **time-shifting energy attributes**, allowing Granular Certificates (GCs) to be allocated to storage and later retrieved for use in 24/7 Carbon-Free Energy (CFE) strategies.

This section details the methodology for **creating, validating, and issuing SCRs and SDRs** in the registry. The FIFO allocation process and Storage Allocation Records (SARs) are covered in the following section.

***

## **Overview of Storage Records**

### **Storage Charge Record (SCR)**

An **SCR** is created whenever energy is charged into a registered storage device. It records the quantity of energy stored and the time of the charging event.

Each SCR contains:

* **Storage Asset ID** – Unique identifier of the storage system.
* **Charging Timestamp (UTC)** – Start and end time of the charging interval.
* **Charged Energy Volume (Wh)** – The total energy absorbed by storage during the interval.
* **Charging Source** – Whether the energy comes from:
  * **A renewable GC-backed source** (linked to a retired GC).
  * **Grid electricity** (if applicable).
* **Round-trip Efficiency Placeholder** – The efficiency loss expected when the energy is later discharged.
* **SCR Status** – Pending, Allocated, or Expired.

SCRs remain **open and pending** until they are linked to an SDR when the stored energy is discharged.

***

### **Storage Discharge Record (SDR)**

An **SDR** is created whenever energy is released from a storage device. It records the quantity of energy discharged and the time of the event.

Each SDR contains:

* **Storage Asset ID** – Unique identifier of the storage system.
* **Discharge Timestamp (UTC)** – Start and end time of the discharge interval.
* **Discharged Energy Volume (Wh)** – The total energy output from storage.
* **Discharge Destination** – The final location of the energy:
  * **Grid injection** (for resale or reallocation).
  * **Behind-the-meter consumption** (onsite usage).
  * **Direct delivery via PPA** (contracted power delivery).
* **Reference to Corresponding SCR(s)** – Links the discharged energy to its original stored source.
* **Storage Efficiency Factor** – Adjusts for round-trip efficiency losses.
* **SDR Status** – Pending, Allocated, or Expired.

SDRs remain **pending** until they are allocated to a **Storage Allocation Record (SAR)**, at which point they can be used for SD-GC issuance.

***

## **Step-by-Step Issuance Process**

### **Step 1: Receive Storage Meter Data**

* The storage facility submits **interval-based metering data** for charging and discharging events.
* Meter data includes:
  * **Timestamp of event**
  * **Energy volume charged/discharged (Wh)**
  * **Storage system ID and meter ID**
  * **Charging source or discharge destination**

### **Step 2: Split Meter Data into Hourly Intervals**

* The registry follows the same **hourly data-splitting methodology** used for generation data.
* If an event spans multiple hours, the energy is **distributed proportionally** based on the power profile.

**Example of Splitting a Charging Event Across Two Hours**

| Original Charge Event    | Split Hourly Intervals                                                            |
| ------------------------ | --------------------------------------------------------------------------------- |
| 17:30 - 19:15 (1,500 Wh) | <p>17:30 - 18:00 → 500 Wh<br>18:00 - 19:00 → 800 Wh<br>19:00 - 19:15 → 200 Wh</p> |

* A similar approach applies to **discharge events**, ensuring hourly granularity.

### **Step 3: Assign Attributes and Create SCR/SDR**

Once the energy is split into hourly blocks, the system **creates an SCR for charge events and an SDR for discharge events**, assigning the appropriate metadata.

**SCR Creation Example**

| Attribute                 | Example Value                     |
| ------------------------- | --------------------------------- |
| **Storage Asset ID**      | STG-001                           |
| **Charging Timestamp**    | 2025-04-03T14:00:00Z to 15:00:00Z |
| **Charged Energy Volume** | 1,200 Wh                          |
| **Charging Source**       | Renewable GC-backed               |
| **Reference to GCs**      | GC-4587 (canceled for storage)    |
| **SCR Status**            | Pending                           |

**SDR Creation Example**

| Attribute                    | Example Value                            |
| ---------------------------- | ---------------------------------------- |
| **Storage Asset ID**         | STG-001                                  |
| **Discharge Timestamp**      | 2025-04-05T18:00:00Z to 19:00:00Z        |
| **Discharged Energy Volume** | 1,080 Wh (accounting for 90% efficiency) |
| **Discharge Destination**    | Grid injection                           |
| **Reference to SCRs**        | SCR-9211 (charged energy source)         |
| **SDR Status**               | Pending                                  |

### **Step 4: Store and Display Records in Registry**

* SCRs and SDRs are stored in the **registry ledger**, maintaining a complete history of energy movement.
* Users can view **all available storage records** on the **Storage Projects Page**.
* Records remain **pending** until they are allocated to a **Storage Allocation Record (SAR)** in the **FIFO matching process**.

***

## **Compliance & Data Integrity**

* The registry **automatically validates** all incoming storage meter data.
* SCRs and SDRs are **immutably recorded** in the ledger to prevent modification.
* A **FIFO allocation method** is enforced to ensure:
  * **Chronological consistency** between SCRs and SDRs.
  * **Preventing selective cherry-picking of storage events**.
  * **Accurate tracking of round-trip efficiency losses**.

***

## **Summary of SCR & SDR Issuance Steps**

| Step | Action                      | Registry Interaction                                      |
| ---- | --------------------------- | --------------------------------------------------------- |
| 1    | Receive storage meter data  | System ingests charging and discharging records           |
| 2    | Split into hourly intervals | Data is proportionally allocated based on timestamps      |
| 3    | Create SCRs & SDRs          | Attributes are assigned and linked to storage assets      |
| 4    | Store in Registry           | Displayed on the **Storage Projects Page**                |
| 5    | Allocate SCRs to SDRs       | Process covered in the **FIFO Allocation & SARs Section** |

***

## **Next Steps: Linking SCRs and SDRs**

Once issued, **SCRs and SDRs must be linked using the FIFO allocation method**. This ensures a structured, chronological process for managing energy time-shifting. The next section details:

* **Storage Allocation Records (SARs)**
* **FIFO allocation of SCRs to SDRs**
* **Conversion of linked SARs into SD-GCs**
