# Customer Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# newReseller

## url
    http://{server}/newCustomer 

## request body
```json

{
    "login_name": "kellCustomer",
    //"owner_status": true, (remove from new requirment)
    "first_name": "ไพบูลย์2",
    "last_name": "ยืนยง",
    "tel_no": "026876091",
    "email": "paiboon.yue@gmail.com",
    "company_name": "simple corporation",
    "password": "123456",
    "is_send_email_alert_overdue": false,
    "is_auto_dispermit": true,
    "reseller_note": "test note",
    "privileges": {
        "is_view_tracking": true,
        "is_view_poi": true,
        "is_edit_poi": true,
        "is_view_history": false,
        "is_send_command": true,
        "is_view_report": false
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

# updateReseller

## url
    http://{server}/updateCustomer/{id}

## request body
```json
{
    "login_name": "kellyCustomer",
    //"owner_status": true, (remove from new requirement)
    "first_name": "ไพบูลย์2",
    "last_name": "ยืนยง",
    "tel_no": "026876091",
    "email": "paiboon.yue@gmail.com",
    "company_name": "simple corporation",
    "is_send_email_alert_overdue": false,
    "is_auto_dispermit": true,
    "reseller_note": "test update data",
    "privileges": {
        "is_view_tracking": true,
        "is_view_poi": true,
        "is_edit_poi": true,
        "is_view_history": false,
        "is_send_command": true,
        "is_view_report": false
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
            "_id": "5b9e226d2b496212505e0138",
            "login_name": "kellyReseller",
            "first_name": "ไพบูลย์2",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "password": "123456",
            "is_send_email_alert_overdue": false,
            "is_auto_dispermit": true,
            "reseller_note": "test update data",
            "privileges": {
                "is_view_tracking": true,
                "is_view_poi": true,
                "is_edit_poi": true,
                "is_view_history": false,
                "is_send_command": true,
                "is_view_report": false
            },
            "user_id": 7,
            "parent_id": "2",
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
# getResellerList

## url
    http://{server}/getCustomerList/{pageNo}/{pageSize}

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
            "login_name": "kellreseller",
            //"owner_status": true, (remove from new requirement)
            "first_name": "ไพบูลย์2",
            "last_name": "ยืนยง",
            "tel_no": "026876091",
            "email": "paiboon.yue@gmail.com",
            "company_name": "simple corporation",
            "password": "123456",
            "is_send_email_alert_overdue": false,
            "is_auto_dispermit": true,
            "reseller_note": "test note",
            "privileges": {
                "is_view_tracking": true,
                "is_view_poi": true,
                "is_edit_poi": true,
                "is_view_history": false,
                "is_send_command": true,
                "is_view_report": false
            },
            "user_id": 6,
            "parent_id": 2,
            "user_level": 3,
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
            "privileges": {
                "is_view_tracking": true,
                "is_view_poi": true,
                "is_edit_poi": true,
                "is_view_history": false,
                "is_send_command": true,
                "is_view_report": false
            },
            "user_id": 7,
            "parent_id": 2,
            "user_level": 3,
            "create_user": "kelly dealer (2)",
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