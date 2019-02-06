# Access Log View

## Request Header (alway pass : ,token)
    for development phase use token in list below but for production have to get from login method

# newPayment

## url
    http://{server}/api/admin/newPayment

## request body
```json
{
	"amount" : 10000,
	"transaction_dtm" : "16-02-1981 23:00",
	"banking": "Kbank",
	"originate_banking" : "Kbank",
	"remark": "ทดสอบ API",
	"devices" : [{
		"device_id":18681
	}],
	"attachs" : [
		{
			"name": "nan.jpg",
			"content" : "ewogICJuYW1lIjogImFwaSIsCiAgInZlcnNpb24iOiAiMS4wLjAiLAogICJkZXNjcmlwdGlvbiI6ICIiLAogICJtYWluIjogInNlcnZlci5qcyIsCiAgInNjcmlwdHMiOiB7CiAgICAidGVzdCI6ICJlY2hvIFwiRXJyb3I6IG5vIHRlc3Qgc3BlY2lmaWVkXCIgJiYgZXhpdCAxIiwKICAgICJzdGFydCI6ICJub2RlIHNlcnZlci5qcyIKICB9LAogICJrZXl3b3JkcyI6IFtdLAogICJhdXRob3IiOiAiIiwKICAibGljZW5zZSI6ICJJU0MiLAogICJkZXBlbmRlbmNpZXMiOiB7CiAgICAiYXN5bmMiOiAiXjIuNi4xIiwKICAgICJib2R5LXBhcnNlciI6ICJeMS4xOC4zIiwKICAgICJjcnlwdG8iOiAiXjEuMC4xIiwKICAgICJkYXRlLWFuZC10aW1lIjogIl4wLjYuMiIsCiAgICAiZXhwcmVzcyI6ICJeNC4xNi4zIiwKICAgICJoZXgtdG8tYmluYXJ5IjogIl4xLjAuMSIsCiAgICAibW9uZ29kYiI6ICJeMy4xLjMiLAogICAgIm5vZGUtZGF0ZXRpbWUtdGhhaSI6ICJeMS4wLjYiLAogICAgIm9yYWNsZWRiIjogIl4yLjMuMCIsCiAgICAicHJvcGVydGllcy1yZWFkZXIiOiAiMC4wLjE2IiwKICAgICJzaG9ydGlkIjogIl4yLjIuMTQiLAogICAgInV0ZjgiOiAiXjMuMC4wIgogIH0KfQo="
		},
        {
			"name": "payment.jpg",
			"content" : "ewogICJuYW1lIjogImFwaSIsCiAgInZlcnNpb24iOiAiMS4wLjAiLAogICJkZXNjcmlwdGlvbiI6ICIiLAogICJtYWluIjogInNlcnZlci5qcyIsCiAgInNjcmlwdHMiOiB7CiAgICAidGVzdCI6ICJlY2hvIFwiRXJyb3I6IG5vIHRlc3Qgc3BlY2lmaWVkXCIgJiYgZXhpdCAxIiwKICAgICJzdGFydCI6ICJub2RlIHNlcnZlci5qcyIKICB9LAogICJrZXl3b3JkcyI6IFtdLAogICJhdXRob3IiOiAiIiwKICAibGljZW5zZSI6ICJJU0MiLAogICJkZXBlbmRlbmNpZXMiOiB7CiAgICAiYXN5bmMiOiAiXjIuNi4xIiwKICAgICJib2R5LXBhcnNlciI6ICJeMS4xOC4zIiwKICAgICJjcnlwdG8iOiAiXjEuMC4xIiwKICAgICJkYXRlLWFuZC10aW1lIjogIl4wLjYuMiIsCiAgICAiZXhwcmVzcyI6ICJeNC4xNi4zIiwKICAgICJoZXgtdG8tYmluYXJ5IjogIl4xLjAuMSIsCiAgICAibW9uZ29kYiI6ICJeMy4xLjMiLAogICAgIm5vZGUtZGF0ZXRpbWUtdGhhaSI6ICJeMS4wLjYiLAogICAgIm9yYWNsZWRiIjogIl4yLjMuMCIsCiAgICAicHJvcGVydGllcy1yZWFkZXIiOiAiMC4wLjE2IiwKICAgICJzaG9ydGlkIjogIl4yLjIuMTQiLAogICAgInV0ZjgiOiAiXjMuMC4wIgogIH0KfQo="
		}
	]
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "payment_id": 1013
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 1
}
```

