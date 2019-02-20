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

# newManyPOI

## url
    http://{server}/newManyPOI/

## request body

```json

[
	{
	    "name" : "test poi 1",
	    "group" : "test",
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
		    "is_entry" : false,
		    "is_leave" : false
		}
	    }
	},
	{
	    "name" : "test poi 2",
	    "group" : "test",
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
		    "is_entry" : false,
		    "is_leave" : false
		}
	    }
	}
]

```

## response (if success)

```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


# getPOIGroupList

## url
    http://{server}/getPOIGroupList

## request body (no)

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "id": "ไม่มีกลุ่ม",
            "desc": "ไม่มีกลุ่ม (5)"
        },
        {
            "id": "B-quick ddd",
            "desc": "B-quick ddd (2)"
        },
        {
            "id": "ฟาย",
            "desc": "ฟาย (1)"
        },
        {
            "id": "poi มาแล้ว",
            "desc": "poi มาแล้ว (1)"
        },
        {
            "id": "poi test",
            "desc": "poi test (1)"
        },
        {
            "id": "xpoi",
            "desc": "xpoi (1)"
        },
        {
            "id": "zzz",
            "desc": "zzz (1)"
        },
        {
            "id": "11",
            "desc": "11 (1)"
        },
        {
            "id": "B-quick 004",
            "desc": "B-quick 004 (1)"
        },
        {
            "id": "B-quick -003",
            "desc": "B-quick -003 (1)"
        },
        {
            "id": "บ้าน Owner",
            "desc": "บ้าน Owner (1)"
        },
        {
            "id": "B-quick ddd sssss",
            "desc": "B-quick ddd sssss (1)"
        },
        {
            "id": "B-quick ddd bbb",
            "desc": "B-quick ddd bbb (1)"
        },
        {
            "id": "B-quick ddd ccc",
            "desc": "B-quick ddd ccc (1)"
        },
        {
            "id": "ss",
            "desc": "ss (1)"
        },
        {
            "id": "group",
            "desc": "group (1)"
        },
        {
            "id": "toto",
            "desc": "toto (1)"
        },
        {
            "id": "กลุ่มเราเอง",
            "desc": "กลุ่มเราเอง (1)"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}

```


