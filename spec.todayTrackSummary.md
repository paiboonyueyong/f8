# Get Today Tracking Summary

## Request Header (alway pass : token)

# getPlayback

## url
    http://{server}/api/report/getTodayTrackSummary

## request body
```json
{ 
  "imei":"868998031020627"
}
```

## response (if success)

```json
{
    "RESULT_DATA": {
        "device_no": "1กท-1287",
        "average_speed": "8",
        "speed_over_times": 4,
        "total_distance": "1.0",
        "running_period": "12",
        "stop_priod": "41",
        "machine_off_period": "624",
        "current_status": "ดับ 621 นาที ( 22 พ.ย. 2561 11:35:01 - 22 พ.ย. 2561 21:55:31 )"
    },
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```
