[Voltar](./acompanhamentopn.md)
# Finalizar pré-natal
### Como chamar o path
~~~ python
{
    "order": 1,
    "publishLevel": 1,
    "permissionLevel": 1,
    "title": "Finalizar Pré-natal",
    "icon":"ea28",
    "name": "open-search",
    "path": "FIMPRENATAL",
    "parameters": [
        {"title":"initialSearchForm", "value":"e53a0c0b-6b9c-4696-a985-5e9fe41cdb5d"},
        {"title":"formParameters","value":f"?email={gestante['email']}"}
    ]
}
~~~

### Corpo do path no manager
``` json
{
    "identifier": "FIMPRENATAL",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/app_profissionais_saude_SANDBOX/CMS/fimPrenatal/response",
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
# ---------------------------- urls base ---------------------------
main_url_neo = "https://neo-qualcomm-homo.mobilex.tech/api/resource"


# --------------------------- pre natal ----------------------------
url = f"""{main_url_neo}/Pre%20Natal"""
email_id = requests.get(url + f"""?filters=[["name","like","%{infos['email']}%"], ["finished","=","0"]]""", headers=headers).json()['data'][0]['name']
response1 = requests.put(url + "/" + email_id, headers=headers, json={"finished": 1, "reason4_submission": reason[int(infos['submission'])]})
response2 = requests.delete(f"{main_url_neo}/Gestante Equipe/{infos['email']}", headers=headers)
~~~