[Voltar](./meuperfil.md)
# Atualize seu cadastro (FORMS)
### Action
- Name: open-search
- Path: ATUALIZAR-CADASTRO-CONNECT
- PermissionLevel: 1
- Parameters: Sim
- Querystring: Não
- Forms: atualizar-cadastro

<p style="color: rgb(255, 50, 50)">!! Lembrando que todos os valores devem ser passados no forms parameter pra evitar perda de dados!! </p>

### Manager
- Identifier: ATUALIZAR-CADASTRO-CONNECT
- Url: https://api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/atualizarCadastro/response
- Method: GET
- Header: Sim
- Querystring: Sim
  
<p>A action chama um forms e em seguida chama a pagina no connect com todos os valores fornecidos no """request.args"""</p>

### REQUISIÇÕES
~~~ python
# dados da gestante
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Gestantes?email=xxx@email", TOKEN)

# post de dados pre natal
put("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", TOKEN)
~~~