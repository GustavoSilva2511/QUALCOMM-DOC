[Voltar](./acompanhamentopn.md)
# Vacinas
### Action
- Name: open
- Path: VACINAS
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Sim
 
### Manager
- Identifier: VACINAS
- Url: https://api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/vacinas/response
- Method: GET
- Header: Sim
- Querystring: Não

### REQUISIÇÕES
~~~ python
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"

url = f'{main_url_neo}/Pre%20Natal?fields=["name"]&filters=[["email","=","{email}"],["finished","=","0"]]'
res = requests.get(url,headers=headers).json()["data"]

url= f'{main_url_neo}/Pre%20Natal/{res[0]["name"]}'
res = requests.get(url,headers=headers).json()["data"]["vaccines"]

res = requests.get(url + item['vaccine_type'] ,headers=headers).json()["data"]['full_name']

~~~