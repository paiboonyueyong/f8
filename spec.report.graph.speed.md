# Get Speed for generate graph

## Request Header (alway pass : token)

# getSpeedGraphByDevice

## url
    http://{server}/api/report/getSpeedGraphByDevice

## request body
```json
{
	"devices": [
            {"device_id":18681}
        ],
    "start_date": "18-12-2018 23:00",
    "end_date": "19-12-2018 23:00"
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:02",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:05",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:07",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:10",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:12",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:15",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:17",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:20",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:23",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:25",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:28",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:30",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:33",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:35",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:38",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:40",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:43",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:45",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:48",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:51",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:53",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:56",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "18-12-2018",
            "time": "23:58",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:01",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:03",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:06",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:08",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:11",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:13",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:16",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:18",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:21",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:23",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:26",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:28",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:31",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:33",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:36",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:39",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:41",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:44",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:46",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:49",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:51",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:54",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:56",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "00:59",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:02",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:04",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:07",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:09",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:12",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:14",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:17",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:19",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:22",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:25",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:27",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:30",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:32",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:35",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:37",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:40",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:42",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:45",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:47",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:50",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:53",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:55",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "01:58",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:00",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:03",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:05",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:08",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:10",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:13",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:15",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:18",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:20",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:23",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:25",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:28",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:30",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:33",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:35",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:38",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:41",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:43",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:46",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:48",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:51",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:53",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:56",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "02:58",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:01",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:04",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:06",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:09",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:11",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:14",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:16",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:19",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:21",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:24",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:27",
            "speed_limit": 300
        },
        {
            "speed": 0,
            "date": "19-12-2018",
            "time": "03:29",
            "speed_limit": 300
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 107
}
```