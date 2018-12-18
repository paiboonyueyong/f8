# Get Report Summary Access Log (สรุปจำนวนผู้ใช้งานระบบ)

## Request Header (alway pass : token)

# getAccessSummary

## url
    http://{server}/api/report/getAccessSummary/type/period

type : (y=year, d=day)
    
## request body

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "count": 66,
            "access_dtm": "09-2018"
        },
        {
            "count": 733,
            "access_dtm": "10-2018"
        },
        {
            "count": 515,
            "access_dtm": "11-2018"
        },
        {
            "count": 343,
            "access_dtm": "12-2018"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 4
}
```