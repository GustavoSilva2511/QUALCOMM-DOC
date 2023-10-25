[Voltar](./historicoexame.md)
# Anexos exame
### LINKS
- [Vizualizar imagem](./visualizarimagem.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Anexos",
        "name": "open",
        "path": "ANEXOSEXAMES",
        "parameters": [
            {
                "title": "querystring",
                "value": f"?name={exame.get('name')}&attachUrl={','.join([exame.get('attach_'+ i) for i in list(['1','2','3','4']) if exame.get('attach_'+ i) != '' and exame.get('attach_'+ i) != None])}&profissional_email={request.args.get('profissional_email')}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "ANEXOSEXAMES",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/anexosExames/anexos",
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

body = {
    "command": "get_all",
    "doctype": "Exame",
    "sub_command": "edit_fields",
    "sub_values": {"vizualization": f"{lista} {request.args.get('profissional_email')}".strip()},
    "filters": {"name": request.args.get("name")}
}
res = requests.post(url, json=body, headers=headers).json()



body = {
    "command": "get_all",
    "doctype": "Exame",
    "filters": {"name": request.args.get("name")}
}
res = requests.post(url, json=body, headers=headers).json()['msg'][0]
~~~