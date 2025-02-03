# Assessing Charging Impact

Assessing the carbon impact during the charging phase of an energy storage system is essential for accurately calculating induced emissions. This section outlines the methodology for calculating emissions during charging periods and details the use of Marginal Emissions Rates (MER) in these calculations. It also addresses considerations related to data time lags and accuracy to ensure reliable results.

## Calculation of Induced Emissions

### Methodology for Calculating Emissions During Charging Periods

The induced emissions associated with charging an energy storage system are calculated by applying the Marginal Emissions Rates (MER) to the amount of energy consumed during each charging period. The following steps provide a systematic approach to this calculation:

#### **Step 1: Data Alignment**

* **Hourly Charging Data**: Utilize the collected hourly meter readings that indicate the amount of energy consumed during each charging hour (in MWh).
* **Timestamp Synchronization**: Ensure that the timestamps of the charging data align precisely with the MER data timestamps to maintain temporal accuracy.

#### **Step 2: Obtain Marginal Emissions Rates**

* **Select Appropriate MERs**: For each charging hour, retrieve the corresponding MER (in metric tons of CO₂ per MWh) from the chosen emissions data provider.
* **Location Specificity**: Confirm that the MERs are specific to the project's geographical location and grid connection point.

#### **Step 3: Calculate Hourly Induced Emissions**

*   **Apply MERs to Charging Data**: Multiply the energy consumed during each charging hour by the corresponding MER to determine the induced emissions for that hour.

    **Formula:**

$$
Induced Emissions_{hour} = Charging Energy_{hour} X MER_{hour}
$$

* **Example Calculation**:
  * Charging Energy at Hour 1: 50 MWh
  * MER at Hour 1: 0.25 tCO₂/MWh
  * Induced Emissions at Hour 1:

$$
50 MWh×0.25 tCO₂/MWh=12.5 tCO₂
$$

#### **Step 4: Sum Total Induced Emissions**

*   **Aggregate Hourly Emissions**: Sum the induced emissions calculated for each charging hour over the reporting period to obtain the total induced emissions.

    **Formula:**

$$
Total Induced Emissions=\sum_{hour=1}^{n} Induced Emissions_{hour}
$$

*   **Example**:

    If the induced emissions for each hour over 100 charging hours are calculated, sum all values:

$$
Total Induced Emissions=Emissions_1+Emissions_2+⋯+Emissions_{100}
$$

#### **Step 5: Documentation**

* **Record Details**: Document all calculations, including:
  * Hourly charging energies.
  * Corresponding MERs.
  * Resulting induced emissions per hour.
* **Maintain Transparency**: Keep records accessible for verification and auditing by the PEC Registry.

## Emissions Data Sources and Methodology

### Use of Marginal Emissions Rates

Marginal Emissions Rates are critical for accurately reflecting the emissions impact of charging an energy storage system. MERs represent the emissions produced by the marginal generating unit—the last unit dispatched to meet demand—which is typically the most carbon-intensive.

### **Importance of MER in Induced Emissions Calculations**

* **Temporal Accuracy**: MERs vary hourly, capturing fluctuations in grid emissions intensity due to changes in demand and generation mix.
* **Locational Accuracy**: MERs are location-specific, reflecting the unique generation portfolio and operational conditions of the grid at the project's location.
* **Enhanced Precision**: Using MERs provides a more precise calculation of induced emissions compared to average emissions rates, leading to more accurate carbon accounting.

### **Calculating Induced Emissions with MER**

* **Hourly Application**: Apply the specific MER for each hour directly to the corresponding charging energy.
* **Avoiding Averaging**: Do not use annual or monthly average MERs, as they can obscure temporal variations and reduce accuracy.

### Handling Data Time Lags and Accuracy

#### **Data Time Lags**

Some emissions data providers may experience delays in publishing MER data due to the time required for data collection, processing, and validation. These time lags can range from a few days to several months, depending on the grid and data provider.

#### **Strategies for Managing Time Lags**

* **Delayed PEC Issuance**: Wait until the MER data is available before finalizing induced emissions calculations and issuing PECs.
* **Interim Estimates**: Use preliminary MER data where available, with the understanding that adjustments may be necessary once final data is released.
* **Communication with Stakeholders**: Inform relevant parties about potential delays in PEC issuance due to data availability constraints.

## **Ensuring Data Accuracy**

### **Selection of Reliable Data Providers**

* **Compliance with PECA Guidelines**: Choose emissions data providers that adhere to the criteria outlined in the PECA guidelines.
* **Data Validation Processes**: Ensure that providers have robust methodologies for data collection and validation.

### **Verification of MER Data**

* **Cross-Referencing**: Compare MER data from multiple sources, if possible, to identify discrepancies.
* **Historical Data Analysis**: Analyze historical MER trends to assess the reasonableness of current data.

### **Documentation of Data Sources and Methodologies**

* **Detailed Records**: Maintain comprehensive documentation of the emissions data sources, including:
  * Provider details.
  * Data acquisition dates.
  * Methodologies used by the provider to calculate MER.
* **Transparency**: Provide this documentation as part of the project impact report submitted to the PEC Registry.

### **Example of Handling Data Time Lags**

Suppose an energy storage project in the ERCOT grid experiences a 60-day delay in MER data publication:

* **Impact on PEC Issuance**: PECs for the affected period cannot be issued until the accurate MER data is available.
* **Operational Adjustments**:
  * Plan for the delay in financial and operational projections.
  * Communicate with corporate buyers regarding the expected timeline.
* **Data Update**: Once the MER data is published, proceed with induced emissions calculations and PEC issuance promptly.
