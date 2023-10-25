[Voltar](../gestantescg.md)
# Serviço de utilidade pública
### LINKS
- [Assistência social - CRAS](./assistenciasocial.md)
- [Cadastro único](./cadastrounico.md)
- [Núcleo de prevenção de violência](./nucleodeprevencaoaviolencia.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "permissionLevel": 1,
        "publishLevel": 0,
        "name": "open",
        "path": "MENU-SERVICO-UTILIDADEPUBLICA"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "MENU-SERVICO-UTILIDADEPUBLICA",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/menuServicoUtilidadePublica/response",
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