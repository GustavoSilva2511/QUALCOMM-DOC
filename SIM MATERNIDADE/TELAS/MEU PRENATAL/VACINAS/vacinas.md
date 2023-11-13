[Voltar](../meuprenatal.md)
# Vacinas
### LINKS
- [Consultar vacina](./consultavacina.md)
- [Cadastrar vacina](./cadastrarvacina.md)

### Action
- Name: open
- Path: CONSULTA-VACINA-CONNECT
- PermissionLevel: 1
- Parameters: Não
- Querystring: Não

### Manager
- Identifier: CONSULTA-VACINA-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/consultaVacina/response
- Method: GET
- Header: Sim
- Querystring: Sim

### REQUISIÇÕES
~~~ python
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)

requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~