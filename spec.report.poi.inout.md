
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
    "startDtm":"2019/01/08 22:40",
    "endDtm":"2019/01/08 23:20",
    "timeStopMinute": 1
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
            "poi_name": "หมู่บ้านพฤกษาวิลเวล-44",
            "dtm_in": "2019-01-08T15:51:20.000Z",
            "time_in": "22:51",
            "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
            "poi_latitude": 12.914545,
            "poi_longitude": 100.913063,
            "duration": 239,
            "user_id": 2,
            "dtm_out": "2019-01-08T15:55:19.000Z",
            "time_out": "22:55"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```