[Voltar](./consultarexame.md)
# Excluir exame
### Action
- Name: open
- Path: EXCLUIR-EXAME-CONNECT
- PermissionLevel: 2
- Parameters: Sim
- Querystring: Sim

### Manager
- Identifier: EXCLUIR-EXAME-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/consultaExame/get_exam
- Method: GET
- Header: Sim
- Querystring: Sim

### REQUISIÇÕES
~~~ python
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)

requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal", json=body, headers=headers)

requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)

requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~