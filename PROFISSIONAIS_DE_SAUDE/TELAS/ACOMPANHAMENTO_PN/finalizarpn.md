[Voltar](./acompanhamentopn.md)
# Finalizar pré-natal
### Action
- Name: open-search
- Path: FIMPRENATAL
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim
- Forms: e53a0c0b-6b9c-4696-a985-5e9fe41cdb5d
- 
### Manager
- Identifier: FIMPRENATAL
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/fimPrenatal/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
# ---------------------------- urls base ---------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"

# --------------------------- pre natal ----------------------------
url = f"""{main_url_neo}/Pre%20Natal"""
email_id = requests.get(url + f"""?filters=[["name","like","%{infos['email']}%"], ["finished","=","0"]]""", headers=headers).json()['data'][0]['name']
response1 = requests.put(url + "/" + email_id, headers=headers, json={"finished": 1, "reason4_submission": reason[int(infos['submission'])]})
response2 = requests.delete(f"{main_url_neo}/Gestante Equipe/{infos['email']}", headers=headers)
~~~