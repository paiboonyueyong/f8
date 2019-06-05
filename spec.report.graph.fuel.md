# Generate graph fuel & speed

## Request Header (alway pass : token)

# getFuelGraphByDevice

## url
    http://{server}/api/report/getFuelGraphByDevice

* หมายเหตุ
    ช่วงเวลา < 3 วัน คำนวน average 5 นาที
    ช่วงเวลา => 3 วัน คำนวน average 1 ชั่วโมง
    ช่วงเวลา => 30 วัน  คำนวน average 1 วัน
    
## request body
```json
{
    "devices": [
        {"device_id":18681}
    ],
    "start_date": "04-02-2019 00:00",
    "end_date": "06-02-2019 23:00"
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "speed": 7,
            "fuel": 40,
            "date": "09-02-2019",
            "time": "18:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 97,
            "date": "09-02-2019",
            "time": "19:00",
            "speed_limit": 300
        },
        {
            "speed": 16,
            "fuel": 73,
            "date": "09-02-2019",
            "time": "20:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "09-02-2019",
            "time": "21:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "09-02-2019",
            "time": "22:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "09-02-2019",
            "time": "23:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "00:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "01:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "02:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "03:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "04:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "05:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "06:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "07:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "08:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "09:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "10:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "11:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "12:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "13:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "14:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "15:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "16:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "17:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "18:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "19:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "20:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "fuel": 100,
            "date": "10-02-2019",
            "time": "21:00",
            "speed_limit": 300
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 28
}
```