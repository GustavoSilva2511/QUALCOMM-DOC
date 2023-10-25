[Voltar](./acompanhamentopn.md)
# Exames
### LINKS
- [Anexos exames](./anexosexame.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Exames",
        "icon":"e971",
        "name": "open",
        "path": "EXAMES",
        "parameters": [
            {
                "title": "querystring",
                "value": f"?email={gestante['email']}&profissional_email={request.args.get('email')}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "EXAMES",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/exames/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": ""
    }
}
```

### REQUISIÇÕES
~~~ python
# --------------------------- Urls base --------------------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"
url_child_table = f"{main_url_script}/childtableapi"

# --------------------------- Requisições --------------------------------
url = main_url_neo + f'''/Pre Natal?fields=["name"]&filters=[["email","=","{email}"],["finished","=","0"]]''';
res = requests.get(url,headers=headers).json()['data']



body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "fields": ["exams"],
    "filters": {
        "email": email, 
        "finished": 0
    }
}
res = requests.post(url_child_table, json=body, headers=headers).json()['msg'][0]['exams']



body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "sub_command": "edit_fields",
    "sub_values": {"hasnew": None},
    "filters": {"email": request.args.get("email")}
}
res = requests.post(url_child_table, json=body, headers=headers)
~~~