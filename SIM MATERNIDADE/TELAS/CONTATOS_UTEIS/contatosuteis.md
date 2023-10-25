[Voltar](../../wikipedia.md)
# Contatos uteis
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "name": "open",
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Contatos Úteis",
        "path": "TELEFONES-UTEIS"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "TELEFONES-UTEIS",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "http",
        "url": "adapter.mobilex.tech/v3.0.0/public/TELEFONES-UTEIS",
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
Esta tela não possui requisições