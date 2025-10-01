---
hidden: true
---

# Alternative Method 2: Issue PECs for Net Emissions

Issue PECs for discharge energy based on net emissions. If the battery has net avoided emissions after accounting for all charging and discharging activities, the net emissions will be spread evenly over the hours of discharging when issuing PECs.

Example Transaction

Step 1: Collect Meter Data:

In one year, the battery had the following activity derived from hourly meter data.

·       Consumed charging energy: 5,000 MWh

·       Injected discharging energy: 4,250 MWh

·       Round-trip efficiency: 85%

Step 2: Assess Net Emissions

Using the PECA emissions source hierarchy, REsurety was chosen as the emissions data provider. (This is automated when meter data is uploaded to the marketplace platform).

·       Average charging emissions factor (LME): 0.20 tCO2/MWh

·       Total induced emissions: 1,000 tCO2

·       Average discharging emissions factor (LME): 0.45 tCO2/MWh

·       Total avoided emissions: 1,912.5 tCO2

·       Net emissions (induced – avoided): 912.5 tCO2

Step 3: Issue PECs

The PEC registry will verify the meter data, emissions data, and retired PECs. Upon completion, a Power Emissions Proof Report will be created to certify the charging impact is neutralized.

·       Issued PECs: 4,250

·       PEC emissions factor: 912.5 / 4,250 = 0.22 tCO2/MWh

Step 5: Settle the Emissionality-indexed PEC agreement

Settling the PEC agreement using a predetermined carbon price (This is automated on the marketplace platform).

·       Carbon price: $100 ($/tCO2)

·       Net emissions (induced – avoided): 912.5 tCO2

·       Storage Operator net profit: $91,250

&#x20;

| Advantages                                       | Disadvantages                                                                                                                   |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Does not require neutralizing charging activity. | It does not comply with the EnergyTag standard, which may limit market adoption.                                                |
| The simplest method of the choices.              | Issued PECs will not have retired RECs associated with them, so they will not comply with the existing GHGP scope 2 accounting. |
|                                                  |                                                                                                                                 |
