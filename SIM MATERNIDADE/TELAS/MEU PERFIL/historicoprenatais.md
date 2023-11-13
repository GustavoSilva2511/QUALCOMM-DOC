[Voltar](./meuperfil.md)
# Histórico Pre Natais
### LINKS
- [Histórico finalizado](./historicofinalizado.md)
- [Histórico atual](../MEU%20PRENATAL/meuprenatal.md)

### Action
- Name: open
- Path: HISTORICO-PRENATAL
- PermissionLevel: 1
- Parameters: Não
- Querystring: Não
  
### Manager
- Identifier: HISTORICO-PRENATAL
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/historicoPreNatal/response
- Method: GET
- Header: Sim
- Querystring: Sim

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