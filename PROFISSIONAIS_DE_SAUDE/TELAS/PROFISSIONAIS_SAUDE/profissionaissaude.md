[Voltar](../../wikipedia.md)
# Profissionais de saúde
### Action
- Name: open
- Path: LISTAPROFISSIONAIS
- PermissionLevel: 1
- Parameters: Não
- Querystring: Não
 
### Manager
- Identifier: LISTAPROFISSIONAIS
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/listaProfissionais/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
# ------------------------- url base ----------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"


# ------------------------- requisições -------------------------
url = f"{main_url_neo}/Profissionais%20de%20Saude"
query_string = """?fields=["*"]&limit_page_length=999999"""
res = requests.get(url+query_string, headers=headers)

~~~