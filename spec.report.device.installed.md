# Get Report Device Install (รายงานการติดตั้ง)

## Request Header (alway pass : token)

# getReportDeviceInstalled

## url
    http://{server}/api/report/getReportDeviceInstalled/pageNo/pageSize

## request body (หากต้องการดึงข้อมูลรถทุกคันให้ส่ง devices:[])
```json
{
    "start_date": "17-12-2018",
    "end_date": "19-12-2018"
}

```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "serial": "1234",
            "imei": "861311007894107",
            "model": "Id5",
            "device_id": 18698,
            "device_no": "ID5test",
            "install_date": "18 ธ.ค. 2561",
            "expire_date": "31 ม.ค. 2562",
            "device_group": "",
            "dealer": "MARLAR",
            "sub_dealer": "fasttest",
            "customer": "simple corporation"
        },
        {
            "imei": "1111111",
            "device_id": 18692,
            "device_no": "1กท-1287",
            "device_group": "Group 1",
            "expire_date": "21 ธ.ค. 2561",
            "install_date": "20 ธ.ค. 2561",
            "dealer": "simple corporation",
            "sub_dealer": "",
            "customer": ""
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}
```