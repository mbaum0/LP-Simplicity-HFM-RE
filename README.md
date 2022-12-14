# LP-Simplicity-HFM-RE
Reverse engineering the BLE protocol used by the Simplicity HFM Bed Frame


## Remote Keycodes

| Description | Data         |
| ----------- | -----------  |
| UBL Toggle  | 6E01 003C AB |
| Head Up     | 6E01 0024 93 |
| Head Down   | 6E01 0025 94 |
| Snore       | 6E01 0046 B5 |
| Dual Up     | 6E01 0029 98 |
| Flat        | 6E01 0031 A0 |
| Feet Up     | 6E01 0026 95 |
| Feet Down   | 6E01 0027 96 |
| Zero G      | 6E01 0045 B4 |
| Massage Head Up   | 6E01 004C BB |
| Massage Head Down | 6E01 004D BC |
| Massage Feet Up   | 6E01 004E BD |
| Massage Feet Down | 6E01 004F BE |
| Massage Wave Mode | 6E01 0039 A8 |
| Memory            | 6E01 002E 9D |
| Button Up         | 6E01 006E DD |


The "Button Up" message is sent any time a button is released. It is the same message for each button.

I found the remote codes by installing the bluetooth logging profile offered by Apple, and using there companion app PacketLogger on my Mac. Once these were linked, I use the L&P adjustable base app to sample different buttons. The ATT messages were picked up by PacketLogger.