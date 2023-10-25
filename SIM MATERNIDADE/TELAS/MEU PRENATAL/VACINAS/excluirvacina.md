[Voltar](./consultavacina.md)
# Excluir vacina
### Como chamar o path
~~~ python
"actions": [   
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 2,
        "title": "Excluir Vacina",
        "name": "open",
        "icon": "e936",
        "path": "EXCLUIR-VACINA-CONNECT",
        "parameters": [
            {"title":"actionConfirmation","value":"type=warning&message=Confirma a exclusão da vacina?&btnYes=Sim&btnNo=Não"},
            {
            "title": "Querystring",
            "value": f"?name={request.args.get('name')}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "EXCLUIR-VACINA-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/excluirVacina/response",
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
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", token)# filters de email



body = {
    "name": name,
    "parent": prenatal(),
    "parentfield": "vaccines",
    "parenttype": "Pre Natal",
    "doctype": "Vacina"
}
delete("https://neo-qualcomm-homo.mobilex.tech/api/method/neo.core.doctype.childapi.api.handler", body, token)



body = {
    "ocult": f"{string}"
}
put("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", body, token)
~~~