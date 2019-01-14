# Device Model

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# getCarTypeList

## url
    http://{server}/api/admin/getDeviceModelList

## request body
```json
{
  "filter": "t3"
}
```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "model_id": 1,
            "model_name": "T333"
        },
        {
            "model_id": 2,
            "model_name": "ID5"
        },
        {
            "model_id": 3,
            "model_name": "Vt900"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 3
}
```
