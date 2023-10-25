[Voltar](../gestantescg.md)
# Unidades de atendimento
### LINKS
- [Unidades de saúde](./unidadesdesaude.md)
- [Maternidades](./maternidades.md)
- [Academias de saúde](./academiasdesaude.md)
- [Serviços de saúde mental](./servicossausemental.md)
  
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "permissionLevel": 1,
        "publishLevel": 0,
        "name": "open",
        "path": "GESTANTES-UNIDADES-ATENDIMENTO-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "GESTANTES-UNIDADES-ATENDIMENTO-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/unidadesDeAtendimento/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": ""
    }
}
```

### REQUISIÇÕES
Esta tela não possui requisições