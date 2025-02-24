---
hidden: true
---

# Methodology Document for Storage Allocation Records (SAR) with Carbon Impact

##

### Overview

This methodology describes a process for time-shifting energy attributes (Granular Certificates, GCs) via storage. We create Storage Allocation Records (SAR) that link each Storage Charge Record (SCR) to each Storage Discharge Record (SDR) using a FIFO approach, assign Storage Loss Records (SLR) to the charging hour, and then calculate the carbon impact of each SAR based on marginal emissions data.

### Key Steps

#### Context: EnergyTag Battery Methodology

EnergyTag’s standard for battery storage offers a robust, transparent approach for attributing renewable energy certificates (RECs) whenever energy is stored in a battery and discharged at a different time. The EnergyTag framework requires a clear chain-of-custody that connects the charged energy (SCR) to the discharged energy (SDR), while quantifying the associated losses (SLR).

We created the concept of a Storage Allocation Record (SAR) to unify all three elements—SCR, SDR, and SLR—into a single traceable record. Each SAR explains how much energy was charged, how much was discharged, how much was lost, and calculates the resulting carbon impact. This ensures that any time-shift of renewable certificates remains auditable under the EnergyTag methodology.

#### Step 2: Generate SCR and SDR (No Losses)

From these meter readings, we create:

* SCR (Storage Charge Record) for hours where net flow <0< 0.
* SDR (Storage Discharge Record) for hours where net flow >0> 0.

A simple clamp ensures we never create more SDR than the total net charge. If a discharge hour requests more than the net-charged MWh left, it is clamped.

If we denote net negative flow in hour hh as Eh−E\_h^- and net positive flow in hour kk as Ek+E\_k^+, then:

Total charge=∑Eh−,Total discharge=∑Ek+.\text{Total charge} = \sum E\_h^- , \quad \text{Total discharge} = \sum E\_k^+.

#### Step 3: Calculate Efficiency and Total Losses

We define an overall storage round-trip efficiency:

η=∑(SDR)∑(SCR)=Total DischargeTotal Charge,if Total Charge>0.\eta = \frac{\sum (\text{SDR})}{\sum (\text{SCR})} = \frac{\text{Total Discharge\}}{\text{Total Charge\}}, \quad \text{if Total Charge} > 0.

Total losses:

L=∑(SCR)−∑(SDR).L = \sum (\text{SCR}) - \sum (\text{SDR}).

#### Step 4: Create Storage Allocation Records (SAR) via FIFO

We produce a FIFO trace linking each SDR hour to one or more SCR hours, then assign SLR to the charge time. For each piece of SDR, we remove Dη\frac{D}{\eta} from the earliest unallocated SCR, leaving a difference:

SLR portion=(Dη)−D.\text{SLR portion} = \left( \frac{D}{\eta} \right) - D.

We attach that lost portion to the charging hour. The final table has columns:

* scr\_local\_time,scr\_id,scr\_mwh\text{scr\\\_local\\\_time}, \text{scr\\\_id}, \text{scr\\\_mwh}
* sdr\_local\_time,sdr\_id,sdr\_mwh\text{sdr\\\_local\\\_time}, \text{sdr\\\_id}, \text{sdr\\\_mwh}
* slr\_local\_time,slr\_id,slr\_mwh\text{slr\\\_local\\\_time}, \text{slr\\\_id}, \text{slr\\\_mwh}
* A unique ID for the SAR row (record\_id)(\text{record\\\_id}).

#### Step 5: Quality Check

We confirm:

$$
∑SCR=∣∑meter negative∣\sum \text{SCR} = | \sum \text{meter negative} | ∑SDR=∑meter positive\sum \text{SDR} = \sum \text{meter positive} ∑SLR=Total Charge−Total Discharge=L\sum \text{SLR} = \text{Total Charge} - \text{Total Discharge} = L
$$



#### Step 6: Carbon Impact with Marginal Emissions

We have a separate DataFrame of marginal emissions rates, MERt\text{MER}\_t, for each hour. We merge these rates onto each SAR record:

$$
scr_mer=MER(scr_local_time)\text{scr\_mer} = \text{MER}_{(\text{scr\_local\_time})}
$$

$$sdr_mer=MER(sdr_local_time)\text{sdr\_mer} = \text{MER}_{(\text{sdr\_local\_time})}$$

slr\_mer=MER(slr\_local\_time)\text{slr\\\_mer} = \text{MER}\_{(\text{slr\\\_local\\\_time})}

Then compute the impacts:

scr\_impact=scr\_mwh×scr\_mer,\text{scr\\\_impact} = \text{scr\\\_mwh} \times \text{scr\\\_mer}, sdr\_impact=sdr\_mwh×sdr\_mer,\text{sdr\\\_impact} = \text{sdr\\\_mwh} \times \text{sdr\\\_mer}, slr\_impact=slr\_mwh×slr\_mer.\text{slr\\\_impact} = \text{slr\\\_mwh} \times \text{slr\\\_mer}.

To avoid double-counting, we exclude SLR from the net calculation, since the entire charge is already accounted for in scr\_impact\text{scr\\\_impact}. The final net impact:

net\_impact=sdr\_impact−scr\_impact.\text{net\\\_impact} = \text{sdr\\\_impact} - \text{scr\\\_impact}.

An SAR with net\_impact>0\text{net\\\_impact} > 0 is net-abating (it reduced overall emissions), while net\_impact<0\text{net\\\_impact} < 0 is net-emissive.

### Equations Summary

* **Total Charge:** ∑(SCR)\sum (\text{SCR})
* **Total Discharge:** ∑(SDR)\sum (\text{SDR})
* **Efficiency:** η=∑SDR∑SCR\eta = \frac{\sum \text{SDR\}}{\sum \text{SCR\}}
* **Losses:** L=∑(SCR)−∑(SDR)L = \sum (\text{SCR}) - \sum (\text{SDR})
* **FIFO SLR for each chunk DD:** (Dη)−D\left( \frac{D}{\eta} \right) - D
* **Impacts:** scr\_impact=scr\_mwh×scr\_mer\text{scr\\\_impact} = \text{scr\\\_mwh} \times \text{scr\\\_mer} sdr\_impact=sdr\_mwh×sdr\_mer\text{sdr\\\_impact} = \text{sdr\\\_mwh} \times \text{sdr\\\_mer} slr\_impact=slr\_mwh×slr\_mer\text{slr\\\_impact} = \text{slr\\\_mwh} \times \text{slr\\\_mer}
* **Net Impact:** net\_impact=sdr\_impact−scr\_impact\text{net\\\_impact} = \text{sdr\\\_impact} - \text{scr\\\_impact}

### Conclusion

This methodology enables traceable time-shifting of GCs with a clear chain-of-custody from charge to discharge, quantifies losses at the charging hour, and calculates net carbon impact using marginal emissions. Potential GC holders can purchase specific SARs to shift their certificates in time and still claim a net carbon effect that can be either abating (positive) or emissive (negative).
