# Get Overall Summary

## Request Header (alway pass : token)

# deviceOverallSummary

## url
    http://{server}/api/report/deviceOverallSummary/{type}/{pageNo}/{pageSize}

type : (
    DLT - รายละเอียดรถที่ส่งสัญญานปัจจุบันและมีการเชื่อมต่อขนส่ง
    PAYMENT - รายละเอียดรถครบกำหนดชำระ
    ONLINE - รายละเอียดรถที่ส่งสัญญานปัจจุบัน
    OFFLINE - รายละเอียดรถไม่ส่งสัญญานเกิน 7 วัน
)
    
## request body

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "summary": {
                "offline": 1,
                "online": 1,
                "online_dlt": 0,
                "due_payment": 1
            },
            "details": [
                {
                    "device_no": "ID5test",
                    "device_id": 18698,
                    "install_date": "18 ธ.ค. 2561",
                    "expire_date": "21 ธ.ค. 2561",
                    "is_send_dlt": true,
                    "dealer": "simple corporation",
                    "sub_dealer": "fasttest",
                    "customer": "Wutthin",
                    "last_status": "เสา",
                    "last_track": "18 ธ.ค. 2561 14:08"
                }
            ]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```