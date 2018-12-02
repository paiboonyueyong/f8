# Get Tracker Event Alert

## Request Header (alway pass : token)

# getList

## url
    http://{server}/api/report/getTrackerEventAlert

## request body
```json
{ 
    "devices": [], /* fliter device */
    "getNotify" : true, /* get message notification */
    "filter": "สายgps" /* filter alert type */
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "is_notify": false, /* true = new notification is coming */
            "alert": [
                {
                    "_id": "5c0385d3b710ba37e02d1fbb",
                    "device_id": 18662,
                    "device_no": "1กย-1287",
                    "symbol_color": "#27AE60",
                    "symbol_id": "taxi",
                    "alert_type_id": "E5",
                    "alert_type": "สายGPSถูกตัด",
                    "latitude": 12.91456,
                    "longitude": 100.912996,
                    "tracking_dtm": "2018-12-02T08:39:31.000Z",
                    "date": "2 ธ.ค.",
                    "time": "15:39"
                },
                {
                    "_id": "5c0385d3b710ba37e02d1fbc",
                    "device_id": 18662,
                    "device_no": "1กย-1287",
                    "symbol_color": "#27AE60",
                    "symbol_id": "taxi",
                    "alert_type_id": "E4",
                    "alert_type": "ไม่ได้ไฟจากรถ",
                    "latitude": 12.91456,
                    "longitude": 100.912996,
                    "tracking_dtm": "2018-12-02T08:39:31.000Z",
                    "date": "2 ธ.ค.",
                    "time": "15:39"
                },
                {
                    "_id": "5c0385d3b710ba37e02d1fba",
                    "device_id": 18662,
                    "device_no": "ID5",
                    "symbol_id": "car-side",
                    "symbol_color": "#5DADE2",
                    "alert_type_id": "E3",
                    "alert_type": "แบตเตอรี่รถอ่อน",
                    "latitude": 12.91456,
                    "longitude": 100.912996,
                    "tracking_dtm": "2018-12-02T08:39:31.000Z",
                    "date": "2 ธ.ค.",
                    "time": "15:39"
                }
            ]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 3
}
```
