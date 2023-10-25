[Voltar](./meuperfil.md)
# Como calcular idade gestacional
### Como chamar o path
~~~ python
"actions": [
    {
    "order": 0,
    "color": "#1AACB6",
    "publishLevel": 0,
    "permissionLevel": 1,
    "title": "Calcular",
    "name": "open",
    "path": "MENU-CALCULO-IDADE-GESTACIONAL-CONNECT"
    }
]

# EM SEGUIDA ABRIRÁ UMA TELA COM OUTRO PATH PRA CHAMAR O FORMS

"actions": [
    {
        "order": 0,
        "color": "#1AACB6",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "Calcular",
        "name": "open-search",
        "icon": "e9ac",
        "path": "CALCULO-IDADE-GESTACIONAL-V2-CONNECT",
            "parameters": [
            {
            "title": "initialSearchForm",
            "value": "Calcule-semana"
            }
        ]
    }
]

~~~

### Corpo do path no manager
~~~ json
{
    "identifier": "MENU-CALCULO-IDADE-GESTACIONAL-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/menuCalculoIdadeGestacional/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]"
    }
}

// SEGUNDO PATH

{
    "identifier": "CALCULO-IDADE-GESTACIONAL-V2-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/calculoIdadeGestacionalV2/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]"
    }
}
~~~

### REQUISIÇÕES
~~~ python
body = {
    "command": "get_all",
    "doctype": "Pre Natal",
    "filters": {
        "finished": 0,
        "email": "xxxx@email"
    }
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, TOKEN)

body = {
    "command": "create",
    "doctype": "Pre Natal",
    "charge": {
        "doctype": "Pre Natal",
        "email": request.args.get("email")
    }
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, TOKEN)

get("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi/ig?menstruation='date'?email=xxx#email")
~~~