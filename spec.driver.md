# Driver Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# newDriver

## url
    http://{server}/api/admin/newDriver 

## request body
```json
{
    "prefix":"คำนำหน้า",
    "first_name":"ชื่อ",
    "last_name":"นามสกุล",
    "gender":"เพศ ชาย หญิง",    
    "telephone":"เบอร์โทร",
    "birthday": "YYYY-MM-DD",
    "card_number":"เลขบัตรประชาชน",
    "card_registrar":"นายทะเบียนประจำ",
    "card_nation":"ประเทศ",
    "license_type":"ประเภทใบขับขี่",
    "license_gov":"ออกที่สาขา",
    "license_number":"เลขที่.",
    "license_start":"YYYY-MM-DD",
    "license_expire":"YYYY-MM-DD",
    "note":"หมายเหตุ"
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

# updateDriver

## url
    http://{server}/api/admin/updateDriver/{driver_id} 

## request body
```json
{
    "prefix":"นาย",
    "first_name":"วุฒินันท์",
    "last_name":"นามสกุล",
    "gender":"เพศ ชาย หญิง",    
    "telephone":"เบอร์โทร",
    "birthday":"YYYY-MM-DD",
    "card_number":"เลขบัตรประชาชน",
    "card_registrar":"นายทะเบียนประจำ",
    "card_nation":"ประเทศ",
    "license_type":"ประเภทใบขับขี่",
    "license_gov":"ออกที่สาขา",
    "license_number":"เลขที่.",
    "license_start":"YYYY-MM-DD",
    "license_expire":"YYYY-MM-DD",
    "note":"หมายเหตุ"
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

# deleteDriver

## url
    http://{server}/api/admin/deleteDriver/{driver_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getDriverInfo

## url
    http://{server}/api/admin/getDriverInfo/{driver_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
    {
        "prefix": "คำนำหน้า",
        "first_name": "ชื่อ",
        "last_name": "นามสกุล",
        "gender": "เพศ ชาย หญิง",
        "telephone": "เบอร์โทร",
        "birthday": "YYYY-MM-DD",
        "card_number": "เลขบัตรประชาชน",
        "card_registrar": "นายทะเบียนประจำ",
        "card_nation": "ประเทศ",
        "license_type": "ประเภทใบขับขี่",
        "license_gov": "ออกที่สาขา",
        "license_number": "เลขที่.",
        "license_start": "YYYY-MM-DD",
        "license_expire": "YYYY-MM-DD",
        "note": "หมายเหตุ",
        "driver_id": 1,
        "create_user": "Wutthin",
        "last_upd_user": "Wutthin",
        "create_dtm": "2018-09-13T17:27:58.194Z",
        "last_upd_dtm": "2018-09-13T17:27:58.194Z"
    }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getDriverList

## url
    http://{server}/api/admin/getDriverList/{pageNumber}/{pageSize} 

## request body
```json
{
    "filter" : "นาย" 
} 
```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "prefix": "คำนำหน้า",
            "first_name": "ชื่อ",
            "last_name": "นามสกุล",
            "gender": "เพศ ชาย หญิง",
            "telephone": "เบอร์โทร",
            "birthday": "2018-01-28T00:00:00.000Z",
            "card_number": "เลขบัตรประชาชน",
            "card_registrar": "นายทะเบียนประจำ",
            "card_nation": "ประเทศ",
            "driver_id": 3,
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-15T10:57:23.572Z",
            "last_upd_dtm": "2018-09-15T10:57:23.572Z",
            "birthDay": "2018-01-28"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getDeviceGroupSummary

## url
    http://{server}/api/admin/getDeviceGroupSummary 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "ทั้งหมด",
            "total": 471
        },
        {
            "_id": "7-11",
            "total": 128
        },
        {
            "_id": "",
            "total": 123
        },
        {
            "_id": "Cup Cake",
            "total": 112
        },
        {
            "_id": "Group Of Death",
            "total": 105
        },
        {
            "_id": "Group of Dead",
            "total": 2
        },
        {
            "_id": "Cup Cake222ผผผ",
            "total": 1
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 7
}
```

# newManyDriver

## url
    http://{server}/api/admin/newManyDriver 

## request body
```json
[
    {
        "prefix":"คำนำหน้า",
        "first_name":"ชื่อ",
        "last_name":"นามสกุล",
        "gender":"เพศ ชาย หญิง",    
        "telephone":"เบอร์โทร",
        "birthday": "YYYY-MM-DD",
        "card_number":"เลขบัตรประชาชน",
        "card_registrar":"นายทะเบียนประจำ",
        "card_nation":"ประเทศ",
        "license_type":"ประเภทใบขับขี่",
        "license_gov":"ออกที่สาขา",
        "license_number":"เลขที่.",
        "license_start":"YYYY-MM-DD",
        "license_expire":"YYYY-MM-DD",
        "note":"หมายเหตุ"
    },
    {
        "prefix":"คำนำหน้า",
        "first_name":"ชื่อ",
        "last_name":"นามสกุล",
        "gender":"เพศ ชาย หญิง",    
        "telephone":"เบอร์โทร",
        "birthday": "YYYY-MM-DD",
        "card_number":"เลขบัตรประชาชน",
        "card_registrar":"นายทะเบียนประจำ",
        "card_nation":"ประเทศ",
        "license_type":"ประเภทใบขับขี่",
        "license_gov":"ออกที่สาขา",
        "license_number":"เลขที่.",
        "license_start":"YYYY-MM-DD",
        "license_expire":"YYYY-MM-DD",
        "note":"หมายเหตุ"
    }
]
```
## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```
