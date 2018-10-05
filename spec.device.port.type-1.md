# Device Port Standard Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# newDevicePort

## url
    http://{server}/newDevicePort

## request body
```json
{
    "port_type":"Analog",
    "port_no": 1,
    "port_catg":"AD"
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

# updateDevicePort

## url
    http://{server}/updateDevicePort/{_id} 

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

# deleteDevicePort

## url
    http://{server}/deleteDevicePort/{_id} 

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
    http://{server}/getDevicePortInfo/{_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
            {
                "_id": "5bb25e81def52fc0e225c044",
                "port_type": "Analog",
                "port_no": 1,
                "port_catg": "AD"
            }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getDevicePortList

## url
    http://{server}/getDevicePortList/{port category}
        -> AD for port analog
        -> IO for port input/outpu
## request body
```json
{
  "filter": "Analog"
}
```

## response (if success for Port Category = AD)
```json
{
    "RESULT_DATA": [
        {
            "_id": "5bb766e321f6b3dbd4261900",
            "port_type": "Analog",
            "port_no": 1,
            "port_catg": "AD",
            "name": "น้ำมัน",
            "min_val": 500,
            "max_val": 0,
            "unit": "%",
            "min": 0,
            "max": 0,
            "extra_rank": ""
        },
        {
            "_id": "5bb766e321f6b3dbd4261901",
            "port_type": "Analog",
            "port_no": 2,
            "port_catg": "AD"
        },
        {
            "_id": "5bb766e321f6b3dbd4261902",
            "port_type": "Analog",
            "port_no": 3,
            "port_catg": "AD"
        },
        {
            "_id": "5bb766e321f6b3dbd4261903",
            "port_type": "Analog",
            "port_no": 4,
            "port_catg": "AD"
        },
        {
            "_id": "5bb766e321f6b3dbd4261904",
            "port_type": "Analog",
            "port_no": 5,
            "port_catg": "AD"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 5
}
```
## response (if success for Port Category = IO)
```json
{
    "RESULT_DATA": [
        {
            "_id": "5bb766e321f6b3dbd4261905",
            "port_type": "Input",
            "port_no": 1,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd4261906",
            "port_type": "Input",
            "port_no": 2,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd4261907",
            "port_type": "Input",
            "port_no": 3,
            "port_catg": "IO",
            "name": "เครื่องยนต์",
            "val_name0": "ดับเครื่อง",
            "command_id0": 0,
            "val_name1": "ติดเครื่อง",
            "command_id1": 0
        },
        {
            "_id": "5bb766e321f6b3dbd4261908",
            "port_type": "Input",
            "port_no": 4,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd4261909",
            "port_type": "Input",
            "port_no": 5,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd426190a",
            "port_type": "Input",
            "port_no": 6,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd426190b",
            "port_type": "Input",
            "port_no": 7,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd426190c",
            "port_type": "Input",
            "port_no": 8,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd426190d",
            "port_type": "Output",
            "port_no": 1,
            "port_catg": "IO",
            "name": "ดับเครื่อง",
            "val_name0": "ยกเลิก",
            "command_id0": 5,
            "val_name1": "สั่งดับเครื่อง",
            "command_id1": 6
        },
        {
            "_id": "5bb766e321f6b3dbd426190e",
            "port_type": "Output",
            "port_no": 2,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd426190f",
            "port_type": "Output",
            "port_no": 3,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd4261910",
            "port_type": "Output",
            "port_no": 4,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd4261911",
            "port_type": "Output",
            "port_no": 5,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd4261912",
            "port_type": "Output",
            "port_no": 6,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd4261913",
            "port_type": "Output",
            "port_no": 7,
            "port_catg": "IO"
        },
        {
            "_id": "5bb766e321f6b3dbd4261914",
            "port_type": "Output",
            "port_no": 8,
            "port_catg": "IO"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 16
}
```