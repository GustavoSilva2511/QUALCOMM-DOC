[Voltar](../../wikipedia.md)
# Gestantes Campina Grande
### LINKS
- [Unidades de atendimento](./UNIDADES_ATT/unidadesdeatendimento.md)
- [Serviços de utilidade pública](./SERVICO_UTI_PUB/servico_uti_pub.md)
  
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "name": "open",
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Gestantes de Campina Grande",
        "path": "MENU-PRINCIPAL-GESTANTES"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "MENU-PRINCIPAL-GESTANTES",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/gestantes_cg/menuPrincipal/response",
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