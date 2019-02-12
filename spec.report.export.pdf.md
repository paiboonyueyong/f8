# Report PDF

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# Export PDF

## url
    http://{server}/api/report/exportPdf/{reportId}

const gReportId = {
    SUMMARY: "01",
    GROUP_SUMMARY: "02",
    WORKLOAD: "03",
    ALERT: "04",
    ROUTE: "05",
    LENGTH: "06",
    PARKING: "07",
    POI: "08",
    AREA: "09",
    RFID: "10"
}

## request body
```json
{
    "title" : "report title xx",
    "result_data" : [
        {
            "device_no": "T333/30s",
            "details": [
                {
                    "device_id": 18681,
                    "status": "วิ่ง",
                    "distance": "12.8 กม.",
                    "symbol_color": "#5DADE2",
                    "symbol_id": "car-side",
                    "date": "2 ธ.ค. 2561",
                    "start_time": "06:57:44",
                    "end_time": "07:09:48",
                    "elapse": "12:04",
                    "is_driver_by_rfid": false,
                    "driver_name": "",
                    "driver_no": ""
                }
            ]
        }
    ]          
}
```
## response (if success)

```json
{
    "file_name": "h_ze_oUEfOV.pdf"
}

```

# Download PDF

## url
    http://{server}/api/report/download/{file_name}


## response (if success)

download pdf file to client




