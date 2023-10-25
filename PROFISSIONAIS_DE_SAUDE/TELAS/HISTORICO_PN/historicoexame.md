[Voltar](./historicopn.md)
# Histórico exame
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Exames",
        "icon":"",
        "name": "open",
        "path": "HISTORICOEXAMES",
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
    "identifier": "HISTORICOEXAMES",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/historicoExames/response",
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
# ------------------------ url base ---------------------------------
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"
url_child_table = f"{main_url_script}/childtableapi"


# -------------------------- requisições ----------------------------
body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {"email": request.args.get("email")}
}
response = requests.post(url_child_table, json=body, headers=headers).json()["msg"]
~~~