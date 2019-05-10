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
            "imei": "868998035969936",
            "latitude": 13.805246,
            "longitude": 100.571213,
            "speed": 0,
            "direction": 84,
            "gps": 0,
            "gsm": 18,
            "heading": "E",
            "status": "เสา",
            "status_code": 5,
            "date": "10-05-2019",
            "time": "06:38:13",
            "driver_name": "MR.TEST2 LICENSE DRIVING",
            "driver_no": "121100000200100",
            "driver_by_tracker": true,
            "place": "ลาดพร้าว 20 อพาร์ทเม้นท์ (0.06 กม.)  ต.จอมพล อ.จตุจักร จ.กรุงเทพมหานคร",
            "place_poi": "ลาดพร้าว 20 อพาร์ทเม้นท์ (0.06 กม.) ",
            "poi": [],
            "device_info": {
                "device_id": 100003,
                "imei": "868998035969936",
                "device_no": "Fasttrack_T333",
                "device_model": "",
                "symbol_id": "",
                "symbol_color": "",
                "device_driver": "",
                "driver_contact": "",
                "speed_limit": "",
                "is_dlt_alert": false,
                "device_group": "",
                "expire_date": "",
                "remarks": "",
                "engin_port_no": 3,
                "car_type_id": "2120",
                "fuel_port": {
                    "port_type": "Analog",
                    "port_no": 1,
                    "name": "น้ำมัน",
                    "min_val": 500,
                    "max_val": 0,
                    "unit": "%",
                    "min": 9,
                    "max": 0,
                    "extra_rank": "",
                    "last_fuel": 100
                },
                "visible": true,
                "icon_label": "",
                "sensor": null,
                "car_type": "รถบรรทุก ลักษณะ 1 ไม่ประจําทาง"
            },
            "fuel": 100,
            "tracking_dtm": "2019-05-09T23:38:13.000Z",
            "last_upd_dtm": "2019-05-09T23:38:48.972Z"
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


# getNearPoiList

## url
    http://{server2}/getNearPoiList

## request body

