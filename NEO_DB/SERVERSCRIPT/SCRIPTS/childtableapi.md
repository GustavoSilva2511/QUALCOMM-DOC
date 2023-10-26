[Voltar](../serverscript.md)
# CHILDTABLE API
Api feita para facilitar a interação com o banco de dados, sendo possível trazer os dados de tabela filha também.

- URL: https://neo-qualcomm-homo.mobilex.tech/api/method/childtableapi
- METODO: POST

### Body básico
~~~ python
json = {
    "command": "commando",
    "doctype": "doctype"
}
~~~
------------------------------------------------- COMANDOS ----------------------------------------------------<br>
É necessário que se passe sempre o json com todos os dados necessários para o funcionamento de cada comando.
### Get_all
~~~ python
json = {
    "command": "get_all",
    "doctype": "nome do doctype"
}
~~~
### Response
~~~ python
# Aqui foi utilizado um exemplo com o doctype de Equipes
"msg": [
    {
        "name": "Nome da equipe",
        "owner": "criador",
        "creation": "2023-04-18 09:42:03.483989",
        "modified": "2023-06-01 01:17:04.345667",
        "modified_by": "Administrator",
        "docstatus": 0,
        "idx": 0,
        "nome_da_equipe": "Nome da equipe",
        "unidade": "Unidade da equipe",
        "doctype": "Equipes"
    },
    {...},
    {...}
]
~~~
-----------------------------------------------------------------------------------------------------------------
### Create
~~~ python
json = {
    "command": "create",
    "doctype": "nome do doctype"
    "charge": {
        # Informações que serão acrescentada na criação do doctype
        # é necessário ter conhecimento dos campos do doctype que esta sendo criado para evitar erros
    }
}
~~~
### Response
~~~ python
# Aqui foi utilizado um exemplo com o doctype de Equipes
"msg": ["Doctype created!"]
~~~
------------------------------------------------------------------------------------------------------------------<br>
-------------------------------------------------- SUB COMMANDS --------------------------------------------------
### no_repeat
Faz com que valores especificados não se repitam
~~~ python
json = {
    "command": "get_all",
    "doctype": "nome do doctype",
    "sub_command": "no_repeat",
    "fields": ["campo de comparação"]
}
~~~
Exemplo, se no "campo de comparação" colocarmos idade, serão retornadas todas as idade sem repetição de numeros
se tiverem duas pessoas com 28 anos, virá apenas um numero 28

--------------------------------------------------------------------------------------------------------------------

### edit_fields
Altera valores de um doctype
~~~ python
json = {
    "command": "get_all",
    "doctype": "nome do doctype",
    "sub_command": "edit_fields",
    "sub_values": {
        "campo1": "novoValor",
        "campo2": "novoValor",
        "campoN": "novoValor"
    }
}
~~~
Exemplo, se eu quiser fazer alteração de iformações de contato, basta saber o campo certo e alterar para o novo valor

--------------------------------------------------------------------------------------------------------------------

### delet_doc
Deleta um doctype especifico
~~~ python
json = {
    "command": "get_all",
    "doctype": "nome do doctype",
    "sub_command": "delete_doc",
    "filters": {"name": "name_id"}
}
~~~
ATENÇÃO: Sempre usar filtro com precisão pra evitar deletar doctypes indesejado, por questão de segurança essa função está limitada a apagar apenas 1 doctype por vez<br>
--------------------------------------------------------------------------------------------------------------------------- <br>
------------------------------------------- VARIAÇÔES PARA JSON ----------------------------------------------------
### Filters
~~~ python
json = {
    "command": "get_all",
    "doctype": "nome do doctype",
    "filters": {
        "campo1": "valor1",
        "campo2": "valor2",
        "campoN": "valorN"
    }
}
~~~
---------------------------------------------------------------------------------------------------------------------
### Fields
~~~ python
json = {
    "command": "get_all",
    "doctype": "nome do doctype",
    "fields": ["campo1", "campo2", "campo3", "campoN"]
}
~~~


