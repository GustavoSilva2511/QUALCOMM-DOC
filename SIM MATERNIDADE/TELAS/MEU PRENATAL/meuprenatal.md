[Voltar](../../wikipedia.md)
# Meu Pré-Natal
## LINKS
- [Cartilha](../CADERNETA/cartilha.md)
- [Consultas](./CONSULTAS/consultas.md)
- [Exames](./EXAMES/exames.md)
- [Vacinas](./VACINAS/vacinas.md)
  
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "name": "open",
        "publishLevel": 1,
        "permissionLevel": 2,
        "path": "MENU-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "MENU-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/menu/menu",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]&nome=[[SURNAME]]&sobrenome=[[NAME]]"
    }
}
```

## REQUISIÇÕES
~~~ python
body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {
        "finished": 0,
        "email": "xxx@email"
    }
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)

requests.get("https://neo-qualcomm-homo.mobilex.tech/api/method/myprofile", headers=headers)
~~~


