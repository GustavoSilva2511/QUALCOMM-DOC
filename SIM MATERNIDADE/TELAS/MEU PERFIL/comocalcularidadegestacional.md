[Voltar](./meuperfil.md)
# Como calcular idade gestacional
### Action1
- Name: open
- Path: MENU-CALCULO-IDADE-GESTACIONAL-CONNECT
- PermissionLevel: 1

EM SEGUIDA ABRIRÁ UMA TELA COM OUTRO PATH PRA CHAMAR O FORMS

### Action2
- Name: open
- Path: CALCULO-IDADE-GESTACIONAL-V2-CONNECT
- PermissionLevel: 1
- parameters: Sim
- Querystring: Não

### Manager1
- Identifier: MENU-CALCULO-IDADE-GESTACIONAL-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/menuCalculoIdadeGestacional/response
- Method: GET
- Header: Sim
- Querystring: Sim

### Manager2
- Identifier: CALCULO-IDADE-GESTACIONAL-V2-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/calculoIdadeGestacionalV2/responsee
- Method: GET
- Header: Sim
- Querystring: Sim

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