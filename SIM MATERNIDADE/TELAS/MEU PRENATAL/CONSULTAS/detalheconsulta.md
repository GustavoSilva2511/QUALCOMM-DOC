[Voltar](./consultas.md)
# Detalhe consulta
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 2,
        "title": "Detalhesconsulta",
        "name": "open",
        "color": "#7c9ffe",
        "path": "DETALHE-CONSULTA-CONNECT",
        "parameters": [
            {
            "title": "querystring",
            "value": f"?data={'/'.join(i['scheduled'].replace('-', '/')[:-9].split('/')[::-1])}&horario={':'.join(i['scheduled'].replace('-', '/')[-9:-3].split(':'))}&semanaGestacao={i['gestational_week']}&local={i['location']}&medico={i['doctor']}&duvidas={i['doubts']}&anotacoes={i['notes']}&name={i['name']}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "DETALHE-CONSULTA-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/detalheConsulta/getDetalhe",
        "method": "GET",
        "header": {
           "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]"
    }
}
```

### REQUISIÇÕES
Esta tela não possui requisições