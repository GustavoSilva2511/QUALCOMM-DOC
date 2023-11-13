[Voltar](./consultavacina.md)
# Excluir vacina
### Action
- Name: open
- Path: EXCLUIR-VACINA-CONNECT
- PermissionLevel: 2
- Parameters: Sim
- Querystring: Sim

### Manager
- Identifier: EXCLUIR-VACINA-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/excluirVacina/response
- Method: GET
- Header: Sim
- Querystring: Sim

### REQUISIÇÕES
~~~ python
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", token)# filters de email

delete("https://neo-qualcomm-homo.mobilex.tech/api/method/neo.core.doctype.childapi.api.handler", body, token)

put("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", body, token)
~~~