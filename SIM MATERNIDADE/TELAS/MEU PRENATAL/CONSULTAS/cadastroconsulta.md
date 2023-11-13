[Voltar](./consultas.md)
# Cadastro de consultas
### Action
- Name: open-searsh
- Path: CRIAR-CONSULTA-CONNECT
- PermissionLevel: 2
- Parameters: Sim
- Querystring: Não
- forms: criar-consulta
  
### Manager
- Identifier: CRIAR-CONSULTA-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/criarConsulta/get_form
- Method: POST
- Header: Sim
- Querystring: Sim

<p>A action chama um forms e em seguida chama a pagina no connect com todos os valores fornecidos no """request.args"""</p>

### REQUISIÇÕES
~~~ python
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", token) # filters com email e finished = 0

#Salvando aquivos caso tenha
post("https://neo-qualcomm-homo.mobilex.tech/api/method/uploadfile?method=application/json", payload, token)

#Salvando os dados da consulta
post("https://neo-qualcomm-homo.mobilex.tech/api/method/neo.core.doctype.childapi.api.handler", body, token)
~~~