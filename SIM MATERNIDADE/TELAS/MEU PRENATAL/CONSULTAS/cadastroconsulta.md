[Voltar](./consultas.md)
# Cadastro de consultas

### Como chamar o path
~~~ python
{
    "order": 0,
    "publishLevel": 1,
    "permissionLevel": 2,
    "title": "Criarconsulta",
    "name": "open-search",
    "icon": "E92B",
    "color": "#7c9ffe",
    "path": "CRIAR-CONSULTA-CONNECT",
    "parameters": [
        {
            "title": "initialSearchForm",
            "value": "criar-consulta"
        }
    ]
}
~~~


### Corpo do path no manager
``` json
{
    "identifier": "CRIAR-CONSULTA-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/criarConsulta/get_form",
        "method": "POST",
        "header": {
            "Authorization": "TOKEN"
        },
        "body": {
            "email": "[[EMAIL]]"
        }
    }
}
```
<p>A action chama um forms e em seguida chama a pagina no connect com todos os valores fornecidos no """request.args"""</p>

### REQUISIÇÕES
~~~ python
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", token) # filters com email e finished = 0

#Salvando aquivos caso tenha
payload = {
    "cmd": "uploadfile",
    "filename": f'{file_name}',
    "filedata": f"{encoded_string}",
    "from_form": "0"
}
post("https://neo-qualcomm-homo.mobilex.tech/api/method/uploadfile?method=application/json", payload, token)

#Salvando os dados da consulta
body = {
    "scheduled": f"{'/'.join(date.split('/')[::-1])}" + ' ' + hour,
    "consult_type": "ad3100814c",
    "consult_name": "worked",
    "gestational_week": semanaGestacao,
    "location": local,
    "doctor": medico,
    "doubts": duvidas,
    "notes": anotacoes,
    "origin": 1,
    "parent": prename(),
    "attach_1": f"files/{file_name}",
    "parentfield": "appointments2",
    "parenttype": "Pre Natal",
    "doctype": "Consultas2"
}
post("https://neo-qualcomm-homo.mobilex.tech/api/method/neo.core.doctype.childapi.api.handler")
~~~