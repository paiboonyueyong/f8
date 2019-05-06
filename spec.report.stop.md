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
                    "device_no": "T333/30s",
                    "device_id": 18681,
                    "status": "ดับ",    //สถานะ
                    "symbol_id": "shuttle-van",
                    "symbol_color": "#9B59B6",
                    "fuel": 100,    // น้ำมัน
                    "engine": "ดับเครื่อง", // เครื่องยนต์
                    "date": "1 มี.ค. 2562", 
                    "elapse": "352:00:30",  //เวลาจอด
                    "start_dtm": "1 มี.ค. 2562",    //วันที่เริ่ม
                    "start_time": "00:00:00",       //เวลาเข้า
                    "start_at_place": "บ้านพฤกษา บุญสัมพันธ์-พัทยากลาง (0.2 กม.) ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",   //สถานที่
                    "start_at_latitude": 12.91458,
                    "start_at_longitude": 100.91328,
                    "end_dtm": "15 มี.ค. 2562", //สิ้นสุด
                    "end_time": "16:00:30", //เวลาออก
                    "end_at_latitude": 14.34217,
                    "end_at_longitude": 99.855388,
                    "end_at_place": "ต.จรเข้สามพัน อ.อู่ทอง จ.สุพรรณบุรี"
                },
                {
                    "device_no": "T333/30s",
                    "device_id": 18681,
                    "status": "ดับ",
                    "symbol_id": "shuttle-van",
                    "symbol_color": "#9B59B6",
                    "fuel": 100,
                    "engine": "ดับเครื่อง", // เครื่องยนต์
                    "date": "15 มี.ค. 2562",
                    "elapse": "58:12",
                    "start_dtm": "15 มี.ค. 2562",
                    "start_time": "16:54:41",
                    "start_at_place": "ต.ห้วยม่วง อ.กำแพงแสน จ.นครปฐม",
                    "start_at_latitude": 14.128066,
                    "start_at_longitude": 100.047945,
                    "end_dtm": "15 มี.ค. 2562",
                    "end_time": "17:52:53",
                    "end_at_latitude": 14.128051,
                    "end_at_longitude": 100.047916,
                    "end_at_place": "ต.ห้วยม่วง อ.กำแพงแสน จ.นครปฐม"
                },
                {
                    "device_no": "T333/30s",
                    "device_id": 18681,
                    "status": "ดับ",
                    "symbol_id": "shuttle-van",
                    "symbol_color": "#9B59B6",
                    "fuel": 100,
                    "engine": "ดับเครื่อง", // เครื่องยนต์
                    "date": "15 มี.ค. 2562",
                    "elapse": "14:40",
                    "start_dtm": "15 มี.ค. 2562",
                    "start_time": "22:47:44",
                    "start_at_place": "ปตท.เอ็นจีวี ถนนปทุมธานี-บางเลน (0.07 กม.) ต.ขุนศรี อ.ไทรน้อย จ.นนทบุรี",
                    "start_at_latitude": 14.023588,
                    "start_at_longitude": 100.285796,
                    "end_dtm": "15 มี.ค. 2562",
                    "end_time": "23:02:24",
                    "end_at_latitude": 14.023633,
                    "end_at_longitude": 100.285706,
                    "end_at_place": "ปตท.เอ็นจีวี ถนนปทุมธานี-บางเลน (0.07 กม.) ต.ขุนศรี อ.ไทรน้อย จ.นนทบุรี"
                },
                {
                    "device_no": "T333/30s",
                    "device_id": 18681,
                    "status": "ดับ",
                    "symbol_id": "shuttle-van",
                    "symbol_color": "#9B59B6",
                    "fuel": 100,
                    "engine": "ดับเครื่อง", // เครื่องยนต์
                    "date": "15 มี.ค. 2562",
                    "elapse": "7:44:13",
                    "start_dtm": "15 มี.ค. 2562",
                    "start_time": "23:49:29",
                    "start_at_place": "ต.ห้วยม่วง อ.กำแพงแสน จ.นครปฐม",
                    "start_at_latitude": 14.128098,
                    "start_at_longitude": 100.047973,
                    "end_dtm": "16 มี.ค. 2562",
                    "end_time": "07:33:42",
                    "end_at_latitude": 14.128093,
                    "end_at_longitude": 100.047973,
                    "end_at_place": "ต.ห้วยม่วง อ.กำแพงแสน จ.นครปฐม"
                }
            ],
            "summary": {
                "total_elapse": "360:57:35"
            }
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 221
}
```