# Get Report Summary Access Log (สรุปจำนวนผู้ใช้งานระบบ)

## Request Header (alway pass : token)

# getAccessSummary

## url
    http://{server}/api/report/getAccessSummary/days

## request body

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "count": 1,
            "access_date": "7 ธ.ค. 2561",
            "access_dtm": "2018-12-06T17:00:00.000Z"
        },
        {
            "count": 3,
            "access_date": "8 ธ.ค. 2561",
            "access_dtm": "2018-12-07T17:00:00.000Z"
        },
        {
            "count": 10,
            "access_date": "9 ธ.ค. 2561",
            "access_dtm": "2018-12-08T17:00:00.000Z"
        },
        {
            "count": 27,
            "access_date": "10 ธ.ค. 2561",
            "access_dtm": "2018-12-09T17:00:00.000Z"
        },
        {
            "count": 20,
            "access_date": "11 ธ.ค. 2561",
            "access_dtm": "2018-12-10T17:00:00.000Z"
        },
        {
            "count": 15,
            "access_date": "12 ธ.ค. 2561",
            "access_dtm": "2018-12-11T17:00:00.000Z"
        },
        {
            "count": 8,
            "access_date": "13 ธ.ค. 2561",
            "access_dtm": "2018-12-12T17:00:00.000Z"
        },
        {
            "count": 3,
            "access_date": "14 ธ.ค. 2561",
            "access_dtm": "2018-12-13T17:00:00.000Z"
        },
        {
            "count": 8,
            "access_date": "15 ธ.ค. 2561",
            "access_dtm": "2018-12-14T17:00:00.000Z"
        },
        {
            "count": 9,
            "access_date": "16 ธ.ค. 2561",
            "access_dtm": "2018-12-15T17:00:00.000Z"
        },
        {
            "count": 24,
            "access_date": "17 ธ.ค. 2561",
            "access_dtm": "2018-12-16T17:00:00.000Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 11
}
```