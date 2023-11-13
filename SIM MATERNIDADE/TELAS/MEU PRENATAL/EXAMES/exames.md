[Voltar](../meuprenatal.md)
# Exames
### LINKS
- [Consultar exame](./consultarexame.md)
- [Cadastrar exames](./cadastroexame.md)

### Action
- Name: open
- Path: CONSULTA-EXAME-CONNECT
- PermissionLevel: 1
- Parameters: Não
- Querystring: Não

### Manager
- Identifier: CONSULTA-EXAME-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/consultaExame/get_exam
- Method: POST
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal") # filters email e finished = 0
~~~