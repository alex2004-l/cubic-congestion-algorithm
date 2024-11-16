### Cubic TCP Algorithm Implementation
---

This repository contains the implementation of the ___CUBIC TCP congestion control algorithm in C++___.
The CUBIC TCP algorithm enhances network performance by employing a cubic growth function to adjust the congestion window size. This approach ensures stability and fairness across multiple network flows, even in challenging environments with high latency and bandwidth.

---
### Features
- Efficient congestion control using the CUBIC algorithm
- TCP-friendliness for compatibility with standard TCP flows
- Dynamic adjustment of congestion window based on network feedback
- Fair bandwidth distribution across multiple flows

---

### Implementation Details
1) Key Components
- CCSrc: Handles packet transmission, congestion window adjustments, and acknowledgment processing.
- CCSink: Manages packet reception, acknowledgment sending, and packet loss notifications.
2) Core Methods
- onAck(): Adjusts the congestion window size based on acknowledgments.
- packetLoss(): Handles packet loss events and updates the congestion window accordingly.
- cubicUpdate(): Updates the congestion window using the cubic function.
- cubicTcpFriendliness(): Ensures compatibility with standard TCP flows.
- sendPacket(): Sends packets within the constraints of the congestion window size.
- receivePacket(): Processes incoming packets and invokes appropriate response methods.

---

### Performance Metrics
`Throughput`
- The implementation maintains high throughput with minor fluctuations, effectively utilizing available bandwidth.

`Queue Size`
- The queue size stabilizes after initial peaks, reflecting the algorithm's ability to adapt to network congestion.

`Fairness`
- The congestion control mechanism ensures equal bandwidth distribution among multiple connections over time.

`Latency`
- After an initial peak, latency stabilizes, demonstrating efficient congestion handling and low delays.

---