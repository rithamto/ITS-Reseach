# 5G NR-V2X: Towards Connected and Cooperative Autonomous Driving

**Published:** 2021
**Authors:** Hamidreza Bagheri, Md Noor-A-Rahim, Zilong Liu, Haeyoung Lee, Dirk Pesch, Klaus Moessner, and Pei Xiao

## 1. Introduction and 3GPP Roadmap
The 5G New Radio (NR) aims to provide ultra-high reliability, low-latency, high throughput, and flexible mobility for connected autonomous driving. 3GPP defined V2X across different releases:
- **LTE-V2X (Release 14/15):** Basic safety services (CAM, BSM).
- **NR-V2X (Release 16+):** Enhanced URLLC, higher throughput, advanced services like vehicle platooning, advanced driver assistance, and remote driving.

## 2. Key Features of 5G New Radio (NR)
### 2.1 The 5G NR Physical Layer (PHY) Design
- **Subcarrier Spacing:** Supports 15, 30, 60, 120, and 240 kHz (compared to fixed 15 kHz in LTE). Larger spacing suppresses Inter-Carrier Interference (ICI) in high mobility.
- **Channel Coding:** Uses LDPC for user data and Polar codes for control channels (replacing Turbo/convolutional codes in LTE) to achieve ultra-low decoding latency.
- **Network Slicing:** Dynamically allocates time and frequency resources for tailored data services.

### 2.2 NR Sidelink Features and Resource Allocation
- **PSFCH (Physical Sidelink Feedback Channel):** Introduces feedback-based re-transmission, replacing blind re-transmission in LTE, drastically improving efficiency.
- **Modulation & Carrier Aggregation:** Supports up to 256-QAM and up to 16 carriers.
- **Sidelink Modes:** Mode-1 (cellular coverage base station scheduling) and Mode-2 (distributed autonomous scheduling without cellular coverage, including sensing-based semi-persistent transmission).

### 2.3 Architecture, Security, and Positioning
- **Dual Connectivity:** Non-standalone (NSA) leveraging 4G, and Standalone (SA) with a cloud-native 5G core.
- **Security:** Introduces SEAF (Security Anchor Function) and encrypts the Subscriber Permanent Identifier (SUPI) to protect against spoofing and tracking.
- **Precise Positioning:** Combines LTE techniques with Multi-RTT, UL-AoA, DL-AoD, and TOA triangulation for 0.1m accuracy, compared to >1m in LTE-V2X.

## 3. Application of Machine Learning for NR-V2X
Machine Learning (ML) can address operational challenges in highly dynamic vehicular environments:
- **PHY Layer:** ML aids in learning synchronization points, estimating highly volatile channels (CSI), and beam tracking. It can optimize adaptive coding and modulation (ACM).
- **Radio Resource Management (RRM):** Decentralized, multi-agent reinforcement learning (RL) allows vehicles to learn optimal resource allocation without huge overhead from centralized controllers.
- **Vehicle Trajectory Prediction:** ML models use historical data to predict future locations, assisting handoff control and routing.
- **Challenges:** Robustness in safety-sensitive tasks, and limited on-board computational resources requiring model reduction/compression.

## 4. 5G NR-V2X Use Cases
- **Trajectory Sharing and Coordinated Driving:** Exchanging intention and sensor data for predictable autonomous maneuvers.
- **Vehicle Platooning:** Traveling together at short inter-vehicle distances, relying on periodic data from the leading vehicle.
- **Extended Sensors Sharing:** Exchanging raw/processed sensor data or live video to see beyond a vehicle's own line-of-sight.
- **Remote Driving:** Teleoperated control of vehicles for incapacitated persons or dangerous environments. These require < 5 ms latency and > 99.999% reliability, achievable only with NR-V2X.
