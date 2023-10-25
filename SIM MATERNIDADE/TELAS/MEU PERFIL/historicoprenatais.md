[Voltar](./meuperfil.md)
# Histórico Pre Natais
### LINKS
- [Histórico finalizado](./historicofinalizado.md)
- [Histórico atual](../MEU%20PRENATAL/meuprenatal.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "color": "#1AACB6",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "Calcular",
        "name": "open",
        "path": "HISTORICO-PRENATAL"
    }
]
~~~


### Corpo do path no manager
``` json
{
    "identifier": "HISTORICO-PRENATAL",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/historicoPreNatal/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]&nome=[[NAME]]&sobrenome=[[SURNAME]]"
    }
}
```

### REQUISIÇÕES
~~~ python
body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {
        "email": "xxx@email"
    }
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~