# Get Playback

## Request Header (alway pass : token)

# getPlayback

## url
    http://{server}/api/report/getPlayback 

## request body
```json
{
  "imei" : "868998031021849",
  "start_date" : "16-10-2018",
  "start_time" : "09:00",
  "end_date" : "16-10-2018",
  "end_time" : "09:15",
  "ignore_tracker" : true // if true ignore tracker transaction
}
```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "imei": "868998031020627",
            "device_id": 18662,
            "device_group": "CubE",
            "device_model": "VIGO",
            "device_no": "1กท-1287",
            "expire_date": "30-08-2019",
            "install_date": "29-08-2018",
            "is_dlt_alert": false,
            "remarks": "เร่งเต็มพิกัด อัดสุดไมล์",
            "speed_limit": "",
            "symbol_color": "#27AE60",
            "symbol_id": "taxi",
            "driver_id": 4,
            "car_type": "รถจักรยานยนต์ (รย.12)",
            "car_province": "ตาก",
            "car_brand": "BAT",
            "total_speed_over": 28,
            "total_distance": "2.4",
            "total_stop_minute": 2444,
            "total_running_minute": 19,
            "total_machine_off_minute": 16,
            "average_speed": 5,
            "tracker": [
                {
                    "speed": 0,
                    "lat": 12.922908,
                    "lng": 100.911326,
                    "heading": "SE",
                    "gps": 10,
                    "date": "09-11-2018",
                    "time": "10:45",
                    "status": "ดับ",
                    "gsm": 22,
                    "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
                    "driver_name": "testTide",
                    "driver_contact": "-",
                    "driver_by_tracker": false,
                    "speed_over": false,
                    "distance": "0.0",
                    "direction": 1
                },
                {
                    "speed": 0,
                    "lat": 12.922906,
                    "lng": 100.911325,
                    "heading": "NE",
                    "gps": 10,
                    "date": "09-11-2018",
                    "time": "10:46",
                    "status": "ดับ",
                    "gsm": 21,
                    "place": "ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
                    "driver_name": "testTide",
                    "driver_contact": "-",
                    "driver_by_tracker": false,
                    "speed_over": false,
                    "distance": "0.0",
                    "direction": 1
                }
	]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2500
}
```
