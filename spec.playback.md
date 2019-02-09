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
   "RESULT_DATA":[
      {
         "imei":"868998035990486",
         "device_id":18773,
         "device_no":"วีโก้",
         "driver_id":"",
         "symbol_color":"",
         "symbol_id":"",
         "total_speed_over":0,
         "total_distance":"23.0",
         "total_stop_minute":21,
         "total_running_minute":52,
         "total_machine_off_minute":165,
         "average_speed":29,
         "tracker":[
            {
               "speed":0,
               "lat":12.914476,
               "lng":100.913126,
               "heading":"SW",
               "gps":5,
               "date":"09-02-2019",
               "time":"18:02:40",
               "status":"จอด",
               "gsm":15,
               "direction":204,
               "fuel":100,
               "place":"ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
               "driver_by_tracker":false,
               "driver_name":"",
               "driver_no":"",
               "driver_contact":"",
               "speed_over":false,
               "distance":"0.0"
            },
            {
               "speed":1,
               "lat":12.914495,
               "lng":100.913203,
               "heading":"E",
               "gps":5,
               "date":"09-02-2019",
               "time":"18:03:21",
               "status":"ดับ",
               "gsm":15,
               "direction":80,
               "fuel":100,
               "place":"ต.หนองปรือ อ.บางละมุง จ.ชลบุรี",
               "driver_by_tracker":false,
               "driver_name":"",
               "driver_no":"",
               "driver_contact":"",
               "speed_over":false,
               "distance":"0.0"
            }
         ]
      }
   ],
   "RESULT_STATUS":"000",
   "RESULT_MESSAGE":"Successfull",
   "RESULT_TOTAL":323
}
```
