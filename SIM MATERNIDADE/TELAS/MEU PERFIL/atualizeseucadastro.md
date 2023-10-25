[Voltar](./meuperfil.md)
# Atualize seu cadastro (FORMS)
### Como chamar o path
~~~ python
"actions": [
    {
        "order": 0,
        "color": "#1AACB6",
        "publishLevel": 0,
        "permissionLevel": 1,
        "title": "Atualizar Cadastro",
        "name": "open-search",
        "icon": "e9ac",
        "path": "ATUALIZAR-CADASTRO-CONNECT",
        "parameters": [
            {
                "title": "formParameters",
                "value": f"""
                    ?emailA={gestante.get('email')}
                    &nomeA={gestante.get('first_name')}
                    &sobrenomeA={gestante.get('last_name')}
                    &numCartaoSUS={gestante.get('card_sus') if 'card_sus' in gestante else ''}
                    &numNIS={gestante.get('n_nis')}
                    &unidadeSaude={gestante.get('health_unit')}
                    &residenteCG={gestante.get('campina_resident')}
                    &atendidaSUS={gestante.get('attended_by_sus')}
                    &idadeGestacional={gestante.get('gestational_weeks')}
                    &nomeSocial={gestante.get('social_name')}
                    &idade={gestante.get('age')}
                    &racaCor={gestante.get('race_color')}
                    &etnia={gestante.get('etnia') if 'etnia' in gestante else ''}
                    &trabalhaFora={ gestante.get('work_out')}
                    &ocupacao={gestante.get('occupation')}
                    &endereco={gestante.get('address')}
                    &referencia={gestante.get('address_reference')}
                    &bairro={gestante.get('district')}
                    &cidade={gestante.get('city')}
                    &CEP={gestante.get('cep')}
                    &estado={gestante.get('state')}{'&dtUltimaMenstruacao=' + str('/'.join(gestante.get('last_menstruation').replace('-','/').split('/')[::-1])) if 'last_menstruation' in gestante else ''}{'&dtNascimento=' + str('/'.join(gestante.get('birth_date').replace('-','/').split('/')[::-1])) if 'birth_date' in gestante else ''}
                    &telefoneFixo={gestante.get('telefone_fixo')}
                    &telefoneCelular={gestante.get('contato_celular')}
                    &contatoEmergencia={gestante.get('nome_contato_emerg')}
                    &telefoneEmergencia={gestante.get('num_contato_emerg')}
                """
            },
            {
            "title": "initialSearchForm",
            "value": "atualizar-cadastro"
            }
        ]
    }
]
~~~
<p style="color: rgb(255, 50, 50)">!! Lembrando que todos os valores devem ser passados no forms parameter pra evitar perda de dados!! </p>

### Corpo do path no manager
``` json
{
    "identifier": "ATUALIZAR-CADASTRO-CONNECT",
    "serviceConfiguration": {
        "permissionLevel": 1,
        "publishLevel": 1,
        "protocol": "https",
        "url": "api-connect.mobilex.tech/api/Qualcom/gestantes_campinagrande_SANDBOX/meuPerfil/atualizarCadastro/response",
        "method": "GET",
        "header": {
            "Authorization": "TOKEN"
        },
        "querystring": "?email=[[EMAIL]]"
    }
}
```
<p>A action chama um forms e em seguida chama a pagina no connect com todos os valores fornecidos no """request.args"""</p>

### REQUISIÇÕES
~~~ python
# dados da gestante
get("https://neo-qualcomm-homo.mobilex.tech/api/resource/Gestantes?email=xxx@email", TOKEN)

# post de dados pre natal
put("https://neo-qualcomm-homo.mobilex.tech/api/resource/Pre Natal", TOKEN)
~~~