# Measure Type

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# newMAMeasureType

## url
    http://{server}/newMAMeasureType 

## request body
```json
{
  "measure_type":"ระยะทางการวิ่ง, ชั่วโมงการทำงาน, ระยะเวลาที่ใช้",
  "measure_unit":"{ 1 : Km., 2 : Hours, 3 : Days}"
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

# deleteMAMeasureType

## url
    http://{server}/deleteMAMeasureType/{_id} 

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
    http://{server}/getMAMeasureTypeList 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "measure_type": "ระยะเวลาที่ใช้",
            "measure_unit": "วัน",
            "measure_type_id": 4,
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-20T18:05:36.561Z",
            "last_upd_dtm": "2018-09-20T18:05:36.561Z"
        },
        {
            "measure_type": "ชั่วโมงการทำงาน",
            "measure_unit": "ชม",
            "measure_type_id": 3,
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-20T18:05:32.957Z",
            "last_upd_dtm": "2018-09-20T18:05:32.957Z"
        },
        {
            "measure_type": "ระยะทางการวิ่ง",
            "measure_unit": "กม",
            "measure_type_id": 2,
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-20T18:04:51.321Z",
            "last_upd_dtm": "2018-09-20T18:04:51.321Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 3
}
```

# getMAMeasureType

## url
    http://{server}/getMAMeasureType/{measure_type_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "measure_type": "ระยะเวลาที่ใช้",
            "measure_unit": "วัน",
            "measure_type_id": 4,
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-20T18:05:36.561Z",
            "last_upd_dtm": "2018-09-20T18:05:36.561Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# updateMAMeasureType

## url
    http://{server}/updateMAMeasureType/{measure_type_id} 

## request body
```json
{
    "measure_type": "ระยะเวลาที่ใช้",
    "measure_unit": "วัน"
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
