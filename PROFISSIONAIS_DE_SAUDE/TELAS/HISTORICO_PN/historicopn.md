[Voltar](../../wikipedia.md)
# Histórico pré-natal
### LINKS
- [Histórico completo](./historicoexame.md)

### Action
- Name: open
- Path: HISTORICOPRENATAIS
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Não
 
### Manager
- Identifier: HISTORICOPRENATAIS
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/historicoPreNatais/response
- Method: GET
- Header: Sim
- Querystring: Sim

### REQUISIÇÕES
~~~ python
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"
url_child_table = f"{main_url_script}/childtableapi"



body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {"email": email},
    "fields": ["exams"]
}
res = requests.post(url_child_table,json=body,headers=headers).json()['msg']



body = {
    "command": "get_all",
    "doctype": "Equipes",
    "fields": ["nome_da_equipe", "unidade"]
}
response = requests.post(url_child_table, json=body, headers=headers).json()["msg"]


body = {
    "command": "get_all",
    "doctype": "Profissionais de Saude",
    "filters": {"email": "carlos.carneiro@mtmtecnologia.com.br"},
    "fields": ["equipes"]
}
response = requests.post(url_child_table, json=body, headers=headers).json()["msg"]


body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "fields": ["name", "email", "finished", "risk", "risk_cb", "exams"]
}
response = requests.post(url_child_table, json=body, headers=headers).json()["msg"]


body = {
    "command": "get_all",
    "doctype": "Gestante",
    "fields": ["full_name", "email", "equipe", "age", "gestational_weeks"]
}
gestantes = requests.post(url_child_table, json=body, headers=headers).json()["msg"]
~~~