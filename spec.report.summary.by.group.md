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
            "details": [
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
                    "symbol_id": "car-side",
                    "symbol_color": "#5DADE2",
                    "total_distance": "0.0 กม.",
                    "stop_machine_on_duration": "8:29:44",
                    "working_duration": "11:55:21",
                    "machine_on_times": 1,
                    "speed_over_times": 0,
                    "stop_machine_on_over_x_mins_times": 17,
                    "stop_machine_on_max_duration": "8:29:44",
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
                    "symbol_id": "taxi",
                    "symbol_color": "#27AE60",
                    "working_duration": "35:11:15",
                    "machine_on_times": 43,
                    "stop_machine_on_duration": "29:25:36",
                    "total_distance": "297.5 กม.",
                    "speed_over_times": 17711,
                    "stop_machine_on_over_x_mins_times": 1,
                    "stop_machine_on_max_duration": "27:54:36",
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
                    "symbol_id": "car-side",
                    "symbol_color": "#5DADE2",
                    "stop_machine_on_duration": "74:40:59",
                    "total_distance": "1025.5 กม.",
                    "working_duration": "118:15:46",
                    "machine_on_times": 1,
                    "speed_over_times": 29430,
                    "stop_machine_on_over_x_mins_times": 30,
                    "stop_machine_on_max_duration": "74:40:59",
                    "fuel_use": 0
                }
            ],
            "summary": {
                "working_duration": "165:22:22",
                "total_distance": "1323 กม.",
                "stop_machine_on_duration": "112:36:19",
                "stop_machine_on_over_x_mins_times": 48,
                "stop_machine_on_max_duration": "111:05:19",
                "speed_over_times": 47141,
                "machine_on_times": 45
            }
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 3
}
```

# getSpeedOverSummary

## url
    http://{server}/api/report/getSpeedOverSummary

## request body
```json
{
	"device_id":18662,
    "start_date" : "02-12-2018",
    "end_date": "05-12-2018"
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "start_dtm": "3 ธ.ค. 2561 08:48:43",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.91458,
            "start_at_longitude": 100.914936,
            "max_speed": 28,
            "distance": "0.3",
            "elapse_time_s": "01:00",
            "end_dtm": "3 ธ.ค. 2561 08:49:43"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 08:51:43",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.915786,
            "start_at_longitude": 100.91529,
            "max_speed": 28,
            "end_at_latitude": 12.914628,
            "end_at_longitude": 100.91347,
            "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "distance": "0.4",
            "elapse_time_s": "02:00",
            "end_dtm": "3 ธ.ค. 2561 08:53:43"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 11:12:20",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.914631,
            "start_at_longitude": 100.9135,
            "max_speed": 31,
            "end_at_latitude": 12.92347,
            "end_at_longitude": 100.909923,
            "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "distance": "1.7",
            "elapse_time_s": "03:59",
            "end_dtm": "3 ธ.ค. 2561 11:16:19"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 11:18:19",
            "start_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.9286,
            "start_at_longitude": 100.90368,
            "max_speed": 44,
            "end_at_latitude": 12.932771,
            "end_at_longitude": 100.904931,
            "end_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "distance": "0.8",
            "elapse_time_s": "02:00",
            "end_dtm": "3 ธ.ค. 2561 11:20:19"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 11:22:19",
            "start_at_place": "ถนนสุขุมวิท ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.93445,
            "start_at_longitude": 100.901828,
            "max_speed": 71,
            "end_at_latitude": 12.939088,
            "end_at_longitude": 100.902673,
            "end_at_place": "ถนนสุขุมวิท ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "distance": "1.6",
            "elapse_time_s": "02:43",
            "end_dtm": "3 ธ.ค. 2561 11:25:02"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 11:31:17",
            "start_at_place": "ถนนสุขุมวิท ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.94662,
            "start_at_longitude": 100.905091,
            "max_speed": 99,
            "end_at_latitude": 12.949468,
            "end_at_longitude": 100.935063,
            "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "distance": "3.8",
            "elapse_time_s": "03:20",
            "end_dtm": "3 ธ.ค. 2561 11:34:37"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 11:35:08",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.95095,
            "start_at_longitude": 100.941145,
            "max_speed": 134,
            "end_at_latitude": 13.583721,
            "end_at_longitude": 100.951758,
            "end_at_place": "ทางหลวงพิเศษหมายเลข 7 ต.บางสมัคร อ.บางปะกง จ.ฉะเชิงเทรา",
            "distance": "83.0",
            "elapse_time_s": "45:13",
            "end_dtm": "3 ธ.ค. 2561 12:20:21"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 12:20:53",
            "start_at_place": "ทางหลวงพิเศษหมายเลข 7 ต.บางสมัคร อ.บางปะกง จ.ฉะเชิงเทรา",
            "start_at_latitude": 13.579531,
            "start_at_longitude": 100.951073,
            "max_speed": 108,
            "end_at_latitude": 13.61766,
            "end_at_longitude": 100.744441,
            "end_at_place": "ถนนบางนา-ตราด ต.บางโฉลง อ.บางพลี จ.สมุทรปราการ",
            "distance": "25.2",
            "elapse_time_s": "19:13",
            "end_dtm": "3 ธ.ค. 2561 12:40:06"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 12:41:06",
            "start_at_place": "ถนนบางนา-ตราด ต.บางโฉลง อ.บางพลี จ.สมุทรปราการ",
            "start_at_latitude": 13.619763,
            "start_at_longitude": 100.739453,
            "max_speed": 80,
            "end_at_latitude": 13.634563,
            "end_at_longitude": 100.739975,
            "end_at_place": "ต.ราชาเทวะ อ.บางพลี จ.สมุทรปราการ",
            "distance": "2.5",
            "elapse_time_s": "02:54",
            "end_dtm": "3 ธ.ค. 2561 12:44:00"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 13:07:01",
            "start_at_place": "ต.ราชาเทวะ อ.บางพลี จ.สมุทรปราการ",
            "start_at_latitude": 13.63928,
            "start_at_longitude": 100.742045,
            "max_speed": 78,
            "end_at_latitude": 13.632516,
            "end_at_longitude": 100.738881,
            "end_at_place": "ต.ราชาเทวะ อ.บางพลี จ.สมุทรปราการ",
            "distance": "5.3",
            "elapse_time_s": "06:59",
            "end_dtm": "3 ธ.ค. 2561 13:14:00"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 13:25:58",
            "start_at_place": "ต.ราชาเทวะ อ.บางพลี จ.สมุทรปราการ",
            "start_at_latitude": 13.63267,
            "start_at_longitude": 100.739111,
            "max_speed": 68,
            "end_at_latitude": 13.643485,
            "end_at_longitude": 100.743983,
            "end_at_place": "ต.ราชาเทวะ อ.บางพลี จ.สมุทรปราการ",
            "distance": "1.8",
            "elapse_time_s": "02:00",
            "end_dtm": "3 ธ.ค. 2561 13:27:58"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 13:29:57",
            "start_at_place": "ต.ราชาเทวะ อ.บางพลี จ.สมุทรปราการ",
            "start_at_latitude": 13.644878,
            "start_at_longitude": 100.745308,
            "max_speed": 88,
            "end_at_latitude": 13.506051,
            "end_at_longitude": 100.995435,
            "end_at_place": "ทางหลวงแผ่นดินหมายเลข 3 ต.บางปะกง อ.บางปะกง จ.ฉะเชิงเทรา",
            "distance": "35.2",
            "elapse_time_s": "35:15",
            "end_dtm": "3 ธ.ค. 2561 14:05:12"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 14:05:34",
            "start_at_place": "ทางหลวงแผ่นดินหมายเลข 3 ต.บางปะกง อ.บางปะกง จ.ฉะเชิงเทรา",
            "start_at_latitude": 13.503073,
            "start_at_longitude": 100.999801,
            "max_speed": 117,
            "end_at_latitude": 13.46972,
            "end_at_longitude": 100.997643,
            "end_at_place": "ทางหลวงแผ่นดินหมายเลข 3 ต.ท่าข้าม อ.บางปะกง จ.ฉะเชิงเทรา",
            "distance": "5.4",
            "elapse_time_s": "03:11",
            "end_dtm": "3 ธ.ค. 2561 14:08:45"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 14:13:50",
            "start_at_place": "ทางหลวงแผ่นดินหมายเลข 34 ต.คลองตำหรุ อ.เมืองชลบุรี จ.ชลบุรี",
            "start_at_latitude": 13.453713,
            "start_at_longitude": 100.99777,
            "max_speed": 116,
            "end_at_latitude": 12.950875,
            "end_at_longitude": 100.941913,
            "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "distance": "62.9",
            "elapse_time_s": "41:27",
            "end_dtm": "3 ธ.ค. 2561 14:55:17"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 14:55:43",
            "start_at_place": "ทางหลวงแผ่นดินหมายเลข 3240 ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.949201,
            "start_at_longitude": 100.934898,
            "max_speed": 98,
            "end_at_latitude": 12.93471,
            "end_at_longitude": 100.907038,
            "end_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "distance": "4.1",
            "elapse_time_s": "04:00",
            "end_dtm": "3 ธ.ค. 2561 14:59:43"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 15:00:13",
            "start_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.928451,
            "start_at_longitude": 100.904053,
            "max_speed": 78,
            "end_at_latitude": 12.914586,
            "end_at_longitude": 100.915276,
            "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "distance": "3.2",
            "elapse_time_s": "05:26",
            "end_dtm": "3 ธ.ค. 2561 15:05:39"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 16:46:25",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.914625,
            "start_at_longitude": 100.913801,
            "max_speed": 16,
            "distance": "0.2",
            "elapse_time_s": "01:00",
            "end_dtm": "3 ธ.ค. 2561 16:47:25"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 16:48:25",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.9126,
            "start_at_longitude": 100.915455,
            "max_speed": 28,
            "end_at_latitude": 12.91459,
            "end_at_longitude": 100.913306,
            "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "distance": "1.1",
            "elapse_time_s": "03:17",
            "end_dtm": "3 ธ.ค. 2561 16:51:42"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 17:13:21",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.914635,
            "start_at_longitude": 100.914411,
            "max_speed": 32,
            "end_at_latitude": 12.908918,
            "end_at_longitude": 100.902015,
            "end_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "distance": "2.4",
            "elapse_time_s": "07:58",
            "end_dtm": "3 ธ.ค. 2561 17:21:19"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 17:22:19",
            "start_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.909616,
            "start_at_longitude": 100.899138,
            "max_speed": 30,
            "distance": "0.1",
            "elapse_time_s": "01:00",
            "end_dtm": "3 ธ.ค. 2561 17:23:19"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 17:31:18",
            "start_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.90908,
            "start_at_longitude": 100.894516,
            "max_speed": 55,
            "end_at_latitude": 12.904841,
            "end_at_longitude": 100.871263,
            "end_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "distance": "2.7",
            "elapse_time_s": "04:59",
            "end_dtm": "3 ธ.ค. 2561 17:36:17"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 17:37:17",
            "start_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.905993,
            "start_at_longitude": 100.869041,
            "max_speed": 47,
            "end_at_latitude": 12.919743,
            "end_at_longitude": 100.864656,
            "end_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "distance": "2.4",
            "elapse_time_s": "05:59",
            "end_dtm": "3 ธ.ค. 2561 17:43:16"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 19:23:59",
            "start_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.920578,
            "start_at_longitude": 100.86272,
            "max_speed": 22,
            "end_at_latitude": 12.918618,
            "end_at_longitude": 100.865208,
            "end_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "distance": "0.6",
            "elapse_time_s": "02:00",
            "end_dtm": "3 ธ.ค. 2561 19:25:59"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 19:26:58",
            "start_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.914136,
            "start_at_longitude": 100.867075,
            "max_speed": 45,
            "end_at_latitude": 12.90912,
            "end_at_longitude": 100.893078,
            "end_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "distance": "4.1",
            "elapse_time_s": "07:59",
            "end_dtm": "3 ธ.ค. 2561 19:34:57"
        },
        {
            "start_dtm": "3 ธ.ค. 2561 19:36:57",
            "start_at_place": "ต.นาเกลือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.909828,
            "start_at_longitude": 100.897918,
            "max_speed": 28,
            "end_at_latitude": 12.914686,
            "end_at_longitude": 100.914975,
            "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "distance": "3.0",
            "elapse_time_s": "08:58",
            "end_dtm": "3 ธ.ค. 2561 19:45:55"
        },
        {
            "start_dtm": "4 ธ.ค. 2561 08:25:50",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.914625,
            "start_at_longitude": 100.914266,
            "max_speed": 12,
            "distance": "0.1",
            "elapse_time_s": "01:00",
            "end_dtm": "4 ธ.ค. 2561 08:26:50"
        },
        {
            "start_dtm": "4 ธ.ค. 2561 08:29:49",
            "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "start_at_latitude": 12.914611,
            "start_at_longitude": 100.913378,
            "max_speed": 16,
            "distance": "0.0",
            "elapse_time_s": "00:24",
            "end_dtm": "4 ธ.ค. 2561 08:30:13"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 27
}
```
