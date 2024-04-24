# Command 18 - sending progress report to watch

## Request

- Tag: 0x01, Value: ?? (len 1) - PERCENT_BYTE (0-100)
- Tag: 0x02, Value: ?? (len 1) - DOWNLOAD STATE 
- Tag: 0x03, Value: ?? (len 1) - DOWNLOAD MODE


PERCENT_BYTE - value between 0 and 100

DOWNLAD_STATE - value 0, 1 or 2
    - 0 - download start
    - 1 - download progress
    - 2 - download failed

DOWNLOAD_MODE - value 0 or 1 
    - 0 - auto download
    - 1 - manual download

AFTER setting 100% the data 