[Voltar](./unidadesdeatendimento.md)
# Academia de saúde
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "color": "#7c9ffe",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "Academias de saúde",
        "name": "open",
        "path": "ACADEMIA-SAUDE-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "ACADEMIA-SAUDE-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/academiaSaude/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": ""
    }
}
```

### REQUISIÇÕES
Esta tela não possui requisições