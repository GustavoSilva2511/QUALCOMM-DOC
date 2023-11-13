[Voltar](./exames.md)
# Consultar Exame
### LINKS
- [Editar dados](./editardados.md)
- [Editar anexos](./editaranexos.md)
- [Excluir exame](./excluirexame.md)

### Action
- Name: open
- Path: DETALHE-CONSULTA-EXAME-CONNECT
- PermissionLevel: 2
- Parameters: Sim
- Querystring: Sim

### Manager
- Identifier: CRIAREXAME2
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/detalheExame/getDetalhe
- Method: GET
- Header: Sim
- Querystring: Sim

### REQUISIÇÕES
~~~ python
body = {
    "command": "get_all",
    "doctype": "Exame",
    "filters": {"name": "name_id"}
}
res = requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~