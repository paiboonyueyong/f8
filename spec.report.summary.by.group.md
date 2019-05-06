# Get Report Summary By Group (สรุปการใช้งานตามกลุ่ม)

## Request Header (alway pass : token)

# getReportSummaryByGroup

## url
    http://{server}/api/report/getReportSummaryByGroup

## request body
```json
{ 
    "device_group":"",
    "start_date" : "11-11-2018",
    "end_date": "23-11-2018",
    "is_speed_over": false,
    "speed_over_interval": 0,
    "stop_interval": 10
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "device_group" : "",
            "details": [
                {
                    "imei": "861311007894107",
                    "device_id": 18698,
                    "device_no": "ID5test",
                    "driver_id": "",
                    "speed_limit": "140",
                    "install_date": "2018-12-17T17:00:00.000Z",
                    "expire_date": "2019-03-30T17:00:00.000Z",
                    "max_speed": 132,   // ความเร็วสูงสุดที่ใช้
                    "max_speed_dtm": "22-12-2018 09:10:02", // เวลาที่ขับเร็วสูงสุด
                    "max_speed_at_latitude": 100.990709,
                    "max_speed_at_longitude": 100.990709,
                    "symbol_id": "car-side",
                    "symbol_color": "#5DADE2",
                    "total_distance": "0.0 กม.",    // สรุประยะทางการวิ่ง
                    "stop_machine_on_duration": "25(วัน) 16:38:56",     // จอดติดเครื่องนานสุด
                    "working_duration": "33(วัน) 08:44:15", // เวลาใช้งานทั้งหมด
                    "machine_on_times": 1,  // เครื่องยนต์ติด
                    "speed_over_times": 0,  // จำนวนครั้งที่วิ่งเร็วเกิน
                    "stop_machine_on_over_x_mins_times": 220,   // จำนวนครั้งจอดเกิน 10 นาที
                    "stop_machine_on_max_duration": "25(วัน) 16:38:56", // เวลาที่จอดติดเครื่อง
                    "fuel_use": 0   // ปริมาณการใช้งานน้ำมัน
                },
                {
                    "imei": "864507032289828",
                    "device_id": 18681,
                    "device_no": "T333/30s",
                    "speed_limit": "140",
                    "driver_id": "",
                    "device_group": "wutthinan",
                    "expire_date": "2019-07-05T17:00:00.000Z",
                    "install_date": "2018-12-01T17:00:00.000Z",
                    "max_speed": 139,
                    "max_speed_dtm": "22-12-2018 09:10:00",
                    "max_speed_at_latitude": 100.991078,
                    "max_speed_at_longitude": 100.991078,
                    "symbol_id": "shuttle-van",
                    "symbol_color": "#9B59B6",
                    "total_distance": "3005.9 กม.",
                    "stop_machine_on_duration": "20(วัน) 02:46:27",
                    "working_duration": "26(วัน) 11:31:15",
                    "machine_on_times": 1,
                    "speed_over_times": 0,
                    "stop_machine_on_over_x_mins_times": 93,
                    "stop_machine_on_max_duration": "20(วัน) 02:46:27",
                    "fuel_use": 0
                }
            ],
            "summary": {
                "working_duration": "59(วัน) 20:15:30",
                "total_distance": "3005.9 กม.",
                "stop_machine_on_duration": "45(วัน) 19:25:23",
                "stop_machine_on_over_x_mins_times": null,
                "stop_machine_on_max_duration": "45(วัน) 19:25:23",
                "speed_over_times": 0,
                "machine_on_times": 2
            }
        },
        {
            "device_group" : "Group 1",
            "details": [
                {
                    "imei": "861311007894107",
                    "device_id": 18698,
                    "device_no": "ID5test",
                    "driver_id": "",
                    "speed_limit": "140",
                    "install_date": "2018-12-17T17:00:00.000Z",
                    "expire_date": "2019-03-30T17:00:00.000Z",
                    "max_speed": 132,
                    "max_speed_dtm": "22-12-2018 09:10:02",
                    "max_speed_at_latitude": 100.990709,
                    "max_speed_at_longitude": 100.990709,
                    "symbol_id": "car-side",
                    "symbol_color": "#5DADE2",
                    "total_distance": "0.0 กม.",
                    "stop_machine_on_duration": "25(วัน) 16:38:56",
                    "working_duration": "33(วัน) 08:44:15",
                    "machine_on_times": 1,
                    "speed_over_times": 0,
                    "stop_machine_on_over_x_mins_times": 220,
                    "stop_machine_on_max_duration": "25(วัน) 16:38:56",
                    "fuel_use": 0
                },
                {
                    "imei": "864507032289828",
                    "device_id": 18681,
                    "device_no": "T333/30s",
                    "speed_limit": "140",
                    "driver_id": "",
                    "device_group": "wutthinan",
                    "expire_date": "2019-07-05T17:00:00.000Z",
                    "install_date": "2018-12-01T17:00:00.000Z",
                    "max_speed": 139,
                    "max_speed_dtm": "22-12-2018 09:10:00",
                    "max_speed_at_latitude": 100.991078,
                    "max_speed_at_longitude": 100.991078,
                    "symbol_id": "shuttle-van",
                    "symbol_color": "#9B59B6",
                    "total_distance": "3005.9 กม.",
                    "stop_machine_on_duration": "20(วัน) 02:46:27",
                    "working_duration": "26(วัน) 11:31:15",
                    "machine_on_times": 1,
                    "speed_over_times": 0,
                    "stop_machine_on_over_x_mins_times": 93,
                    "stop_machine_on_max_duration": "20(วัน) 02:46:27",
                    "fuel_use": 0
                }
            ],
            "summary": {
                "working_duration": "59(วัน) 20:15:30",
                "total_distance": "3005.9 กม.",
                "stop_machine_on_duration": "45(วัน) 19:25:23",
                "stop_machine_on_over_x_mins_times": null,
                "stop_machine_on_max_duration": "45(วัน) 19:25:23",
                "speed_over_times": 0,
                "machine_on_times": 2
            }
        }

    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}
```
