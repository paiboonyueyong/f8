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
    "speed_over_interval": 0
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "details": {
                "working_duration": "104:35:48",
                "total_distance": "1323 กม.",
                "stop_machine_on_duration": "59:47:08",
                "stop_machine_on_over_10_mins_times": 43,
                "stop_machine_on_max_duration": "82:34:56",
                "speed_over_times": 47141,
                "machine_on_times": 45
            },
            "summary": [
                {
                    "imei": "861311007894107",
                    "device_id": 18698,
                    "device_no": "18698",
                    "driver_id": "",
                    "speed_limit": "80",
                    "max_speed": 7,
                    "max_speed_dtm": "05-12-2018 10:46:16",
                    "max_speed_at_latitude": 100.965713,
                    "max_speed_at_longitude": 100.965713,
                    "total_distance": "0.0 กม.",
                    "stop_machine_on_duration": "3:22:25",
                    "working_duration": "7:33:47",
                    "machine_on_times": 1,
                    "speed_over_times": 0,
                    "stop_machine_on_over_10_mins_times": 13,
                    "stop_machine_on_max_duration": "3:22:25",
                    "fuel_use": 0
                },
                {
                    "imei": "868998031020627",
                    "device_id": 18662,
                    "device_group": "Group_Name_AAA",
                    "device_model": "VIGO",
                    "device_no": "1กย-1287",
                    "expire_date": "2019-08-29T17:00:00.000Z",
                    "install_date": "2018-08-28T17:00:00.000Z",
                    "is_dlt_alert": false,
                    "remarks": "เร่งเต็มพิกัด อัดสุดไมล์",
                    "speed_limit": "10",
                    "driver_id": "",
                    "max_speed": 134,
                    "max_speed_dtm": "03-12-2018 11:51:14",
                    "max_speed_at_latitude": 100.99631,
                    "max_speed_at_longitude": 100.99631,
                    "working_duration": "07:49",
                    "machine_on_times": 43,
                    "stop_machine_on_duration": "22:10",
                    "total_distance": "297.5 กม.",
                    "speed_over_times": 17711,
                    "stop_machine_on_over_10_mins_times": 0,
                    "stop_machine_on_max_duration": "09:58",
                    "fuel_use": 0
                },
                {
                    "imei": "864507032289828",
                    "device_id": 18681,
                    "device_no": "T333/30s",
                    "speed_limit": "60",
                    "driver_id": "",
                    "device_group": "wutthinan",
                    "max_speed": 135,
                    "max_speed_dtm": "02-12-2018 07:08:48",
                    "max_speed_at_latitude": 101.001348,
                    "max_speed_at_longitude": 101.001348,
                    "stop_machine_on_duration": "79:02:33",
                    "total_distance": "1025.5 กม.",
                    "working_duration": "113:54:12",
                    "machine_on_times": 1,
                    "speed_over_times": 29430,
                    "stop_machine_on_over_10_mins_times": 30,
                    "stop_machine_on_max_duration": "79:02:33",
                    "fuel_use": 0
                }
            ]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 3
}
```
