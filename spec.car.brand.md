# Car Brand Management

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# newCarBrand

## url
    http://{server}/newCarBrand

## request body
```json
{
  "name": "Toyota"
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

# updateCarBrand

## url
    http://{server}/updateCarBrand/{_id} 

## request body
```json
{
  "name": "Toyota"
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

# deleteCarBrand

## url
    http://{server}/deleteCarBrand/{_id} 

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
    http://{server}/getCarBrandInfo/{_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
            {
                "_id" : "5bad09a4dde869054d5f8ec7", 
                "name" : "ไม่ระบุ",
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

# getCarBrandList

## url
    http://{server}/getCarBrandList

## request body
```json
{
  "filter": "to"
}
```

## response (if success)

```json
{
    "RESULT_DATA": [
            {
                "_id" : "5bad09a4dde869054d5f8ec7", 
                "name" : "ไม่ระบุ",
                "create_user": "Wutthin",
                "last_upd_user": "Wutthin",
                "create_dtm": "2018-09-30T15:43:33.288Z",
                "last_upd_dtm": "2018-09-30T16:21:38.602Z"
            },
            {
                "_id" : "5bad09a4dde869054d5f8ec8", 
                "name" : "101SAVE",
                "create_user": "Wutthin",
                "last_upd_user": "Wutthin",
                "create_dtm": "2018-09-30T15:43:33.288Z",
                "last_upd_dtm": "2018-09-30T16:21:38.602Z"
            }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 151
}
```
