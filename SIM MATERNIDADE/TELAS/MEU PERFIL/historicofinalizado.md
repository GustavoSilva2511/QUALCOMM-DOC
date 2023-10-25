[Voltar](./historicoprenatais.md)
# Histórico finalizado
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "name": "open",
        "publishLevel": 1,
        "permissionLevel": 2,
        "path": "PRENATAL-FINALIZADO",
        "parameters": [
            {
                "title": "querystring",
                "value": f"?name=xxx-xxx"
            }
        ]
    }
]
~~~


### Corpo do path no manager
``` json
{
    "identifier": "PRENATAL-FINALIZADO",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/preNatalFinalizado/response",
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
    "doctype": "Pre Natal",
    "filters": {
        "finished": 1,
        "name": "xxx-xxx"
    }
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, TOKEN)
~~~