# Storage Discharge Granular Certificate (SD-GC) Issuance

## **Introduction**

The **Storage Discharge Granular Certificate (SD-GC)** represents energy that has been stored and subsequently discharged, maintaining the original environmental attributes of the energy source while accounting for storage efficiency losses. Additionally, this methodology introduces a novel approach to tracking the **net marginal carbon impact** of energy storage, providing users with a **more accurate carbon footprint assessment** of their time-shifted energy use.

SD-GCs are issued through the **conversion of Storage Allocation Records (SARs)**, which are created by linking **Storage Charge Records (SCRs) and Storage Discharge Records (SDRs)** using a **First-In, First-Out (FIFO) allocation method**. This ensures the integrity of the stored energy lifecycle while accurately attributing the carbon intensity impact.

***

## **Prerequisites for SD-GC Issuance**

Before an SD-GC can be issued, the following conditions must be met:

1. **A SAR must exist** – A **valid Storage Allocation Record (SAR)** must be available in the registry.
2. **GC Allocation to SAR** – A user must allocate **CFE Granular Certificates (CFE GCs)** from their account to a SAR, canceling the original GCs in exchange for an SD-GC.
3. **SCR-SDR Linkage Complete** – The SAR must correctly link **one or more SCRs and SDRs**, ensuring that energy is properly accounted for.
4. **Carbon Impact Calculation Applied** – The registry calculates the **net marginal carbon impact** of the SAR and applies it to the GCs being shifted using the following formula:

$$
SD\text{-}GC_{impact} = GC_{impact} + SAR_{impact}
$$

Where:

* **GC\_impact** = Carbon impact of the original GC before storage.
* **SAR\_impact** = Carbon emissions associated with energy storage, accounting for grid charging mix and losses.
* **SD-GC\_impact** = Adjusted carbon impact of the discharged energy.

***

## **Step-by-Step Process for SD-GC Issuance**

### **Step 1: User Selects SAR for GC Allocation**

* The user navigates to the **Storage Projects Page** in the registry.
* Available SARs are displayed with key attributes, including:
  * **Storage Asset ID**
  * **Charging and Discharging Time Intervals**
  * **Available Capacity for Allocation**
  * **SAR Carbon Impact Estimate**
* The user selects a SAR and **allocates CFE GCs** from their account.

### **Step 2: Validate GC Allocation**

* The registry verifies the following conditions:
  * The **allocated CFE GCs are valid and unallocated**.
  * The **GC’s generation timestamp precedes the charging timestamp** of the SAR.
  * The **GC volume matches or is proportionally allocated to the SAR’s available capacity**.
* If the validation is successful, the system **cancels the allocated GC(s)** and marks the SAR as "Pending SD-GC Issuance."

### **Step 3: Calculate SD-GC Volume and Carbon Impact**

* The **carbon impact adjustment** is calculated:

$$
SD\text{-}GC_{impact} = GC_{impact} + SAR_{impact}
$$

* This ensures that the **adjusted carbon impact** of the discharged energy is correctly recorded.

### **Step 4: Issue SD-GC to User’s Account**

* The registry **creates and issues an SD-GC** with the following attributes:
  * **Unique SD-GC ID**
  * **Original GC Source** (Energy Type, Production Device, Location)
  * **Storage Asset Details**
  * **Charging Timestamp (from SCR)**
  * **Discharge Timestamp (from SDR)**
  * **Final SD-GC Volume (Wh)**
  * **Net Carbon Impact Adjustment**
* The issued SD-GC is **deposited into the user’s account**, where it can be retired, transferred, or used for compliance claims.

***

## **Example SD-GC Issuance Workflow**

| Step | Action                                    | Registry Interaction                                      |
| ---- | ----------------------------------------- | --------------------------------------------------------- |
| 1    | User selects SAR for GC allocation        | User picks available SAR from the Storage Projects Page   |
| 2    | System validates GC allocation            | Ensures the GC is valid and meets allocation rules        |
| 3    | GC is canceled, and SAR is marked pending | Registry cancels the original GC and confirms allocation  |
| 4    | Net carbon impact calculated              | SD-GC impact is adjusted using SAR carbon impact          |
| 5    | SD-GC is issued                           | User receives an SD-GC reflecting the time-shifted energy |

***

## **Compliance & Data Integrity**

* **Time-Based Integrity** – The SD-GC maintains a clear link to its original generation source while shifting its availability based on storage activity.
* **Preventing Double Counting** – The registry ensures that once an SD-GC is issued, the corresponding original GC is permanently canceled.
* **Carbon Transparency** – The new methodology ensures users receive an **accurate carbon footprint** for their time-shifted clean energy.
* **FIFO Enforcement** – The registry enforces a **first-in, first-out (FIFO) allocation**, ensuring energy is time-shifted in chronological order.

***

## **Summary & Key Benefits of SD-GC Issuance**

| Feature                                   | Description                                                                                |
| ----------------------------------------- | ------------------------------------------------------------------------------------------ |
| **Enables Time-Shifting of Clean Energy** | Allows users to store and later retrieve energy while maintaining its original attributes. |
| **Accounts for Storage Carbon Impact**    | Adjusts the carbon footprint of shifted energy based on storage grid interaction.          |
| **Supports 24/7 CFE Strategies**          | Helps organizations match clean energy consumption with storage-backed renewable supply.   |
| **Ensures Compliance with EnergyTag**     | Prevents double counting and maintains accuracy in clean energy reporting.                 |
