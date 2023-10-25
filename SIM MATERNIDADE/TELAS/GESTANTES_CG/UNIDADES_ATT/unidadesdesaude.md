[Voltar](./unidadesdeatendimento.md)
# Unidades de saude
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "color": "#1AACB6",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "Unidades de saúde",
        "name": "open",
        "icon": "e9ac",
        "path": "UNIDADE-SAUDE-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "UNIDADE-SAUDE-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/unidadeSaude/response",
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