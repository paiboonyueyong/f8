# Authentication Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> reseller = "reseller"

# changePassword

## url
    http://{server}/changePassword/{id}

## request body
```json
{
    "password": "newPassword",   
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


# login
    This method not have header

## url
    http://{server}/login

## request body

```json

{
	"userLogin":"Dealer1",
	"password":"dealer1234"
}

```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "5b9ce7f08ceb581d5c0a8570",
            "login_name": "Dealer1",
            "first_name": "ไพบูลย์ dearer1",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation2",
            "line_api_token": "xxxyyyzzz",
            "password": "dealer1234",
            "is_send_daily_report": true,
            "user_id": 2,
            "parent_id": 1,
            "user_level": 2,
            "create_user": "Paiboo1 (1)",
            "create_dtm": "2018-09-15T11:07:28.042Z",
            "last_upd_dtm": "2018-09-16T08:13:16.464Z",
            "last_upd_user": "Paiboo1 (1)",
            "token": "4d5a5c80192d317397ce30c73e0ffe1c456db819f85564587710725644d8c1b6"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```
