# Employee Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# newEmployee

## url
    http://{server}/newEmployee 

## request body
```json

{
    "login_name": "kellEmployee",
    "first_name": "ไพบูลย์2",
    "last_name": "ยืนยง",
    "tel_no": "026876091",
    "email": "paiboon.yue@gmail.com",
    "company_name": "simple corporation",
    "password": "123456",
    "is_send_email_alert_overdue": false,
    "is_auto_dispermit": true,
    "reseller_note": "test note"
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

## response (if duplicate login name)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "U01",
    "RESULT_MESSAGE": "Duplicate Login Name"
}

```

# updateEmployee

## url
    http://{server}/updateEmployee/{id}

## request body
```json
{
    "login_name": "kellyEmployee",
    "first_name": "ไพบูลย์2",
    "last_name": "ยืนยง",
    "tel_no": "026876091",
    "email": "paiboon.yue@gmail.com",
    "company_name": "simple corporation",
    "is_send_email_alert_overdue": false,
    "is_auto_dispermit": true,
    "reseller_note": "test update data"
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

## response (if duplicate login name)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "U01",
    "RESULT_MESSAGE": "Duplicate Login Name"
}

```

# deleteUser
    Use to delete admin, dealer, customer, employee

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
            "_id": "5b9e226d2b496212505e0138",
            "login_name": "kellyEmployee",
            "first_name": "ไพบูลย์2",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "password": "123456",
            "is_send_email_alert_overdue": false,
            "is_auto_dispermit": true,
            "reseller_note": "test update data",
            "user_id": 7,
            "parent_id": 2,
            "user_level": 3,
            "create_user": "kelly dealer (2)",
            "create_dtm": "2018-09-16T09:29:17.520Z",
            "last_upd_dtm": "2018-09-16T09:50:23.902Z",
            "last_upd_user": "kellyDealer (1)"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```
# getEmployeeList

## url
    http://{server}/getEmployeeList/{pageNo}/{pageSize}

## request body (body empty = getAll)

```json

{    
	"filter":"ไพ"
}

```

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "5b9e208670fccd37780a6a4b",
            "login_name": "kellEmployee",
            "first_name": "ไพบูลย์2",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "password": "123456",
            "is_send_email_alert_overdue": false,
            "is_auto_dispermit": true,
            "reseller_note": "test note",
            "user_id": 6,
            "parent_id": 2,
            "user_level": 4,
            "create_user": "kelly dealer (2)",
            "create_dtm": "2018-09-16T09:21:10.093Z"
        },
        {
            "_id": "5b9e226d2b496212505e0138",
            "login_name": "kellyReseller",
            "owner_status": true,
            "first_name": "ไพบูลย์2",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "password": "newPassword",
            "is_send_email_alert_overdue": false,
            "is_auto_dispermit": true,
            "reseller_note": "test update data",
            "user_id": 7,
            "parent_id": 2,
            "user_level": 4,
            "create_user": "kelly customer (2)",
            "create_dtm": "2018-09-16T09:29:17.520Z",
            "last_upd_dtm": "2018-09-16T10:18:05.435Z",
            "last_upd_user": "IwantTochange (7)"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}

```