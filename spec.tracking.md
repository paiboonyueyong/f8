# Tracking Realtime Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# getTrackingList

## url
    http://{server2}/getTrackingList

## request body (body empty = getAll)

```json

{
 "filter" : [{
            "imei": "868998031020627",
            "device_id": 18685,
            "device_no": "18685",
            "id": "111"
        },
        {
            "imei": "868998031020628",
            "device_id": 18686,
            "device_no": "18686",
            "id": "1"
        }]
}

```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "imei": "868998031020627",
            "latitude": 12.914493,
            "longitude": 100.91308,
            "speed": 0,
            "heading": "E",
            "status": "ดับ",
            "place": "12.914493 100.91308",
            "date": "30-10-2018",
            "time": "17:37",
            "driver_name": "",
            "driver_no": "",
            "device_info": {
                "device_id": 18662,
                "imei": "868998031020627",
                "device_no": "1กท-1287",
                "device_model": "VIGO",
                "symbol_id": "car.jpeg",
                "symbol_color": "Blue",
                "device_driver": "",
                "speed_limit": 80,
                "is_dlt_alert": true
            },
            "tracking_dtm": "2018-10-30T10:37:14.000Z",
            "last_upd_dtm": "2018-10-30T10:39:01.313Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}

```


# getNearTrackingList

## url
    http://{server2}/getNearTrackingList/{poiId}

## no request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "device_no": "1กท-1287",
            "status": "ดับ",
            "distance": 263.86
        },
        {
            "device_no": "ID5",
            "status": "ดับ",
            "distance": 263.872
        },
        {
            "device_no": "T333/30s",
            "status": "จอด",
            "distance": 267.511
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# getAddressLocation

## url
    http://{server2}/getAddressLocation/

## body

```json

{
	"latitude":13,
	"longitude":100
}

