# Device Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# newDevice

## url
    http://{server}/api/admin/newDevice

## request body
```json
{
  "imei": "International Mobile Equipment Identity",
  "sim_no": "",
  "model": "รุ่น Tracker",
  "network_operator": "AIS", // AIS/DTACK/TRUE,
  "box_id": "",   // !!! New 2019/04/24,
   "type": "", // !!! New 2019/04/24,
  "external_device" : true // กล่องจูน = true
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

# deleteDevice

## url
    http://{server}/api/admin/deleteDevice/{device_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# updateDervice

## url
    http://{server}/api/admin/updateDevice/{device_id} 

## request body
```json
{
    "device_group": "Group of Dead", // "จัดกลุ่ม"
    "device_no": "4กท-2018", // "ทะเบียนรถ"
    "device_model": "Fortuner", // "รุ่นรถ"
    "device_driver": "", // "คนขับรถ"
    "driver_id": "", // "คนขับรถ"
    "speed_limit": 90, // "จำกัดความเร็ว กม./ชม."
    "petroleum_km_rate": 11, // "อัตราการใช้น้ำมัน กม./ลิตร"
    "petroleum_liter_rate": 20, // "อัตราการใช้น้ำมัน ลิตร/ชม."
    "remarks": "เร่งเต็มพิกัด อัดสุดไมล์", // "หมายเหตุ"
    "is_dlt_alert": true, // "แจ้งเตือนกรมขนส่ง"
    "install_date": "11-10-2018", // "วันที่ติดตั้ง"
    "expire_date": "11-10-2019", // "วันครบกำหนด"
    "reseller_note": "ขายได้ขายดี", // "Reseller Note"
    "symbol_id": "car.jpeg", // "ตั้งค่า Marker สัญลักษณ์"
    "symbol_color": "Red", // "ตั้งค่า Marker สี"
    "icon_label": "label",       // !!! new 2019/05/01
    "petroleum_from_date": "11-10-2018", // "ตั้งค่าน้ำมัน เริ่มจากวันที่"
    "petroleum_to_date": "01-11-2018", // "ตั้งค่าน้ำมัน ถึงวันที่"
    "install_with_rfid": true, // ติดตั้งพร้อมเครื่องรูดบัตร !!! New (2019-01-08)
    "imei": "International Mobile Equipment Identity", // !!! New (2019-01-14)
    "sim_no": "", // !!! New (2019-01-14)
    "model": "รุ่น Tracker", // !!! New (2019-01-14)
    "type"
    "network_operator": "", // AIS/DTAC/TRUE
    "last_paid_sim_no": "01-11-2018", // "เติมเงินค่า sim ครั้งล่าสุด"
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

# setDevicePortInOut

## url
    http://{server}/api/admin/updateDevice/{device_id} 

## request body
```json
{
    "input_outputs" :[
      {
          "port_type": "Input", 
          "port_no" : 1,
          "name": "เครื่องยนต์", 
          "val_name0": "ดับเครื่อง", 
          "command_id0": 4, 
          "val_name1": "ดิดเครื่อง",
          "command_id1": 1
      },
      {
          "port_type": "Output",
          "port_no" : 1,
          "name": "ถ่ายรูป",
          "val_name0": "ถ่ายรูปกล้อง1",
          "command_id0": 1,
          "val_name1": "ถ่ายรูปกล้อง2",
          "command_id1": 2
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

# setDevicePortAnalog

## url
    http://{server}/api/admin/updateDevice/{device_id} 

## request body
```json
{
  "ad" :[
      {
          "port_type": "Analog",
          "port_no": 1,
          "name": "น้ำมัน",
          "min_val": 4090,
          "max_val": 0,
          "unit": "%",
          "min": 0,
          "max": 0,
          "extra_rank": "Extra rank"
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

# setDeviceSpacial

## url
    http://{server}/api/admin/updateDevice/{device_id} 

## request body
```json
{
  "special_setting" : {
      "is_send_dlt": true, 
      "is_send_scg": false,  
      "is_send_ambulance": false,  
      "is_send_sccc": false,  
      "is_send_post_office": false,  
      "dlt_group": 1,  
      "change_detail": "รายการใหม่",  
      "inform_date": "03-10-2018",  
      "car_type_id": 9,  
      "car_no": "2sb-1018",  
      "car_province": "กรุงเทพมหานคร", 
      "car_brand": "TOYOTA",  
      "chassis": "MMKST22P805100902", 
      "company": "บริษัท ไทยในประเทศ", 
      "dlt_card_no": "0000000001",  
      "db_card_no": "ไม่มี",
      "fix_place": "อู่ซ่อม",
      "fix_place_start_date": "20-10-2018",
      "fix_place_finish_date": "30-10-2018"
  }
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

# setDeviceAlert

## url
    http://{server}/api/admin/updateDevice/{device_id} 

## request body
 ```json
{
  "alert" : [
      {
          "alert_type": "Big Cola กาญจนบุรี (100.0)",
          "alert_when": "เข้าสู่",
          "alert_channel": {
              "email": true,
              "line": true
          }
      },
      {
          "alert_type": "เครื่องยนต์",
          "alert_when": "ติดเครื่อง",
          "alert_channel": {
              "email": true,
              "line": true
          }
      },
      {
          "alert_type": "เครื่องยนต์",
          "alert_when": "ดับเครื่อง",
          "alert_channel": {
              "email": true,
              "line": true
          }
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

# getDeviceInfo

## url
    http://{server}/api/admin/getDeviceInfo/{device_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "serial": "0101010",
            "imei": "0101010181080000",
            "sim_no": "",
            "model": "รุ่น Tracker",
            "box_id": "",   // !!! New 2019/04/24,
            "type": "GPSiam", // !!! New 2019/04/24,
            "device_id": 18647,
            "user_id": "1",
            "dealer_id": "",
            "customer_id": "",
            "create_user": "Admin",
            "last_upd_user": "Admin",
            "create_dtm": "2018-10-10T15:53:38.649Z",
            "last_upd_dtm": "2018-10-10T16:15:02.940Z",
            "device_driver": "",
            "device_group": "Group of Dead",
            "device_model": "Fortuner",
            "device_no": "4กท-2018",
            "expire_date": "11-10-2019",
            "install_date": "11-10-2018",
            "is_dlt_alert": true,
            "petroleum_from_date": "11-10-2018",
            "petroleum_km_rate": 11,
            "petroleum_liter_rate": 20,
            "petroleum_to_date": "01-11-2018",
            "remarks": "เร่งเต็มพิกัด อัดสุดไมล์",
            "reseller_note": "ขายได้ขายดี",
            "speed_limit": 90,
            "symbol_color": "Red",
            "symbol_id": "car.jpeg",
            "icon_label": "label",       // !!! new 2019/05/01
            "last_paid_sim_no": "11-10-2018",
            "unit_id": "XXXXXX0101010181080000",   // new 2019/05/01
            "input_outputs": [
                {
                    "port_type": "Input",
                    "port_no": 1,
                    "name": "เครื่องยนต์",
                    "val_name0": "ดับเครื่อง",
                    "command_id0": 4,
                    "val_name1": "ดิดเครื่อง",
                    "command_id1": 1
                },
                {
                    "port_type": "Output",
                    "port_no": 1,
                    "name": "ถ่ายรูป",
                    "val_name0": "ถ่ายรูปกล้อง1",
                    "command_id0": 1,
                    "val_name1": "ถ่ายรูปกล้อง2",
                    "command_id1": 2
                }
            ],
            "ad": [
                {
                    "port_type": "Analog",
                    "port_no": 1,
                    "name": "น้ำมัน",
                    "min_val": 4090,
                    "max_val": 0,
                    "unit": "%",
                    "min": 0,
                    "max": 0,
                    "extra_rank": "Extra rank"
                }
            ],
            "special_setting": {
                "is_send_dlt": true,
                "is_send_scg": false,
                "is_send_ambulance": false,
                "is_send_sccc": false,
                "is_send_post_office": false,
                "dlt_group": 1,
                "change_detail": "รายการใหม่",
                "inform_date": "03-10-2018",
                "car_type_id": 9,
                "car_no": "2sb-1018",
                "car_province": "กรุงเทพมหานคร",
                "car_brand": "TOYOTA",
                "chassis": "MMKST22P805100902",
                "company": "บริษัท ไทยในประเทศ",
                "dlt_card_no": "0000000001",
                "db_card_no": "ไม่มี",
                "fix_place": "อู่ซ่อม",
                "fix_place_start_date": "20-10-2018",
                "fix_place_finish_date": "30-10-2018",
                "attachs": [
                    {
                        "name": "nan.jpg",
                        "img": "/viewDeviceAttach/18681/document/nan.jpg"
                    }
                ],
                "offline_attachs" : [
                    {
                        "name": "nan.jpg",
                        "img": "/viewDeviceAttach/18681/document/nan.jpg"
                    }
                ]
            },
            "alert":  [
                {
                    "alert_type_id" : 1,
                    "alert_type": "เครื่องยนต์",
                    "alert_group" : "STATE",
                    "alert_when" : "0",
                    "alert_channel" : {
                        "email" : true,
                        "line" : true
                    },
                    "alert_id" : 56,
                    "alert_last_dtm" : "",
                    "is_alert" : false
                },
                {
                    "alert_type_id" : 10,
                    "alert_type": "หมู่บ้านพฤกษาวิลเวล-33xx-ss 29",
                    "alert_group" : "POI",
                    "alert_when" : "I",
                    "alert_channel" : {
                        "email" : true,
                        "line" : true
                    },
                    "alert_id" : 57,
                    "alert_last_dtm" : "",
                    "is_alert" : false
                },
                {
                    "alert_type_id" : 5,
                    "alert_type": "หยุดนอก POI เกิน 10 นาที",
                    "alert_group" : "OTHER",
                    "alert_channel" : {
                        "email" : true,
                        "line" : true
                    },
                    "alert_id" : 59,
                    "alert_last_dtm" : "",
                    "is_alert" : false
                }
            ]
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getDeviceList

## url
    http://{server}/api/admin/getDeviceList/{pageNumber}/{pageSize} 

## request body
```json
{
  "filter": "11143",
  "sort": {"device_id": -1} 
}
```

** sort รองรับ field device_no, device_id, imei, model, network_operator ค่าที่เป็นไปได้ -1 คือ เรียกจากมากไปน้อย 1 คือ เรียกจากน้อยไปมาก

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "serial": "516814786012322702550983525249",
            "imei": "878322312872687",
            "sim_no": "0814617649",
            "model": "รุ่นนี่ดี",
            "type": "GPSiam",
            "device_id": 11143,
            "device_status": "Active",
            "create_user": "Admin",
            "last_upd_user": "Admin",
            "create_dtm": "2018-10-03T15:32:02.237Z",
            "last_upd_dtm": "2018-10-05T17:58:28.794Z",
            "device_group": "7-11",
            "device_model": "Altis",
            "device_no": "ฉล-4112",
            "expire_date": "05-10-2019",
            "install_date": "05-10-2018",
            "is_dlt_alert": false,
            "speed_limit": 100,
            "tracking_dtm": "19 ก.พ. 2562 20:48:22"  // !! new 19/02/2019
        },
        {
            "imei": "861311007894107",
            "sim_no": "0952919110",
            "model": "id5",
            "dealer_id": "",
            "customer_id": "",
            "create_user": "chin",
            "last_upd_user": "chin",
            "create_dtm": "2018-11-27T02:32:53.783Z",
            "last_upd_dtm": "2019-02-19T10:54:55.249Z",
            "device_id": 18698,
            "device_no": "ID5test",
            "driver_id": "",
            "speed_limit": "140",
            "symbol_color": "#5DADE2",
            "symbol_id": "car-side",
            "visible": true,
            "install_date": "17-12-2018",
            "expire_date": "30-03-2019",
            "install_with_rfid": true,
            "rfid_checked": false,
            "network_operator": "AIS",
            "device_group": "wutthinan",
            "external_device": true,
            "tracking_dtm": "19 ก.พ. 2562 20:48:22"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}
```

#getActiveDeviceUserRelated

## url
    http://{server}/api/admin/getActiveDeviceUserRelated/{size}

    0 : getAll
    others : limit size

## request body
```json
{
  "filter": "International Mobile Equipment Identity"
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "device_id": 10641,
            "device_no": "4กท-2018",
            "id": 10641
        },
        {
            "device_id": 10642,
            "device_no": "4กท-182l",
            "id": 10642
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}
```

# getDeviceUserRelated

## url
    http://{server}/api/admin/getDeviceUserRelated/{user_id}/{pageNo}/{pageSize}

## request body
```json
{
  "filter": "International Mobile Equipment Identity"
}
```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "serial": "516814786012322702550983525249",
            "imei": "878322312872687",
            "sim_no": "0814617649",
            "model": "รุ่นนี่ดี",
            "type": "GPSiam",
            "device_id": 11143,
            "device_status": "Active",
            "create_user": "Admin",
            "last_upd_user": "Admin",
            "create_dtm": "2018-10-03T15:32:02.237Z",
            "last_upd_dtm": "2018-10-05T17:58:28.794Z",
            "device_group": "7-11",
            "device_model": "Altis",
            "device_no": "ฉล-4112",
            "expire_date": "2019-10-05T00:00:00.000Z",
            "install_date": "2018-10-05T00:00:00.000Z",
            "is_dlt_alert": false,
            "speed_limit": 100,
            "tracking_dtm": "19 ก.พ. 2562 20:48:22" // !! new 19-02-2019
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```

# getDeviceNoUserRelated

## url
    http://{server}/api/admin/getDeviceNoUserRelated/{user_id}

## request body
```json
{
  "filter": "International Mobile Equipment Identity"
}
```

## response (if success)

```json
{
    "RESULT_DATA": [
       {
            "imei": "744775269012206",
            "model": "รุ่นนี่ดี",
            "type": "GPSiam",
            "device_id": 10641,
            "device_no": "4กท-2018",
            "expire_date": "20-11-2019",
            "install_date": "24-10-2018"
        },
        {
            "imei": "595159467112314",
            "model": "รุ่นนี่ดี",
            "type": "GPSiam",
            "device_id": 10642,
            "device_no": "4กท-182l",
            "expire_date": "11-10-2019",
            "install_date": "11-10-2018"
        },
        {
            "imei": "919521583213150",
            "model": "รุ่นนี่ดี",
            "type": "GPSiam",
            "device_id": 10643,
            "device_no": "มฟ-6935",
            "expire_date": "05-10-2019",
            "install_date": "05-10-2018"
        },
        {
            "imei": "158413810855509",
            "model": "รุ่นนี่ดี",
            "type": "GPSiam",
            "device_id": 10644,
            "device_no": "ยฐ-4941",
            "expire_date": "05-10-2019",
            "install_date": "05-10-2018"
        },
        {
            "imei": "906393724394719",
            "model": "รุ่นนี่ดี",
            "type": "GPSiam",
            "device_id": 10645,
            "device_no": "ฟป-6298",
            "expire_date": "05-10-2019",
            "install_date": "05-10-2018"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 5
}
```

# addDeviceAlert

## url
    http://{server}/api/admin/addDeviceAlert/{device_id}

## request body
```json
{
	"alert_type_id": "1",
	"alert_group": "STATE",
	"alert_when": "0",	//สำหรับ state {0 = ดับ, 1 = ติด}, สำหรับ POI {I = in, O = out}
	"alert_channel": {
		"email": true,
		"line": true
	}
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

# updateDeviceAlert

## url
    http://{server}/api/admin/updateDeviceAlert/{device_id}/{alert_id}

## request body
```json
{
    "alert_type_id": "10",
	"alert_group": "POI",
	"alert_when": "I",	//สำหรับ state {0 = ดับ, 1 = ติด}, สำหรับ POI {I = in, O = out}
	"alert_channel": {
		"email": true,
		"line": true
	}
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

## url
    http://{server}/api/admin/deleteDeviceAlert/{device_id}/{alert_id}

## request body

## response (if success)
```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

## url
    http://{server}/api/admin/getDeviceGroupList

## request body
{
    "filter":
}

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "name": "wutthinan"
        },
        {
            "name": "Group_Name_AAA"
        },
        {
            "name": ""
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 3
}
```

# setChangeDetail

## url
    http://{server}/api/admin/setDeviceChangeDetail/{device_id} 

## request body
 ```json
{
	"special_setting.change_detail" : "หยุดใช้งาน"
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

# getDeviceAdnGroupList

## url
    http://{server}/api/admin/getDeviceAndGroupList

## request body


## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "name": "[wutthinan]",
            "type": "GROUP"
        },
        {
            "name": "[Group_Name_AAA]",
            "type": "GROUP"
        },
        {
            "name": "[Group 1]",
            "type": "GROUP"
        },
        {
            "name": "18703",
            "device_id": 18703,
            "type": "DEVICE"
        },
        {
            "name": "18704",
            "device_id": 18704,
            "type": "DEVICE"
        },
        {
            "name": "18705",
            "device_id": 18705,
            "type": "DEVICE"
        },
        {
            "name": "18706",
            "device_id": 18706,
            "type": "DEVICE"
        },
        {
            "name": "18707",
            "device_id": 18707,
            "type": "DEVICE"
        },
        {
            "name": "18708",
            "device_id": 18708,
            "type": "DEVICE"
        },
        {
            "name": "18709",
            "device_id": 18709,
            "type": "DEVICE"
        },
        {
            "name": "18710",
            "device_id": 18710,
            "type": "DEVICE"
        },
        {
            "name": "18711",
            "device_id": 18711,
            "type": "DEVICE"
        },
        {
            "name": "18712",
            "device_id": 18712,
            "type": "DEVICE"
        },
        {
            "name": "18713",
            "device_id": 18713,
            "type": "DEVICE"
        },
        {
            "name": "18714",
            "device_id": 18714,
            "type": "DEVICE"
        },
        {
            "name": "18715",
            "device_id": 18715,
            "type": "DEVICE"
        },
        {
            "name": "18716",
            "device_id": 18716,
            "type": "DEVICE"
        },
        {
            "name": "1กท-1287",
            "device_id": 18692,
            "type": "DEVICE"
        },
        {
            "name": "1กย-1287",
            "device_id": 18662,
            "type": "DEVICE"
        },
        {
            "name": "ID5",
            "device_id": 18679,
            "type": "DEVICE"
        },
        {
            "name": "T333/30s",
            "device_id": 18681,
            "type": "DEVICE"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 21
}
```

# getDeviceExtendExpireHistory

## url
    http://{server}/api/admin/getDeviceExtendExpireHistory/{pageNo}/{pageSize}

## request body
```json
{
	"filter": "",
	"is_all": true // ดูทั้งหมด
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "device_id": 18698,
            "device_no": "ID5test",
            "user_id": 1,
            "user_name": "Admin2",
            "extend_dtm": "9 ม.ค. 2562",
            "expire_date": "5 มี.ค. 2562",
            "new_expire_date": "31 มี.ค. 2562",
            "verified": true,
            "verified_dtm": "9 ม.ค. 2562",
            "verified_user": "Admin2"
        },
        {
            "device_id": 18679,
            "device_no": "ID5",
            "user_id": 1,
            "user_name": "Admin2",
            "extend_dtm": "9 ม.ค. 2562",
            "expire_date": "3 พ.ค. 2562",
            "new_expire_date": "29 พ.ค. 2562",
            "verified": false,
            "verified_dtm": "",
            "verified_user": ""
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}
```

# setDeviceExtendExpireVerifed

## url
    http://{server}/api/admin/setDeviceExtendExpireVerifed/{device_id}

## request body

## response (if success)
```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# addDeviceAttach

## url
    http://{server}/api/admin/addDeviceAttach/{device_id}/{type}

**
    type : {
        offline = เอกสารหยุดเกิน 7 วัน
        document = เอกสารทั่วไป
    }

## request body
```json
{
    "name" : "picture.jpg",
    "content" : "iVBORw0KGgoAAAANSUhEUgAAB4AAAAQ4CAIAAABnsVYUAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAAFiUAABYlAUlSJPAAAP=="
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

# deleteDeviceAttach

## url
    http://{server}/api/admin/deleteDeviceAttach/{device_id}/{img name}/{type}

**
    type : {
        offline = เอกสารหยุดเกิน 7 วัน
        document = เอกสารทั่วไป
    }

## request body
```json
```

## response (if success)
```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# newManyDevice

## url
    http://{server}/api/admin/newManyDevice

## request body
```json
[
    {
        "imei": "869103024249400",
        "sim_no": "",
        "model": "T333",
        "network_operator": "AIS", // AIS/DTACK/TRUE
        "device_no" : "43197",  // !!! New 2019/04/20
        "install_date" : "",    // !!! New 2019/04/20
        "box_id": "",   // !!! New 2019/04/24,
        "type": "", // !!! New 2019/04/24,
        "symbol_color" : "#9B59B6", // !!! New 2019/04/30,
	    "symbol_id" : "car-side",    // !!! New 2019/04/30,
        "special_setting": {    // !!! New 2019/04/20
            "car_no": "300648",    // !!! New 2019/04/20
            "car_province": "ยะลา",    // !!! New 2019/04/20
            "chassis": "MMKST22P405111721",    // !!! New 2019/04/20
            "change_detail": "รถกลับมาใช้งานได้ตามปกติแล้ว",    // !!! New 2019/04/20
            "inform_date": "03-10-2018",    // !!! New 2019/04/20,
            "car_type_id": "1422",    // !!! New 2019/04/24,
            "car_brand": "NISSAN",    // !!! New 2019/04/24,
            "company": "บริษัท แมจิค รูทส์ จำกัด"    // !!! New 2019/04/24,
        }
    },
    {
        "imei": "869103024249400",
        "sim_no": "",
        "model": "T333",
        "network_operator": "AIS", // AIS/DTACK/TRUE
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

# getDeviceAttachNames

## url
    http://{server}/api/admin/getDeviceAttachNames/{device_id}/{type}

**
    type : {
        offline = เอกสารหยุดเกิน 7 วัน
        document = เอกสารทั่วไป
    }

## request body
```json
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "name": "6605.jpg",
            "img": "/viewDeviceAttach/18698/document/6605.jpg"
        },
        {
            "name": "set proxy.txt",
            "img": "/viewDeviceAttach/18698/document/set proxy.txt"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}
```

# getDeviceListByGroup
// !!! new 2019/05/01
## url
    http://{server}/api/admin/getDeviceListByGroup/{pageNumber}/{pageSize} 

## request body
```json
{
  "filter": "Wutthin"
}
```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "box_id": "Test0009",
            "device_no": "Test0009",
            "imei": "Test0009",
            "sim_no": "Test0009",
            "model": "T333",
            "network_operator": "AIS",
            "external_device": false,
            "create_user": "Admin2",
            "last_upd_user": "Admin2",
            "create_dtm": "2019-04-28T11:36:03.601Z",
            "last_upd_dtm": "2019-04-28T11:36:03.601Z",
            "device_id": 19375,
            "visible": true,
            "tracking_dtm": ""
        },
        {
            "box_id": 11010,
            "device_no": "t30-4994",
            "type": "GPSiam",
            "model": "ID5 (3G)",
            "imei": 861311007963230,
            "install_date": "23-04-2019",
            "special_setting": {
                "car_no": 304994,
                "car_province": "ภูเก็ตt",
                "chassis": "LH1841003373test",
                "car_brand": "",
                "company": "",
                "car_type_id": 1225,
                "change_detail": "",
                "inform_date": "23-04-2019"
            },
            "device_id": 19374,
            "create_user": "Admin2",
            "last_upd_user": "Admin2",
            "create_dtm": "2019-04-27T12:44:56.807Z",
            "last_upd_dtm": "2019-05-01T05:03:41.289Z",
            "driver_id": "",
            "expire_date": null,
            "symbol_color": "orange",
            "symbol_id": "rocket-alt-2",
            "visible": true,
            "tracking_dtm": ""
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 543
}
```

# getDeviceDLTList
// !!! new 2019/05/01
## url
    http://{server}/api/admin/getDeviceDLTList

## request body

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "device_id": 19375,
            "car_no": "",
            "car_province": "กรุงเทพมหานคร",
            "chassis": "",
            "car_type_id": "2810",
            "type": "",
            "model": "T333",
            "imei": "Test0009",
            "install_date": "",
            "tracking_dtm": "",
            "change_detail": "",
            "inform_date": ""
        },
        {
            "device_id": 19353,
            "car_no": "",
            "car_province": "",
            "chassis": "MMKST22P305131703",
            "car_type_id": "1225",
            "type": "",
            "model": "t333",
            "imei": "868998035987219",
            "install_date": "09/03/2562",
            "tracking_dtm": "",
            "change_detail": "",
            "inform_date": ""
        },
        {
            "device_id": 19352,
            "car_no": "",
            "car_province": "สมุทรปราการ",
            "chassis": "JN1UC4E26Z0000009",
            "car_type_id": "1225",
            "type": "",
            "model": "T333",
            "imei": "868998031027788",
            "install_date": "03/12/2561",
            "tracking_dtm": "",
            "change_detail": "",
            "inform_date": ""
        },
        {
            "device_id": 18773,
            "car_no": "",
            "car_province": "ชลบุรี",
            "chassis": "",
            "car_type_id": "2100",
            "type": "",
            "model": "t333",
            "imei": "868998035990486",
            "install_date": "",
            "tracking_dtm": "01/05/2562 14:31",
            "change_detail": "test",
            "inform_date": "24/05/2562"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 4
}
```

# getDeviceUserDetaiList
// !!! new 2019/05/01
## url
    http://{server}/api/admin/getDeviceUserDetaiList

## request body

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "device_id": 18773,
            "device_group": "",
            "device_no": "วีโก้",
            "user_name": "poom",
            "name": "",
            "company": "fasttrack",
            "install_date": "01/05/2562",
            "expire_date": "05/11/2565",
            "speed_limit": "300",
            "alert_engine_on": "Email, Line",
            "alert_engine_off": "Line"
        },
        {
            "device_id": 18772,
            "device_group": "",
            "device_no": "18772",
            "user_name": "",
            "name": "",
            "company": "",
            "install_date": "",
            "expire_date": "",
            "speed_limit": 0,
            "alert_engine_on": "",
            "alert_engine_off": ""
        },
        {
            "device_id": 18698,
            "device_group": "wutthin",
            "device_no": "ID5test",
            "user_name": "Wutthin",
            "name": "วุฒินันท์",
            "company": "",
            "install_date": "",
            "expire_date": "",
            "speed_limit": "140",
            "alert_engine_on": "",
            "alert_engine_off": ""
        }
     ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 543
}
```