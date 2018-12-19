# Get Report (รายงานการแจ้งเตือน)

## Request Header (alway pass : token)
Remark dropdown ประเภทการแจ้งเตือน ใช้
    http://{server}/api/admin/getAlertTypeList 
    Body : {
        "alert_method":"GUI"
    }

# getReportEventAlert

## url
    http://{server}/api/report/getReportEventAlert/pageNo/pageSize

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
            "device_id": 18662,
            "device_no": "1กย-1287",
            "symbol_color": "#27AE60",
            "symbol_id": "taxi",
            "alert_type_id": "S1",
            "alert_type": "เครื่องยนต์ติด",
            "latitude": 12.91461,
            "longitude": 100.913021,
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "tracking_dtm": "2018-12-04T01:24:46.000Z",
            "status": "จอด",
            "speed": 0,
            "date": "4 ธ.ค. 2561",
            "time": "08:24:46"
        },
        {
            "device_id": 18662,
            "device_no": "1กย-1287",
            "symbol_color": "#27AE60",
            "symbol_id": "taxi",
            "alert_type_id": "S2",
            "alert_type": "เครื่องยนต์ดับ",
            "latitude": 12.91461,
            "longitude": 100.913021,
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "tracking_dtm": "2018-12-04T01:24:46.000Z",
            "status": "ดับ",
            "speed": 0,
            "date": "4 ธ.ค. 2561",
            "time": "08:24:46"
        },
        {
            "device_id": 18662,
            "device_no": "1กย-1287",
            "symbol_color": "#27AE60",
            "symbol_id": "taxi",
            "alert_type_id": "O2",
            "alert_type": "ความเร็วเกิน",
            "latitude": 12.914625,
            "longitude": 100.914266,
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "tracking_dtm": "2018-12-04T01:25:50.000Z",
            "status": "เร็ว",
            "speed": 12,
            "date": "4 ธ.ค. 2561",
            "time": "08:25:50"
        },
        {
            "device_id": 18698,
            "device_no": "ID5test",
            "symbol_color": "#5DADE2",
            "symbol_id": "car-side",
            "alert_type_id": "E6",
            "alert_type": "ไม่มีสัญญาณGPS",
            "latitude": 12.850376,
            "longitude": 100.96575,
            "place": "ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
            "tracking_dtm": "2018-12-03T19:57:06.000Z",
            "status": "เสา",
            "speed": 0,
            "date": "4 ธ.ค. 2561",
            "time": "02:57:06"
        },
        {
            "device_id": 18698,
            "device_no": "ID5test",
            "symbol_color": "#5DADE2",
            "symbol_id": "car-side",
            "alert_type_id": "E7",
            "alert_type": "รับสัญญาณGPS",
            "latitude": 12.850345,
            "longitude": 100.965761,
            "place": "ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
            "tracking_dtm": "2018-12-03T19:57:19.000Z",
            "status": "จอด",
            "speed": 0,
            "date": "4 ธ.ค. 2561",
            "time": "02:57:19"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 5
}
```