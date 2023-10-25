[Voltar](./anexosexame.md)
# Vizualizar imagem
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "publishLevel": 1,
        "permissionLevel": 1,
        "title": url.split("/")[-1],
        "name": "open-view",
        "parameters": [
            {
                "title": "url",
                "value": "imagem_link"
            }
        ]
    }
]
~~~

### Corpo do path no manager
Esta é apenas uma função nativa do connect

### REQUISIÇÕES
Esta aba não possui requisições