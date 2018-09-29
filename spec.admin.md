# Admin Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> owner = "owner (เจ้าของระบบ)" 

# newAdmin

## url
    http://{server}/newAdmin 

## request body
```json
{
    "login_name": "Admin1",
    "first_name": "ไพบูลย์ Admin",
    "last_name": "ยืนยง",
    "tel_no": "026876091",
    "email": "paiboon.yue@gmail.com",
    "password": "admin1234"
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


# updateAdmin

## url
    http://{server}/updateAdmin/{id}

## request body
```json
{
    "login_name": "Admin1",
    "first_name": "ไพบูลย์ Admin",
    "last_name": "ยืนยง",
    "tel_no": "026876091",
    "email": "paiboon.yue@gmail.com"
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
            "_id": "5b9fce91f2d80a47f00aafad",
            "login_name": "Admin2",
            "first_name": "ไพบูลย์ Admin2",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "password": "admin1234",
            "user_id": 8,
            "parent_id": 1,
            "user_level": 1,
            "create_user": "director (1)",
            "create_dtm": "2018-09-17T15:56:01.207Z",
            "last_upd_dtm": "2018-09-17T16:01:52.851Z",
            "last_upd_user": "director (1)"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# getAdminList

## url
    http://{server}//getAdminList/{pageNo}/{pageSize}

## request body (body empty = getAll)

```json

{    
	"filter":"Adm"
}

```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "5b9fce91f2d80a47f00aafad",
            "login_name": "Admin2",
            "first_name": "ไพบูลย์ Admin2",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "password": "admin1234",
            "user_id": 8,
            "parent_id": 1,
            "user_level": 1,
            "create_user": "director (1)",
            "create_dtm": "2018-09-17T15:56:01.207Z",
            "last_upd_dtm": "2018-09-17T16:01:52.851Z",
            "last_upd_user": "director (1)"
        },
        {
            "_id": "5b9fcec4f2d80a47f00aafae",
            "login_name": "Admin2",
            "first_name": "ไพบูลย์ Admin",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "password": "admin1234",
            "user_id": 9,
            "parent_id": 1,
            "user_level": 1,
            "create_user": "director (1)",
            "create_dtm": "2018-09-17T15:56:52.489Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}

```
