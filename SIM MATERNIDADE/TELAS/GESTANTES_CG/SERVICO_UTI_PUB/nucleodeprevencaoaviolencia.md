[Voltar](./servico_uti_pub.md)
# Núcleo de prevenção de violência
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "color": "#7c9ffe",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "Núcleo de prevenção de violência",
        "name": "open",
        "path": "SERVICO-UTILIDADE-PUBLICA"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "SERVICO-UTILIDADE-PUBLICA",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/servicoUtilidadePublica/response",
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