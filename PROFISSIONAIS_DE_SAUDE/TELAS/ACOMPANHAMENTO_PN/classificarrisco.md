[Voltar](./acompanhamentopn.md)
# Classificar risco
### LINKS


### Como chamar o path
~~~ python
"actions": [
    {
        "order": 1,
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Classificar Risco",
        "icon":"e969",
        "name": "open-search",
        "path": "CLASSIFICARISCO",
        "parameters": [
            {"title":"initialSearchForm", "value":"a7e4a25a-4caf-4080-8ade-3eb153bcf3be"},
            {"title":"formParameters","value":f"?email={gestante['email']}"}
        ]
    }
]
~~~

### Corpo do path no manager
``` json
// MAPEAMENTO ATT
{
    "identifier": "CLASSIFICARISCO",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/classificaRisco/response",
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
# ----------------------- url base ----------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"

# ------------------------ requisição -------------------------
url = f"""{main_url_neo}/Pre%20Natal"""
email_id = requests.get(url + f"""?filters=[["name","like","%{infos['email']}%"], ["finished","=","0"]]""", headers=headers).json()['data'][0]['name']
~~~