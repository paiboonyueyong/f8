# Access Log View

## Request Header (alway pass : user_id,user_name,token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin" 
        -> dealer = "dealer" 
        -> customer = "customer"
        -> employee = "employee"

# getDriverList

## url
    http://{server}/getAccessLog/{pageNumber}/{pageSize} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "ip": "203.150.199.100",
            "agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/68.0.3440.106 Safari/537.36",
            "access_time": "2018-09-15 22:55"
        },
        {
            "ip": "203.150.199.101",
            "agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/68.0.3440.106 Safari/537.36",
            "access_time": "2018-09-15 22:56"
        },
        {
            "ip": "203.150.199.101",
            "agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/68.0.3440.106 Safari/537.36",
            "access_time": "2018-09-15 22:56"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```