```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "address": "ต.หนองขนาน อ.เมืองเพชรบุรี จ.เพชรบุรี"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# getProvinceList

## url
    http://{server2}/getProvinceList/

## no request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "PROV_CODE": "81",
            "PROV_NAMT": "กระบี่"
        },
        {
            "PROV_CODE": "10",
            "PROV_NAMT": "กรุงเทพมหานคร"
        },
        {
            "PROV_CODE": "71",
            "PROV_NAMT": "กาญจนบุรี"
        },
        {
            "PROV_CODE": "46",
            "PROV_NAMT": "กาฬสินธุ์"
        },
        {
            "PROV_CODE": "62",
            "PROV_NAMT": "กำแพงเพชร"
        },
        {
            "PROV_CODE": "40",
            "PROV_NAMT": "ขอนแก่น"
        },
        {
            "PROV_CODE": "22",
            "PROV_NAMT": "จันทบุรี"
        },
        {
            "PROV_CODE": "24",
            "PROV_NAMT": "ฉะเชิงเทรา"
        },
        
        { 
            "...": "..."
        },
        {
            "PROV_CODE": "58",
            "PROV_NAMT": "แม่ฮ่องสอน"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# getDistrictList

## url
    http://{server2}/getDistrictList/{provCode}

## no request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "DISTRICT_CODE": "18",
            "DISTRICT_NAME": "คลองสาน"
        },
        {
            "DISTRICT_CODE": "46",
            "DISTRICT_NAME": "คลองสามวา"
        },
        {
            "DISTRICT_CODE": "33",
            "DISTRICT_NAME": "คลองเตย"
        },
        {
            "DISTRICT_CODE": "43",
            "DISTRICT_NAME": "คันนายาว"
        },
        {
            "DISTRICT_CODE": "30",
            "DISTRICT_NAME": "จตุจักร"
        },
        {
            "DISTRICT_CODE": "35",
            "DISTRICT_NAME": "จอมทอง"
        },
        {
            "DISTRICT_CODE": "36",
            "DISTRICT_NAME": "ดอนเมือง"
        },
        {
            "DISTRICT_CODE": "26",
            "DISTRICT_NAME": "ดินแดง"
        },
        {
            "DISTRICT_CODE": "02",
            "DISTRICT_NAME": "ดุสิต"
        },
        {
            "DISTRICT_CODE": "19",
            "DISTRICT_NAME": "ตลิ่งชัน"
        },
        {
            "DISTRICT_CODE": "48",
            "DISTRICT_NAME": "ทวีวัฒนา"
        },
        {
            "DISTRICT_CODE": "49",
            "DISTRICT_NAME": "ทุ่งครุ"
        },
        {
            "DISTRICT_CODE": "15",
            "DISTRICT_NAME": "ธนบุรี"
        },
        {
            "DISTRICT_CODE": "20",
            "DISTRICT_NAME": "บางกอกน้อย"
        },
        {
            "DISTRICT_CODE": "16",
            "DISTRICT_NAME": "บางกอกใหญ่"
        },
        {
            "DISTRICT_CODE": "06",
            "DISTRICT_NAME": "บางกะปิ"
        },
        {
            "DISTRICT_CODE": "21",
            "DISTRICT_NAME": "บางขุนเทียน"
        },
        {
            "DISTRICT_CODE": "31",
            "DISTRICT_NAME": "บางคอแหลม"
        },
        {
            "DISTRICT_CODE": "29",
            "DISTRICT_NAME": "บางซื่อ"
        },
        {
            "DISTRICT_CODE": "47",
            "DISTRICT_NAME": "บางนา"
        },
        {
            "DISTRICT_CODE": "50",
            "DISTRICT_NAME": "บางบอน"
        },
        {
            "DISTRICT_CODE": "25",
            "DISTRICT_NAME": "บางพลัด"
        },
        {
            "DISTRICT_CODE": "04",
            "DISTRICT_NAME": "บางรัก"
        },
        {
            "DISTRICT_CODE": "05",
            "DISTRICT_NAME": "บางเขน"
        },
        {
            "DISTRICT_CODE": "40",
            "DISTRICT_NAME": "บางแค"
        },
        {
            "DISTRICT_CODE": "27",
            "DISTRICT_NAME": "บึงกุ่ม"
        },
        {
            "DISTRICT_CODE": "07",
            "DISTRICT_NAME": "ปทุมวัน"
        },
        {
            "DISTRICT_CODE": "32",
            "DISTRICT_NAME": "ประเวศ"
        },
        {
            "DISTRICT_CODE": "08",
            "DISTRICT_NAME": "ป้อมปราบศัตรูพ่าย"
        },
        {
            "DISTRICT_CODE": "14",
            "DISTRICT_NAME": "พญาไท"
        },
        {
            "DISTRICT_CODE": "01",
            "DISTRICT_NAME": "พระนคร"
        },
        {
            "DISTRICT_CODE": "09",
            "DISTRICT_NAME": "พระโขนง"
        },
        {
            "DISTRICT_CODE": "22",
            "DISTRICT_NAME": "ภาษีเจริญ"
        },
        {
            "DISTRICT_CODE": "10",
            "DISTRICT_NAME": "มีนบุรี"
        },
        {
            "DISTRICT_CODE": "12",
            "DISTRICT_NAME": "ยานนาวา"
        },
        {
            "DISTRICT_CODE": "37",
            "DISTRICT_NAME": "ราชเทวี"
        },
        {
            "DISTRICT_CODE": "24",
            "DISTRICT_NAME": "ราษฎร์บูรณะ"
        },
        {
            "DISTRICT_CODE": "11",
            "DISTRICT_NAME": "ลาดกระบัง"
        },
        {
            "DISTRICT_CODE": "38",
            "DISTRICT_NAME": "ลาดพร้าว"
        },
        {
            "DISTRICT_CODE": "45",
            "DISTRICT_NAME": "วังทองหลาง"
        },
        {
            "DISTRICT_CODE": "39",
            "DISTRICT_NAME": "วัฒนา"
        },
        {
            "DISTRICT_CODE": "34",
            "DISTRICT_NAME": "สวนหลวง"
        },
        {
            "DISTRICT_CODE": "44",
            "DISTRICT_NAME": "สะพานสูง"
        },
        {
            "DISTRICT_CODE": "13",
            "DISTRICT_NAME": "สัมพันธวงศ์"
        },
        {
            "DISTRICT_CODE": "28",
            "DISTRICT_NAME": "สาทร"
        },
        {
            "DISTRICT_CODE": "42",
            "DISTRICT_NAME": "สายไหม"
        },
        {
            "DISTRICT_CODE": "03",
            "DISTRICT_NAME": "หนองจอก"
        },
        {
            "DISTRICT_CODE": "23",
            "DISTRICT_NAME": "หนองแขม"
        },
        {
            "DISTRICT_CODE": "41",
            "DISTRICT_NAME": "หลักสี่"
        },
        {
            "DISTRICT_CODE": "17",
            "DISTRICT_NAME": "ห้วยขวาง"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```

# getSubDistrictList

## url
    http://{server2}/getSubDistrictList/{provCode}/{districtCode}

## no request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "SUBDISTRICT_CODE": "06",
            "SUBDISTRICT_NAME": "ขุมทอง"
        },
        {
            "SUBDISTRICT_CODE": "02",
            "SUBDISTRICT_NAME": "คลองสองต้นนุ่น"
        },
        {
            "SUBDISTRICT_CODE": "03",
            "SUBDISTRICT_NAME": "คลองสามประเวศ"
        },
        {
            "SUBDISTRICT_CODE": "05",
            "SUBDISTRICT_NAME": "ทับยาว"
        },
        {
            "SUBDISTRICT_CODE": "01",
            "SUBDISTRICT_NAME": "ลาดกระบัง"
        },
        {
            "SUBDISTRICT_CODE": "04",
            "SUBDISTRICT_NAME": "ลำปลาทิว"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```

# getAreaTrackingList

## url
    http://{server2}/getAreaTrackingList/{provCode}/{districtCode}/{subDistrictCode}

    No specific area send 0

    example

    http://{server2}/getAreaTrackingList/10/0/0
    http://{server2}/getAreaTrackingList/10/10/0
    http://{server2}/getAreaTrackingList/10/10/10

## no request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "device_no": "T333/30s",
            "status": "จอด"
        },
        {
            "device_no": "ID5",
            "status": "ดับ"
        },
        {
            "device_no": "1กย-1287",
            "status": "ดับ"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}


