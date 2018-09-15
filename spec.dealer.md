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
    "is_send_daily_report": true
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



