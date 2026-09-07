# DSRC & C-V2X Comparison for Connected and Automated Vehicles in Different Traffic Scenarios

**Published:** March 2022
**Authors:** Yuanzhe Jin, Xiangguo Liu, Qi Zhu

## 1. Introduction
This research compares the two primary V2X communication protocols—DSRC and C-V2X—across three traffic scenarios: ramp merging, intersections, and platoon braking, simulated using Veins and Sumo.
- **DSRC (Dedicated Short Range Communications):** Uses the 5.9GHz band, does not rely on cellular infrastructure, and intentionally controls communication area via antenna directivity. It has strong stability and avoids single-point failures.
- **C-V2X:** Uses cellular networks, supports high-speed scenarios, and provides low-latency direct communication. It leverages semi-permanent scheduling performance.

## 2. Simulation Results and Scenarios
### 2.1 Ramp Merging
- **Setup:** A 24-degree merging ramp where vehicles merge into a straight road. Measured the "road time" required to pass.
- **Results:** At low traffic densities, both protocols perform similarly. At high vehicle densities, **C-V2X performs better** (lower road time) than DSRC.
- **Explanation:** C-V2X uses a lower Inter-Packet Gap (IPG), meaning more frequent communication. In high density, frequent communication allows vehicles to find the appropriate merging time quickly. DSRC has a larger IPG, causing vehicles to miss merging opportunities while waiting for communication.
- **Merge Angle Effect:** Increasing the merge angle increases the communication distance needed, which indirectly increases road time due to positive correlation.

### 2.2 Intersections
- **Setup:** Delay-tolerant intelligent junction management controlling CAVs passing without deadlocks.
- **Results:** At low vehicle densities, performance is similar. At high densities (> 250 cars/hour), **DSRC performs slightly better** than C-V2X.
- **Explanation:** DSRC maintains a longer communication range. Approaching an intersection from a longer distance allows the infrastructure to allocate passing time optimally with only one-time communication, making DSRC's longer maximum hearing range (MHR) advantageous.

### 2.3 Platoon Brake
- **Setup:** A 10 km straight road where a truck platoon must brake simultaneously. Measured Brake Time (B-Time) and Min Inter-vehicle Distance (MIVD).
- **Results:**
  - **Brake Time:** **C-V2X performs better** (shorter brake time). The gap widens as vehicle density increases.
  - **MIVD:** C-V2X maintains a stable minimum distance regardless of vehicle density. DSRC's MIVD drops sharply as vehicle density increases, meaning vehicles get dangerously close.
- **Explanation:** Platoon braking requires vehicles to send messages sequentially. The shorter communication interval (IPG) of C-V2X ensures faster propagation of the braking signal down the platoon, whereas DSRC's delay causes following vehicles to brake late.

## 3. Conclusion
There is a fundamental trade-off between **Maximum Hearing Range (MHR)** and **Inter-Packet Gap (IPG)**.
- **C-V2X:** Tends to have more frequent communication (lower IPG), which excels in dynamic situations requiring rapid updates like Ramp Merging and Platoon Braking.
- **DSRC:** Tends to maintain a greater Maximum Hearing Range, which is highly beneficial in structured scenarios like Intersections where early notification is key.
- Future CAV systems should ideally utilize machine learning to dynamically choose their communication protocol based on the surrounding traffic scenario.
