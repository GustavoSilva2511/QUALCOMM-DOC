[Voltar](./editaranexos.md)
# Adicionar imagem
### Action
- Name: open-att-attendance-add
- Path: SAVE_IMG
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim
- Forms: addimage

### Manager
- Identifier: SAVE_IMG
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/criarExame2/save_img
- Method: POST
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)

requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal", json=body, headers=headers)
~~~