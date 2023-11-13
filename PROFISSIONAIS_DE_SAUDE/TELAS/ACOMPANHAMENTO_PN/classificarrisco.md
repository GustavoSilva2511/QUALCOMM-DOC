[Voltar](./acompanhamentopn.md)
# Classificar risco
### Action
- Name: open-search
- Path: CLASSIFICARISCO
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Não
- Forms: a7e4a25a-4caf-4080-8ade-3eb153bcf3be
  
### Manager
- Identifier: CLASSIFICARISCO
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/classificaRisco/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
# ----------------------- url base ----------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"

# ------------------------ requisição -------------------------
url = f"""{main_url_neo}/Pre%20Natal"""
email_id = requests.get(url + f"""?filters=[["name","like","%{infos['email']}%"], ["finished","=","0"]]""", headers=headers).json()['data'][0]['name']
~~~