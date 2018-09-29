# News Management

## Request Header (new and delte need to pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# newNews

## url
    http://{server}/newNews 

## request body
```json
{
  "title":"หัวข้อ",
  "details":"คำนำหน้า"
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

# deleteNews

## url
    http://{server}/deleteNews/{_id} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```
# getNewsList

## url
    http://{server}/getNewsList 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "5b9d2eb7a852e92b3403cc1c",
            "title": "หัวข้อ",
            "details": "คำนำหน้า",
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-15T16:09:27.474Z",
            "last_upd_dtm": "2018-09-15T16:09:27.474Z"
        },
        {
            "_id": "5b9d2eb6a852e92b3403cc1b",
            "title": "หัวข้อ",
            "details": "คำนำหน้า",
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-15T16:09:26.867Z",
            "last_upd_dtm": "2018-09-15T16:09:26.867Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getNewsList

## url
    http://{server}/getNewsList/{pageNumber}/{pageSize} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "5b9d2eb7a852e92b3403cc1c",
            "title": "หัวข้อ",
            "details": "คำนำหน้า",
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-15T16:09:27.474Z",
            "last_upd_dtm": "2018-09-15T16:09:27.474Z"
        },
        {
            "_id": "5b9d2eb6a852e92b3403cc1b",
            "title": "หัวข้อ",
            "details": "คำนำหน้า",
            "create_user": "Wutthin",
            "last_upd_user": "Wutthin",
            "create_dtm": "2018-09-15T16:09:26.867Z",
            "last_upd_dtm": "2018-09-15T16:09:26.867Z"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```