---
title: WDI_TLV_CONNECT_BSS_ENTRY (dot11wificxtypes.hpp)
description: WDI_TLV_CONNECT_BSS_ENTRY is a WiFiCx TLV that contains a list of candidate connect BSS entries.
ms.date: 06/17/2021
keywords:
 - WDI_TLV_CONNECT_BSS_ENTRY Network Drivers Starting with Windows Vista
---

# WDI\_TLV\_CONNECT\_BSS\_ENTRY (dot11wificxtypes.hpp)

[!INCLUDE [WiFiCx topic note](../includes/wificx-version-warning.md)]


WDI\_TLV\_CONNECT\_BSS\_ENTRY is a TLV that contains a list of candidate connect BSS entries.

## TLV Type


0x34

## Length


The sum (in bytes) of the sizes of all contained TLVs.

## Values


| Type                                                                                        | Multiple TLV instances allowed | Optional | Description                                                                                                                                                   |
|---------------------------------------------------------------------------------------------|--------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WDI\_TLV\_BSSID**](wdi-tlv-bssid.md)                                                    |                                |          | The BSSID of the BSS.                                                                                                                                         |
| [**WDI\_TLV\_PROBE\_RESPONSE\_FRAME**](wdi-tlv-probe-response-frame.md)                    |                                | X        | The probe response frame. If no probe response has been received, this would be empty.                                                                        |
| [**WDI\_TLV\_BEACON\_FRAME**](wdi-tlv-beacon-frame.md)                                     |                                | X        | The beacon frame. If no beacon has been received, this would be empty.                                                                                        |
| [**WDI\_TLV\_BSS\_ENTRY\_SIGNAL\_INFO**](wdi-tlv-bss-entry-signal-info.md)                 |                                |          | The signal information for this BSS entry.                                                                                                                    |
| [**WDI\_TLV\_BSS\_ENTRY\_CHANNEL\_INFO**](wdi-tlv-bss-entry-channel-info.md)               |                                |          | The channel information for this BSS entry.                                                                                                                   |
| [**WDI\_TLV\_BSS\_ENTRY\_DEVICE\_CONTEXT**](wdi-tlv-bss-entry-device-context.md)           |                                | X        | The IHV provided context data about this peer.                                                                                                                |
| [**WDI\_TLV\_PMKID**](wdi-tlv-pmkid.md)                                                    |                                | X        | The 16 byte PMKID value for this BSS entry.                                                                                                                   |
| [**WDI\_TLV\_EXTRA\_ASSOCIATION\_REQUEST\_IES**](wdi-tlv-extra-association-request-ies.md) |                                | X        | The IE to be included in the (re)association request frame for this BSSID. If present, this should be included in addition to the common IE.                  |
| [**WDI\_TLV\_FT\_INITIAL\_ASSOC\_PARAMETERS**](wdi-tlv-ft-initial-assoc-parameters.md)     |                                | X        | The initial Mobility Domain association parameters.                                                                                                           |
| [**WDI\_TLV\_FT\_REASSOC\_PARAMETERS**](wdi-tlv-ft-reassoc-parameters.md)                  |                                | X        | The fast transition parameters (MDIE, R0KH-ID, PMKR0Name, SNonce). This is only present for Fast Transition (not during initial mobility domain association). |
| [**WDI\_TLV\_BSS\_SELECTION\_PARAMETERS**](wdi-tlv-bss-selection-parameters.md)            |                                | X        | [**WDI\_BSS\_SELECTION\_FLAGS**](/windows-hardware/drivers/ddi/dot11wificxtypes/ne-dot11wificxtypes-wdi_bss_selection_flags) that provide information used by the host for BSS selection.                               |

 

## Requirements

|Requirement|Value|
|--- |--- |
|Minimum supported client|Windows 11|
|Minimum supported server|Windows Server 2022|
|Header|dot11wificxtypes.hpp|

 

