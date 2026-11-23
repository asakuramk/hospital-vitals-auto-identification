# Hospital investigation questionnaire

## Electronic information board
- Manufacturer, product, model, management software and vendor?
- Who updates it, using which terminal, and how frequently?
- Are names typed manually or selected from a patient list?
- Does the system store patient IDs, room IDs and bed IDs?
- Is it connected to the EHR or bed-management system?
- Is authorized read-only API, HL7, CSV or database export supported?
- Are update timestamps and change history available?
- How are transfers, discharges and stale entries handled?

## Physical environment
- Room layout, bed spacing, metal obstacles and curtains?
- Existing bed numbers and stable identifiers?
- Power outlets and network availability for fixed receivers?
- Security and infection-control restrictions on installation?

## Blood-pressure monitor
- Manufacturer, model, firmware and BLE specification?
- Does it advertise while idle and during measurement?
- Is there a documented BLE GATT service or approved SDK for measurements?
- Can one device be shared safely across patients?

## Identity and governance
- What independent bedside confirmation is currently required?
- What patient identifiers may be used and who authorizes access?
- What retention, access control, encryption and audit requirements apply?
