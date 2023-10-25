[Voltar](./exames.md)
# Cadastro exame
### Como chamar o path
~~~ python
# Forms de atendimento
{
    "order": 0,
    "publishLevel": 1,
    "permissionLevel": 2,
    "title": "Criar exame",
    "name": "open-att-attendance-add",
    "icon": "E92B",
    "color": "#7c9ffe",
    "parameters": [
        {
            "title":"querystring", 
            "value":"?serviceId=cadastro-de-exames-sandbox&formId=cadastrarexamesandbox"
        }
    ]
}
~~~

### Corpo do path no manager
``` json
// No manager, atendimento -> configurações -> categorias e serviços, existe um serviço chamado cadastro-de-exames
// Mapeamento attendence
{
    "identifier": "CRIAREXAME2",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/criarExame2/response",
        "method": "POST",
        "header": {
            "Authorization": "TOKEN"
        },
        "body": {
            "Atendimento": "[[att]]"
        },
            "querystring": ""
    }
}

```

### REQUISIÇÕES
~~~ python
body = {
    "command": "get_all",
    "doctype": "Exame",
    "filters": {"name": "name_id"}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)




body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "sub_command": "edit_fields",
    "sub_values": {"hasnew": "1"},
    "filters": {"email": "xxx@email"}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)



body = {
    "scheduled": f"{'/'.join(campos['Data'][0].split('/')[::-1]) if bool(len(campos['Data'])) else ''}" + ' ' + campos['Hora'][0] if bool(len(campos['Hora'])) else "",
    "schedule_type": campos['Exame'][0].split(',')[1] if bool(len(campos['Exame'])) else "",
    "schedule": campos['Exame'][0].split(',')[0] if bool(len(campos['Exame'])) else "",
    "locale": campos['Local'][0] if bool(len(campos['Local'])) else "",
    "parent": parent,
    "parentfield": "exams",
    "parenttype": "Pre Natal",
    "doctype": "Exame"
}
for i, img in enumerate(exame_a):
    body.update({f'attach_{i+1}': '/files/' + img.lower()})
post("https://neo-qualcomm-homo.mobilex.tech/api/method/neo.core.doctype.childapi.api.handler", body, token)



body = {
    "imagesurls": json.dumps(request.get_json()['Atendimento']['imagesUrls'], ensure_ascii=False)
}
requests.put("https://neo-qualcomm-homo.mobilex.tech/api/resource", json=body, headers=headers)



body = {
    "command": "save_images",
    "name": parent
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal", json=body, headers=headers)

~~~