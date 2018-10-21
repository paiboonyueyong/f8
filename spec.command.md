# Command Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# newCommand

## url
    http://{server}/newCommand

## request body
```json
{
  "command_name": "ดับเครื่อง"
}
```
## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# updateCommand

## url
    http://{server}/updateCommand/{command_id} 

## request body
```json
{
  "command_name": "ดับเครื่อง"
}
```
## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# deleteCommand

## url
    http://{server}/deleteCommand/{command_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getCommandInfo

## url
    http://{server}/getCommandInfo/{command_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
            {
                "command_id": 3,
                "command_name": "ดับเครื่อง",
                "create_user": "Wutthin",
                "last_upd_user": "Wutthin",
                "create_dtm": "2018-09-30T15:43:33.288Z",
                "last_upd_dtm": "2018-09-30T16:21:38.602Z"
            }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getCommandList

## url
    http://{server}/getCommandList 

## request body
```json
{
  "filter": "ดับเครื่อง"
}
```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "command_id": 0,
            "command_name": "-- ไม่มี --"
        },
        {
            "command_id": 1,
            "command_name": "ถ่ายรูปกล้อง1 (จีน)"
        },
        {
            "command_id": 2,
            "command_name": "ถ่ายรูปกล้อง2 (จีน)"
        },
        {
            "command_id": 3,
            "command_name": "time zone setting (ID5 + จีน)"
        },
        {
            "command_id": 4,
            "command_name": "ดับเครื่อง (1) (จีน)"
        },
        {
            "command_id": 5,
            "command_name": "ยกเลิกดับเครื่อง(1) (จีน)"
        },
        {
            "command_id": 6,
            "command_name": "ดับเครื่อง(2) (จีน)"
        },
        {
            "command_id": 7,
            "command_name": "ยกเลิกดับเครื่อง(2) (จีน)"
        },
        {
            "command_id": 14,
            "command_name": "ย้ายไป server2 ธรรมดา"
        },
        {
            "command_id": 15,
            "command_name": "toyota เครื่องจีน ย้ายไปport 8400 server2"
        },
        {
            "command_id": 16,
            "command_name": "set even flag"
        },
        {
            "command_id": 17,
            "command_name": "set authorized no. (จีน)"
        },
        {
            "command_id": 18,
            "command_name": "add sms even flag"
        },
        {
            "command_id": 19,
            "command_name": "delete sms even flag"
        },
        {
            "command_id": 20,
            "command_name": "toyota เครื่องID5 ย้ายไป port 8300 server2"
        },
        {
            "command_id": 21,
            "command_name": "เครื่องFM เปลี่ยน DTAC"
        },
        {
            "command_id": 22,
            "command_name": "เครื่องจีนใช้ dtac server 2"
        },
        {
            "command_id": 23,
            "command_name": "ยกเลิกเสียงรบกวน (2) ไม่ใช้งาน"
        },
        {
            "command_id": 30,
            "command_name": "Sleep Mode (จีน)"
        },
        {
            "command_id": 31,
            "command_name": "reboot GPS (จีน)"
        },
        {
            "command_id": 32,
            "command_name": "reboot GSM (ID5 + จีน)"
        },
        {
            "command_id": 33,
            "command_name": "IMEI and serial (ID5 + จีน)"
        },
        {
            "command_id": 34,
            "command_name": "Time interval (จีน)"
        },
        {
            "command_id": 37,
            "command_name": "distance interval"
        },
        {
            "command_id": 38,
            "command_name": "heading change (ID5 + จีน)"
        },
        {
            "command_id": 39,
            "command_name": "even flag GPRS + distance interval"
        },
        {
            "command_id": 40,
            "command_name": "ลบข้อมูลเก่า (จีน)"
        },
        {
            "command_id": 41,
            "command_name": "ดับเครื่อง 1 (FM1100)"
        },
        {
            "command_id": 42,
            "command_name": "ยกเลิกดับเครื่อง 1 (FM1100)"
        },
        {
            "command_id": 43,
            "command_name": "ดับเครื่อง 2 (FM1100)"
        },
        {
            "command_id": 44,
            "command_name": "ยกเลิกดับเครื่อง 2 (FM1100)"
        },
        {
            "command_id": 47,
            "command_name": "sleep mode (FM1100)"
        },
        {
            "command_id": 48,
            "command_name": "reboot (FM1100)"
        },
        {
            "command_id": 49,
            "command_name": "เปิดการทำงานเสียงรบกวน (FM1100)"
        },
        {
            "command_id": 50,
            "command_name": "ตั้งความเร็วเสียงรบกวน (FM1100)"
        },
        {
            "command_id": 51,
            "command_name": "ลบข้อมูลในmem (FM1100)"
        },
        {
            "command_id": 52,
            "command_name": "ตั้งความเร็วเสียงรบกวน (ID5 + จีน)"
        },
        {
            "command_id": 53,
            "command_name": "ย้ายไป server1 ธรรมดา"
        },
        {
            "command_id": 54,
            "command_name": "ย้ายไป server1 รูดบัตร"
        },
        {
            "command_id": 71,
            "command_name": "เปลี่ยน input สวิสต์กุญแจ (ID5)"
        },
        {
            "command_id": 72,
            "command_name": "ดูเลข IMEI บน simcard (ID5)"
        },
        {
            "command_id": 73,
            "command_name": "ถ่ายรูปกล้อง1 (ID5)"
        },
        {
            "command_id": 74,
            "command_name": "ถ่ายรูปกล้อง2 (ID5)"
        },
        {
            "command_id": 75,
            "command_name": "เปิดทำงานกล้อง1 ID5"
        },
        {
            "command_id": 76,
            "command_name": "Time interval (ID5)"
        },
        {
            "command_id": 77,
            "command_name": "ดูรุ่น firmware (ID5)"
        },
        {
            "command_id": 78,
            "command_name": "ยกเลิกดับเครื่อง 1 (ID5)"
        },
        {
            "command_id": 79,
            "command_name": "ดับเครื่อง 1 (ID5)"
        },
        {
            "command_id": 80,
            "command_name": "ยกเลิกดับเครื่อง 2 (ID5)"
        },
        {
            "command_id": 81,
            "command_name": "ดับเครื่อง 2 (ID5)"
        },
        {
            "command_id": 82,
            "command_name": "set autohrize no. (T333)"
        },
        {
            "command_id": 83,
            "command_name": "ตั้งแจ้งเตือน sms (T333)"
        },
        {
            "command_id": 86,
            "command_name": "เปลี่ยน # no. (T333)"
        },
        {
            "command_id": 85,
            "command_name": "เปิดการทำงานเครื่องรูดบัตร (ID5)"
        },
        {
            "command_id": 87,
            "command_name": "ปิดการทำงาน กล้อง+เครื่องรูด (ID5)"
        },
        {
            "command_id": 87,
            "command_name": "ย้ายไป port 8801 server2"
        },
        {
            "command_id": 89,
            "command_name": "เพิ่ม license type บัตรของ T330"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 57
}
```
