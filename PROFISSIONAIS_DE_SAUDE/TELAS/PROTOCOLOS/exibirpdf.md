[Voltar](./protocolos.md)
# Exibir pdf
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "name": "open-pdf",
        "title": "Fluxo Entrega Voluntária",
        "path": "EXIBE_PDF",
        "parameters": [
            {
                "title":"querystring",
                "value":"?name=568e9f2a57"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "EXIBE_PDF",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/protocolos/exibe_pdf",
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
# -------------------- url base --------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"

# ------------------- requisições --------------------
url = f"{main_url_neo}/Protocolos%20PDF/{name}"
res = requests.get(url, headers=headers)

~~~