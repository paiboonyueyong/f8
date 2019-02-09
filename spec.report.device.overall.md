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
    LICENSE - รายละเอียดรถป้ายแดง
    ALL - รายละเอียดรถทุกคัน
    RFID - กล่องที่ติดพร้อมเครื่องรูดบัตรแต่ยังไม่มีการรูดขึ้นมาจากเครื่อง  !!! New (2019-01-08)
)
    
## request body

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "summary": {
                "total": 8,
                "offline": 1,
                "online": 7,
                "online_dlt": 0,
                "due_payment": 1,
                "update_license": 7,
                "rfid_check": 0         // !!! New (2019-01-08)
            },
            "details": [
                {
                    "device_no": "ID5test",
                    "device_id": 18698,
                    "install_date": "18 ธ.ค. 61",
                    "expire_date": "21 ธ.ค. 61",
                    "is_send_dlt": true,
                    "is_update_change_detail": true,
                    "dealer": "simple corporation",
                    "sub_dealer": "fasttest",
                    "customer": "Wutthin",
                    "moving": "3:31",
                    "stop_machine_on": "17:33",
                    "machine_off": "00:00",
                    "speed_over": "00:00"
                },
                {
                    "device_no": "1กย-1287",
                    "device_id": 18662,
                    "install_date": "29 ส.ค. 61",
                    "expire_date": "30 ส.ค. 62",
                    "is_send_dlt": false,
                    "is_update_change_detail": true,
                    "dealer": "",
                    "sub_dealer": "",
                    "customer": "Wutthin",
                    "moving": "00:00",
                    "stop_machine_on": "9:57",
                    "machine_off": "11:10",
                    "speed_over": "00:00"
                },
                {
                    "device_no": "T333/30s",
                    "device_id": 18681,
                    "install_date": "2 ธ.ค. 61",
                    "expire_date": "30 ก.ย. 61",
                    "is_send_dlt": false,
                    "is_update_change_detail": false,
                    "dealer": "",
                    "sub_dealer": "",
                    "customer": "chinchin",
                    "moving": "00:00",
                    "stop_machine_on": "00:00",
                    "machine_off": "00:00",
                    "speed_over": "00:00",
                    "machine_on": "00:00"
                },
                {
                    "device_no": "18703",
                    "device_id": 18703,
                    "install_date": "",
                    "expire_date": "",
                    "is_send_dlt": false,
                    "is_update_change_detail": true,
                    "dealer": "ชิณภัทร",
                    "sub_dealer": "",
                    "customer": "chinchin",
                    "moving": "00:00",
                    "stop_machine_on": "00:00",
                    "machine_off": "00:00",
                    "speed_over": "00:00",
                    "machine_on": "00:00"
                }
            ]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 7
}
```

# Tracking Status Summary

## url
    http://{server}/api/report/getTrackingStatusSummary

* หมายเหตุ
    speed_over = เร็ว
    moving = วิ่ง
    stop = จอด
    parking = ดับ
    gsm = เสา

## request body

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "speed_over": 0,
            "moving": 0,
            "stop": 1,
            "parking": 38,
            "gsm": 0
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
``` 
