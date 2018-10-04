# Device Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# newDevice

## url
    http://{server}/newDevice

## request body
```json
{
  "serial": "0101010",
  "imei": "International Mobile Equipment Identity",
  "sim_no": "",
  "model": "รุ่น Tracker",
  "vendor": "ยี่ห้อ Tracker",
  "user_id": "ผู้ถือครอง"
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

# updateDervice

## url
    http://{server}/updateDevice/{device_id} 

## request body
```json
{
  "serial": "0101010",
  "imei": "International Mobile Equipment Identity",
  "sim_no": "",
  "model": "รุ่น Tracker",
  "vendor": "ยี่ห้อ Tracker",
  "user_id": "ผู้ถือครอง"
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
    http://{server}/deleteDevice/{device_id} 

## request body

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
    http://{server}/getDeviceInfo/{device_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "serial": "0101010",
            "imei": "International Mobile Equipment Identity",
            "sim_no": "",
            "model": "รุ่น Tracker",
            "vendor": "ยี่ห้อ Tracker",
            "user_id": "1",
            "device_id": 3,
            "device_status": "Defected",
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

# getDeviceList

## url
    http://{server}/getDeviceList/{pageNumber}/{pageSize} 

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
            "serial": "0101010",
            "imei": "International Mobile Equipment Identity",
            "sim_no": "",
            "model": "รุ่น Tracker",
            "vendor": "ยี่ห้อ Tracker",
            "device_id": 3,
            "device_status": "Defected",
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-30T15:43:33.288Z",
            "last_upd_dtm": "2018-09-30T16:21:38.602Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```

# getDeviceAvailable

## url
    http://{server}/getDeviceAvailable/{size}

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "serial": "053268847340649473214271273623",
            "imei": "900209508036247",
            "sim_no": "0811537362",
            "model": "รุ่นนี่ดี",
            "vendor": "FastTrack",
            "device_id": 6,
            "device_status": "Available",
            "create_user": "Admin",
            "last_upd_user": "Admin",
            "create_dtm": "2018-09-30T16:49:43.518Z",
            "last_upd_dtm": "2018-09-30T16:49:43.518Z"
        },
        {
            "serial": "932351005276174173600174697718",
            "imei": "447901496645878",
            "sim_no": "0816739238",
            "model": "รุ่นนี่ดี",
            "vendor": "FastTrack",
            "device_id": 7,
            "device_status": "Available",
            "create_user": "Admin",
            "last_upd_user": "Admin",
            "create_dtm": "2018-09-30T16:49:43.844Z",
            "last_upd_dtm": "2018-09-30T16:49:43.844Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 10002
}
```

# getDeviceActive

## url
    http://{server}/getDeviceActive/{pageNumber}/{pageSize} 

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
            "serial": "0101010",
            "imei": "International Mobile Equipment Identity",
            "sim_no": "",
            "model": "รุ่น Tracker",
            "vendor": "ยี่ห้อ Tracker",
            "device_id": 3,
            "device_status": "Active",
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-30T15:43:33.288Z",
            "last_upd_dtm": "2018-09-30T16:21:38.602Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```

# setDeviceDefect

## url
    http://{server}/setDeviceDefect/{device_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# assignDealer

## url
    http://{server}/assignDealer/{dealer_id} 

## request body
[
  {"device_id": 19},
  {"device_id": 20}
]

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# setDeviceCarInfo

## url
    http://{server}/setDeviceCarInfo/{device_id} 

## request body

```json
{
	"device_group": "Group of Dead", // "จัดกลุ่ม"
	"device_no": "4กท-2018", // "ทะเบียนรถ"
	"device_model": "Fortuner", // "รุ่นรถ"
	"device_driver": "", // "คนขับรถ"
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
	"petroleum_to_date": "01-11-2018" // "ตั้งค่าน้ำมัน ถึงวันที่"
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
    http://{server}/setDevicePortInOut/{device_id} 

## request body
```json
[
    {
	    "port_type": "Input", // Input/Output
	    "port_no" : 1,
	    "name": "เครื่องยนต์", // ชื่อ
	    "val_name0": "ดับเครื่อง", // ค่า 0 ชื่อ
	    "command_id0": 4, // คำสั่ง
	    "val_name1": "ดิดเครื่อง", // ค ่า 0 ชื่อ
	    "command_id1": ึ // คำสั่ง
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
    http://{server}/setDevicePortAnalog/{device_id} 

## request body
```json
[
	{
	    "port_type": "Analog",
	    "port_no": 1,
	    "name": "น้ำมัน",
	    "min_val": 500,
	    "max_val": 0,
	    "unit": "%",
	    "min": 0,
	    "max": 0,
	    "extra_rank": "Extra rank"
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

# setDeviceSpacial

## url
    http://{server}/setDeviceSpacial/{device_id} 

## request body
```json
{
	"is_send_dlt": true,  // ข้อมูลส่งกรมขนส่งทางบก
	"is_send_scg": false,  // ข้อมูลส่ง SCG
	"is_send_ambulance": false,  // ข้อมูลส่ง รถพยาบาล
	"is_send_sccc": false,  // ข้อมูลส่ง SCCC
	"is_send_post_office": false,  // ข้อมูลส่ง ไปรษณีย์
	"dlt_group": 1,  // กลุ่มรถ ([1] รถติดตั้งอุปกรณ์ใหม่ ,[2] ติดตั้งก่อน 25 / 01 / 59,[3] รถวัตถุอันตราย,[99] ยกเลิก)
	"file_attach": "",  // แนบไฟล์ (30 - 9130.jpg)
	"change_detail": "รายการใหม่",  // รายละเอียดการแก้ไขเปลี่ยนแปลง
	"inform_date": "03-10-2018",  // วันที่แจ้ง
	"car_type_id": 9,  // ประเภทรถ get จาก dorpdown
	"car_no": "2sb-1018",  // ทะเบียนรถ (ex. 0309130)
	"car_province": "กรุงเทพมหานคร",  // จังหวัด
	"car_brand": "TOYOTA",  // ยี่ห้อรถ
	"chassis": "MMKST22P805100902",  // Chassis
	"company": "บริษัท ไทยในประเทศ",  // บริษัท
	"dlt_card_no": "0000000001",  // เลขบัตรส่งขนส่ง
	"db_card_no": "ไม่มี"  // เลขบัตรในฐานข้อมูล (ex ไม่มี)
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
    http://{server}/setDeviceAlert/{device_id} 

## request body
```json
 [
    {
        "alert_type": "Big Cola กาญจนบุรี (100.0)", // ประเภทแจ้งเตือน
        "alert_when": "เข้าสู่", // เมื่อเปลี่ยนเป็น
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
```

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

#getActiveDeviceNo

## url
    http://{server}/getActiveDeviceNo

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