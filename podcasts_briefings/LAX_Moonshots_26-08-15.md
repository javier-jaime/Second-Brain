---

title: Energy & AI: Grid Bottlenecks, Frontier Solutions and Exponential Technologies  
date: 2026-08-15  
tags: Peter Diamandis, Salim Ismail, Dave Blundin, Alexander Wissner-Gross, Ramez Naam

---

## **Summary**

The rapid expansion of Artificial Intelligence has transitioned energy from a fringe clean tech sector into the primary bottleneck for global compute. While the cost of electricity remains low relative to the capital expenditure of chips, the physical infrastructure of the electrical grid, specifically transmission lines and interconnection queues, has become the central constraint. In the United States, wait times for connecting large scale loads now stretch toward 2031 and 2032\.

To circumvent this, the industry is pursuing three primary strategies: immediate grid flexibility through interruptible loads and batteries, behind the meter power generation using natural gas turbines, and the long term development of modular fission and fusion. Simultaneously, a transition toward off grid locations, including deserts, the ocean floor, and sun synchronous orbits, is being explored to accommodate the unbounded demand for intelligence.

## **The Grid as the Primary Bottleneck**

The current crisis in AI expansion is not driven by the cost of energy or the lack of power generation, but by the inability to move power to where it is needed.

### **Interconnection and Regulatory Delays**

The time required to hook up a new power project to the grid has increased from 15 months two decades ago to approximately 45 months today. For data centers requiring hundreds of megawatts, the situation is even more dire. In regions like Texas, governed by **ERCOT**, the queue for load interconnection is overwhelmed by requests exceeding 200 gigawatts.

### **The Power Demand Gap**

There is a significant discrepancy between the pace of chip manufacturing and the pace of grid expansion. Projections suggest that the power draw from chips produced by companies like **Nvidia**, **AMD**, and **Cerebras** will require roughly 230 gigawatts of capacity by 2030, while the United States grid buildout is only projected to reach 100 gigawatts in the same period. This has led to a situation where companies have acquired chips but lack the warm shells, or data center frames, to house and power them.

## **Flexibility and Behind the Meter Power**

In response to grid constraints, developers are adopting strategies to bypass traditional utility timelines.

### **Interruptible Loads and Time-Shifting**

New regulations, pioneered in Texas and encouraged by federal regulators, allow for a fast path to power for data centers that agree to be interruptible loads. By utilizing on site batteries to fill up during off peak hours (such as midnight) and drawing from that stored energy during peak afternoon demand, data centers can be connected in 12 to 18 months rather than five to seven years.

* **Gentic** is a startup leading the deployment of battery backed, load shifting data center sites.  
* **Emerald AI**, funded by **Nvidia**, uses software orchestration to move compute jobs to data centers with available capacity.  
* **WeaveGrid** manages electric vehicle charging to reduce stress on the last mile of the grid, a technology now being adapted for data centers.

### **Behind the Meter Generation**

Hyperscalers are increasingly building their own power plants on site. Natural gas turbines, once a commodity, now have backlogs stretching seven years.

* **GE** and **Hitachi** are expanding assembly lines for large turbines.  
* **Bloom Supersonic** has pivoted from aircraft engines to manufacturing natural gas turbines for data center power.  
* **Tesla** and other manufacturers are seeing increased demand for modular energy production that can be trucked to a site to get a data center operational before permanent infrastructure is built.

## **Exponential Declines in Solar and Storage**

Solar and battery technologies continue to follow [Wright](https://en.wikipedia.org/wiki/Theodore_Paul_Wright)'s Law, where every doubling of cumulative scale reduces costs by approximately 30%.

| Technology | Historical Cost Change | Future Outlook |
| :---- | :---- | :---- |
| Solar Panels | 1000x decline since 1975 | Could drop another 4x to 8x with further scale. |
| Lithium-Ion Batteries | 14x decline since 2010 | Dominant but limited by lithium availability. |
| Sodium-Ion Batteries | Emerging | Potential to drop battery costs by a factor of 10\. |

"New technologies like sodium ion batteries could drop the cost of batteries by a factor of 10."

Gigawatt scale solar and battery projects are already proving competitive with nuclear and fossil fuels. In the United Arab Emirates, a 1 gigawatt 24/7 solar project achieved costs roughly one third the price of the most recent United States nuclear plants.

## **The Nuclear Renaissance: Fission and SMRs**

Nuclear power is undergoing a shift from massive, unique construction projects toward repeatable manufacturing.

### **Small Modular Reactors (SMRs)**

The goal of SMRs is to move assembly from the construction site to the factory, where learning rates can drive down costs.

* **Valar Atomics** recently raised \$1 billion dollars for SMR development.  
* **Oklo** and **X-Energy** are developing designs that focus on modularity.  
* **Radiant Nuclear** is building microreactors small enough to fit in shipping containers.

### **Passive Safety**

Modern Gen 3+ and Gen 4 designs are designed to be passive safe, meaning they do not require active pumping of coolant to prevent a meltdown. This design choice addresses the primary failure mode seen in older plants like Fukushima.

## **The Frontier of Fusion**

Fusion technology has moved from academic research into a venture backed industry with over 50 startups. A critical regulatory milestone was achieved when the United States decided to regulate fusion like radiological imaging machines in hospitals rather than like fission reactors.

### **Leading Fusion Approaches**

1. **Magnetic Confinement (Tokamaks):** **Commonwealth Fusion Systems** is using new superconducting magnets to shrink the size of traditional donut shaped reactors.  
2. **Inertial Confinement (Lasers):** The National Ignition Facility reached a triple product above one, proving theoretical net energy gain.  
3. **Magneto Inertial Fusion:** **Helion** uses a rail gun approach to slam plasma together and capture energy directly as electricity, bypassing the need for steam turbines.

"The most aggressive timeline is **Helion**, they have a power purchase agreement from **Microsoft** to provide 50 megawatts of power in 2028."

## **Out-of-World Compute: Oceans and Space**

As land based constraints mount, the industry is looking to environments with infinite cooling and fewer regulatory hurdles.

### **Wave Powered Ocean Data Centers**

**Panthalassa** builds data centers shaped like lollipops that bob on ocean waves to generate power while utilizing the 40 degree Fahrenheit water for free cooling. This approach targets power costs as low as 2 cents per kilowatt-hour.

### **Space-Based Data Centers**

**SpaceX** aims to launch compute into orbit to bypass the terrestrial grid entirely. However, the scale required is immense. To launch 10 gigawatts of compute per year, **SpaceX** would need to conduct five or six **Starship** launches every day.

"10 gigawatts a year is like five or six launches of Starship a day, unless we hit that exponential absolutely full on and go right down that path this looks prohibitive for 15-20 years."

## **Conclusion**

While scaling compute is the current predictable path to higher intelligence, the ultimate unlock may be algorithmic efficiency. The human brain operates on approximately 20 watts of power, while current AI models require kilowatts for inference and hundreds of megawatts for training. Discovering new ways to manipulate information that mimic the efficiency of biological neural architectures remains the most significant, albeit unpredictable, variable in the relationship between AI and power.