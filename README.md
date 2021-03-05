# `requests` LIBRARY

KREIRACU NOVI PYTHON FILE

- `touch dog.py`

IDEJA JE DA OVDE VRSIM INTERAKCIJU SA [API-EM](https://shibe.online/)

ONO STO SECAS OD RANIJE JESTE DA JE CONCURRENCY PYTHONA, POTPUNO DRUGACIJI OD JAVASCRIPT-A; JER U JAVASCRIPTU RECIMO IMAS PROMISE-E, A U PYTHON-U MISLIM DA IH NEMAS

```py
import requests

# OVO URL API-A SA KOJIM ZELIM DA INTERECCT-UJEM
# U SUSTINI JSON KOJI DOBIJAS JE URL SLIKE PSA
api_url = "https://shibe.online/api/shibes?count=1"

# DAKL, NA OVAJ NACIN CU IMATI PPRISTUP RESPONSE OBJEKTU

response = requests.get(api_url)

# PRINT-OVACU STATUS CODE SA RESPONSE-A

status_code = response.status_code

print("status code: ", status_code)

```

**MOZES DA RUN-UJES OVAJ FILE, A ONO STO BI TREBAL ODA VIDIS STAMPANO U TERMINALU JESTE STATUS CODE**

```bash
status code:  200
```
