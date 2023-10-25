[Voltar](../../wikipedia.md)
# Unidades de saúde
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "name": "open",
        "path": "DISTRITOS"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "DISTRITOS",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/distritos/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": ""
    }
}
```

### ACTIONS 
~~~ python
"actions": [
    {
        "order": 2,
        "publishLevel": 1,
        "permissionLevel": 1,
        "name": "share",
        "title": "Compartilhar Unidade de saúde",
        "parameters": [
            {
                "title": "text",
                "value": f"{unit['full_name']}\n{unit.get('address', 'Endereço não atribuído')}\nTel.: 83 3077-1321"
            }
        ]
    },
    {
        "order": 0,
        "permissionLevel": 1,
        "publishLevel": 1,
        "title": "Abrir no mapa",
        "icon": "e9db",
        "name": "maps",
        "parameters": [
            {
                "title": "Endereço",
                "value": unit.get('address', "Endereço não atribuído")
            }
        ]
    },
    {
        "order": 1,
        "permissionLevel": 1,
        "publishLevel": 1,
        "title": "Ligar para",
        "icon": "e9ef",
        "name": "call",
        "parameters": [
            {
                "title": unit.get('full_name'),
                "value": "83 3077-1321"
            }
        ]
    }
]
~~~

### REQUISIÇÕES
~~~ python
# -------------------- url base ----------------------
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"

# -------------------- requisição ---------------------
url = f"{main_url_script}/childtableapi"
body = {
    "command": "get_all",
    "order_by": "district",
    "doctype": "Unidades de Atendimento Completo",
    "fields": ["district"],
    "sub_command": "no_repeat"
}
res = requests.post(url, json=body, headers=headers).json()['msg']



url = f"{main_url_script}/childtableapi"
body = {
    "command": "get_all",
    "order_by": "full_name",
    "doctype": "Unidades de Atendimento Completo",
    "filters": {"district": district}    
}
res = requests.post(url, json=body, headers=headers).json()['msg']
~~~