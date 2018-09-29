# Dealer Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> reseller = "reseller"

# newDealer

## url
    http://{server}/newDealer 

## request body
```json
{
    "login_name": "Dealer1",
    "first_name": "ไพบูลย์ dealer",
    "last_name": "ยืนยง",
    "tel_no": "026876091,028976718",
    "email": "paiboon.yue@gmail.com",
    "company_name": "simple corporation",
    "line_api_token": "xxxyyyzzz",
    "password": "dealer1234",
    "is_send_daily_report": true,
    "is_create_subdealer": false /* new requirement */
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


# updateDealer

## url
    http://{server}/updateDealer/{id}

## request body
```json
{
    "login_name": "Dealer1",
    "first_name": "ไพบูลย์ dearer1",
    "last_name": "ยืนยง",
    "tel_no": "026876091",
    "email": "paiboon.yue@gmail.com",
    "company_name": "simple corporation2",
    "line_api_token": "xxxyyyzzz",
    "is_send_daily_report": true,
    "is_create_subdealer": false /* new requirement */
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
# deleteUser
    Use to delete admin, dealer, reseller

## url
    http://{server}/deleteUser/{id}

## request body (No)

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getUserInfo
    Use to get information of user all level

## url
    http://{server}/getUserInfo/{id}

## request body (No)

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "5b9e1557fff63308f8c4e603",
            "login_name": "Dealer2",
            "first_name": "Toto dealer",
            "last_name": "กันนี่",
            "tel_no": "026876091,028976718",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "line_api_token": "xxxyyyzzz",
            "password": "dealer128",
            "is_send_daily_report": true,
            "is_create_subdealer": false, /* new requirement */
            "user_id": 3,
            "parent_id": 1,
            "user_level": 2,
            "create_user": "Paiboo1 (1)",
            "create_dtm": "2018-09-16T08:33:27.011Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# getDealerList

## url
    http://{server}//getDealerList/{pageNo}/{pageSize}

## request body (body empty = getAll)

```json

{    
	"filter":"to"
}

```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "5b9e1557fff63308f8c4e603",
            "login_name": "Dealer2",
            "first_name": "Toto dealer",
            "last_name": "กันนี่",
            "tel_no": "026876091,028976718",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "line_api_token": "xxxyyyzzz",
            "password": "dealer128",
            "is_send_daily_report": true,
            "is_create_subdealer": false, /* new requirement */
            "user_id": 3,
            "parent_id": 1,
            "user_level": 2,
            "create_user": "Paiboo1 (1)",
            "create_dtm": "2018-09-16T08:33:27.011Z"
        },
        {
            "_id": "5b9e16915cb77c16802c6eef",
            "login_name": "Dealer5",
            "first_name": "Toto2 dealer",
            "last_name": "กันนี่",
            "tel_no": "026876091,028976718",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "line_api_token": "xxxyyyzzz",
            "password": "dealer128",
            "is_send_daily_report": true,
            "is_create_subdealer": false, /* new requirement */
            "user_id": 5,
            "parent_id": "1",
            "user_level": 2,
            "create_user": "Paiboo1 (1)",
            "create_dtm": "2018-09-16T08:38:41.466Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}

```



