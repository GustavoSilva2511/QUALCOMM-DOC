[Voltar](../../wikipedia.md)
# Canais de atendimento
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "name": "open",
        "path": "CANAISATENDIMENTO"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "CANAISATENDIMENTO",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/canaisAtendimento/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": ""
    }
}
```

### REQUISIÇÕES
Esta pagina não possui requisições