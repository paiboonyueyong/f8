# Device Assignment Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# assignDevice

## url
    http://{server}/assignDevice/{userId}/{deviceId}

## request body (No)

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```

# cancelDevice

## url
    http://{server}/cancelDevice/{userId}/{deviceId}

## request body (No)

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getUserDeviceRelate

## url
    http://{server}/getUserDeviceRelated/{deviceId}/{pageNo}/{pageSize}


## request body (No)


## response (if success)

```json

{
    "RESULT_DATA": [
        {
            "_id": "5b9e208670fccd37780a6a4b",
            "login_name": "kellreseller",
            "first_name": "ไพบูลย์2",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "password": "123456",
            "is_send_email_alert_overdue": false,
            "is_auto_dispermit": true,
            "reseller_note": "test note",
            "privileges": {
                "is_view_tracking": true,
                "is_view_poi": true,
                "is_edit_poi": true,
                "is_view_history": false,
                "is_send_command": true,
                "is_view_report": false
            },
            "user_id": 6,
            "parent_id": 2,
            "user_level": 3,
            "create_user": "kelly dealer (2)",
            "create_dtm": "2018-09-16T09:21:10.093Z",
            "last_login_dtm": "2018-09-30T13:04:21.579Z",
            "last_upd_dtm": "2018-10-09T09:22:40.495Z",
            "last_upd_user": "kelly (1)",
            "devices": [
                {
                    "device_id": 11142
                },
                {
                    "device_id": 11141
                },
                {
                    "device_id": 11140
                },
                {
                    "device_id": 11139
                },
                {
                    "device_id": 11143
                }
            ]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
        
```
