# Service 0x09 command 0x0E

## Request 

0x03, len 4, unix time (when request was made) 
0x04, len 1 - probably network status
    - 1 - ??
    - 2 - maybe ok?
    - 3 - maybe disconnected?
if value of tag 0x04 is == 1
    0x01, STR - version of software
    0x02, len 8, - band byte size as long

0x05, len 1, possible values 0 or 2
    - 0 - ??
    - 2 - ??
0x06, 0x01, ??? (not required )

## Response

first tag int value 

0x7F, ERROR_CODE (success if OK)

