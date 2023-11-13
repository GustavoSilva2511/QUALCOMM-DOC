[Voltar](./consultarexame.md)
# Consulta exame
### LINKS
- [Visualizar imagem](./visualizarimagem.md)
- [Adicionar imagem](./adicionarimagem.md)
- [Deletar imagem](./deletarimagem.md)

### Action
- Name: open
- Path: EDITAREXAME
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim

### Manager
- Identifier: EDITAREXAME
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/editarExame/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)


get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal") # filters de email

post("https://neo-qualcomm-homo.mobilex.tech/api/method/uploadfile?method=application/json", payload, token)
~~~