# Maintenance

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# getMaintenanceInfo

## url
    http://{server}/getMaintenanceInfo/{device_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "device_id": 18662,
            "device_no": "1กท-1287",
            "ma_list": [
                {
                    "ma_name": "น้ำมันเครื่อง",
                    "measure_type_id": 2,
                    "alert_repeat": 5000,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "counter": 2500,
                    "next_alert_when": "177010",
                    "ma_list_id": 963,
                    "is_alert": false,
                    "last_alert_dtm": "1 พ.ย. 2561 23:38",
                    "measure_type": "ระยะทางการวิ่ง",
                    "measure_unit": "กม"
                },
                {
                    "ma_name": "เปลี่ยนกรองอากาศ",
                    "measure_type_id": 2,
                    "alert_repeat": 10000,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "counter": 5000,
                    "next_alert_when": "182010",
                    "ma_list_id": 964,
                    "is_alert": true,
                    "last_alert_dtm": "1 พ.ย. 2561 23:38",
                    "measure_type": "ระยะทางการวิ่ง",
                    "measure_unit": "กม"
                },
                {
                    "ma_name": "เติมน้ำหม้อน้ำ",
                    "measure_type_id": 4,
                    "alert_repeat": 10,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "counter": 2,
                    "next_alert_when": "8",
                    "ma_list_id": 965,
                    "measure_type": "ระยะเวลาที่ใช้",
                    "measure_unit": "วัน"
                },
                {
                    "ma_name": "วัดน้ำมันเครื่อง",
                    "measure_type_id": 3,
                    "alert_repeat": 2,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "counter": 0,
                    "next_alert_when": "10-11-2018",
                    "ma_list_id": 966,
                    "measure_type": "ชั่วโมงการทำงาน",
                    "measure_unit": "ชม"
                },
                {
                    "ma_name": "เปลี่ยนยาง",
                    "measure_type_id": 3,
                    "alert_repeat": 2,
                    "is_email_alert": true,
                    "is_line_alert": false,
                    "counter": 0,
                    "next_alert_when": "10-11-2018",
                    "ma_list_id": 967,
                    "measure_type": "ชั่วโมงการทำงาน",
                    "measure_unit": "ชม"
                }
            ],
            "create_user": "Admin2",
            "last_upd_user": "Admin2",
            "create_dtm": "2018-11-01T16:34:52.611Z",
            "last_upd_dtm": "2018-11-01T16:34:52.611Z",
            "ma_id": 16,
            "alert_history": [
                {
                    "ma_name": "น้ำมันเครื่อง",
                    "alert_when": "177010",
                    "alert_repeat": 5000,
                    "last_alert_dtm": "1 พ.ย. 2561 23:38",
                    "measure_type": "ระยะทางการวิ่ง",
                    "measure_unit": "กม"
                }
            ]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# updateMaintenance
    if ma_list size equals = 0 then delete transaction.
    if ma_list.ma_list_id isn't present then autu insert transaction

## url
    http://{server}/updateMaintenance

