[Voltar](./acompanhamentopn.md)
# Exames
### LINKS
- [Anexos exames](./anexosexame.md)

### Action
- Name: open
- Path: EXAMES
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim
  
### Manager
- Identifier: EXAMES
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/exames/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
# --------------------------- Urls base --------------------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"
url_child_table = f"{main_url_script}/childtableapi"

# --------------------------- Requisições --------------------------------
url = main_url_neo + f'''/Pre Natal?fields=["name"]&filters=[["email","=","{email}"],["finished","=","0"]]''';
res = requests.get(url,headers=headers).json()['data']

res = requests.post(url_child_table, json=body, headers=headers).json()['msg'][0]['exams']

res = requests.post(url_child_table, json=body, headers=headers)
~~~