---
name: 'BPN adoption as GOLD_ID '
about: investigate and document all requested changes to adapt BPN as new GOLD_ID
title: ''
labels: ''
assignees: ''

---

**Actually**: 
The current MDM API receive the column TOM ID which corresponding to a 14 digit UPC, based on that UPC the MDM interface process apply a conversion procedure to obtain a GOLD ID. 

The get the GOLD ID, the conversion process remove the left-leading zeros and the last right check digit from the UPC code.

**New process**:
The new MDM API will receive the new TOM ID which will be the BPN code instead of the 14 digits UPC code. Then the MDM interface will assign the new TOM ID as GOLD ID without any conversion.

**Changes to considered**
PKG_RESERVED_INVENTORY: Reserve inventory Process required for CGO calculation
PKG_DEMAND_HISTORY: Process to insert the sales history required for CGO calculation
PKG_MOVEMENTS_API: Interfaces about Reception, Adjustments, shipments and closing  Purchase orders
PKG_INVENTORY: API used in the snapshot alignment
