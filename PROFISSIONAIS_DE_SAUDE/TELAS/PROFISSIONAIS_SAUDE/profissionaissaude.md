[Voltar](../../wikipedia.md)
# Profissionais de saúde
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "name": "open",
        "path": "LISTAPROFISSIONAIS"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "LISTAPROFISSIONAIS",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/listaProfissionais/response",
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
# ------------------------- url base ----------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"


# ------------------------- requisições -------------------------
url = f"{main_url_neo}/Profissionais%20de%20Saude"
query_string = """?fields=["*"]&limit_page_length=999999"""
res = requests.get(url+query_string, headers=headers)

~~~