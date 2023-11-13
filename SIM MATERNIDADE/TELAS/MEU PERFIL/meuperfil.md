[Voltar](../../wikipedia.md)
 
# Meu perfil

## LINKS
- [Atualize seu cadastro](./atualizeseucadastro.md)
- [Como calcular idade gestacional](./comocalcularidadegestacional.md)
- [Historico de Pré Natais](./historicoprenatais.md)

### Action
- Name: open
- Path: MENU-MEU-PERFIL-CONNECT
- PermissionLevel: 2
- Parameters: Não
- Querystring: Não
  
### Manager
- Identifier: MENU-MEU-PERFIL-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/menuMeuPerfil/response
- Method: GET
- Header: Sim
- Querystring: Sim

## REQUISIÇÕES
~~~ python
# Dados do perfil
get("https://neo-qualcomm-homo.mobilex.tech/api/method/myprofile?email=xxx@email", TOKEN)

# dados da gestante
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Gestantes?NAME_ID", TOKEN)
~~~
