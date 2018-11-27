# Tracking Realtime Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# getTrackingList

## url
    http://{server2}/getTrackingList

## request body (body empty = getAll)

```json

{
 "filter" : [{
            "imei": "868998031020627",
            "device_id": 18685,
            "device_no": "18685",
            "id": "111"
        },
        {
            "imei": "868998031020628",
            "device_id": 18686,
            "device_no": "18686",
            "id": "1"
        }]
}

```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "imei": "868998031020627",
            "latitude": 12.914493,
            "longitude": 100.91308,
            "speed": 0,
            "heading": "E",
            "status": "ดับ",
            "place": "12.914493 100.91308",
            "date": "30-10-2018",
            "time": "17:37",
            "driver_name": "",
            "driver_no": "",
            "device_info": {
                "device_id": 18662,
                "imei": "868998031020627",
                "device_no": "1กท-1287",
                "device_model": "VIGO",
                "symbol_id": "car.jpeg",
                "symbol_color": "Blue",
                "device_driver": "",
                "speed_limit": 80,
                "is_dlt_alert": true
            },
            "tracking_dtm": "2018-10-30T10:37:14.000Z",
            "last_upd_dtm": "2018-10-30T10:39:01.313Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}

```


# getNearTrackingList

## url
    http://{server2}/getNearTrackingList/{poiId}

## no request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "device_no": "1กท-1287",
            "status": "ดับ",
            "distance": 263.86
        },
        {
            "device_no": "ID5",
            "status": "ดับ",
            "distance": 263.872
        },
        {
            "device_no": "T333/30s",
            "status": "จอด",
            "distance": 267.511
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# getNearTrackingList

## url
    http://{server2}/getAddressLocation/

## body

```json

{
	"latitude":13,
	"longitude":100
}

```

## response (if success)

```json
{
    "RESULT_DATA": "ต.หนองขนาน อ.เมืองเพชรบุรี จ.เพชรบุรี",
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```