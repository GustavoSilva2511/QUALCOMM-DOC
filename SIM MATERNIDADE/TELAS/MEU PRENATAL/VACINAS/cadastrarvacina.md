[Voltar](./vacinas.md)
# Cadastrar vacina
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 2,
        "title": "Criar consulta",
        "name": "open-search",
        "icon": "E92B",
        "color": "#7c9ffe",
        "path": "CRIAR-VACINA-CONNECT",
        "parameters": [
            {
                "title": "initialSearchForm",
                "value": "cadastro-vacina"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "CRIAR-VACINA-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/criarVacina/response",
        "method": "GET",
        "header": {
        "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]"
    }
}
```

### REQUISIÇÕES
~~~ python
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", token)# filters de email



body = {
    "scheduled": f"{'/'.join(date.split('/')[::-1])}" ' ' + hour,
    "vaccine_type": vacina.split(',')[1],
    "vaccine_name": vacina.split(',')[0],
    "location": local,
    "parent": prename(),
    "parentfield": "vaccines",
    "parenttype": "Pre Natal",
    "doctype": "Vacina"
}
post("https://neo-qualcomm-homo.mobilex.tech/api/method/neo.core.doctype.childapi.api.handler", body, token)



body = {
    "ocult": f"{string}"
}
put(f"https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal/{prename()}", body, token)
~~~