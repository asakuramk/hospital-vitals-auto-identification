# System architecture

Goal: identify the bedside location of a shared wireless blood-pressure monitor with no additional device carried by nurses. EHR integration is deferred.

## Data flow
1. Compatible BLE blood-pressure monitor emits discoverable radio signals and, if supported, measurement records.
2. Fixed ESP32 receivers collect receiver ID, timestamp, device identifier (where available), and RSSI.
3. An on-premises server estimates room/bed proximity and records confidence.
4. A separately validated room/bed/patient assignment source supplies candidate patient IDs.
5. Identity confirmation and clinical safety checks precede any patient-specific record or EHR submission.

## Limitations
- RSSI is not reliable proof of an exact bed, especially with curtains, metal furniture and people moving.
- Some monitors do not advertise continuously; BLE connections or encryption may limit access.
- A board manually updated by nurses may be stale and may contain names without patient IDs.
- Bed assignment is not proof that the person measured is the assigned patient.
- No patient data should be sent to public GitHub. Use fictional data in development.
