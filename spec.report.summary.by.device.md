# Get Report Summary By Device (สรุปการใช้งาน)

## Request Header (alway pass : token)

# getReportSummaryByDevice

## url
    http://{server}/api/report/getReportSummaryByDevice/pageNo/pageSize

## request body (หากต้องการดึงข้อมูลรถทุกคันให้ส่ง devices:[])
```json
{
	"devices":[
        {
            "device_id": 18662
        },
        {
            "device_id": 18679
        },
	    {
            "device_id": 18681
        },
        {
            "device_id": 18685
        },
        {
            "device_id": 18687
        },
	    {
            "device_id": 18688
        },
	    {
            "device_id": 18692
        },
	    {
            "device_id": 18698
        }
    ],
    "start_date" : "12-12-2018 02:00",
    "end_date": "13-12-2018 17:50"
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "device_no": "18685",
            "device_id": 18685,
            "moving": {	// การเดินทาง
                "max_period": "00:00",
                "max_period_dtm": "-",
                "max_period_distance": 0,
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00"
            },
            "speed_over": { // ความเร็วเกินกำหนด
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00",
                "max_speed": 0,
                "max_speed_dtm": "-"
            },
            "stop_machine_on": { // จอดขณะติดเครื่อง
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "stop_machine_off": { // จอดขณะดับครื่อง
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "no_gps": {	 // ไม่มีสัญญาณ GPS
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "machine_on": {  // ระยะเวลาติดเครื่อง
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            }
        },
        {
            "device_no": "18688",
            "device_id": 18688,
            "moving": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "max_period_distance": 0,
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00"
            },
            "speed_over": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00",
                "max_speed": 0,
                "max_speed_dtm": "-"
            },
            "stop_machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "stop_machine_off": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "no_gps": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            }
        },
        {
            "device_no": "18698",
            "device_id": 18698,
            "moving": {
                "max_period": "8:01:48",
                "max_period_dtm": "13 ธ.ค. 2561 15:40:55 - 13 ธ.ค. 2561 23:42:43",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "14:14:06"
            },
            "speed_over": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00",
                "max_speed": 0,
                "max_speed_dtm": "-"
            },
            "stop_machine_on": {
                "max_period": "2:56:10",
                "max_period_dtm": "13 ธ.ค. 2561 05:26:34 - 13 ธ.ค. 2561 08:22:44",
                "total_elapse_times": "27:29"
            },
            "stop_machine_off": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "no_gps": {
                "max_period": "01:08",
                "max_period_dtm": "12 ธ.ค. 2561 15:10:33 - 12 ธ.ค. 2561 15:11:41",
                "total_elapse_times": "01:08"
            },
            "machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "46:52"
            }
        },
        {
            "device_no": "ID5",
            "device_id": 18679,
            "moving": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "max_period_distance": 0,
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00"
            },
            "speed_over": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00",
                "max_speed": 0,
                "max_speed_dtm": "-"
            },
            "stop_machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "stop_machine_off": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "46:52"
            },
            "no_gps": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            }
        },
        {
            "device_no": "1กท-1287",
            "device_group": "Group 1",
            "device_id": 18692,
            "moving": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "max_period_distance": 0,
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00"
            },
            "speed_over": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00",
                "max_speed": 0,
                "max_speed_dtm": "-"
            },
            "stop_machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "stop_machine_off": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "no_gps": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            }
        },
        {
            "device_no": "4กำ-2240",
            "device_group": "Group of Dead",
            "device_id": 18687,
            "moving": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "max_period_distance": 0,
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00"
            },
            "speed_over": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00",
                "max_speed": 0,
                "max_speed_dtm": "-"
            },
            "stop_machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "stop_machine_off": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "no_gps": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            }
        },
        {
            "device_no": "1กย-1287",
            "device_group": "Group_Name_AAA",
            "device_id": 18662,
            "moving": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "max_period_distance": 0,
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00"
            },
            "speed_over": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00",
                "max_speed": 0,
                "max_speed_dtm": "-"
            },
            "stop_machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "stop_machine_off": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "46:52"
            },
            "no_gps": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            }
        },
        {
            "device_no": "1ธค-2018",
            "device_group": "wutthinan",
            "device_id": 18681,
            "moving": {
                "max_period": "8:01:29",
                "max_period_dtm": "13 ธ.ค. 2561 15:40:53 - 13 ธ.ค. 2561 23:42:22",
                "total_distance": "256.2 กม.",
                "total_elapse_times": "11:59:02"
            },
            "speed_over": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_distance": "0.0 กม.",
                "total_elapse_times": "00:00",
                "max_speed": 0,
                "max_speed_dtm": "-"
            },
            "stop_machine_on": {
                "max_period": "13:53:01",
                "max_period_dtm": "12 ธ.ค. 2561 18:29:12 - 13 ธ.ค. 2561 08:22:13",
                "total_elapse_times": "43:20"
            },
            "stop_machine_off": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "no_gps": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "00:00"
            },
            "machine_on": {
                "max_period": "00:00",
                "max_period_dtm": "-",
                "total_elapse_times": "46:52"
            }
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 8
}
```