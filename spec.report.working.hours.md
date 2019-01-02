# Get Report Working Hours (ชั่วโมงการทำงาน)

## Request Header (alway pass : token)

# getReportWorkingHours

## url
    http://{server}/api/report/getReportWorkingHours

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
            "device_no": "ID5test",
            "device_id": 18698,
            "total_elapse": "662:27",
            "hours": [
                {
                    "date": "14 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "15 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "16 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "17 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "18 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "19 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "20 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "21 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "22 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "23 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "24 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "25 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "26 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "27 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "28 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "29 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "30 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "1 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "2 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "3 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "4 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "5 ธ.ค. 61",
                    "elapse": "13:39",
                    "hours": [
                        {
                            "start_time": "10:20",
                            "end_time": "23:59",
                            "elapse": "13:39"
                        }
                    ]
                },
                {
                    "date": "6 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "7 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "8 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "9 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "10 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "11 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "12 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "13 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "14 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "15 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "16 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "17 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "18 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "19 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "20 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "21 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "22 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "23 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "24 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "25 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "26 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "27 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "28 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "29 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "30 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "31 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "1 ม.ค. 62",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "2 ม.ค. 62",
                    "elapse": "00:48",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "00:48",
                            "elapse": "00:48"
                        }
                    ]
                }
            ]
        },
        {
            "device_no": "1กย-1287",
            "device_id": 18662,
            "total_elapse": "279:28",
            "hours": [
                {
                    "date": "14 พ.ย. 61",
                    "elapse": "4:02",
                    "hours": [
                        {
                            "start_time": "11:31",
                            "end_time": "11:31",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:31",
                            "end_time": "15:33",
                            "elapse": "4:02"
                        }
                    ]
                },
                {
                    "date": "15 พ.ย. 61",
                    "elapse": "10:08",
                    "hours": [
                        {
                            "start_time": "10:11",
                            "end_time": "10:11",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:24",
                            "end_time": "10:24",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:24",
                            "end_time": "13:51",
                            "elapse": "3:27"
                        },
                        {
                            "start_time": "13:52",
                            "end_time": "13:52",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:52",
                            "end_time": "13:53",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "14:04",
                            "end_time": "14:04",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "14:04",
                            "end_time": "14:15",
                            "elapse": "00:11"
                        },
                        {
                            "start_time": "14:37",
                            "end_time": "14:37",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "14:45",
                            "end_time": "14:45",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "14:45",
                            "end_time": "17:48",
                            "elapse": "3:03"
                        },
                        {
                            "start_time": "17:56",
                            "end_time": "17:56",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "17:56",
                            "end_time": "19:00",
                            "elapse": "1:04"
                        },
                        {
                            "start_time": "19:00",
                            "end_time": "19:00",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "19:00",
                            "end_time": "19:00",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "19:17",
                            "end_time": "19:17",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "19:17",
                            "end_time": "21:38",
                            "elapse": "2:21"
                        }
                    ]
                },
                {
                    "date": "16 พ.ย. 61",
                    "elapse": "1:57",
                    "hours": [
                        {
                            "start_time": "06:58",
                            "end_time": "06:58",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "06:58",
                            "end_time": "06:59",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:08",
                            "end_time": "10:08",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:08",
                            "end_time": "10:46",
                            "elapse": "00:37"
                        },
                        {
                            "start_time": "10:56",
                            "end_time": "10:56",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:56",
                            "end_time": "11:20",
                            "elapse": "00:23"
                        },
                        {
                            "start_time": "12:12",
                            "end_time": "12:12",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "12:12",
                            "end_time": "12:36",
                            "elapse": "00:23"
                        },
                        {
                            "start_time": "12:49",
                            "end_time": "12:49",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "12:49",
                            "end_time": "13:20",
                            "elapse": "00:30"
                        },
                        {
                            "start_time": "18:47",
                            "end_time": "18:47",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "18:47",
                            "end_time": "18:47",
                            "elapse": "00:00"
                        }
                    ]
                },
                {
                    "date": "17 พ.ย. 61",
                    "elapse": "00:26",
                    "hours": [
                        {
                            "start_time": "07:50",
                            "end_time": "07:50",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "07:50",
                            "end_time": "08:16",
                            "elapse": "00:26"
                        }
                    ]
                },
                {
                    "date": "18 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "19 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "20 พ.ย. 61",
                    "elapse": "2:33",
                    "hours": [
                        {
                            "start_time": "13:57",
                            "end_time": "13:57",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:57",
                            "end_time": "13:59",
                            "elapse": "00:01"
                        },
                        {
                            "start_time": "15:01",
                            "end_time": "15:01",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "15:01",
                            "end_time": "15:58",
                            "elapse": "00:56"
                        },
                        {
                            "start_time": "15:59",
                            "end_time": "15:59",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "15:59",
                            "end_time": "15:59",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "16:17",
                            "end_time": "16:17",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "16:20",
                            "end_time": "16:20",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "16:40",
                            "end_time": "16:40",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "16:40",
                            "end_time": "16:41",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "17:17",
                            "end_time": "17:17",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "17:17",
                            "end_time": "18:51",
                            "elapse": "1:34"
                        }
                    ]
                },
                {
                    "date": "21 พ.ย. 61",
                    "elapse": "1:15",
                    "hours": [
                        {
                            "start_time": "08:37",
                            "end_time": "09:02",
                            "elapse": "00:24"
                        },
                        {
                            "start_time": "10:53",
                            "end_time": "10:53",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:53",
                            "end_time": "11:14",
                            "elapse": "00:21"
                        },
                        {
                            "start_time": "13:03",
                            "end_time": "13:03",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:03",
                            "end_time": "13:34",
                            "elapse": "00:30"
                        }
                    ]
                },
                {
                    "date": "22 พ.ย. 61",
                    "elapse": "00:57",
                    "hours": [
                        {
                            "start_time": "10:33",
                            "end_time": "10:33",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:33",
                            "end_time": "10:56",
                            "elapse": "00:23"
                        },
                        {
                            "start_time": "10:59",
                            "end_time": "10:59",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:59",
                            "end_time": "11:27",
                            "elapse": "00:27"
                        },
                        {
                            "start_time": "11:28",
                            "end_time": "11:28",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:28",
                            "end_time": "11:35",
                            "elapse": "00:06"
                        }
                    ]
                },
                {
                    "date": "23 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": [
                        {
                            "start_time": "15:05",
                            "end_time": "15:05",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "15:05",
                            "end_time": "15:06",
                            "elapse": "00:00"
                        }
                    ]
                },
                {
                    "date": "24 พ.ย. 61",
                    "elapse": "00:10",
                    "hours": [
                        {
                            "start_time": "10:01",
                            "end_time": "10:01",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:01",
                            "end_time": "10:11",
                            "elapse": "00:10"
                        }
                    ]
                },
                {
                    "date": "25 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "26 พ.ย. 61",
                    "elapse": "00:03",
                    "hours": [
                        {
                            "start_time": "09:13",
                            "end_time": "09:13",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:13",
                            "end_time": "09:14",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "15:27",
                            "end_time": "15:30",
                            "elapse": "00:02"
                        }
                    ]
                },
                {
                    "date": "27 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "28 พ.ย. 61",
                    "elapse": "00:21",
                    "hours": [
                        {
                            "start_time": "13:01",
                            "end_time": "16:20",
                            "elapse": "3:18"
                        },
                        {
                            "start_time": "13:02",
                            "end_time": "13:07",
                            "elapse": "00:05"
                        },
                        {
                            "start_time": "14:31",
                            "end_time": "00:29",
                            "elapse": "00:57"
                        }
                    ]
                },
                {
                    "date": "29 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "30 พ.ย. 61",
                    "elapse": "00:23",
                    "hours": [
                        {
                            "start_time": "14:07",
                            "end_time": "14:27",
                            "elapse": "00:19"
                        },
                        {
                            "start_time": "14:28",
                            "end_time": "14:32",
                            "elapse": "00:04"
                        }
                    ]
                },
                {
                    "date": "1 ธ.ค. 61",
                    "elapse": "2:01",
                    "hours": [
                        {
                            "start_time": "08:23",
                            "end_time": "08:23",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "08:23",
                            "end_time": "08:25",
                            "elapse": "00:01"
                        },
                        {
                            "start_time": "09:18",
                            "end_time": "09:18",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:18",
                            "end_time": "09:19",
                            "elapse": "00:01"
                        },
                        {
                            "start_time": "12:11",
                            "end_time": "12:11",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "12:11",
                            "end_time": "13:10",
                            "elapse": "00:59"
                        },
                        {
                            "start_time": "13:36",
                            "end_time": "13:36",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:36",
                            "end_time": "13:41",
                            "elapse": "00:05"
                        },
                        {
                            "start_time": "13:42",
                            "end_time": "13:42",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:42",
                            "end_time": "13:42",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:44",
                            "end_time": "13:44",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:44",
                            "end_time": "14:02",
                            "elapse": "00:17"
                        },
                        {
                            "start_time": "14:49",
                            "end_time": "14:49",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "14:49",
                            "end_time": "15:05",
                            "elapse": "00:16"
                        },
                        {
                            "start_time": "15:20",
                            "end_time": "15:20",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "15:20",
                            "end_time": "15:41",
                            "elapse": "00:20"
                        }
                    ]
                },
                {
                    "date": "2 ธ.ค. 61",
                    "elapse": "00:01",
                    "hours": [
                        {
                            "start_time": "16:46",
                            "end_time": "16:46",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "16:46",
                            "end_time": "16:48",
                            "elapse": "00:01"
                        }
                    ]
                },
                {
                    "date": "3 ธ.ค. 61",
                    "elapse": "5:02",
                    "hours": [
                        {
                            "start_time": "08:30",
                            "end_time": "08:30",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "08:30",
                            "end_time": "08:53",
                            "elapse": "00:23"
                        },
                        {
                            "start_time": "11:11",
                            "end_time": "11:11",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:11",
                            "end_time": "11:25",
                            "elapse": "00:14"
                        },
                        {
                            "start_time": "11:28",
                            "end_time": "11:28",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:28",
                            "end_time": "12:44",
                            "elapse": "1:15"
                        },
                        {
                            "start_time": "13:06",
                            "end_time": "13:06",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:06",
                            "end_time": "15:05",
                            "elapse": "1:58"
                        },
                        {
                            "start_time": "16:35",
                            "end_time": "16:35",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "16:35",
                            "end_time": "16:40",
                            "elapse": "00:04"
                        },
                        {
                            "start_time": "16:45",
                            "end_time": "16:45",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "16:45",
                            "end_time": "16:51",
                            "elapse": "00:06"
                        },
                        {
                            "start_time": "17:11",
                            "end_time": "17:11",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "17:11",
                            "end_time": "17:44",
                            "elapse": "00:32"
                        },
                        {
                            "start_time": "19:21",
                            "end_time": "19:21",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "19:21",
                            "end_time": "19:21",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "19:21",
                            "end_time": "19:48",
                            "elapse": "00:27"
                        }
                    ]
                },
                {
                    "date": "4 ธ.ค. 61",
                    "elapse": "6:25",
                    "hours": [
                        {
                            "start_time": "08:24",
                            "end_time": "08:24",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "08:24",
                            "end_time": "08:30",
                            "elapse": "00:05"
                        },
                        {
                            "start_time": "17:38",
                            "end_time": "17:38",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "17:38",
                            "end_time": "17:42",
                            "elapse": "00:03"
                        },
                        {
                            "start_time": "17:42",
                            "end_time": "17:42",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "17:42",
                            "end_time": "17:42",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "17:42",
                            "end_time": "17:44",
                            "elapse": "00:01"
                        },
                        {
                            "start_time": "17:45",
                            "end_time": "23:59",
                            "elapse": "6:14"
                        }
                    ]
                },
                {
                    "date": "5 ธ.ค. 61",
                    "elapse": "21:39",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "21:39",
                            "elapse": "21:39"
                        }
                    ]
                },
                {
                    "date": "6 ธ.ค. 61",
                    "elapse": "14:35",
                    "hours": [
                        {
                            "start_time": "08:29",
                            "end_time": "15:44",
                            "elapse": "7:14"
                        },
                        {
                            "start_time": "16:38",
                            "end_time": "23:59",
                            "elapse": "7:21"
                        },
                        {
                            "start_time": "16:38",
                            "end_time": "16:37",
                            "elapse": "00:59"
                        }
                    ]
                },
                {
                    "date": "7 ธ.ค. 61",
                    "elapse": "9:02",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "09:02",
                            "elapse": "9:02"
                        }
                    ]
                },
                {
                    "date": "8 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "9 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "10 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "11 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "12 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "13 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "14 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "15 ธ.ค. 61",
                    "elapse": "00:03",
                    "hours": [
                        {
                            "start_time": "11:03",
                            "end_time": "11:04",
                            "elapse": "00:01"
                        },
                        {
                            "start_time": "11:09",
                            "end_time": "11:10",
                            "elapse": "00:01"
                        },
                        {
                            "start_time": "11:12",
                            "end_time": "11:12",
                            "elapse": "00:00"
                        }
                    ]
                },
                {
                    "date": "16 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "17 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "18 ธ.ค. 61",
                    "elapse": "12:49",
                    "hours": [
                        {
                            "start_time": "11:00",
                            "end_time": "17:52",
                            "elapse": "6:51"
                        },
                        {
                            "start_time": "17:52",
                            "end_time": "17:52",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "18:01",
                            "end_time": "23:59",
                            "elapse": "5:58"
                        }
                    ]
                },
                {
                    "date": "19 ธ.ค. 61",
                    "elapse": "23:24",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "08:46",
                            "elapse": "8:46"
                        },
                        {
                            "start_time": "09:22",
                            "end_time": "23:59",
                            "elapse": "14:37"
                        }
                    ]
                },
                {
                    "date": "20 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "21 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "22 ธ.ค. 61",
                    "elapse": "9:35",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "01:26",
                            "elapse": "1:26"
                        },
                        {
                            "start_time": "01:28",
                            "end_time": "01:32",
                            "elapse": "00:03"
                        },
                        {
                            "start_time": "01:31",
                            "end_time": "09:37",
                            "elapse": "8:05"
                        }
                    ]
                },
                {
                    "date": "23 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "24 ธ.ค. 61",
                    "elapse": "12:21",
                    "hours": [
                        {
                            "start_time": "11:38",
                            "end_time": "23:59",
                            "elapse": "12:21"
                        }
                    ]
                },
                {
                    "date": "25 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "26 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "27 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "28 ธ.ค. 61",
                    "elapse": "17:02",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "17:02",
                            "elapse": "17:02"
                        }
                    ]
                },
                {
                    "date": "29 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "30 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "31 ธ.ค. 61",
                    "elapse": "00:00",
                    "hours": []
                },
                {
                    "date": "1 ม.ค. 62",
                    "elapse": "13:14",
                    "hours": [
                        {
                            "start_time": "10:46",
                            "end_time": "23:59",
                            "elapse": "13:14"
                        }
                    ]
                },
                {
                    "date": "2 ม.ค. 62",
                    "elapse": "00:48",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "00:48",
                            "elapse": "00:48"
                        }
                    ]
                }
            ]
        },
        {
            "device_no": "T333/30s",
            "device_id": 18681,
            "total_elapse": "1047:07",
            "hours": [
                {
                    "date": "14 พ.ย. 61",
                    "elapse": "5:12",
                    "hours": [
                        {
                            "start_time": "18:44",
                            "end_time": "19:09",
                            "elapse": "00:24"
                        },
                        {
                            "start_time": "19:09",
                            "end_time": "19:09",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "19:09",
                            "end_time": "19:10",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "19:13",
                            "end_time": "23:59",
                            "elapse": "4:46"
                        }
                    ]
                },
                {
                    "date": "15 พ.ย. 61",
                    "elapse": "8:37",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "08:37",
                            "elapse": "8:37"
                        },
                        {
                            "start_time": "08:37",
                            "end_time": "08:37",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:37",
                            "end_time": "09:37",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:37",
                            "end_time": "09:37",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:37",
                            "end_time": "09:37",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:39",
                            "end_time": "09:39",
                            "elapse": "00:00"
                        }
                    ]
                },
                {
                    "date": "16 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": [
                        {
                            "start_time": "11:17",
                            "end_time": "11:17",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:22",
                            "end_time": "11:22",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:22",
                            "end_time": "11:22",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:22",
                            "end_time": "11:22",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "13:48",
                            "end_time": "13:48",
                            "elapse": "00:00"
                        }
                    ]
                },
                {
                    "date": "17 พ.ย. 61",
                    "elapse": "12:34",
                    "hours": [
                        {
                            "start_time": "10:53",
                            "end_time": "10:53",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:53",
                            "end_time": "10:53",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:53",
                            "end_time": "10:53",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:53",
                            "end_time": "10:53",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:53",
                            "end_time": "10:53",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:53",
                            "end_time": "10:54",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:55",
                            "end_time": "10:55",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:55",
                            "end_time": "10:55",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "10:57",
                            "end_time": "10:57",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:26",
                            "end_time": "11:26",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:26",
                            "end_time": "11:26",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:26",
                            "end_time": "11:26",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "11:26",
                            "end_time": "23:59",
                            "elapse": "12:33"
                        }
                    ]
                },
                {
                    "date": "18 พ.ย. 61",
                    "elapse": "00:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "00:00",
                            "elapse": "00:00"
                        }
                    ]
                },
                {
                    "date": "19 พ.ย. 61",
                    "elapse": "00:01",
                    "hours": [
                        {
                            "start_time": "09:25",
                            "end_time": "09:25",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:25",
                            "end_time": "09:25",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:25",
                            "end_time": "09:26",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:26",
                            "end_time": "09:26",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:26",
                            "end_time": "09:27",
                            "elapse": "00:00"
                        },
                        {
                            "start_time": "09:27",
                            "end_time": "09:27",
                            "elapse": "00:00"
                        }
                    ]
                },
                {
                    "date": "20 พ.ย. 61",
                    "elapse": "12:28",
                    "hours": [
                        {
                            "start_time": "08:40",
                            "end_time": "12:46",
                            "elapse": "4:06"
                        },
                        {
                            "start_time": "12:46",
                            "end_time": "15:27",
                            "elapse": "2:40"
                        },
                        {
                            "start_time": "18:18",
                            "end_time": "23:59",
                            "elapse": "5:41"
                        }
                    ]
                },
                {
                    "date": "21 พ.ย. 61",
                    "elapse": "23:59",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "15:21",
                            "elapse": "15:21"
                        },
                        {
                            "start_time": "15:21",
                            "end_time": "23:59",
                            "elapse": "8:38"
                        }
                    ]
                },
                {
                    "date": "22 พ.ย. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "23 พ.ย. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "24 พ.ย. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "25 พ.ย. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "26 พ.ย. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "27 พ.ย. 61",
                    "elapse": "23:25",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "11:19",
                            "elapse": "11:19"
                        },
                        {
                            "start_time": "11:54",
                            "end_time": "23:59",
                            "elapse": "12:05"
                        }
                    ]
                },
                {
                    "date": "28 พ.ย. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "29 พ.ย. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "30 พ.ย. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "1 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "2 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "3 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "4 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "5 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "6 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "7 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "8 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "9 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "10 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "11 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "12 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "13 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "14 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "15 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "16 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "17 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "18 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "19 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "20 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "21 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "22 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "23 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "24 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "25 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "26 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "27 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "28 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "29 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "30 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "31 ธ.ค. 61",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "1 ม.ค. 62",
                    "elapse": "24:00",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "23:59",
                            "elapse": "24:00"
                        }
                    ]
                },
                {
                    "date": "2 ม.ค. 62",
                    "elapse": "00:48",
                    "hours": [
                        {
                            "start_time": "00:00",
                            "end_time": "00:48",
                            "elapse": "00:48"
                        }
                    ]
                }
            ]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 3
}
```