```json

{
 "latitude": 13.55939,
 "longitude": 100.752446
}

```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "name": "pop bla bla",
            "distance": 0.012
        },
        {
            "name": "ฟฟฟ",
            "distance": 0.383
        },
        {
            "name": "Sunlong",
            "distance": 8.277
        },
        {
            "name": "testXX",
            "distance": 39.322
        },
        {
            "name": "อู่RUM",
            "distance": 53.276
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
            "prov_code": "81",
            "prov_name": "กระบี่",
            "extent": {
                "minx": 98.611598,
                "miny": 7.467277,
                "maxx": 99.414993,
                "maxy": 8.68184
            }
        },
        {
            "prov_code": "10",
            "prov_name": "กรุงเทพมหานคร",
            "extent": {
                "minx": 100.327912,
                "miny": 13.49339,
                "maxx": 100.938516,
                "maxy": 13.955198
            }
        },
        { 
            "...": "..."
        },
        {
            "prov_code": "71",
            "prov_name": "กาญจนบุรี",
            "extent": {
                "minx": 98.181068,
                "miny": 13.725532,
                "maxx": 99.879323,
                "maxy": 15.66074
            }
        },
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
            "district_code": "18",
            "district_name": "คลองสาน",
            "extent": {
                "minx": 100.492206,
                "miny": 13.705137,
                "maxx": 100.512712,
                "maxy": 13.739218
            }
        },
        {
            "district_code": "46",
            "district_name": "คลองสามวา",
            "extent": {
                "minx": 100.670762,
                "miny": 13.815493,
                "maxx": 100.799463,
                "maxy": 13.931409
            }
        },
        {
            "district_code": "33",
            "district_name": "คลองเตย",
            "extent": {
                "minx": 100.550695,
                "miny": 13.696096,
                "maxx": 100.601659,
                "maxy": 13.742849
            }
        },
        {
            "district_code": "43",
            "district_name": "คันนายาว",
            "extent": {
                "minx": 100.645987,
                "miny": 13.781206,
                "maxx": 100.704964,
                "maxy": 13.857255
            }
        },
        {
            "district_code": "30",
            "district_name": "จตุจักร",
            "extent": {
                "minx": 100.537117,
                "miny": 13.794601,
                "maxx": 100.591118,
                "maxy": 13.858942
            }
        },
        {
            "district_code": "35",
            "district_name": "จอมทอง",
            "extent": {
                "minx": 100.4347,
                "miny": 13.655675,
                "maxx": 100.488983,
                "maxy": 13.717891
            }
        },
        {
            "district_code": "36",
            "district_name": "ดอนเมือง",
            "extent": {
                "minx": 100.558893,
                "miny": 13.887631,
                "maxx": 100.626682,
                "maxy": 13.955198
            }
        },
        {
            "district_code": "26",
            "district_name": "ดินแดง",
            "extent": {
                "minx": 100.543431,
                "miny": 13.755126,
                "maxx": 100.574896,
                "maxy": 13.80107
            }
        },
        {
            "district_code": "02",
            "district_name": "ดุสิต",
            "extent": {
                "minx": 100.49904,
                "miny": 13.752637,
                "maxx": 100.537424,
                "maxy": 13.800358
            }
        },
        {
            "district_code": "19",
            "district_name": "ตลิ่งชัน",
            "extent": {
                "minx": 100.406127,
                "miny": 13.740006,
                "maxx": 100.469658,
                "maxy": 13.801348
            }
        },
        {
            "district_code": "48",
            "district_name": "ทวีวัฒนา",
            "extent": {
                "minx": 100.327912,
                "miny": 13.736036,
                "maxx": 100.411058,
                "maxy": 13.804126
            }
        },
        {
            "district_code": "49",
            "district_name": "ทุ่งครุ",
            "extent": {
                "minx": 100.47007,
                "miny": 13.586158,
                "maxx": 100.521038,
                "maxy": 13.663071
            }
        },
        {
            "district_code": "15",
            "district_name": "ธนบุรี",
            "extent": {
                "minx": 100.468536,
                "miny": 13.694815,
                "maxx": 100.498638,
                "maxy": 13.742173
            }
        },
        {
            "district_code": "20",
            "district_name": "บางกอกน้อย",
            "extent": {
                "minx": 100.453534,
                "miny": 13.742949,
                "maxx": 100.490972,
                "maxy": 13.787616
            }
        },
        {
            "district_code": "16",
            "district_name": "บางกอกใหญ่",
            "extent": {
                "minx": 100.461602,
                "miny": 13.72222,
                "maxx": 100.49197,
                "maxy": 13.748209
            }
        },
        {
            "district_code": "06",
            "district_name": "บางกะปิ",
            "extent": {
                "minx": 100.601016,
                "miny": 13.738385,
                "maxx": 100.678887,
                "maxy": 13.819398
            }
        },
        {
            "district_code": "21",
            "district_name": "บางขุนเทียน",
            "extent": {
                "minx": 100.376482,
                "miny": 13.49339,
                "maxx": 100.481726,
                "maxy": 13.682558
            }
        },
        {
            "district_code": "31",
            "district_name": "บางคอแหลม",
            "extent": {
                "minx": 100.489998,
                "miny": 13.682679,
                "maxx": 100.531761,
                "maxy": 13.712461
            }
        },
        {
            "district_code": "29",
            "district_name": "บางซื่อ",
            "extent": {
                "minx": 100.506277,
                "miny": 13.797854,
                "maxx": 100.545031,
                "maxy": 13.849628
            }
        },
        {
            "district_code": "47",
            "district_name": "บางนา",
            "extent": {
                "minx": 100.579458,
                "miny": 13.648503,
                "maxx": 100.653792,
                "maxy": 13.684429
            }
        },
        {
            "district_code": "50",
            "district_name": "บางบอน",
            "extent": {
                "minx": 100.344676,
                "miny": 13.619703,
                "maxx": 100.446797,
                "maxy": 13.693684
            }
        },
        {
            "district_code": "25",
            "district_name": "บางพลัด",
            "extent": {
                "minx": 100.465939,
                "miny": 13.761929,
                "maxx": 100.517672,
                "maxy": 13.813275
            }
        },
        {
            "district_code": "04",
            "district_name": "บางรัก",
            "extent": {
                "minx": 100.512032,
                "miny": 13.718082,
                "maxx": 100.544745,
                "maxy": 13.738047
            }
        },
        {
            "district_code": "05",
            "district_name": "บางเขน",
            "extent": {
                "minx": 100.586481,
                "miny": 13.842544,
                "maxx": 100.685775,
                "maxy": 13.89978
            }
        },
        {
            "district_code": "40",
            "district_name": "บางแค",
            "extent": {
                "minx": 100.352677,
                "miny": 13.66804,
                "maxx": 100.427821,
                "maxy": 13.753926
            }
        },
        {
            "district_code": "27",
            "district_name": "บึงกุ่ม",
            "extent": {
                "minx": 100.624478,
                "miny": 13.770707,
                "maxx": 100.676567,
                "maxy": 13.847368
            }
        },
        {
            "district_code": "07",
            "district_name": "ปทุมวัน",
            "extent": {
                "minx": 100.515674,
                "miny": 13.722772,
                "maxx": 100.552912,
                "maxy": 13.7531
            }
        },
        {
            "district_code": "32",
            "district_name": "ประเวศ",
            "extent": {
                "minx": 100.634106,
                "miny": 13.656329,
                "maxx": 100.712385,
                "maxy": 13.737862
            }
        },
        {
            "district_code": "08",
            "district_name": "ป้อมปราบศัตรูพ่าย",
            "extent": {
                "minx": 100.503898,
                "miny": 13.738047,
                "maxx": 100.517383,
                "maxy": 13.763651
            }
        },
        {
            "district_code": "14",
            "district_name": "พญาไท",
            "extent": {
                "minx": 100.527886,
                "miny": 13.762716,
                "maxx": 100.561985,
                "maxy": 13.797854
            }
        },
        {
            "district_code": "01",
            "district_name": "พระนคร",
            "extent": {
                "minx": 100.487645,
                "miny": 13.738633,
                "maxx": 100.509399,
                "maxy": 13.772666
            }
        },
        {
            "district_code": "09",
            "district_name": "พระโขนง",
            "extent": {
                "minx": 100.58392,
                "miny": 13.677935,
                "maxx": 100.640236,
                "maxy": 13.706842
            }
        },
        {
            "district_code": "22",
            "district_name": "ภาษีเจริญ",
            "extent": {
                "minx": 100.413361,
                "miny": 13.687613,
                "maxx": 100.471675,
                "maxy": 13.747934
            }
        },
        {
            "district_code": "10",
            "district_name": "มีนบุรี",
            "extent": {
                "minx": 100.696776,
                "miny": 13.773224,
                "maxx": 100.80801,
                "maxy": 13.84929
            }
        },
        {
            "district_code": "12",
            "district_name": "ยานนาวา",
            "extent": {
                "minx": 100.516982,
                "miny": 13.668942,
                "maxx": 100.554867,
                "maxy": 13.719251
            }
        },
        {
            "district_code": "37",
            "district_name": "ราชเทวี",
            "extent": {
                "minx": 100.519167,
                "miny": 13.74789,
                "maxx": 100.564969,
                "maxy": 13.774338
            }
        },
        {
            "district_code": "24",
            "district_name": "ราษฎร์บูรณะ",
            "extent": {
                "minx": 100.475564,
                "miny": 13.652963,
                "maxx": 100.523401,
                "maxy": 13.695262
            }
        },
        {
            "district_code": "11",
            "district_name": "ลาดกระบัง",
            "extent": {
                "minx": 100.706606,
                "miny": 13.68956,
                "maxx": 100.878833,
                "maxy": 13.800391
            }
        },
        {
            "district_code": "38",
            "district_name": "ลาดพร้าว",
            "extent": {
                "minx": 100.588341,
                "miny": 13.794815,
                "maxx": 100.637122,
                "maxy": 13.849268
            }
        },
        {
            "district_code": "45",
            "district_name": "วังทองหลาง",
            "extent": {
                "minx": 100.588383,
                "miny": 13.751201,
                "maxx": 100.630655,
                "maxy": 13.802839
            }
        },
        {
            "district_code": "39",
            "district_name": "วัฒนา",
            "extent": {
                "minx": 100.550075,
                "miny": 13.704666,
                "maxx": 100.606842,
                "maxy": 13.748519
            }
        },
        {
            "district_code": "34",
            "district_name": "สวนหลวง",
            "extent": {
                "minx": 100.598152,
                "miny": 13.700762,
                "maxx": 100.659177,
                "maxy": 13.750121
            }
        },
        {
            "district_code": "44",
            "district_name": "สะพานสูง",
            "extent": {
                "minx": 100.659011,
                "miny": 13.732497,
                "maxx": 100.716681,
                "maxy": 13.798328
            }
        },
        {
            "district_code": "13",
            "district_name": "สัมพันธวงศ์",
            "extent": {
                "minx": 100.499807,
                "miny": 13.729393,
                "maxx": 100.515909,
                "maxy": 13.746848
            }
        },
        {
            "district_code": "28",
            "district_name": "สาทร",
            "extent": {
                "minx": 100.508171,
                "miny": 13.700886,
                "maxx": 100.553754,
                "maxy": 13.726166
            }
        },
        {
            "district_code": "42",
            "district_name": "สายไหม",
            "extent": {
                "minx": 100.608697,
                "miny": 13.874248,
                "maxx": 100.692368,
                "maxy": 13.950251
            }
        },
        {
            "district_code": "03",
            "district_name": "หนองจอก",
            "extent": {
                "minx": 100.787422,
                "miny": 13.737877,
                "maxx": 100.938516,
                "maxy": 13.946491
            }
        },
        {
            "district_code": "23",
            "district_name": "หนองแขม",
            "extent": {
                "minx": 100.330228,
                "miny": 13.654708,
                "maxx": 100.385253,
                "maxy": 13.738002
            }
        },
        {
            "district_code": "41",
            "district_name": "หลักสี่",
            "extent": {
                "minx": 100.543629,
                "miny": 13.849628,
                "maxx": 100.594813,
                "maxy": 13.914457
            }
        },
        {
            "district_code": "17",
            "district_name": "ห้วยขวาง",
            "extent": {
                "minx": 100.563297,
                "miny": 13.741142,
                "maxx": 100.604095,
                "maxy": 13.803112
            }
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
            "subdistrict_code": "01",
            "subdistrict_name": "มีนบุรี",
            "extent": {
                "minx": 100.696776,
                "miny": 13.773224,
                "maxx": 100.749246,
                "maxy": 13.838456
            }
        },
        {
            "subdistrict_code": "02",
            "subdistrict_name": "แสนแสบ",
            "extent": {
                "minx": 100.735632,
                "miny": 13.775433,
                "maxx": 100.80801,
                "maxy": 13.84929
            }
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


