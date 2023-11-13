[Voltar](./historicopn.md)
# Histórico exame
### LINKS
- [Anexos exame](./anexosexame.md)
  
### Action
- Name: open
- Path: HISTORICOEXAMES
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim
 
### Manager
- Identifier: HISTORICOEXAMES
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/historicoExames/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
# ------------------------ url base ---------------------------------
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"
url_child_table = f"{main_url_script}/childtableapi"


# -------------------------- requisições ----------------------------
body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {"email": request.args.get("email")}
}
response = requests.post(url_child_table, json=body, headers=headers).json()["msg"]
~~~