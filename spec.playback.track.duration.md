# Get Playback Tacker Duration

## Request Header (alway pass : token)

# getPlaybackTackerDuration

## url
    http://{server}/api/report/getPlaybackTackerDuration

## request body
```json
{ 
  "imei":"868998031020627",
  "dtm": "21-11-2018 15:00:00" //"DD-MM-YYYY HH:mm"
}
```

## response (if success)

```json
{
    "RESULT_DATA": {
        "status": "ดับ",
        "status_code": 4,
        "duration": 75551,
        "current_status": "ดับ 1259 นาที ( 21 พ.ย. 2561 13:34 - 22 พ.ย. 2561 10:33 )",
        "start_dtm": "21-11-2018 13:34:10",
        "end_dtm": "22-11-2018 10:33:21"
    },
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```
