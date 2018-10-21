# Car Type Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# newCarType

## url
    http://{server}/newCarType

## request body
```json
{
  "car_type": "ดับเครื่อง"
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

# updateCarType

## url
    http://{server}/updateCarType/{car_type_id} 

## request body
```json
{
  "car_type": "ดับเครื่อง"
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

# deleteCarType

## url
    http://{server}/deleteCarType/{car_type_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getCommandInfo

## url
    http://{server}/getCarTypeInfo/{car_type_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
            {
                "command_id": 3,
                "command_name": "ดับเครื่อง",
                "create_user": "Wutthin",
                "last_upd_user": "Wutthin",
                "create_dtm": "2018-09-30T15:43:33.288Z",
                "last_upd_dtm": "2018-09-30T16:21:38.602Z"
            }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getCarTypeList

## url
    http://{server}/getCarTypeList

## request body
```json
{
  "filter": "โดยสาร"
}
```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "car_type_id": 1,
            "car_type": "-- ไม่มี --"
        },
        {
            "car_type_id": 2,
            "car_type": "รถโดยสาร ไม่ได้ระบุมาตรฐานและประเภทรถ"
        },
        {
            "car_type_id": 3,
            "car_type": "รถบรรทุก ไม่ได้ระบุลักษณะและประเภทรถ"
        },
        {
            "car_type_id": 4,
            "car_type": "รถโดยสาร มาตรฐาน 1 ก ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 5,
            "car_type": "รถโดยสาร มาตรฐาน 1 ก ส่วนบุคคล"
        },
        {
            "car_type_id": 6,
            "car_type": "รถโดยสาร มาตรฐาน 1 ก ไม่ประจำทาง"
        },
        {
            "car_type_id": 7,
            "car_type": "รถโดยสาร มาตรฐาน 1 ก ประจำทาง"
        },
        {
            "car_type_id": 8,
            "car_type": "รถโดยสาร มาตรฐาน 1 ข ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 9,
            "car_type": "รถโดยสาร มาตรฐาน 1 ข ส่วนบุคคล"
        },
        {
            "car_type_id": 10,
            "car_type": "รถโดยสาร มาตรฐาน 1 ข ไม่ประจำทาง"
        },
        {
            "car_type_id": 11,
            "car_type": "รถโดยสาร มาตรฐาน 1 ข ประจำทาง"
        },
        {
            "car_type_id": 12,
            "car_type": "รถโดยสาร มาตรฐาน 2 ก ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 13,
            "car_type": "รถโดยสาร มาตรฐาน 2 ก ส่วนบุคคล"
        },
        {
            "car_type_id": 14,
            "car_type": "รถโดยสาร มาตรฐาน 2 ก ไม่ประจำทาง"
        },
        {
            "car_type_id": 15,
            "car_type": "รถโดยสาร มาตรฐาน 2 ก ประจำทาง"
        },
        {
            "car_type_id": 16,
            "car_type": "รถโดยสาร มาตรฐาน 2 ข ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 17,
            "car_type": "รถโดยสาร มาตรฐาน 2 ข ส่วนบุคคล"
        },
        {
            "car_type_id": 18,
            "car_type": "รถโดยสาร มาตรฐาน 2 ข ไม่ประจำทาง"
        },
        {
            "car_type_id": 19,
            "car_type": "รถโดยสาร มาตรฐาน 2 ข ประจำทาง"
        },
        {
            "car_type_id": 20,
            "car_type": "รถโดยสาร มาตรฐาน 2 ค ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 21,
            "car_type": "รถโดยสาร มาตรฐาน 2 ค ส่วนบุคคล"
        },
        {
            "car_type_id": 22,
            "car_type": "รถโดยสาร มาตรฐาน 2 ค ไม่ประจำทาง"
        },
        {
            "car_type_id": 23,
            "car_type": "รถโดยสาร มาตรฐาน 2 ค ประจำทาง"
        },
        {
            "car_type_id": 24,
            "car_type": "รถโดยสาร มาตรฐาน 2 ง ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 25,
            "car_type": "รถโดยสาร มาตรฐาน 2 ง ส่วนบุคคล"
        },
        {
            "car_type_id": 26,
            "car_type": "รถโดยสาร มาตรฐาน 2 ง ไม่ประจำทาง"
        },
        {
            "car_type_id": 27,
            "car_type": "รถโดยสาร มาตรฐาน 2 ง ประจำทาง"
        },
        {
            "car_type_id": 28,
            "car_type": "รถโดยสาร มาตรฐาน 2 จ ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 29,
            "car_type": "รถโดยสาร มาตรฐาน 2 จ ส่วนบุคคล"
        },
        {
            "car_type_id": 30,
            "car_type": "selected>รถโดยสาร มาตรฐาน 2 จ ไม่ประจำทาง"
        },
        {
            "car_type_id": 31,
            "car_type": "รถโดยสาร มาตรฐาน 2 จ ประจำทาง"
        },
        {
            "car_type_id": 32,
            "car_type": "รถโดยสาร มาตรฐาน 3 ก ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 33,
            "car_type": "รถโดยสาร มาตรฐาน 3 ก ส่วนบุคคล"
        },
        {
            "car_type_id": 34,
            "car_type": "รถโดยสาร มาตรฐาน 3 ก ไม่ประจำทาง"
        },
        {
            "car_type_id": 35,
            "car_type": "รถโดยสาร มาตรฐาน 3 ก ประจำทาง"
        },
        {
            "car_type_id": 36,
            "car_type": "รถโดยสาร มาตรฐาน 3 ข ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 37,
            "car_type": "รถโดยสาร มาตรฐาน 3 ข ส่วนบุคคล"
        },
        {
            "car_type_id": 38,
            "car_type": "รถโดยสาร มาตรฐาน 3 ข ไม่ประจำทาง"
        },
        {
            "car_type_id": 39,
            "car_type": "รถโดยสาร มาตรฐาน 3 ข ประจำทาง"
        },
        {
            "car_type_id": 40,
            "car_type": "รถโดยสาร มาตรฐาน 3 ค ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 41,
            "car_type": "รถโดยสาร มาตรฐาน 3 ค ส่วนบุคคล"
        },
        {
            "car_type_id": 42,
            "car_type": "รถโดยสาร มาตรฐาน 3 ค ไม่ประจำทาง"
        },
        {
            "car_type_id": 43,
            "car_type": "รถโดยสาร มาตรฐาน 3 ค ประจำทาง"
        },
        {
            "car_type_id": 44,
            "car_type": "รถโดยสาร มาตรฐาน 3 ง ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 45,
            "car_type": "รถโดยสาร มาตรฐาน 3 ง ส่วนบุคคล"
        },
        {
            "car_type_id": 46,
            "car_type": "รถโดยสาร มาตรฐาน 3 ง ไม่ประจำทาง"
        },
        {
            "car_type_id": 47,
            "car_type": "รถโดยสาร มาตรฐาน 3 ง ประจำทาง"
        },
        {
            "car_type_id": 48,
            "car_type": "รถโดยสาร มาตรฐาน 3 จ ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 49,
            "car_type": "รถโดยสาร มาตรฐาน 3 จ ส่วนบุคคล"
        },
        {
            "car_type_id": 50,
            "car_type": "รถโดยสาร มาตรฐาน 3 จ ไม่ประจำทาง"
        },
        {
            "car_type_id": 51,
            "car_type": "รถโดยสาร มาตรฐาน 3 จ ประจำทาง"
        },
        {
            "car_type_id": 52,
            "car_type": "รถโดยสาร มาตรฐาน 3 ฉ ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 53,
            "car_type": "รถโดยสาร มาตรฐาน 3 ฉ ส่วนบุคคล"
        },
        {
            "car_type_id": 54,
            "car_type": "รถโดยสาร มาตรฐาน 3 ฉ ไม่ประจำทาง"
        },
        {
            "car_type_id": 55,
            "car_type": "รถโดยสาร มาตรฐาน 3 ฉ ประจำทาง"
        },
        {
            "car_type_id": 56,
            "car_type": "รถโดยสาร มาตรฐาน 4 ก ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 57,
            "car_type": "รถโดยสาร มาตรฐาน 4 ก ส่วนบุคคล"
        },
        {
            "car_type_id": 58,
            "car_type": "รถโดยสาร มาตรฐาน 4 ก ไม่ประจำทาง"
        },
        {
            "car_type_id": 59,
            "car_type": "รถโดยสาร มาตรฐาน 4 ก ประจำทาง"
        },
        {
            "car_type_id": 60,
            "car_type": "รถโดยสาร มาตรฐาน 4 ข ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 61,
            "car_type": "รถโดยสาร มาตรฐาน 4 ข ส่วนบุคคล"
        },
        {
            "car_type_id": 62,
            "car_type": "รถโดยสาร มาตรฐาน 4 ข ไม่ประจำทาง"
        },
        {
            "car_type_id": 63,
            "car_type": "รถโดยสาร มาตรฐาน 4 ข ประจำทาง"
        },
        {
            "car_type_id": 64,
            "car_type": "รถโดยสาร มาตรฐาน 4 ค ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 65,
            "car_type": "รถโดยสาร มาตรฐาน 4 ค ส่วนบุคคล"
        },
        {
            "car_type_id": 66,
            "car_type": "รถโดยสาร มาตรฐาน 4 ค ไม่ประจำทาง"
        },
        {
            "car_type_id": 67,
            "car_type": "รถโดยสาร มาตรฐาน 4 ค ประจำทาง"
        },
        {
            "car_type_id": 68,
            "car_type": "รถโดยสาร มาตรฐาน 4 ง ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 69,
            "car_type": "รถโดยสาร มาตรฐาน 4 ง ส่วนบุคคล"
        },
        {
            "car_type_id": 70,
            "car_type": "รถโดยสาร มาตรฐาน 4 ง ไม่ประจำทาง"
        },
        {
            "car_type_id": 71,
            "car_type": "รถโดยสาร มาตรฐาน 4 ง ประจำทาง"
        },
        {
            "car_type_id": 72,
            "car_type": "รถโดยสาร มาตรฐาน 4 จ ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 73,
            "car_type": "รถโดยสาร มาตรฐาน 4 จ ส่วนบุคคล"
        },
        {
            "car_type_id": 74,
            "car_type": "รถโดยสาร มาตรฐาน 4 จ ไม่ประจำทาง"
        },
        {
            "car_type_id": 75,
            "car_type": "รถโดยสาร มาตรฐาน 4 จ ประจำทาง"
        },
        {
            "car_type_id": 76,
            "car_type": "รถโดยสาร มาตรฐาน 4 ฉ ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 77,
            "car_type": "รถโดยสาร มาตรฐาน 4 ฉ ส่วนบุคคล"
        },
        {
            "car_type_id": 78,
            "car_type": "รถโดยสาร มาตรฐาน 4 ฉ ไม่ประจำทาง"
        },
        {
            "car_type_id": 79,
            "car_type": "รถโดยสาร มาตรฐาน 4 ฉ ประจำทาง"
        },
        {
            "car_type_id": 80,
            "car_type": "รถโดยสาร มาตรฐาน 5 ก ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 81,
            "car_type": "รถโดยสาร มาตรฐาน 5 ก ส่วนบุคคล"
        },
        {
            "car_type_id": 82,
            "car_type": "รถโดยสาร มาตรฐาน 5 ก ไม่ประจำทาง"
        },
        {
            "car_type_id": 83,
            "car_type": "รถโดยสาร มาตรฐาน 5 ก ประจำทาง"
        },
        {
            "car_type_id": 84,
            "car_type": "รถโดยสาร มาตรฐาน 5 ข ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 85,
            "car_type": "รถโดยสาร มาตรฐาน 5 ข ส่วนบุคคล"
        },
        {
            "car_type_id": 86,
            "car_type": "รถโดยสาร มาตรฐาน 5 ข ไม่ประจำทาง"
        },
        {
            "car_type_id": 87,
            "car_type": "รถโดยสาร มาตรฐาน 5 ข ประจำทาง"
        },
        {
            "car_type_id": 88,
            "car_type": "รถโดยสาร มาตรฐาน 6 ก ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 89,
            "car_type": "รถโดยสาร มาตรฐาน 6 ก ส่วนบุคคล"
        },
        {
            "car_type_id": 90,
            "car_type": "รถโดยสาร มาตรฐาน 6 ก ไม่ประจำทาง"
        },
        {
            "car_type_id": 91,
            "car_type": "รถโดยสาร มาตรฐาน 6 ก ประจำทาง"
        },
        {
            "car_type_id": 92,
            "car_type": "รถโดยสาร มาตรฐาน 6 ข ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 93,
            "car_type": "รถโดยสาร มาตรฐาน 6 ข ส่วนบุคคล"
        },
        {
            "car_type_id": 94,
            "car_type": "รถโดยสาร มาตรฐาน 6 ข ไม่ประจําทาง"
        },
        {
            "car_type_id": 95,
            "car_type": "รถโดยสาร มาตรฐาน 6 ข ประจําทาง"
        },
        {
            "car_type_id": 96,
            "car_type": "รถโดยสาร มาตรฐาน 7 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 97,
            "car_type": "รถโดยสาร มาตรฐาน 7 ส่วนบุคคล"
        },
        {
            "car_type_id": 98,
            "car_type": "รถโดยสาร มาตรฐาน 7 ไม่ประจําทาง"
        },
        {
            "car_type_id": 99,
            "car_type": "รถบรรทุก ลักษณะ 1 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 100,
            "car_type": "รถบรรทุก ลักษณะ 1 ส่วนบุคคล"
        },
        {
            "car_type_id": 101,
            "car_type": "รถบรรทุก ลักษณะ 1 ไม่ประจําทาง"
        },
        {
            "car_type_id": 102,
            "car_type": "รถบรรทุก ลักษณะ 2 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 103,
            "car_type": "รถบรรทุก ลักษณะ 2 ส่วนบุคคล"
        },
        {
            "car_type_id": 104,
            "car_type": "รถบรรทุก ลักษณะ 2 ไม่ประจําทาง"
        },
        {
            "car_type_id": 105,
            "car_type": "รถบรรทุก ลักษณะ 3 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 106,
            "car_type": "รถบรรทุก ลักษณะ 3 ส่วนบุคคล"
        },
        {
            "car_type_id": 107,
            "car_type": "รถบรรทุก ลักษณะ 3 ไม่ประจําทาง"
        },
        {
            "car_type_id": 108,
            "car_type": "รถบรรทุก ลักษณะ 4 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 109,
            "car_type": "รถบรรทุก ลักษณะ 4 ส่วนบุคคล"
        },
        {
            "car_type_id": 110,
            "car_type": "รถบรรทุก ลักษณะ 4 ไม่ประจําทาง"
        },
        {
            "car_type_id": 111,
            "car_type": "รถบรรทุกวัตถุอันตราย ประจำทาง"
        },
        {
            "car_type_id": 112,
            "car_type": "รถบรรทุก ลักษณะ 5 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 113,
            "car_type": "รถบรรทุก ลักษณะ 5 ส่วนบุคคล"
        },
        {
            "car_type_id": 114,
            "car_type": "รถบรรทุก ลักษณะ 5 ไม่ประจําทาง"
        },
        {
            "car_type_id": 115,
            "car_type": "รถบรรทุก ลักษณะ 6 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 116,
            "car_type": "รถบรรทุก ลักษณะ 6 ส่วนบุคคล"
        },
        {
            "car_type_id": 117,
            "car_type": "รถบรรทุก ลักษณะ 6 ไม่ประจําทาง"
        },
        {
            "car_type_id": 118,
            "car_type": "รถบรรทุก ลักษณะ 7 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 119,
            "car_type": "รถบรรทุก ลักษณะ 7 ส่วนบุคคล"
        },
        {
            "car_type_id": 120,
            "car_type": "รถบรรทุก ลักษณะ 7 ไม่ประจำทาง"
        },
        {
            "car_type_id": 121,
            "car_type": "รถบรรทุก ลักษณะ 8 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 122,
            "car_type": "รถบรรทุก ลักษณะ 8 ส่วนบุคคล"
        },
        {
            "car_type_id": 123,
            "car_type": "รถบรรทุก ลักษณะ 8 ไม่ประจำทาง"
        },
        {
            "car_type_id": 124,
            "car_type": "รถบรรทุก ลักษณะ 9 ไม่ได้ระบุประเภทรถ"
        },
        {
            "car_type_id": 125,
            "car_type": "รถบรรทุก ลักษณะ 9 ไม่ได้ระบุประเภทรถ (รถวัตถุอันตราย)"
        },
        {
            "car_type_id": 126,
            "car_type": "รถบรรทุก ลักษณะ 9 ส่วนบุคคล"
        },
        {
            "car_type_id": 127,
            "car_type": "รถบรรทุก ลักษณะ 9 ส่วนบุคคล (รถวัตถุอันตราย)"
        },
        {
            "car_type_id": 128,
            "car_type": "รถบรรทุก ลักษณะ 9 ไม่ประจำทาง"
        },
        {
            "car_type_id": 129,
            "car_type": "รถบรรทุก ลักษณะ 9 ไม่ประจำทาง (รถวัตถุอันตราย)"
        },
        {
            "car_type_id": 130,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.3)"
        },
        {
            "car_type_id": 131,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.3)"
        },
        {
            "car_type_id": 132,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.3)"
        },
        {
            "car_type_id": 133,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.3)"
        },
        {
            "car_type_id": 134,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.4)"
        },
        {
            "car_type_id": 135,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.4)"
        },
        {
            "car_type_id": 136,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.4)"
        },
        {
            "car_type_id": 137,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.4)"
        },
        {
            "car_type_id": 138,
            "car_type": "รถยนต์บรรทุกส่วนบุคคล (รย.4)"
        },
        {
            "car_type_id": 139,
            "car_type": "รถยนต์รับจ้างระหว่างจังหวัด (รย.5)"
        },
        {
            "car_type_id": 140,
            "car_type": "รถยนต์รับจ้างบรรทุกคนโดยสารไม่เกินเจ็ดคน (รย.6)"
        },
        {
            "car_type_id": 141,
            "car_type": "รถยนต์สี่ล้อเล็กรับจ้าง (รย.7)"
        },
        {
            "car_type_id": 142,
            "car_type": "รถยนต์รับจ้างสามล้อ (รย.8)"
        },
        {
            "car_type_id": 143,
            "car_type": "รถยนต์บริการธุรกิจ (รย.9)"
        },
        {
            "car_type_id": 144,
            "car_type": "รถยนต์บริการทัศนาจร (รย.10)"
        },
        {
            "car_type_id": 145,
            "car_type": "รถยนต์บริการให้เช่า (รย.11)"
        },
        {
            "car_type_id": 146,
            "car_type": "รถจักรยานยนต์ (รย.12)"
        },
        {
            "car_type_id": 147,
            "car_type": "รถแทรกเตอร์ (รย.13)"
        },
        {
            "car_type_id": 148,
            "car_type": "รถบดถนน (รย.14)"
        },
        {
            "car_type_id": 149,
            "car_type": "รถใช้งานเกษตรกรรม (รย.15)"
        },
        {
            "car_type_id": 150,
            "car_type": "รถพ่วง (รย.16)"
        },
        {
            "car_type_id": 151,
            "car_type": "รถจักรยานยนต์สาธารณะ (รย.17)"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 151
}
```
