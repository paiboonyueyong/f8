# User Device Alert Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# getDeviceAlertList

## url
    http://{server}/getDeviceAlertList/

## no request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "alert_type_id": "S1",
            "alert_type": "เครื่องยนต์ติด",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "S2",
            "alert_type": "เครื่องยนต์ดับ",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "O2",
            "alert_type": "ความเร็วเกิน",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "S3",
            "alert_type": "ดัมป์เปิด",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "S4",
            "alert_type": "ดัมป์ดับ",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "O1",
            "alert_type": "แจ้งเตือนเลื่อนรถ",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "E2",
            "alert_type": "แบตเตอรี่อ่อน",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "E3",
            "alert_type": "แบตเตอรี่รถอ่อน",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "E4",
            "alert_type": "ไม่ได้ไฟจากรถ",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "E6",
            "alert_type": "ไม่มีสัญญาณGPS",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "E7",
            "alert_type": "รับสัญญาณGPS",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "E5",
            "alert_type": "สายGPSถูกตัด",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "E1",
            "alert_type": "รูดบัตร",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "O3",
            "alert_type": "เข้า POI",
            "alert_method": "GUI"
        },
        {
            "alert_type_id": "O4",
            "alert_type": "ออกจาก POI",
            "alert_method": "GUI"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# setDeviceAlert

## url
    http://{server}/setDeviceAlert/

## request body

```json
[
    {
        "alert_type_id": "S1",
        "is_alert_type": true
    },
    {
        "alert_type_id": "S2",
        "is_alert_type": true
    },
    {
        "alert_type_id": "O2",
        "is_alert_type": true
    },
    {
        "alert_type_id": "S3",
        "is_alert_type": true
    },
    {
        "alert_type_id": "S4",
        "is_alert_type": true
    },
    {
        "alert_type_id": "O1",
        "is_alert_type": true
    },
    {
        "alert_type_id": "E2",
        "is_alert_type": true
    },
    {
        "alert_type_id": "E3",
        "is_alert_type": true
    },
    {
        "alert_type_id": "E4",
        "is_alert_type": true
    },
    {
        "alert_type_id": "E6",
        "is_alert_type": true
    },
    {
        "alert_type_id": "E7",
        "is_alert_type": true
    },
    {
        "alert_type_id": "E5",
        "is_alert_type": true
    },
    {
        "alert_type_id": "E1",
        "is_alert_type": true
    },
    {
        "alert_type_id": "O3",
        "is_alert_type": true
    },
    {
        "alert_type_id": "O4",
        "is_alert_type": true
    }
  ]

```

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```