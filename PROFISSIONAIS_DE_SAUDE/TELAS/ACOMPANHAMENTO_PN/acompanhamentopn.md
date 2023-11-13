[Voltar](../../wikipedia.md)
# Acompanhamento pre-natal
### LINKS
- [Exames](./exames.md)
- [Vacinas](./vacinas.md)
- [Classificar Risco](./classificarrisco.md)
- [Finalizar pré-natal](./finalizarpn.md)

### Action
- Name: open
- Path: LISTAGESTANTES
- PermissionLevel: 1
- Parameters: Não
- Querystring: Não
  
### Manager
- Identifier: LISTAGESTANTES
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/listaGestantes/response
- Method: GET
- Header: Sim
- Querystring: Sim

### REQUISIÇÕES
~~~ python
# -------------------------- Url's Base --------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"


# --------------------- Requisições --------------------------

url = f"""{main_url_neo}/Profissionais%20de%20Saude/{email_do_profissional}?limit_page_length=1"""
res = requests.get(url, headers=headers)



url = f"{main_url_script}/childtableapi"
body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {
        "email": email, 
        "finished": 0
    },
    "fields": ["exams"]
}

res = requests.post(url,json=body,headers=headers).json()['msg']
~~~