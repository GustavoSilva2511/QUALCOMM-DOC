[Voltar](../../wikipedia.md)
# Meu Pré-Natal
## LINKS
- [Cartilha](../CADERNETA/cartilha.md)
- [Consultas](./CONSULTAS/consultas.md)
- [Exames](./EXAMES/exames.md)
- [Vacinas](./VACINAS/vacinas.md)
  
### Action
- Name: open
- Path: MENU-CONNECT
- PermissionLevel: 2
- Parameters: Não
- Querystring: Não
  
### Manager
- Identifier: MENU-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/menu/menu
- Method: GET
- Header: Sim
- Querystring: Sim

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


