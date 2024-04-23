# Service 0x09 command 0x01 - configure OTA

## Request

Tag: 0x01, value: STR  - NEW_VERSION
Tag: 0x02, value: SHORT (len 2 ) - 256?
Tag: 0x03, value: BYTE (len 1) - 2?

NEW_VERSION- "3.1.0.122(C00M03)" - must match contents of the file in offset 0x4C

## Response

Tag: 0x04, Value: number (len ??) - BATTERY_TRESHOLD
Tag: 127, Value: error code (len 4) - ERROR_CODE

if BATTERY_TRESHOLD <= -1:

else if BATTERY_TRESHOLD < 20

else E


