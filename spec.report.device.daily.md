# Get Report (สรุปรายคัน)

## Request Header (alway pass : token)

# getReportDeviceDaily

## url
    http://{server}/api/report/getReportDeviceDaily

## request body (หากต้องการดึงข้อมูลรถทุกคันให้ส่ง devices:[])
```json
{
    "devices": [
        {"device_id":18681},
        {"device_id":18698},
        {"device_id":18662}
    ],
    "start_date": "14-11-2018",
    "end_date": "02-01-2019"
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "device_id": 18808,
            "device_no": "Mirage 1กว-7666", //  ทะเบียนรถ
            "details": [
                {
                    "speed_over_elapse": 0,   // ระยะเวลากระทำความผิดขับเร็วเกินกฎหมายกำหนด (วินาที)
                    "speed_over_times": 0,    // จำนวนครั้งที่ขับรถเร็วเกินกฏหมายกำหนด (ครั้ง)
                    "max_speed": 0,       //  ความเร็วสูสดสุด (km/h)
                    "violate_law": 0,   // จำนวนครั้งที่กระทำความผิดขับรถต่อเนื่องนานรเกินที่กำหนด (ครั้ง)
                    "vilate_license": 0,    // จำนวนครั้งกระทำความผิดไม่แสนดงตัวคนขับ (ครั้ง)
                    "date": "1 พ.ค. 62"   // วันเดือนปี
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "2 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "3 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "4 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "5 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "6 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "7 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "8 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "9 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "10 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "11 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 324,
                    "speed_over_times": 2,
                    "max_speed": 128,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "12 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 1648,
                    "speed_over_times": 11,
                    "max_speed": 152,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "13 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "14 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "15 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 126,
                    "speed_over_times": 0,
                    "max_speed": 128,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "16 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "17 พ.ค. 62"
                },
                {
                    "speed_over_elapse": 0,
                    "speed_over_times": 0,
                    "max_speed": 0,
                    "violate_law": 0,
                    "vilate_license": 0,
                    "date": "18 พ.ค. 62"
                }
            ],
            "summary": {
                "speed_over_elapse": 2098,
                "speed_over_times": 13,
                "max_speed": 152,
                "violate_law": 0,
                "vilate_license": 0
            }
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```