[Voltar](../meuprenatal.md)
# Vacinas
### LINKS
- [Consultar vacina](./consultavacina.md)
- [Cadastrar vacina](./cadastrarvacina.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "permissionLevel": 1,
        "publishLevel": 1,
        "name": "open",
        "path":"CONSULTA-VACINA-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "CONSULTA-VACINA-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/consultaVacina/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]"
    }
}
```

### REQUISIÇÕES
~~~ python
body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {
        "email": request.args.get("email"),
        "finished": 0
    }
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)



body = {
    "command": "get_all",
    "doctype": "Vacina",
    "filters": {"parent": id_gestante}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~