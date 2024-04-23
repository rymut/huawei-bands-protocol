# Service 0x09 command 0x06

Device initialize communication by sending response to GB and then request is pushed to device.
Response is send after all OTA data is recieved by device 

## Request (response to device)

No payload (empty TLvs)

## Response (request from device)

- 0x01, len 0x01, value 0 or 1 - verify true false