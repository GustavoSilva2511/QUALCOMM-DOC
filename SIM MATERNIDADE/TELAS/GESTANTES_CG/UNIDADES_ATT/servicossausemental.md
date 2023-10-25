[Voltar](./unidadesdeatendimento.md)
# Serviços de saúde mental
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "color": "#1AACB6",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "Serviços de saúde mental",
        "name": "open",
        "path": "COORDENACAO-SAUDE-MENTAL-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "COORDENACAO-SAUDE-MENTAL-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/coordenacaoSaudeMental/response",
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