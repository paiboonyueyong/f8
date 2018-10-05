# Maintenance Template Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# newMATemplate

## url
    http://{server}/newMATemplate

## request body
```json
{
    "name": "ถ่ายน้ำมันเครื่อง เปลี่ยนไส้กรอง",
    "ma_list" : [
        {
            "ma_name": "น้ำมันเครื่อง",
            "measure_type_id": 3,
            "alert_repeat":5000,
            "is_email_alert": true,
            "is_line_alert": false
        },
        {
            "ma_name": "เปลี่ยนกรองอากาศ",
            "measure_type_id": 3,
            "alert_repeat":5000,
            "is_email_alert": true,
            "is_line_alert": false

        }
    ]
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

# deleteMATemplate

## url
    http://{server}/deleteMATemplate/{template_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```
# getMAMeasureTypeList

## url
    http://{server}/getMATemplateList/{pageNumber}/{pageSize} 

## request body
{
    "filter" : "น้ำมัันเครื่อง" 
}
## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "name": "ถ่ายน้ำมันเครื่อง เปลี่ยนไส้กรอง",
            "ma_list": [
                {
                    "ma_name": "น้ำมันเครื่อง",
                    "measure_type_id": 3,
                    "alert_repeat": 5000,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "measure_type": "ชั่วโมงการทำงาน",
                    "measure_unit": "ชม"
                },
                {
                    "ma_name": "เปลี่ยนกรองอากาศ",
                    "measure_type_id": 3,
                    "alert_repeat": 5000,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "measure_type": "ชั่วโมงการทำงาน",
                    "measure_unit": "ชม"
                }
            ],
            "template_id": 3,
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-20T18:30:39.034Z",
            "last_upd_dtm": "2018-09-20T18:30:39.034Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```

# getMATemplateInfo

## url
    http://{server}/getMATemplateInfo/{template_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "name": "ถ่ายน้ำมันเครื่อง เปลี่ยนไส้กรอง",
            "ma_list": [
                {
                    "ma_name": "น้ำมันเครื่อง",
                    "measure_type_id": 3,
                    "alert_repeat": 5000,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "measure_type": "ชั่วโมงการทำงาน",
                    "measure_unit": "ชม"
                },
                {
                    "ma_name": "เปลี่ยนกรองอากาศ",
                    "measure_type_id": 3,
                    "alert_repeat": 5000,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "measure_type": "ชั่วโมงการทำงาน",
                    "measure_unit": "ชม"
                }
            ],
            "template_id": 3,
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-20T18:30:39.034Z",
            "last_upd_dtm": "2018-09-20T18:30:39.034Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# updateMATemplate

## url
    http://{server}/updateMATemplate/{template_id} 

## request body
```json
{
    "name": "ถ่ายน้ำมันเครื่อง และ เปลี่ยนไส้กรอง",
    "ma_list": [
        {
            "ma_name": "น้ำมันเครื่อง",
            "measure_type_id": 3,
            "alert_repeat": 10000,
            "is_email_alert": true,
            "is_line_alert": false
        },
        {
            "ma_name": "เปลี่ยนกรองอากาศ",
            "measure_type_id": 3,
            "alert_repeat": 10000,
            "is_email_alert": true,
            "is_line_alert": false
        }
    ]
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
