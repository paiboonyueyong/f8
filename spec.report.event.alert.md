# Get Report (รายงานการแจ้งเตือน)

## Request Header (alway pass : token)
Remark 
    1. dropdown ประเภทการแจ้งเตือน ใช้
        http://{server}/api/admin/getAlertTypeList 
        Body : {
            "alert_method":"GUI"
        }
    2. dropdown ทะเบียนใช้ 
        http://{server}/api/admin/getDeviceAdnGroupList

# getReportEventAlert

## url
    http://{server}/api/report/getReportEventAlert/pageNo/pageSize

## request body (หากต้องการดึงข้อมูลรถทุกคันให้ส่ง devices:[])
```json
{
	"devices":[
        {
            "name": "[wutthinan]",
            "group_id":"wutthinan",
            "type": "GROUP"
        },
        {
            "name": "[Group_Name_AAA]",
            "group_id":"Group_Name_AAA",
            "type": "GROUP"
        },
        {
            "name": "[Group 1]",
			"group_id":"Group 1",            
            "type": "GROUP"
        },
        {
            "name": "18703",
            "device_id": 18703,
            "type": "DEVICE"
        },
        {
            "name": "18704",
            "device_id": 18704,
            "type": "DEVICE"
        },
        {
            "name": "18705",
            "device_id": 18705,
            "type": "DEVICE"
        },
        {
            "name": "18706",
            "device_id": 18706,
            "type": "DEVICE"
        },
        {
            "name": "18707",
            "device_id": 18707,
            "type": "DEVICE"
        },
        {
            "name": "18708",
            "device_id": 18708,
            "type": "DEVICE"
        },
        {
            "name": "18709",
            "device_id": 18709,
            "type": "DEVICE"
        },
        {
            "name": "18710",
            "device_id": 18710,
            "type": "DEVICE"
        },
        {
            "name": "18711",
            "device_id": 18711,
            "type": "DEVICE"
        },
        {
            "name": "18712",
            "device_id": 18712,
            "type": "DEVICE"
        },
        {
            "name": "18713",
            "device_id": 18713,
            "type": "DEVICE"
        },
        {
            "name": "18714",
            "device_id": 18714,
            "type": "DEVICE"
        },
        {
            "name": "18715",
            "device_id": 18715,
            "type": "DEVICE"
        },
        {
            "name": "18716",
            "device_id": 18716,
            "type": "DEVICE"
        },
        {
            "name": "1กท-1287",
            "device_id": 18692,
            "type": "DEVICE"
        },
        {
            "name": "1กย-1287",
            "device_id": 18662,
            "type": "DEVICE"
        },
        {
            "name": "ID5",
            "device_id": 18679,
            "type": "DEVICE"
        },
        {
            "name": "T333/30s",
            "device_id": 18681,
            "type": "DEVICE"
        }
    ],
    "start_date": "11-11-2018 23:00",
	"end_date": "20-12-2018 23:00"
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