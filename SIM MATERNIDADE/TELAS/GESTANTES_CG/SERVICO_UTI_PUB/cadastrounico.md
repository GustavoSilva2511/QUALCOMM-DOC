[Voltar](./servico_uti_pub.md)
# Cadastro unico
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "color": "#7c9ffe",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "Cadastro único",
        "name": "open",
        "path": "CADASTRO-UNICO-CAMPINA-GRANDE"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "CADASTRO-UNICO-CAMPINA-GRANDE",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/cadastroUnico/response",
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