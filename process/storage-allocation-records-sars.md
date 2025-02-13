# Storage Allocation Records (SARs)

## **Introduction**

The Storage Allocation Record (**SAR**) is a registry mechanism that enables users to allocate Granular Certificates (**GCs**) for time-shifting through energy storage. SARs are created from Storage Charge Records (**SCRs**) and Storage Discharge Records (**SDRs**) and serve as an intermediate step before issuing **Storage Discharge GCs (SD-GCs)**.

This process ensures that GC users can transparently view, select, and allocate their certificates to storage projects while maintaining compliance with EnergyTag's **Granular Certificate Standard**.

***

## **SAR Lifecycle and Registry Interaction**

### **SAR Creation**

* When a storage system **charges**, an **SCR** is recorded in the registry, capturing:
  * The **time interval** of charging.
  * The **energy volume charged** (Wh).
  * The **source attributes** of any canceled GCs (if applicable).
  * The **location and technology** of the storage system.
* When the storage system **discharges**, an **SDR** is recorded, capturing:
  * The **time interval** of discharge.
  * The **energy volume discharged** (Wh), adjusted for round-trip losses.
  * The **efficiency factor** of the storage system.
  * A reference to the **SCR(s)** used to charge the energy.
* A **SAR** is automatically created in the registry by **linking one or more correlated SCRs and SDRs** following a **First-In, First-Out (FIFO) allocation method**.

### **Displaying SARs in the Registry**

* SARs are displayed on a **separate Storage Projects page** in the registry, distinct from active GCs.
* Each SAR includes:
  * **Storage asset details** (location, technology, efficiency factor).
  * **Charging and discharging time intervals**.
  * **Available volume for allocation**.
  * **Expected SD-GC issuance window**.
  * **Status** (Available, Partially Allocated, Fully Allocated).

### **GC Allocation to SARs**

* A GC holder can select an available SAR and allocate **matching GCs** from their account.
* The system verifies:
  * The GC is **valid and unallocated**.
  * The GC’s **generation timestamp precedes the SAR's charging time**.
  * The GC’s **volume aligns with the available SAR capacity**.
* Once confirmed, the system **cancels the allocated GC** and moves the SAR to "Pending Conversion."

### **Conversion of SAR to SD-GC**

* Once a SAR has been **fully allocated** with GCs, the registry:
  * **Links the SAR to the allocated GC attributes**.
  * **Issues an SD-GC** with the following details:
    * Original **generation attributes** from the canceled GC.
    * The **storage discharge timestamp**.
    * The **storage facility details**.
    * The **energy volume discharged** (Wh), adjusted for losses.
  * The SD-GC is deposited into the **user's account** for further trading, retirement, or matching.

***

## **FIFO Allocation Method**

* SARs follow a **First-In, First-Out (FIFO)** allocation, ensuring that:
  * Older **SCRs and SDRs are matched first**.
  * Storage energy is used in a **chronologically correct order**.
  * **Market participants cannot selectively "cherry-pick" storage records**, preserving integrity.

#### **Example of FIFO Allocation**

| Timestamp            | Energy Volume | SAR Status |
| -------------------- | ------------- | ---------- |
| SCR 1 (Jan 1, 12:00) | 1000 Wh       | Linked     |
| SDR 1 (Jan 2, 15:00) | 900 Wh        | Linked     |
| SAR 1 (Jan 1-2)      | 900 Wh        | Available  |
| SCR 2 (Jan 3, 14:00) | 800 Wh        | Linked     |
| SDR 2 (Jan 4, 18:00) | 700 Wh        | Available  |

* When a GC user selects **SAR 1**, their GCs will **first** allocate to the **900 Wh linked to the earliest SCR-SDR pair** before moving to SAR 2.

***

## **Market & Transparency Benefits**

### **Enabling Pre-Market Insights**

* SARs **offer visibility** into storage utilization before SD-GCs are issued.
* Users can **pre-plan GC shifting** based on available storage capacity.

### **Avoiding Double Counting**

* Since **SD-GCs are only issued when a GC is allocated to a SAR**, there is **no risk of duplicate claims** on stored energy attributes.

### **Supporting 24/7 CFE Strategies**

* By allowing users to **select SARs and align their clean energy goals**, the registry enhances **time-based energy procurement**.

***

## **Summary of SAR Processing Steps**

| Step | Action                                | Registry Interaction                          |
| ---- | ------------------------------------- | --------------------------------------------- |
| 1    | Storage system **charges**            | SCR recorded                                  |
| 2    | Storage system **discharges**         | SDR recorded                                  |
| 3    | Registry **links** SCR + SDR          | SAR created                                   |
| 4    | SAR displayed in **Storage Projects** | Users can view & allocate                     |
| 5    | GC **allocated** to SAR               | GC canceled & SAR moves to Pending Conversion |
| 6    | SAR **converted** to SD-GC            | SD-GC issued & sent to user’s account         |

***

## **Conclusion**

The introduction of **Storage Allocation Records (SARs)** as a market instrument enhances **registry transparency, user flexibility, and market efficiency**. By allowing GC users to view and allocate storage-based shifting opportunities **before committing their GCs**, SARs provide a structured, **compliant pathway** for integrating energy storage into the Granular Certificate ecosystem.
