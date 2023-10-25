[Voltar](./consultarexame.md)
# Consulta exame
### LINKS
- [Visualizar imagem](./visualizarimagem.md)
- [Adicionar imagem](./adicionarimagem.md)
- [Deletar imagem](./deletarimagem.md)


### Como chamar o path
~~~ python
{
    "order": 1,
    "publishLevel": 1,
    "permissionLevel": 1,
    "title": "Editar anexos",
    "name": "open",
    "icon": "e935",
    "path": "EDITAREXAME",
    "parameters": [
        {
            "title": "Querystring",
            "value": f"?name={request.args.get('name')}"
        }
    ]
}
~~~

### Corpo do path no manager
``` json
{
    "identifier": "EDITAREXAME",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/editarExame/response",
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
body = {
    "command": "get_all",
    "doctype": "Exame",
    "filters": {"name": "name_id"}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)


get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal") # filters de email


payload = {
    "cmd": "uploadfile",
    "filename": f'{file_name}',
    "filedata": f"{encoded_string}",
    "from_form": "0"
}
post("https://neo-qualcomm-homo.mobilex.tech/api/method/uploadfile?method=application/json", payload, token)
~~~