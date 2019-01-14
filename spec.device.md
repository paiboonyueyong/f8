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
  "network_operator": "AIS" // AIS/DTACK/TRUE
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
    "petroleum_from_date": "11-10-2018", // "ตั้งค่าน้ำมัน เริ่มจากวันที่"
    "petroleum_to_date": "01-11-2018", // "ตั้งค่าน้ำมัน ถึงวันที่"
    "install_with_rfid": true, // ติดตั้งพร้อมเครื่องรูดบัตร !!! New (2019-01-08)
    "imei": "International Mobile Equipment Identity", // !!! New (2019-01-14)
    "sim_no": "", // !!! New (2019-01-14)
    "model": "รุ่น Tracker", // !!! New (2019-01-14)
    "network_operator": "" // AIS/DTAC/TRUE
    
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
      "file_name": "", 
      "file_attach": "Y29uc3QgX21vbmdvZGIgPSByZXF1aXJlKCdtb25nb2RiJyk7DQpjb25zdCBtb25nb2RiID0gcmVxdWlyZSgnLi9EQUwvbW9uZ29kYicpOw0KY29uc3QgbG9nZ2VyID0gcmVxdWlyZ==",  
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
            "vendor": "ยี่ห้อ Tracker",
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
                "file_name": "",
                "file_attach": "Y29uc3QgX21vbmdvZGIgPSByZXF1aXJlKCdtb25nb2RiJyk7DQpjb25zdCBtb25nb2RiID0gcmVxdWlyZSgnLi9EQUwvbW9uZ29kYicpOw0KY29uc3QgbG9nZ2VyID0gcmVxdWlyZ==",
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
  "availableOnly": true
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
            "vendor": "FastTrack",
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
            "stock_on_user_id": 0
        },
        {
            "serial": "004514248453579315758599954957",
            "imei": "261114383014958",
            "sim_no": "0817013733",
            "model": "รุ่นนี่ดี",
            "vendor": "FastTrack",
            "device_id": 14578,
            "device_status": "Available",
            "create_user": "Admin",
            "last_upd_user": "Admin",
            "create_dtm": "2018-10-03T16:07:04.872Z",
            "last_upd_dtm": "2018-10-03T16:07:04.872Z",
            "stock_on_user_id": 0
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
            "vendor": "FastTrack",
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
            "stock_on_user_id": 0
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
            "vendor": "FastTrack",
            "device_id": 10641,
            "device_no": "4กท-2018",
            "expire_date": "20-11-2019",
            "install_date": "24-10-2018"
        },
        {
            "imei": "595159467112314",
            "model": "รุ่นนี่ดี",
            "vendor": "FastTrack",
            "device_id": 10642,
            "device_no": "4กท-182l",
            "expire_date": "11-10-2019",
            "install_date": "11-10-2018"
        },
        {
            "imei": "919521583213150",
            "model": "รุ่นนี่ดี",
            "vendor": "FastTrack",
            "device_id": 10643,
            "device_no": "มฟ-6935",
            "expire_date": "05-10-2019",
            "install_date": "05-10-2018"
        },
        {
            "imei": "158413810855509",
            "model": "รุ่นนี่ดี",
            "vendor": "FastTrack",
            "device_id": 10644,
            "device_no": "ยฐ-4941",
            "expire_date": "05-10-2019",
            "install_date": "05-10-2018"
        },
        {
            "imei": "906393724394719",
            "model": "รุ่นนี่ดี",
            "vendor": "FastTrack",
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
    http://{server}/api/admin/getDeviceAdnGroupList

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