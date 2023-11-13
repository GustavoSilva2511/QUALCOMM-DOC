[Voltar](./editaranexos.md)
# Deletar imagem
### Action
- Name: open
- Path: DELETEIMAGE
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim

### Manager
- Identifier: DELETEIMAGE
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/deleteImage/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)

res = requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal",, json=body, headers=headers)
~~~