[Voltar](./protocolos.md)
# Exibir pdf
### Action
- Name: open-pdf
- Path: EXIBE_PDF
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim
 
### Manager
- Identifier: EXIBE_PDF
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/protocolos/exibe_pdf
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
# -------------------- url base --------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"

# ------------------- requisições --------------------
url = f"{main_url_neo}/Protocolos%20PDF/{name}"
res = requests.get(url, headers=headers)

~~~