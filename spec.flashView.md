# Flash View Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# getFlashViewCode

## url
    http://{server}/getFlashViewCode 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "flash_view_cd": "XM7lxMXXOkIa"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# newFlashView

## url
    http://{server}/newFlashView 

## request body
```json
{
    "flash_view_cd" : "XM7lxMXXOkIa",
    "cars" : [
        {
        "device_id" : "1",
        "device_no" : "4กพ-2240"
        }
    ],
    "start_date" : "2018-09-10",
    "start_time" : "00:00",
    "end_date" : "2018-12-10",
    "end_time" : "20:10",
    "remarks" : "ทดสอบ"
}
```
## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# updateFlashView

## url
    http://{server}/updateFlashView/{flash_view_cd} 

## request body
```json
{
    "cars" : [
        {
            "device_id" : "1",
            "device_no" : "4กพ-2240"
        },
        {
            "device_id" : "2",
            "device_no" : "5กพ-2240"
        },
        {
            "device_id" : "3",
            "device_no" : "5กก-1287"
        }
    ],
  "start_date" : "2018-09-11",
  "start_time" : "10:00",
  "end_date" : "2018-12-10",
  "end_time" : "20:10",
  "remarks" : "ทดสอบ"
}
```
## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# deleteFlashView

## url
    http://{server}/deleteFlashView/{flash_view_cd} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getFlashViewInfo

## url
    http://{server}/getFlashViewInfo/{flash_view_cd} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "flash_view_cd": "XM7lxMXXOkIa",
            "cars": [
                {
                    "device_id": "1",
                    "device_no": "4กพ-2240"
                },
                {
                    "device_id": "2",
                    "device_no": "5กพ-2240"
                },
                {
                    "device_id": "3",
                    "device_no": "5กก-1287"
                }
            ],
            "remarks": "ทดสอบ",
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-15T16:27:49.002Z",
            "last_upd_dtm": "2018-09-15T16:27:49.002Z",
            "start_date": "2018-09-10",
            "start_time": "00:00",
            "end_date": "2018-12-10",
            "end_time": "20:10"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getFlashViewList

## url
    http://{server}/getFlashViewList/{pageNumber}/{pageSize} 

## request body
```json
{
    "filter" : "4กพ-2240" 
} 
```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "flash_view_cd": "XM7lxMXXOkIa",
            "cars": [
                {
                    "device_id": "1",
                    "device_no": "4กพ-2240"
                },
                {
                    "device_id": "2",
                    "device_no": "5กพ-2240"
                },
                {
                    "device_id": "3",
                    "device_no": "5กก-1287"
                }
            ],
            "remarks": "ทดสอบ",
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-15T16:27:49.002Z",
            "last_upd_dtm": "2018-09-15T16:27:49.002Z",
            "start_date": "2018-09-10",
            "start_time": "00:00",
            "end_date": "2018-12-10",
            "end_time": "20:10"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```
