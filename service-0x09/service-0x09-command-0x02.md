# Service 0x09 command 0x02

## Request 

No payload

## Result

* tag: 0x01 - len 2 (int) - app wait timeout
* tag: 0x02 - len 2 (int) - request timeout
* tag: 0x03 -  (len 2) - unit size
* tag: 0x04 - (len 2) - Interval
* tag: 0x05 - (len 1) - is Ack Enable == 1
* tag: 0x06 - (len 1) - is offset enable


Defaults:
* AppWaitTimeout: 30 (seconds)
* RequestTimeout: 180
* AckEnable: false
* Interval: 0
* OffsetEnable: false