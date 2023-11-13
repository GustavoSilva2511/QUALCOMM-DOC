[Voltar](./vacinas.md)
# Cadastrar vacina
### Action
- Name: open-search
- Path: CRIAR-VACINA-CONNECT
- PermissionLevel: 2
- Parameters: Sim
- Querystring: Não
- Forms: cadastro-vacina

### Manager
- Identifier: CRIAR-VACINA-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/criarVacina/response
- Method: GET
- Header: Sim
- Querystring: Sim

### REQUISIÇÕES
~~~ python
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", token)# filters de email

post("https://neo-qualcomm-homo.mobilex.tech/api/method/neo.core.doctype.childapi.api.handler", body, token)

put(f"https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal/{prename()}", body, token)
~~~