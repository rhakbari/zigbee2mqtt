---
title: "Tuya TS0601 8-Gang Switch Control via MQTT"
description: "Integrate your Tuya TS0601 8-Gang Switch via Zigbee2MQTT with any smart home infrastructure without using the vendor's bridge or gateway."
addedAt: 2024-10-30T10:15:34
pageClass: device-page
---
<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Tuya TS0601 8-Way Switch

|     |     |
|-----|-----|
| Model | Melery_WLS098_zigbee_8_gang_switch  |
| Vendor  | [Tuya](/supported-devices/#v=Tuya)  |
| Description | 8-way switch |
| Exposes | switch, linkquality |
| Picture | ![Tuya TS0601 8-Way Switch](/images/devices/TS0601_TZE204_wktrysab_Tuya.png) |

<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->

## Notes
The Tuya TS0601 8-Way Switch provides control for up to eight individual switch channels. Each switch can be monitored and toggled independently, making it a versatile option for multi-point control in smart home setups. 

<!-- Notes END: Do not edit below this line -->

## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `onEvent`: Synchronizes the switch's internal clock with the Zigbee network.
* `configure`: Sends a "magic packet" to configure the device on initial setup.

## Exposes

### Switch (binary) for each endpoint
Each of the 8 switches (`l1` to `l8`) can be toggled independently.  
Each switch's status is represented as a binary value and can be found in the published state with properties:
- `state_l1`, `state_l2`, ..., `state_l8`

**Values**:  
- `true` - Switch ON  
- `false` - Switch OFF

It's not possible to read (`/get`) or write (`/set`) these values individually, but each switch can be toggled via the respective endpoint.

### Linkquality (numeric)
Signal quality indicator of the Zigbee connection for the device.

- **Range**: `0` (minimum) to `255` (maximum)
- **Unit**: `lqi`
