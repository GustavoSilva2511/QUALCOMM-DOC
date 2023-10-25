[Voltar](../../wikipedia.md)
 
# Meu perfil

## LINKS
- [Atualize seu cadastro](./atualizeseucadastro.md)
- [Como calcular idade gestacional](./comocalcularidadegestacional.md)
- [Historico de Pré Natais](./historicoprenatais.md)

### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "name": "open",
        "publishLevel": 1,
        "permissionLevel": 2,
        "path": "MENU-MEU-PERFIL-CONNECT"
    }
]
~~~


### Corpo do path no manager
``` json
{
    "identifier": "MENU-MEU-PERFIL-CONNECT",
    "serviceConfiguration": {
      "permissionLevel": 1,
      "publishLevel": 1,
      "protocol": "https",
      "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/menuMeuPerfil/response",
      "method": "GET",
      "header": {
        "Authorization": "TOKEN connect"
      },
      "querystring": "?email=[[EMAIL]]&nome=[[SURNAME]]&sobrenome=[[NAME]]"
    }
}
```
## REQUISIÇÕES

~~~ python
# Dados do perfil
get("https://neo-qualcomm-homo.mobilex.tech/api/method/myprofile?email=xxx@email", TOKEN)

# dados da gestante
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Gestantes?NAME_ID", TOKEN)
~~~
