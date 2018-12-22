# Get Report Distance (รายงานการจอด)

## Request Header (alway pass : token)

# getReportDistance

## url
    http://{server}/api/report/getReportStop/pageNo/pageSize

elapse_time_over มีหน่วยเป็นนาที เป็น option ในการกรองข้อมูลให้เลือกช่วงเวลากี่นาทีขึ้นไป

## request body (หากต้องการดึงข้อมูลรถทุกคันให้ส่ง devices:[])
```json
{
	"devices": [
            {"device_id":18681},
            {"device_id":18698}
        ],
    "start_date": "17-12-2018 23:00",
    "end_date": "19-12-2018 23:00",
    "elapse_time_over": 4
}

```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "details": [
                {
                    "device_id": 18681,
                    "status": "จอด",
                    "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
                    "start_at_latitude": 12.914666,
                    "start_at_longitude": 100.913103,
                    "end_at_latitude": 12.914565,
                    "end_at_longitude": 100.913428,
                    "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
                    "device_no": "T333/30s",
                    "date": "17 ธ.ค. 2561",
                    "start_time": "23:00:00",
                    "end_time": "23:07:47",
                    "elapse": "07:47"
                },
                {
                    "device_id": 18681,
                    "status": "จอด",
                    "start_at_place": "ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
                    "start_at_latitude": 12.850223,
                    "start_at_longitude": 100.96577,
                    "end_at_latitude": 12.850366,
                    "end_at_longitude": 100.965725,
                    "end_at_place": "ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
                    "device_no": "T333/30s",
                    "date": "17 ธ.ค. 2561",
                    "start_time": "23:25:13",
                    "end_time": "09:59:34",
                    "elapse": "10:34:21"
                },
                {
                    "device_id": 18681,
                    "status": "จอด",
                    "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
                    "start_at_latitude": 12.91453,
                    "start_at_longitude": 100.913135,
                    "end_at_latitude": 12.91459,
                    "end_at_longitude": 100.913195,
                    "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
                    "device_no": "T333/30s",
                    "date": "18 ธ.ค. 2561",
                    "start_time": "10:20:29",
                    "end_time": "10:31:56",
                    "elapse": "11:27"
                },
                {
                    "device_id": 18681,
                    "status": "จอด",
                    "start_at_place": "ทางหลวงแผ่นดินหมายเลข 3 ต.ทุ่งสุขลา อ.ศรีราชา จ.ชลบุรี",
                    "start_at_latitude": 13.086876,
                    "start_at_longitude": 100.9178,
                    "end_at_latitude": 13.086758,
                    "end_at_longitude": 100.917683,
                    "end_at_place": "ทางหลวงแผ่นดินหมายเลข 3 ต.ทุ่งสุขลา อ.ศรีราชา จ.ชลบุรี",
                    "device_no": "T333/30s",
                    "date": "18 ธ.ค. 2561",
                    "start_time": "11:18:44",
                    "end_time": "11:28:12",
                    "elapse": "09:28"
                },
                {
                    "device_id": 18681,
                    "status": "จอด",
                    "start_at_place": "ต.หนองปลาไหล อ.บางละมุง จ.ชลบุรี",
                    "start_at_latitude": 12.969698,
                    "start_at_longitude": 100.972493,
                    "end_at_latitude": 12.969541,
                    "end_at_longitude": 100.972501,
                    "end_at_place": "ต.หนองปลาไหล อ.บางละมุง จ.ชลบุรี",
                    "device_no": "T333/30s",
                    "date": "18 ธ.ค. 2561",
                    "start_time": "11:43:08",
                    "end_time": "11:53:35",
                    "elapse": "10:27"
                }
            ],
            "summary": {
                "total_elapse": "11:13:30"
            }
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 59
}
```