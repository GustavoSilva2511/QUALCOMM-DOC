[Voltar](../../wikipedia.md)
# Unidades de saúde
### Action
- Name: open
- Path: DISTRITOS
- PermissionLevel: 1
- Parameters: Não
- Querystring: Não
 
### Manager
- Identifier: DISTRITOS
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/distritos/response
- Method: GET
- Header: Sim
- Querystring: Não

### Funções
- Name: share
- PermissionLevel: 1
- Parameters: sim
--------------------------
- Name: maps
- PermissionLevel: 1
- Parameters: sim
--------------------------
- Name: call
- PermissionLevel: 1
- Parameters: sim
--------------------------

### REQUISIÇÕES
~~~ python
# -------------------- url base ----------------------
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"

# -------------------- requisição ---------------------
url = f"{main_url_script}/childtableapi"
body = {
    "command": "get_all",
    "order_by": "district",
    "doctype": "Unidades de Atendimento Completo",
    "fields": ["district"],
    "sub_command": "no_repeat"
}
res = requests.post(url, json=body, headers=headers).json()['msg']



url = f"{main_url_script}/childtableapi"
body = {
    "command": "get_all",
    "order_by": "full_name",
    "doctype": "Unidades de Atendimento Completo",
    "filters": {"district": district}    
}
res = requests.post(url, json=body, headers=headers).json()['msg']
~~~