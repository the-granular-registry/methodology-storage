---
hidden: true
---

# Carbon Shifting Example2

This example demonstrates how an energy storage operator can monetize carbon arbitrage by charging the storage system during periods of low Marginal Emissions Rates (MER) and discharging during periods of high MER. By utilizing a carbon price, the operator captures financial benefits from reducing greenhouse gas emissions through effective time-shifting of carbon-free energy.

## Step-by-Step Calculations

### **Step 1: Collect Meter Data**

An energy storage system operates over a reporting period with the following activity:

* **Charging Energy Consumed**: 5,000 MWh
* **Discharging Energy Delivered**: 4,250 MWh
* **Round-Trip Efficiency**: 85% (calculated as $$\frac{4,250 \text{ MWh}}{5,000 \text{ MWh}} \times 100\%$$

### **Step 2: Assess Charging Induced Emissions**

Using Marginal Emissions Rates (MER) provided by an approved emissions data provider (e.g., REsurety), calculate the induced emissions during charging.

* **Average Charging MER**: 0.20 tCO₂/MWh
* **Total Induced Emissions during Charging**:

$$
Gross Induced Emissions = \sum_{hour=1}^nChargingEnergy_{hour}XMER_{hour}
$$

* For this example, we can use the average



### **Step 3: Neutralize Charging Impact by Retiring PECs**

To neutralize the charging impact, retire PECs corresponding to the charging hours, sourced from the same balance authority area, complying with the EnergyTag Standard.

* **PECs Retired**: 5,000 MWh (matching the charging energy)
* **Average MER of Retired PECs**: 0.18 tCO₂/MWh
*   **Emissions Offset by Retired PECs**:

    Emissions Offset=PECs Retired×Average MER of PECs\text{Emissions Offset} = \text{PECs Retired} \times \text{Average MER of PECs}Emissions Offset=PECs Retired×Average MER of PECs Emissions Offset=5,000 MWh×0.18 tCO₂/MWh=900 tCO₂\text{Emissions Offset} = 5,000 \text{ MWh} \times 0.18 \text{ tCO₂/MWh} = 900 \text{ tCO₂}Emissions Offset=5,000 MWh×0.18 tCO₂/MWh=900 tCO₂
*   **Remaining Induced Emissions**:

    Remaining Induced Emissions=Total Induced Emissions−Emissions Offset\text{Remaining Induced Emissions} = \text{Total Induced Emissions} - \text{Emissions Offset}Remaining Induced Emissions=Total Induced Emissions−Emissions Offset Remaining Induced Emissions=1,000 tCO₂−900 tCO₂=100 tCO₂\text{Remaining Induced Emissions} = 1,000 \text{ tCO₂} - 900 \text{ tCO₂} = 100 \text{ tCO₂}Remaining Induced Emissions=1,000 tCO₂−900 tCO₂=100 tCO₂

**Step 4: Calculate Gross Discharge Avoided Emissions**

Calculate the gross avoided emissions during discharging by applying the MER for the discharging periods.

* **Average Discharging MER**: 0.45 tCO₂/MWh
*   **Gross Avoided Emissions during Discharge**:

    Gross Avoided Emissions=Discharging Energy×Average Discharging MER\text{Gross Avoided Emissions} = \text{Discharging Energy} \times \text{Average Discharging MER}Gross Avoided Emissions=Discharging Energy×Average Discharging MER Gross Avoided Emissions=4,250 MWh×0.45 tCO₂/MWh=1,912.5 tCO₂\text{Gross Avoided Emissions} = 4,250 \text{ MWh} \times 0.45 \text{ tCO₂/MWh} = 1,912.5 \text{ tCO₂}Gross Avoided Emissions=4,250 MWh×0.45 tCO₂/MWh=1,912.5 tCO₂

**Step 5: Assign Remaining Induced Emissions Across Discharge Hours**

Allocate the total remaining induced emissions uniformly across all discharge hours to calculate the net avoided emissions.

* **Total Discharging Hours**: Assume 425 hours (assuming an average discharge rate of 10 MWh/hour).
*   **Remaining Induced Emissions per Hour**:

    Remaining Induced Emissions per Hour=Remaining Induced EmissionsTotal Discharge Hours\text{Remaining Induced Emissions per Hour} = \frac{\text{Remaining Induced Emissions\}}{\text{Total Discharge Hours\}}Remaining Induced Emissions per Hour=Total Discharge HoursRemaining Induced Emissions​ Remaining Induced Emissions per Hour=100 tCO₂425 hours≈0.235 tCO₂/hour\text{Remaining Induced Emissions per Hour} = \frac{100 \text{ tCO₂\}}{425 \text{ hours\}} \approx 0.235 \text{ tCO₂/hour}Remaining Induced Emissions per Hour=425 hours100 tCO₂​≈0.235 tCO₂/hour
*   **Net Avoided Emissions per Hour**:

    For each hour, calculate:

    Net Avoided Emissionshour=(Discharged Energyhour×Discharging MERhour)−Remaining Induced Emissions per Hour\text{Net Avoided Emissions}\_{\text{hour\}} = (\text{Discharged Energy}\_{\text{hour\}} \times \text{Discharging MER}\_{\text{hour\}}) - \text{Remaining Induced Emissions per Hour}Net Avoided Emissionshour​=(Discharged Energyhour​×Discharging MERhour​)−Remaining Induced Emissions per Hour
*   **Total Net Avoided Emissions**:

    Total Net Avoided Emissions=Gross Avoided Emissions−Remaining Induced Emissions\text{Total Net Avoided Emissions} = \text{Gross Avoided Emissions} - \text{Remaining Induced Emissions}Total Net Avoided Emissions=Gross Avoided Emissions−Remaining Induced Emissions Total Net Avoided Emissions=1,912.5 tCO₂−100 tCO₂=1,812.5 tCO₂\text{Total Net Avoided Emissions} = 1,912.5 \text{ tCO₂} - 100 \text{ tCO₂} = 1,812.5 \text{ tCO₂}Total Net Avoided Emissions=1,912.5 tCO₂−100 tCO₂=1,812.5 tCO₂

**Step 6: Issue PECs for Discharged Energy**

Issue PECs for each hour of discharged energy where net avoided emissions are positive.

* **Total PECs Issued**: 4,250 PECs (one for each MWh of discharged energy)
*   **Net Avoided Emissions per PEC**:

    Net Avoided Emissions per PEC=Total Net Avoided EmissionsTotal Discharged Energy\text{Net Avoided Emissions per PEC} = \frac{\text{Total Net Avoided Emissions\}}{\text{Total Discharged Energy\}}Net Avoided Emissions per PEC=Total Discharged EnergyTotal Net Avoided Emissions​ Net Avoided Emissions per PEC=1,812.5 tCO₂4,250 MWh≈0.426 tCO₂/MWh\text{Net Avoided Emissions per PEC} = \frac{1,812.5 \text{ tCO₂\}}{4,250 \text{ MWh\}} \approx 0.426 \text{ tCO₂/MWh}Net Avoided Emissions per PEC=4,250 MWh1,812.5 tCO₂​≈0.426 tCO₂/MWh

**Step 7: Financial Calculations**

Utilize a carbon price to monetize the net avoided emissions.

* **Carbon Price**: $100 per tCO₂
*   **Revenue from Issued PECs**:

    Revenue=Total Net Avoided Emissions×Carbon Price\text{Revenue} = \text{Total Net Avoided Emissions} \times \text{Carbon Price}Revenue=Total Net Avoided Emissions×Carbon Price Revenue=1,812.5 tCO₂×$100/tCO₂=$181,250\text{Revenue} = 1,812.5 \text{ tCO₂} \times \\$100/\text{tCO₂} = \\$181,250Revenue=1,812.5 tCO₂×$100/tCO₂=$181,250
*   **Cost of Retired PECs**:

    Assuming the cost of acquiring and retiring PECs is $18 per MWh.

    Cost of Retired PECs=PECs Retired×Cost per PEC\text{Cost of Retired PECs} = \text{PECs Retired} \times \text{Cost per PEC}Cost of Retired PECs=PECs Retired×Cost per PEC Cost of Retired PECs=5,000 MWh×$18/MWh=$90,000\text{Cost of Retired PECs} = 5,000 \text{ MWh} \times \\$18/\text{MWh} = \\$90,000Cost of Retired PECs=5,000 MWh×$18/MWh=$90,000
*   **Net Profit**:

    Net Profit=Revenue−Cost of Retired PECs\text{Net Profit} = \text{Revenue} - \text{Cost of Retired PECs}Net Profit=Revenue−Cost of Retired PECs Net Profit=$181,250−$90,000=$91,250\text{Net Profit} = \\$181,250 - \\$90,000 = \\$91,250Net Profit=$181,250−$90,000=$91,250

#### Financial Implications and Carbon Accounting Outcomes

**Financial Implications**

* **Cost to Neutralize Charging Emissions**: $90,000 (cost of acquiring and retiring PECs)
* **Revenue from Issued PECs**: $181,250 (from monetizing net avoided emissions)
* **Net Profit**: $91,250

**Carbon Accounting Outcomes**

* **Total Induced Emissions from Charging**: 1,000 tCO₂
* **Emissions Offset by Retired PECs**: 900 tCO₂
* **Remaining Induced Emissions**: 100 tCO₂
* **Gross Avoided Emissions from Discharging**: 1,912.5 tCO₂
* **Net Avoided Emissions**: 1,812.5 tCO₂ (after subtracting remaining induced emissions)
* **Net Carbon Impact**: A net reduction of 1,812.5 tCO₂

**Summary**

By strategically charging during periods of low MER and discharging during periods of high MER, the energy storage operator effectively:

* **Reduces Overall Emissions**: Achieves a substantial net reduction in greenhouse gas emissions.
* **Monetizes Carbon Arbitrage**: Captures financial benefits through the carbon price mechanism.
* **Enhances Sustainability Goals**: Supports corporate and grid-level objectives for emissions reductions.

**Impact on Corporate Buyers:**

* **Accurate Scope 2 Reporting**: Corporations purchasing the issued PECs can accurately report reductions in their Scope 2 emissions.
* **Supports 24/7 Carbon-Free Energy Goals**: Facilitates matching energy consumption with carbon-free energy on an hourly basis.

**Operational Benefits:**

* **Optimized Energy Storage Utilization**: Maximizes the economic and environmental value of the storage asset.
* **Market Incentives Alignment**: Aligns operational strategies with market incentives for emissions reductions.
