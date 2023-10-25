[Voltar](./servico_uti_pub.md)
# Assistencia social - CRAS
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "color": "#7c9ffe",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "CRAS",
        "name": "open",
        "path": "ASSISTENCIA-SOCIAL-CRAS",
        "parameters": []
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "ASSISTENCIA-SOCIAL-CRAS",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/cras/response",
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