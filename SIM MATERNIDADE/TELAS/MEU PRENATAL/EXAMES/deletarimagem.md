[Voltar](./editaranexos.md)
# Deletar imagem
### Como chamar o path
~~~ python
{
    "order": 1,
    "publishLevel": 1,
    "permissionLevel": 1,
    "title": "Excluir",
    "icon": "e936",
    "name": "open",
    "path": "DELETEIMAGE",
    "parameters": [
        {
            "title":"actionConfirmation",
            "value":"type=warning&message=Deseja excluir a imagem?&btnYes=Sim&btnNo=Não"
            
        },
        {   
            "title": "Querystring",
            "value": f"?name={request.args.get('name')}&field={attach['name']}&link={attach['link']}&parent={exam[0].get('parent')}"
        }
    ]
}
~~~

### Corpo do path no manager
``` json
{
    "identifier": "DELETEIMAGE",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/deleteImage/response",
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
payload = {
    "command" : "delete_attach",
    "field" : request.args.get("field"),
    "path" : request.args.get("link")
}
body = {
    "command": "get_all",
    "doctype": "Exame",
    "sub_command": "edit_fields",
    "sub_values": {request.args.get("field"): None, "attach_edited": str(payload)},
    "filters": {"name": request.args.get("name")}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)



body = {
    "name": request.args.get("parent")
}
res = requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal",, json=body, headers=headers)
~~~