# getPaymentList

## url
    http://{server}/api/admin/getPaymentList/{pageNo}/{pageSize}

**
    img : ให้ reference ด้วย http://{server}/api/admin/ + ข้อมูลที่ได้จาก response

## request body
```json
{
    "filter": "t33",
    "include_verified": true // ให้แสดงรายการตรวจสอบแล้วด้วย default แสดงเฉพาะที่ยังไม่ตรวจสอบ
}
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "amount": 10000,
            "transaction_dtm": "16 ก.พ. 2524 23:00"
            "banking": "Kbank",
            "originate_banking": "Kbank",
            "remark": "ทดสอบ API",
            "devices": [
                {
                    "device_id": 18681,
                    "device_no": "T333/30s",
                    "device_group": "wutthinan",
                    "expire_date": "16 ก.พ. 2524 23:00",
                    "install_date": "16 ก.พ. 2524 23:00",
                    "install_with_rfid": true
                }
            ],
            "attachs": [
                {
                    "name": "nan.jpg",
                    "img": "/paymentReceipt/1014/nan.jpg"
                },
                {
                    "name": "payment.jpg",
                    "img": "/paymentReceipt/1014/payment.jpg"
                }
            ],
            "payment_id": 1014,
            "user_id": 167,
            "verified": false
        },
        {
            "amount": 10000,
            "transaction_dtm": "16 ก.พ. 2524 23:00",
            "banking": "Kbank",
            "originate_banking": "Kbank",
            "remark": "ทดสอบ API",
            "devices": [
                {
                    "device_id": 18681,
                    "device_no": "T333/30s",
                    "device_group": "wutthinan",
                    "expire_date": "16 ก.พ. 2524 23:00",
                    "install_date": "16 ก.พ. 2524 23:00",
                    "install_with_rfid": true
                }
            ],
            "attachs": [
                {
                    "name": "nan.jpg",
                    "img": "/paymentReceipt/1013/nan.jpg"
                }
            ],
            "payment_id": 1013,
            "user_id": 167,
            "verified": false
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull",
    "RESULT_TOTAL": 2
}
```

# setPaymentVerified

## url
    http://{server}/api/admin/setPaymentVerified/{payment_id}

## request body
```json
```

## response (if success)
```json
{
    "RESULT_DATA": [],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```

# getPaymentInfo

## url
    http://{server}/api/admin/getPaymentInfo/{payment_id}

## request body
```json
```

## response (if success)
```json
{
    "RESULT_DATA": [
        {
            "amount": 10000,
            "transaction_dtm": "16 ก.พ. 2524 23:00",
            "banking": "Kbank",
            "originate_banking": "Kbank",
            "remark": "ทดสอบ API",
            "devices": [
                {
                    "device_id": 18681,
                    "device_no": "T333/30s",
                    "device_group": "wutthinan",
                    "expire_date": "6 ก.ค. 2562 00:00",
                    "install_date": "2 ธ.ค. 2561 00:00",
                    "install_with_rfid": true
                }
            ],
            "attachs": [
                {
                    "name": "nan.jpg",
                    "img": "/paymentReceipt/1013/nan.jpg"
                }
            ],
            "payment_id": 1013,
            "user_id": 167,
            "verified": true
        }
    ],
    "RESULT_STATUS": "000",
    "RESULT_MESSAGE": "Successfull"
}
```
