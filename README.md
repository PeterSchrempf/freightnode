# FreightNode Systems: FN-Core Architecture & Fleet API

> **DRIVERLESS FREIGHT. ZERO EMISSIONS. ZERO COMPROMISE.**

Welcome to the engineering documentation for **[FreightNode Systems](https://freightno.de/)**. 
We build autonomous urban freight pods engineered for scale. No drivers. No fuel. No downtime. FreightNode provides the raw infrastructure layer that moves goods through cities around the clock.

🌐 **System Access:** (https://freightno.de/)

---

## ⚙️ FN-Core Transport Pod Specifications

The FN-Core is an autonomous urban freight vehicle engineered for continuous, scalable operation. It is deployed as white-label logistics infrastructure for carriers and municipal networks.

* **Perception Stack:** Roof-mounted spinning LiDAR, solid-state corner units, radar & camera fusion (360° coverage)
* **Compute:** Redundant on-board inference, dual-rail fail-operational architecture (512 TOPS)
* **Duty Cycle:** 24/7 Continuous autonomous operation (no shift limits)
* **Charging:** 11kW wireless inductive pads (depots and curbside nodes)
* **Payload:** 650 kg sealed cargo volume, modular roll-cage compatible
* **Powertrain:** Dual-motor electric drive, zero tailpipe output

---

## 💻 Fleet Integration API

FreightNode does not compete with operators; we arm them. The following endpoints allow authorized carriers to integrate FN-Core nodes directly into their logistics backend.

*Note: All endpoints require mTLS authentication and an active fleet-lease contract.*

### Initialize Node Dispatch
Deploys an available FN-Core pod to a loading zone.
`POST /api/v1/nodes/dispatch`
```json
{
  "node_id": "FNC-9942",
  "target_coords": [50.1109, 8.6821],
  "payload_config": "standard_rollcage"
}
