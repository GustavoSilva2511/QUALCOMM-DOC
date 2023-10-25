[Voltar](./consultarexame.md)
# Editar dados
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 2,
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Editar dados",
        "name": "open-att-attendance-add",
        "icon": "e935",
        "parameters": [
            {
                "title":"querystring", 
                "value":"?serviceId=edit-exam&formId=editexam"
            },
            {
                "title": "formParameters",
                "value": f"?name={name}&data={data}&hora={hora}&local={local}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
// Mapeamento serviço de atendimento atendimento
{
    "identifier": "EDIT_EXAM",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/editarExame/edit_exam",
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
    "sub_command": "edit_fields",
    "sub_values": {
        "locale": locale,
        "scheduled": f"{date} {hour}"
    },
    "filters": {"name": exam_id}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~