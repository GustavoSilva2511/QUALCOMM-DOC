[Voltar](../meuprenatal.md)
# Exames
### LINKS
- [Consultar exame](./consultarexame.md)
- [Cadastrar exames](./cadastroexame.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "permissionLevel": 1,
        "publishLevel": 1,
        "name": "open",
        "path":"CONSULTA-EXAME-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "CONSULTA-EXAME-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/consultaExame/get_exam",
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
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal") # filters email e finished = 0
~~~