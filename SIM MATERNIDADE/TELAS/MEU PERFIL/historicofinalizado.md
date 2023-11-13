[Voltar](./historicoprenatais.md)
# Histórico finalizado
### Action
- Name: open
- Path: PRENATAL-FINALIZADO
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim
  
### Manager
- Identifier: PRENATAL-FINALIZADO
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/preNatalFinalizado/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {
        "finished": 1,
        "name": "xxx-xxx"
    }
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, TOKEN)
~~~