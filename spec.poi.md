# POI Management

## Request Header (alway pass : user_id,user_name,token) 
    for development phase use token in list below but for production have to get from login method 
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# newPOI

## url
    http://{server}/newPOI 

## request body
```json
{
    "name" : "หมู่บ้านพฤกษาวิลเวล 29",
    "group" : "B-quick ddd",
    "radius" : 50.0,
    "location" : {
        "latitude" : 14.988135,
        "longitude" : 102.096535
    },
    "icon" : {
        "name" : "bicycle",
        "color" : "indigo",
        "is_small" : false
    },
    "alert" : {
        "email" : "paiboon.yue@gmail.com",
        "line_token" : "349ab29a-xtab-423b-a5hc-5623bc39b8c8",
        "when" : {
            "is_entry" : true,
            "is_leave" : false
        }
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


# updatePOI

## url
    http://{server}/updatePOI/{id}

## request body
```json

{
    "name" : "Sweet Dug2",
    "group" : "B-quick ddd",
    "radius" : 50.0,
    "location" : {
        "latitude" : 14.988135,
        "longitude" : 102.096535
    },
    "icon" : {
        "name" : "bicycle",
        "color" : "indigo",
        "is_small" : false
    },
    "alert" : {
        "email" : "paiboon.yue@gmail.com",
        "line_token" : "349ab29a-xtab-423b-a5hc-5623bc39b8c8",
        "when" : {
            "is_entry" : true,
            "is_leave" : false
        }
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

# deletePOI

## url
    http://{server}/deletePOI/{id}

## request body (No)

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getPOIInfo

## url
    http://{server}/getPOIInfo/{id}

## request body (No)

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "_id": "5b9e76449a33c715f0cdad3f",
            "name": "หมู่บ้านพฤกษาวิลเวจ The Season",
            "group": "B-quick ddd",
            "radius": 50,
            "location": {
                "latitude": 14.988135,
                "longitude": 102.096535
            },
            "icon": {
                "name": "bicycle",
                "color": "indigo",
                "is_small": false
            },
            "alert": {
                "email": "paiboon.yue@gmail.com",
                "line_token": "349ab29a-xtab-423b-a5hc-5623bc39b8c8",
                "when": {
                    "is_entry": true,
                    "is_leave": false
                }
            },
            "poi_id": 1,
            "user_id": 2,
            "create_user": "kelly (2)",
            "create_dtm": "2018-09-16T15:27:00.571Z",
            "last_upd_dtm": "2018-09-16T15:37:36.418Z",
            "last_upd_user": "kelly (2)"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# setPOIVisible

## url
    http://{server}/setPOIVisible/{id}

## request body

```json

{    
	"isVisible":true
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

