# Cooperative Adaptive Cruise Control (CACC) For Partially Automated Truck Platooning

**Published:** March 2018
**Authors:** Steven E. Shladover, Xiao-Yun Lu, Shiyan Yang, Hani Ramezani, John Spring, Christopher Nowakowski, David Nelson, Deborah Thompson, Aravind Kailas, Brian McAuliffe

## 1. Project Overview & Motivation
Cooperative Adaptive Cruise Control (CACC) is an intermediate step toward automated truck platooning on freight corridors. Unlike full automated platooning, CACC only automates truck speed control using V2V communication and forward sensors; drivers remain responsible for steering and lane keeping. CACC relies on a Constant-Time Gap (CTG) control strategy rather than a Constant Distance Gap (CDG). The project implemented CACC on three Volvo Class-8 truck tractors to evaluate control system performance, fuel economy, driver acceptance, and traffic impacts.

## 2. CACC System Design
- **Implementation:** The system was an enhancement to Volvo's European production Adaptive Cruise Control (ACC) system. It included a PC-104 computer, DSRC transceivers, a supplementary touchscreen Driver-Vehicle Interface (DVI), and a 5 Hz GPS.
- **Time Gaps:** The system provided five gap settings. For CACC, the time gaps ranged from 0.6 s to 1.8 s. For ACC, the gaps ranged from 1.1 s to 1.9 s.

## 3. Vehicle Following Control Performance
- **Cut-in and Cut-out:** The system successfully responded to confederate vehicles cutting in and out, safely increasing gaps when needed and catching up afterward.
- **Steady-State Tracking:** At a 0.6 s time gap (18 m distance at 65 mph), the maximum distance error was relatively small (around 1.19 m for the third truck). Disturbances were neither significantly amplified nor attenuated (string stability).
- **Speed Variations:** During acceleration/deceleration maneuvers, max distance tracking error was around 2.5 m, suggesting a safe minimum following distance of 10 m for highway maneuvers.

## 4. Fuel Consumption in Steady Cruising
Testing used a modified SAE J1321 procedure, testing different parameters (gap distances, standard vs. aerodynamic trailers, speeds, and loads):
- **Aerodynamic Trailer Treatments:** Individual trucks saw 6.3% to 7.6% fuel savings just from aerodynamic trailers.
- **Platoon Savings (Standard Trailer):** The lead truck saw negligible savings (0.5%). The middle truck saved 6-7.5%, and the trailing truck saved 9.5-11% at gaps of 44 m to 18 m.
- **Platoon Savings (Aerodynamic Trailer):** With aerodynamic trailers, the savings were even higher (mutually reinforcing). The middle truck saved 7-9.5%, and the trailing truck saved 10-12.5%.
- Overall, a three-truck platoon using CACC at time gaps between 0.6s and 1.5s saved a total of 5-6% of its fuel consumption when cruising at 65 mph.

## 5. Driver Acceptance and Gap Selection
- **On-Road Experiment:** 9 professional drivers tested the system on California freeways. 
- **Preferences:** Drivers generally preferred the intermediate gap settings (1.2 s and 1.5 s) because the shortest gaps obstructed their view, while the longest gaps encouraged cut-ins.
- **Actual Usage:** Drivers split into two groups. Group 1 preferred and used intermediate gaps (1.2 s and 1.8 s). Group 2 (more experienced) predominantly used the shortest gap (0.6 s) for over 60% of their CACC usage.

## 6. Overall Traffic and Energy Impacts
- **Microsimulation:** Evaluated the I-710 corridor from the Port of Long Beach to downtown Los Angeles using the MOVES model.
- **Traffic Congestion:** Assuming widespread CACC adoption, average truck speeds increased from 33.3 mph to 39.7 mph (19.3% increase). Passenger car speeds also improved due to relieved bottleneck congestion.
- **Energy Consumption:** Truck CACC reduced normalized fuel consumption for trucks by an average of 3.05%. Because urban speeds were only moderate, these savings came primarily from reduced speed variations (smoothing traffic) rather than aerodynamic drafting.

## 7. Conclusions
- A production ACC system can be modified into a high-performance CACC system affordably.
- Drivers are comfortable using CACC in mixed public traffic.
- Substantial fuel savings (up to 10-12% for trailing trucks) are achievable, especially when combined with aerodynamic trailer skirts and boat tails.
- Widespread use relieves urban freeway congestion and improves traffic flow.
