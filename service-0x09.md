# Service 0x09

## Commands

- 1 - queryOtaAllow
- 2 - queryOtaAllowHandle
- 3 - 
- 4 - 
- 6 - parserPackageVerifyReport
- 9 - transfer file
- 10 - 
- 11 - checkDeviceReadyForUpdate
- 13 - sendUpdateChange
- 14 - sendUpdateMessage
- 15 - sendDeviceRequestCheckAnswer
- 16 - answerDeviceRequestStatus/answerDeviceRequestDownloadOta
- 17 - answerUserIsAgreeDownload
- 18 - sendOtaDownloadPercent
- 19 - queryDeviceTransmitMode
- 20 - sendChangelogToDevice
- 21 - queryChangelogFromDevice

## State graph 

```mermaid
sequenceDiagram
    loop until download
        Phone->>Watch: 0x12 - update progress
    end
    Phone ->>+ Watch: 0x12 - query transfer mode
    Watch ->>- Phone: 0x12 - response
    Phone ->>+ Watch: 0x01 - query update ota
    Watch->>-Phone: 0x01 - update status
    Phone->>+Watch: 0x02 - query communication options
    Watch->>-Phone: 0x02 - get options

    Phone->>+Watch: 0x09 
    loop sending parts
        Watch->>-Phone: 0x03 - ack
        alt ifAck
            Phone->>Watch: 0x03
        end
        loop sending
            Phone->>Watch: 0x04
        end
    end
    Watch->>+Phone: 0x06
    Phone->>-Watch: 0x06

```



0x126d - first file send  (contains OTA File Size)
AFter first part is sent         Watch->>Phone: 0x05

20 block in first segment
- fist
0x126d
        0x2a0f - once 
        0x1280 once
0x2c0f - mostly

