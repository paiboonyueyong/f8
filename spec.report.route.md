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
            "latitude": 12.848633,
            "longitude": 100.950633,
            "speed": 0,
            "gps": 11,
            "gsm": 12,
            "status": "จอด",    // เครื่องยนต์
            "date": "3 พ.ค. 2562",
            "time": "14:09:22",
            "driver_name": "",      //  พนักงานขับรถ
            "driver_no": "",
            "place": "บริษัท สมบัติพลาสติก จำกัด (0.02 กม.) ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
            "speed_over": false,
            "fuel": 0,  // น้ำมัน
            "tracking_dtm": "2019-05-03T07:09:22.000Z",
            "is_driver_by_rfid": false,
            "device_no": "59 (85-7932)"
        },
        {
            "latitude": 12.848633,
            "longitude": 100.950633,
            "speed": 0,
            "gps": 11,
            "gsm": 12,
            "status": "จอด",
            "date": "3 พ.ค. 2562",
            "time": "14:10:22",
            "driver_name": "",
            "driver_no": "",
            "place": "บริษัท สมบัติพลาสติก จำกัด (0.02 กม.) ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
            "speed_over": false,
            "fuel": 0.05,
            "tracking_dtm": "2019-05-03T07:10:22.000Z",
            "is_driver_by_rfid": false,
            "device_no": "59 (85-7932)"
        },
        {
            "latitude": 12.848633,
            "longitude": 100.950633,
            "speed": 0,
            "gps": 12,
            "gsm": 14,
            "status": "จอด",
            "date": "3 พ.ค. 2562",
            "time": "14:11:22",
            "driver_name": "",
            "driver_no": "",
            "place": "บริษัท สมบัติพลาสติก จำกัด (0.02 กม.) ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
            "speed_over": false,
            "fuel": 0,
            "tracking_dtm": "2019-05-03T07:11:22.000Z",
            "is_driver_by_rfid": false,
            "device_no": "59 (85-7932)"
        },
        {
            "latitude": 12.848633,
            "longitude": 100.950633,
            "speed": 0,
            "gps": 10,
            "gsm": 14,
            "status": "จอด",
            "date": "3 พ.ค. 2562",
            "time": "14:12:22",
            "driver_name": "",
            "driver_no": "",
            "place": "บริษัท สมบัติพลาสติก จำกัด (0.02 กม.) ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
            "speed_over": false,
            "fuel": 0.11,
            "tracking_dtm": "2019-05-03T07:12:22.000Z",
            "is_driver_by_rfid": false,
            "device_no": "59 (85-7932)"
        },
        {
            "latitude": 12.848633,
            "longitude": 100.950633,
            "speed": 0,
            "gps": 12,
            "gsm": 16,
            "status": "จอด",
            "date": "3 พ.ค. 2562",
            "time": "14:13:23",
            "driver_name": "",
            "driver_no": "",
            "place": "บริษัท สมบัติพลาสติก จำกัด (0.02 กม.) ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
            "speed_over": false,
            "fuel": 1,
            "tracking_dtm": "2019-05-03T07:13:23.000Z",
            "is_driver_by_rfid": false,
            "device_no": "59 (85-7932)"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 18695154
}
```