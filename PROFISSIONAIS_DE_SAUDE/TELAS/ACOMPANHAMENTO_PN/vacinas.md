[Voltar](./acompanhamentopn.md)
# Vacinas
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Vacinas",
        "icon":"e93c",
        "name": "open",
        "path": "VACINAS",
        "parameters": [
            {
                "title": "querystring",
                "value": f"?email={gestante['email']}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "VACINAS",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/vacinas/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": ""
    }
}
```

### REQUISIÇÕES
~~~ python
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"

url = f'{main_url_neo}/Pre%20Natal?fields=["name"]&filters=[["email","=","{email}"],["finished","=","0"]]'
res = requests.get(url,headers=headers).json()["data"]

url= f'{main_url_neo}/Pre%20Natal/{res[0]["name"]}'
res = requests.get(url,headers=headers).json()["data"]["vaccines"]

res = requests.get(url + item['vaccine_type'] ,headers=headers).json()["data"]['full_name']

~~~