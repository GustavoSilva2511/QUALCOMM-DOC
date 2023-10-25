[Voltar](../meuprenatal.md)
# Consulta
### LINKS
- [Detalhe da consulta](./detalheconsulta.md)
- [Cadastro de consulta](./cadastroconsulta.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "permissionLevel": 1,
        "publishLevel": 1,
        "name": "open",
        "path":"CONSULTA-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "CONSULTA-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/consulta2/response",
        "method": "POST",
        "header": {
            "Authorization": "TOKEN"
        },
        "body": {
            "email": "[[EMAIL]]"
        }
    }
}

```

### REQUISIÇÕES
~~~ python
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", token)
~~~