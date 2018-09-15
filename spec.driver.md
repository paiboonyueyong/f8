# Driver Management 

## header (alway pass) 
    (user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        ->  admin = "admin" 
        -> dealer = "dealer" 
        -> reseller = "reseller" 

# newDriver 

## url 
    http://{server}/newDriver  

## body 
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
    http://{server}/updateDriver/{driver_id}  

## body 
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
    http://{server}/deleteDriver/{driver_id}  

## body 

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
    http://{server}/getDriverInfo/{driver_id}  

## body 

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
    http://{server}/getDriverList/{pageNumber}/{pageSize}  

## body 
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
