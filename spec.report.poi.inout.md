
# Get Report Poi In-Out (เข้า-ออก POI)

## Request Header (alway pass : token)

# getReportPoiInOut

## url
    http://{server}/api/report/getReportPoiInOut/{pageNo}/{pageSize}

## request body
```json

{
    "deviceId":18662,
    "poiId":6,
    "startDtm":"08/01/2019 22:40", // DD/MM/YYYY HH:MM
    "endDtm":"08/01/2019 23:20", // DD/MM/YYYY HH:MM
    "timeStopMinute": 1 // duration of car stop (unit is minute)
}

```

## response (if success)

```json
{
    				
    "RESULT_DATA": [
        {
            "device_id": 18662,
            "device_no": "1กย-1287",
            "poi_id": 6,
            "poi_name": "หมู่บ้านพฤกษาวิลเวล-44", // ถึงสถานที่
            "dtm_in": "08/01/2019", // วันที่
            "time_in": "22:51", // เวลาเข้า
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี", // ที่อยู่	
            "poi_latitude": 12.914545, // ละติจูด	
            "poi_longitude": 100.913063, // ลองติจูด
            "duration": 239, // เวลาที่อยู่ (นาที)
            "user_id": 2,
            "dtm_out": "08/01/2019",
            "time_out": "22:55" //เวลาออก
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}

```