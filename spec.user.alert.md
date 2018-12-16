# User Alert

## Request Header (alway pass : token)
    for development phase use token in list below but for production have to get from login method
        -> admin = "admin"
        -> dealer = "dealer"
        -> reseller = "reseller"

# getUserAlert
    
PAYMENT - ถึงกำหนดชำระ
CAR NO - แจ้งอัพเดททะเบียน
TRACKING - รถไม่ส่งสัญญาน

## url
    http://{server}/api/admin/getUserAlert/{pageNumber}/{pageSize} 

## request body

## response (if success)

```json
{
    "RESULT_DATA": [
        {
            "device_id": 18681,
            "Mesage": "เลขเครื่อง #$#T333/30s#$# รถที่ติดตั้งจีพีเอส ถึงกำหนดชำระค่าบริการวันที่ 26 พ.ย. 2561",
            "group": "PAYMENT"
        },
        {
            "device_id": 18679,
            "Mesage": "เลขเครื่อง #$#ID5#$# รถป้ายแดงที่ติดตั้งจีพีเอส หากได้ป้ายทะเบียนแล้ว รบกวนแจ้งกลับทางเราเพื่อทำการบันทึกข้อมูลใหม่",
            "group": "CAR NO"
        },
        {
            "device_id": 18698,
            "Mesage": "เลขเครื่อง #$#18698#$# รถป้ายแดงที่ติดตั้งจีพีเอส หากได้ป้ายทะเบียนแล้ว รบกวนแจ้งกลับทางเราเพื่อทำการบันทึกข้อมูลใหม่",
            "group": "CAR NO"
        },
        {
            "device_id": 18662,
            "Mesage": "เลขเครื่อง #$#1กย-1287#$# รถป้ายแดงที่ติดตั้งจีพีเอส เมื่อวันที่ 29 ส.ค. 2561 หากได้ป้ายทะเบียนแล้ว รบกวนแจ้งกลับทางเราเพื่อทำการบันทึกข้อมูลใหม่",
            "group": "CAR NO"
        },
        {
            "device_id": 18679,
            "Mesage": "รถทะเบียน #$#ID5 #$# ได้หยุดส่งข้อมูลเกิน 7 วัน กรุณาแจ้งสาเหตุที่เครื่องหยุดส่ง โดยพิมพ์ใส่ในช่องนี้",
            "group": "TRACKING"
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 5
}
```