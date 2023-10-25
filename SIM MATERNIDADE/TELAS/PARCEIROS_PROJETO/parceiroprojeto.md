[Voltar](../../wikipedia.md)
# Parceiros do projeto
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "name": "open",
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Parceiros do projeto",
        "path": "PARCEIROS-PROJETO-CONNECT"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "PARCEIROS-PROJETO",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "http",
        "url": "adapter.mobilex.tech/v3.0.0/public/PARCEIROS-PROJETO",
        "method": "GET",
        "header": {
            "logInfo": "[[LOGINFO]]",
            "client_secret": "client_secret",
            "client_id": "client_id"
        }
    }
}
```

### REQUISIÇÕES
Esta pagina não possui requisições