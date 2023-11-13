[Voltar](../../wikipedia.md)
# Convidar gestante
### Action
- Name: open-search
- Path: CONVIDARGESTANTE
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Não
 
### Manager
- Identifier: CONVIDARGESTANTE
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/convidarGestante/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
# ------------------------ urls base -----------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"
main_url_script = "https://neo-qualcomm-homo.mobilex.tech/api/method"

# ------------------------- requisições ---------------------------
url = f"{main_url_neo}/Email%20Template/Convite%20Gestante"
get_template = requests.get(url, headers=headers)



url = f"{main_url_script}/childtableapi"
body = {
    "command": "get_all",
    "doctype": "Gestante Equipe",
    "filters": {"name": email}
}

response = requests.post(url, json=body, headers=headers).json()['msg']



url = f"{main_url_script}/childtableapi"
body = {
    "command": "get_all",
    "doctype": "Gestante",
    "filters": {"email": email},
    "sub_command": "edit_fields",
    "sub_values": {"equipe": equipe}
}
response = requests.post(url, json=body, headers=headers).json()['msg']



url = f"{main_url_script}/childtableapi"
body = {
    "command": "get_all",
    "doctype": "Gestante",
    "filters": {"email": email}
}
response = requests.post(url, json=body, headers=headers).json()['msg']



url = f"{main_url_neo}/Gestante%20Equipe"
response = requests.post(url, json=infos, headers=headers)

# --------------------------- envio de email ------------------------
content = template_subject()
message = Mail(
                from_email='noreply@mobilex.tech',
                to_emails=email,
                subject=content[1],
                html_content=content[0].replace('$$name$$', name.replace(' ', '')))
sg = SendGridAPIClient('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')
response = sg.send(message)

~~~