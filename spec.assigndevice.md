# Device Assignment Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# assignDevice

## url
    http://{server}/assignDevice/{userId}/{deviceId}

## request body (No)

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```

# cancelDevice

## url
    http://{server}/cancelDevice/{userId}/{deviceId}

## request body (No)

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getUserDeviceRelate

## url
    http://{server}/getUserDeviceRelated/{deviceId}/{pageNo}/{pageSize}


## request body (No)


## response (if success)

```json

{
    "RESULT_DATA": [
        {
            "first_name": "ห้ามลบ",
            "last_name": "ใช้ทดสอบ",
            "user_id": 5
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
        
```


# getUserNoDeviceRelate (for dropdownlist) 

## url
    http://{server}/getUserNoDeviceRelated/{deviceId}


## request body (No)


## response (if success)

```json

{
    "RESULT_DATA": [
        {
            "first_name": "ห้ามลบ",
            "last_name": "ใช้ทดสอบ",
            "user_id": 5
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
        
```
