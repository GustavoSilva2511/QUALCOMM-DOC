[Voltar](./historicoexame.md)
# Anexos exame
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
body = {
    "command": "get_all",
    "doctype": "Exame",
    "sub_command": "edit_fields",
    "sub_values": {"vizualization": f"{lista} {request.args.get('profissional_email')}".strip()},
    "filters": {"name": request.args.get("name")}
}
res = requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers).json()



body = {
    "command": "get_all",
    "doctype": "Exame",
    "filters": {"name": request.args.get("name")}
}
res = requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers).json()['msg'][0]
~~~