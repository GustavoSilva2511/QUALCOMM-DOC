[Voltar](../../wikipedia.md)
# Cartilha
### LINKS
Diversos links semelhantes

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "permissionLevel": 1,
        "publishLevel": 1,
        "name": "open",
        "path":"MENU-PRINCIPAL-CARTILHA"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "MENU-PRINCIPAL-CARTILHA",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/cartilhaGestate/menuPrincipal/response",
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