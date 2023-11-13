[Voltar](./exames.md)
# Anexos exame
### LINKS
- [Vizualizar imagem](./visualizarimagem.md)

### Action
- Name: open
- Path: ANEXOSEXAMES
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim
  
### Manager
- Identifier: ANEXOSEXAMES
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/anexosExames/anexos
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
res = requests.post(url, json=body, headers=headers).json()

res = requests.post(url, json=body, headers=headers).json()['msg'][0]
~~~