[Voltar](./exames.md)
# Cadastro exame
### Action
- Name: open-att-attendance-add
- Path: CRIAREXAME2
- PermissionLevel: 2
- Parameters: Sim
- Querystring: Sim
- Forms: cadastrarexamesandbox

### Manager
No manager, atendimento -> configurações -> categorias e serviços, existe um serviço chamado cadastro-de-exames
Mapeamento attendence

- Identifier: CRIAREXAME2
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/criarExame2/response
- Method: POST
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)

requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)

post("https://neo-qualcomm-homo.mobilex.tech/api/method/neo.core.doctype.childapi.api.handler", body, token)

requests.put("https://neo-qualcomm-homo.mobilex.tech/api/resource", json=body, headers=headers)

requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal", json=body, headers=headers)
~~~