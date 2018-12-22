# Get Report Distance (รายงานการรูดบัตร)

## Request Header (alway pass : token)

# getReportRFID

## url
    http://{server}/api/report/getReportRFID/pageNo/pageSize

elapse_time_over มีหน่วยเป็นนาที เป็น option ในการกรองข้อมูลให้เลือกช่วงเวลากี่นาทีขึ้นไป
is_not_scan true คือกรองเฉพาะข้อมูลที่ไม่มีการรูดบัตร

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
    "end_date": "13-12-2018 17:50",
    "elapse_time_over": 4,
    "is_not_scan": true
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
                    "status": "วิ่ง",
                    "start_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
                    "start_at_latitude": 12.914565,
                    "start_at_longitude": 100.913428,
                    "symbol_id": "shuttle-van",
                    "symbol_color": "#9B59B6",
                    "distance": "12.0 กม.",
                    "end_at_latitude": 12.850223,
                    "end_at_longitude": 100.96577,
                    "end_at_place": "ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
                    "device_no": "T333/30s",
                    "date": "17 ธ.ค. 2561",
                    "start_time": "23:07:47",
                    "end_time": "23:25:13",
                    "elapse": "17:26",
                    "is_driver_by_rfid":true, // true คือ รูดบัตร, false คือ ไ่ม่รูดบัตร
                    "driver_no":"141000015500100", // รหัสบัตรขับขี่
                    "driver_name": "MR.SONGKRAN YENSABAICHAI" // ชื่อคนขับ
                },
                {
                    "device_id": 18681,
                    "status": "วิ่ง",
                    "start_at_place": "ต.ห้วยใหญ่ อ.บางละมุง จ.ชลบุรี",
                    "start_at_latitude": 12.850366,
                    "start_at_longitude": 100.965725,
                    "symbol_id": "shuttle-van",
                    "symbol_color": "#9B59B6",
                    "distance": "12.0 กม.",
                    "end_at_latitude": 12.91453,
                    "end_at_longitude": 100.913135,
                    "end_at_place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
                    "device_no": "T333/30s",
                    "date": "18 ธ.ค. 2561",
                    "start_time": "09:59:34",
                    "end_time": "10:20:29",
                    "elapse": "20:55",
                    "is_driver_by_rfid":true, // true คือ รูดบัตร, false คือ ไ่ม่รูดบัตร
                    "driver_no":"141000015500100", // รหัสบัตรขับขี่
                    "driver_name": "MR.SONGKRAN YENSABAICHAI" // ชื่อคนขับ
                }
            ],
            "summary": {
                "total_distance": "24.0 กม.",
                "total_elapse": "38:21"
            }
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 37
}
```