## request body
```json
{
    "device_id": 18662,
    "device_no": "1กท-1287",
    "ma_list": [
        {
            "ma_name": "น้ำมันเครื่อง",
            "measure_type_id": 2,
            "alert_repeat": 5000,
            "is_email_alert": true,
            "is_line_alert": false,
            "counter": 2500,
            "next_alert_when": "177010",
            "ma_list_id": 921,
            "remark": "ทดสอบ"
        },
        {
            "ma_name": "เปลี่ยนกรองอากาศ",
            "measure_type_id": 2,
            "alert_repeat": 10000,
            "is_email_alert": true,
            "is_line_alert": false,
            "counter": 5000,
            "next_alert_when": "182010",
            "ma_list_id": 922,
            "remark": "ทดสอบ"
        },
        {
            "ma_name": "เติมน้ำหม้อน้ำ",
            "measure_type_id": 4,
            "alert_repeat": 10,
            "is_email_alert": true,
            "is_line_alert": false,
            "counter": 2,
            "next_alert_when": "8",
            "ma_list_id": 923,
            "remark": "ทดสอบ"
        },
        {
            "ma_name": "วัดน้ำมันเครื่อง",
            "measure_type_id": 3,
            "alert_repeat": 2,
            "is_email_alert": true,
            "is_line_alert": false,
            "counter": 0,
            "next_alert_when": "10-11-2018",
            "ma_list_id": 924,
            "remark": "ทดสอบ"
        },
        {
            "ma_name": "เปลี่ยนยาง",
            "measure_type_id": 3,
            "alert_repeat": 2,
            "is_email_alert": true,
            "is_line_alert": false,
            "counter": 0,
            "next_alert_when": "10-11-2018",
            "remark": "ทดสอบ"
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

# resetMAAlert
    if ma_list size equals = 0 then delete transaction.
    if ma_list.ma_list_id isn't present then autu insert transaction

## url
    http://{server}/resetMAAlert/{device_id}/{ma_list_id}

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getMaintenanceAlertList

## url
    http://{server}/getMaintenanceAlertList/{pageNo}/{pageSize}

## request body
{
    "filter" : "",
    "isGroupOrder" : true
}

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "ma_name": "น้ำมันเครื่อง",
            "measure_type_id": 2,
            "alert_repeat": 5000,
            "is_email_alert": true,
            "is_line_alert": false,
            "counter": 2500,
            "next_alert_when": "177010",
            "ma_list_id": 933,
            "last_alert_dtm": "01-11-2018 22:47:11",
            "is_alert": true,
            "measure_type": "ระยะทางการวิ่ง",
            "measure_unit": "กม",
            "device_id": 18662,
            "device_no": "1กท-1287",
            "device_group": "Group",
            "remark": "หมายเหตุ"
        },
        {
            "ma_name": "เปลี่ยนกรองอากาศ",
            "measure_type_id": 2,
            "alert_repeat": 10000,
            "is_email_alert": true,
            "is_line_alert": false,
            "counter": 5000,
            "next_alert_when": "12000",
            "is_alert": true,
            "email_sent": false,
            "line_sent": false,
            "ma_list_id": 959,
            "measure_type": "ระยะทางการวิ่ง",
            "measure_unit": "กม",
            "device_id": 18665,
            "device_no": "1ศย-2240",
            "device_group": "Group",
            "remark": "หมายเหตุ"
        },
        {
            "ma_name": "เปลี่ยนยาง",
            "measure_type_id": 3,
            "alert_repeat": 2,
            "is_email_alert": true,
            "is_line_alert": false,
            "counter": 0,
            "next_alert_when": "10-11-2018",
            "is_alert": true,
            "email_sent": false,
            "line_sent": false,
            "ma_list_id": 962,
            "measure_type": "ชั่วโมงการทำงาน",
            "measure_unit": "ชม",
            "device_id": 18665,
            "device_no": "1ศย-2240",
            "device_group": "Group",
            "remark": "หมายเหตุ"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 3
}
```

# newMaintenance
    Maybe not use because if doesn't pass ma_list_id in ma_list [] in update method then auto new

## url
    http://{server}/newMaintenance

## request body
```json
{
    "device_id": 18662,
    "device_no": "1กท-1287",
    "ma_list" : [
        {
            "ma_name": "น้ำมันเครื่อง",
            "measure_type_id": 2,
            "alert_repeat":5000,
            "is_email_alert": true,
            "is_line_alert": false,
		    "counter": 2500,
            "next_alert_when": "177010",
            "remark": "หมายเหตุ"
        },
        {
            "ma_name": "เปลี่ยนกรองอากาศ",
            "measure_type_id": 2,
            "alert_repeat":10000,
            "is_email_alert": true,
            "is_line_alert": false,
		    "counter": 5000,
            "next_alert_when": "182010",
            "remark": "หมายเหตุ"
        },
        {
            "ma_name": "เติมน้ำหม้อน้ำ",
            "measure_type_id": 4,
            "alert_repeat":10,
            "is_email_alert": true,
            "is_line_alert": false,
		    "counter": 2,
            "next_alert_when": "8",
            "remark": "หมายเหตุ"
        },
        {
            "ma_name": "วัดน้ำมันเครื่อง",
            "measure_type_id": 3,
            "alert_repeat":2,
            "is_email_alert": true,
            "is_line_alert": false,
		    "counter": 0,
            "next_alert_when": "10-11-2018",
            "remark": "หมายเหตุ"
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

# deleteMaintenance
    Maybe not use because if pass ma_list is [] in update method then auto delete

## url
    http://{server}/deleteMaintenance/{device_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# moveMaintenance
    Move maintenance list to another device

## url
    http://{server}/moveMaintenance/{device_id}/{new_device_id}

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```