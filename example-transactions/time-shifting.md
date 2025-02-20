# Time Shifting

## **Collect Meter Data**

A battery had the following activity derived from hourly meter data.

| Consumed charging energy (MWh)    | 5,000 |
| --------------------------------- | ----- |
| Injected discharging energy (MWh) | 4,250 |
| Round-trip efficiency             | 85%   |

## Assess the Impact of Charging Activity

Using the GRF emissions source hierarchy, REsurety was chosen as the emissions data provider.&#x20;

* Hours of charging
* Volume of Energy (MWh)

<table data-full-width="true"><thead><tr><th width="102">Hour</th><th width="108">MWh</th><th width="182">Average MER (tCO2/MWh)</th><th width="217">Total Carbon Impact (tCO2)</th></tr></thead><tbody><tr><td>1</td><td>0</td><td></td><td>0</td></tr><tr><td>2</td><td>0</td><td></td><td>0</td></tr><tr><td>3</td><td>0</td><td></td><td>0</td></tr><tr><td>4</td><td>0</td><td></td><td>0</td></tr><tr><td>5</td><td>0</td><td></td><td>0</td></tr><tr><td>6</td><td>200</td><td>0.15</td><td>30</td></tr><tr><td>7</td><td>1000</td><td>0.25</td><td>250</td></tr><tr><td>8</td><td>2000</td><td>0.2</td><td>400</td></tr><tr><td>9</td><td>1100</td><td>0.1</td><td>110</td></tr><tr><td>10</td><td>700</td><td>0.3</td><td>210</td></tr><tr><td>11</td><td>0</td><td></td><td>0</td></tr><tr><td>12</td><td>0</td><td></td><td>0</td></tr><tr><td>13</td><td>0</td><td></td><td>0</td></tr><tr><td>14</td><td>0</td><td></td><td>0</td></tr><tr><td>15</td><td>0</td><td></td><td>0</td></tr><tr><td>16</td><td>0</td><td></td><td>0</td></tr><tr><td>17</td><td>0</td><td></td><td>0</td></tr><tr><td>18</td><td>0</td><td></td><td>0</td></tr><tr><td>19</td><td>0</td><td></td><td>0</td></tr><tr><td>20</td><td>0</td><td></td><td>0</td></tr><tr><td>21</td><td>0</td><td></td><td>0</td></tr><tr><td>22</td><td>0</td><td></td><td>0</td></tr><tr><td>23</td><td>0</td><td></td><td>0</td></tr><tr><td>24</td><td>0</td><td></td><td>0</td></tr></tbody></table>

| Average charging MER (tCO2/MWh)     | 0.20  |
| ----------------------------------- | ----- |
| Total charging carbon impact (tCO2) | 1,000 |
| Consumed charging energy (MWh)      | 5,000 |

## Neutralize Charging Impact (Hourly-Matching)

GCs are retired to match hours of charging and sourced from the same balance authority, complying with the EnergyTag Standard.

| Retired GCs                            | 5000              |
| --------------------------------------- | ----------------- |
| Retired GC Average MER (tCO2/MWh)      | 0.18              |
| Percent hourly-matched                  | 100%              |
| Carbon Impact of Retired GCs (tCO2)     | -900              |
| Remaining charging carbon impact (tCO2) | 1,000 – 900 = 100 |
| Percent emissions-matched               | 90%               |

## Submit Project Data for Verification and GC Issuance&#x20;

The GC registry verifies the meter data, emissions data, and retired GCs. Upon completion, a GC Matching Report will be created along with the issued GCs.

| Average discharging MER (tCO2/MWh)      | 0.45                      |
| --------------------------------------- | ------------------------- |
| Gross discharge carbon impact (tCO2)    | 4,250 \* 0.45 = -1,912.5  |
| Adjusted discharge carbon impact (tCO2) | -1,912.5 + 100 = -1,812.5 |
| Issued GCs                             | 4,250                     |
| Issued GC Average MER (tCO2/MWh)       | 0.43                      |

## Contract Settlement

Settling the GC agreement using a predetermined carbon price.

| Issued GCs Sales Revenue | $181,250 |
| ------------------------- | -------- |
| Retired GC Cost          | -$90,000 |
| Net Profit                | $91,250  |

## Carbon Accounting

This battery has converted 5,000 low-impact GCs into 4,250 high-impact GCs by shifting the hours of CFE generation. Adding a ‘virtual hybrid’ to low-impact PPAs will fill gaps in 24/7 PPAs.
