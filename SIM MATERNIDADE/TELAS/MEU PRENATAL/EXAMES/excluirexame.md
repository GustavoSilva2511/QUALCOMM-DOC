[Voltar](./consultarexame.md)
# Excluir exame
### Como chamar o path
~~~ python
"actions": [   
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 2,
        "title": "Excluir Exame",
        "name": "open",
        "icon": "e936",
        "path": "EXCLUIR-EXAME-CONNECT",
        "parameters": [
            {"title":"actionConfirmation","value":"type=warning&message=Confirma a exclusão do exame?&btnYes=Sim&btnNo=Não"},
            {
                "title": "Querystring",
                "value": f"?name={name}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "EXCLUIR-EXAME-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/excluirExame/response",
        "method": "GET",
        "header": {
        "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]"
    }
}
```

### REQUISIÇÕES
~~~ python
body = {
    "command": "get_all",
    "doctype": "Exame",
    "filters": {"name": request.args.get("name")}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)



body = {
    "name": getId()
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal", json=body, headers=headers)



body = {
    "command": "get_all",
    "doctype": "Exame",
    "filters": {"name": request.args.get("name")},
    "sub_command": "delete_doc"
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)



payload = {
    "command" : "delete_path",
    "exam_id": request.args.get("name")
}
body = {
    "command": "get_all",
    "doctype": "Exame",
    "sub_command": "edit_fields",
    "sub_values": {"attach_edited": str(payload)},
    "filters": {"name": request.args.get("name")}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~