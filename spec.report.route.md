# Get Report Route (รายงานเส้นทางการวิ่ง)

## Request Header (alway pass : token)

# getReportRoute

## url
    http://{server}/api/report/getReportRoute/pageNo/pageSize

## request body (หากต้องการดึงข้อมูลรถทุกคันให้ส่ง devices:[])
```json
{
	"devices":[
        {
            "device_id": 18662
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
            "latitude": 12.914626,
            "longitude": 100.913115,
            "speed": 0,
            "gps": 10,
            "gsm": 17,
            "status": "จอด",
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "date": "17 ธ.ค. 2561",
            "time": "23:00",
            "driver_name": "Wutthin",
            "driver_no": "9876543210",
            "driver_contact": "0961881211",
            "speed_over": false,
            "tracking_dtm": "2018-12-17T16:00:19.000Z",
            "device_no": "T333/30s"
        },
        {
            "latitude": 12.914626,
            "longitude": 100.913115,
            "speed": 0,
            "gps": 10,
            "gsm": 17,
            "status": "จอด",
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "date": "17 ธ.ค. 2561",
            "time": "23:00",
            "driver_name": "Wutthin",
            "driver_no": "9876543210",
            "driver_contact": "0961881211",
            "speed_over": false,
            "tracking_dtm": "2018-12-17T16:00:49.000Z",
            "device_no": "T333/30s"
        },
        {
            "latitude": 12.914626,
            "longitude": 100.913115,
            "speed": 0,
            "gps": 10,
            "gsm": 17,
            "status": "จอด",
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "date": "17 ธ.ค. 2561",
            "time": "23:01",
            "driver_name": "Wutthin",
            "driver_no": "9876543210",
            "driver_contact": "0961881211",
            "speed_over": false,
            "tracking_dtm": "2018-12-17T16:01:19.000Z",
            "device_no": "T333/30s"
        },
        {
            "latitude": 12.914626,
            "longitude": 100.913115,
            "speed": 0,
            "gps": 10,
            "gsm": 17,
            "status": "จอด",
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "date": "17 ธ.ค. 2561",
            "time": "23:01",
            "driver_name": "Wutthin",
            "driver_no": "9876543210",
            "driver_contact": "0961881211",
            "speed_over": false,
            "tracking_dtm": "2018-12-17T16:01:49.000Z",
            "device_no": "T333/30s"
        },
        {
            "latitude": 12.914626,
            "longitude": 100.913115,
            "speed": 0,
            "gps": 10,
            "gsm": 17,
            "status": "จอด",
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "date": "17 ธ.ค. 2561",
            "time": "23:02",
            "driver_name": "Wutthin",
            "driver_no": "9876543210",
            "driver_contact": "0961881211",
            "speed_over": false,
            "tracking_dtm": "2018-12-17T16:02:18.000Z",
            "device_no": "T333/30s"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 7878
}
```