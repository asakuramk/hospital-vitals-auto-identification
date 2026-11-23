# Phase 1: four-bed room positioning proof of concept

## Scope
Use one simulated four-bed room, one BLE transmitter or compatible monitor and up to four ESP32 receivers. No real patient identifiers or EHR writes.

## Capture
For each radio observation log timestamp, receiver ID, device ID if observable, RSSI and test ground-truth bed. Record transmitter orientation, curtain state and human movement.

## Tests
- Each of four beds: repeated stationary and measurement-position trials.
- Movement between beds, hallway, doorway and adjacent room.
- Curtains open/closed; monitor held/placed at different orientations.
- Multiple BLE devices and interrupted network connectivity.

## Metrics
Report confusion matrix per bed, false positive bedside assignment rate, unresolved rate, time-to-location, and packet loss. Include confidence thresholds and explicit abstention for ambiguous signals. Do not set a clinical acceptance threshold before hospital safety review.

## Decision gates
1. Verify device BLE compatibility.
2. Validate room-level location and then bed-level location; if unreliable, evaluate alternative positioning or bedside confirmation.
3. Separately validate patient ID matching against authoritative assignments.
4. Add measurement capture after positioning assessment.
5. Evaluate EHR integration only after clinical safety and security validation.
