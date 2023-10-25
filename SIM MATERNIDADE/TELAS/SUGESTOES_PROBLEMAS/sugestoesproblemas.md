[Voltar](../../wikipedia.md)
# Envie sugestões e problemas
### LINKS
- [Enviar sugestão ou problema](./enviarsugestaoouproblema.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "name": "open",
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": "Sugestões e Problemas",
        "path": "FALE-CONOSCO"
    }
]
~~~

### Corpo do path no manager
``` json
{
    "identifier": "FALE-CONOSCO",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "http",
        "url": "adapter.mobilex.tech/v3.0.0/public/FALE-CONOSCO",
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