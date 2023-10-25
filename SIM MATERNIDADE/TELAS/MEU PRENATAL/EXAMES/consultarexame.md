[Voltar](./exames.md)
# Consultar Exame
### LINKS
- [Editar dados](./editardados.md)
- [Editar anexos](./editaranexos.md)
- [Excluir exame](./excluirexame.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 2,
        "title": "Detalhes consulta",
        "name": "open",
        "color": "#7c9ffe",
        "path": "DETALHE-CONSULTA-EXAME-CONNECT",
        "parameters": [
            {
                "title": "querystring",
                "value": f"?data={'/'.join(i['scheduled'].replace('-', '/')[:-9].split('/')[::-1])}&horario={':'.join(i['scheduled'].replace('-', '/')[-9:-3].split(':'))}&name={i['name']}&exame={i['schedule']}&tipoExame={i['schedule_type']}&semanaGestacao={i['gestational_week']}&local={i.get('locale')}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "DETALHE-CONSULTA-EXAME-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/detalheExame/getDetalhe",
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
body = {
    "command": "get_all",
    "doctype": "Exame",
    "filters": {"name": "name_id"}
}
res = requests.post("https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi", json=body, headers=headers)
~~~