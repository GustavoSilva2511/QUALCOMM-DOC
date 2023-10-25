[Voltar](./editaranexos.md)
# Adicionar imagem
### Como chamar o path
~~~ python
"action": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Adicionar",
        "name": "open-att-attendance-add",
        "parameters": [
            {
                "title":"querystring", 
                "value":"?serviceId=save-img&formId=addimage"
            },
            {
                "title": "formParameters",
                "value": f"?attach={attach['name']}&idexam={request.args.get('name')}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
  {
    "identifier": "SAVE_IMG",
    "serviceConfiguration": {
      "permissionLevel": 1,
      "publishLevel": 1,
      "protocol": "https",
      "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/criarExame2/save_img",
      "method": "POST",
      "header": {
        "Authorization": "TOKEN"
      },
      "body": {
        "Atendimento": "[[att]]"
      },
      "querystring": ""
    }
  },

```

### REQUISIÇÕES
~~~ python
payload = {
    "command": "add_attach",
    "name_img": image[0]["name"].split("/")[-1],
    "link_img": image[0]["link"],
    "attach_index": attach_index
}
body = {
    "command": "get_all",
    "doctype": "Exame",
    "sub_command": "edit_fields",
    "sub_values": {
        "attach_edited": str(payload),
        "vizualization": None    
    },
    "filters": {"name": exam_id}
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)


body = {
    "name": "name_id"
}
requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal", json=body, headers=headers)
~~~