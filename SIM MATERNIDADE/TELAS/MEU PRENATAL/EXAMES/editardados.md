[Voltar](./consultarexame.md)
# Editar dados
### Action
- Name: open-att-attendance-add
- Path: EDIT_EXAM
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim

### Manager
- Identifier: EDIT_EXAM
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/editarExame/edit_exam
- Method: POST
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~