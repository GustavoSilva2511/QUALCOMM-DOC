[Voltar](./vacinas.md)
# Consulta vacinas
### LINKS
- [Excluir vacina](./excluirvacina.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 2,
        "title": "Detalhes vacina",
        "name": "open",
        "color": "#7c9ffe",
        "path": "DETALHE-VACINA-CONNECT",
        "parameters": [
            {
                "title": "querystring",
                "value": f"?data={'/'.join(vacina['scheduled'].replace('-', '/')[:-9].split('/')[::-1])}&horario={':'.join(vacina['scheduled'].replace('-', '/')[-9:-3].split(':'))}&vacina={vacina['vaccine_name']}&name={vacina['name']}&local={vacina['location'] if ('location' in vacina) else ''}"
            }
        ]
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "DETALHE-VACINA-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes/detalheVacina/response",
        "method": "GET",
        "header": {
        "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]"
    }
}
```

### REQUISIÇÕES
Esta pagina não faz requisições