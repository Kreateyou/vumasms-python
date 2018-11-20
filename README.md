# vumasms-python
VumaSMS REST API client for Python. API support for bulk SMS, Numbers, Verify (2FA) and more.

# Installation
```
pip install vumasms
```
# Upgrade
if you had already installed the package to upgrade to the latest run the following command
``` 
pip install vumasms --upgrade
``` 

Create a python script and in it add the following,
```
from vumasms.VumaSMS import VumaSMS
API_TOKEN = "<from vuma portal>";
API_SECRET = "<from vuma portal>"
SMS_BODY = { 
             "to":["2547XXXXXXX"],
             "sender":"VUMA",
             "message":"Test message from the vumasms Python Client",
             "scheduled_date":"",
             "scheduled_type":""
           }
vuma = VumaSMS(API_TOKEN,API_SECRET)
print vuma.send_sms(SMS_BODY)
```
Where API_TOKEN and API_SECRET are obtained from [VumaSMS portal](https://www.vumasms.com "Vumsms's Homepage") under setting Api Credentials 
