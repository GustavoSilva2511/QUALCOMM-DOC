[Voltar](../serverscript.md)
# Prenatal
Api feita para acessar comandos feito diretamente no codigo do doctype

- URL: https://neo-qualcomm-homo.mobilex.tech/api/method/prenatal
- METODO: POST

### Body básico
~~~ python
json = {
    "name": request.args.get("parent")
}
~~~
A ausência de commando faz com que o comando padrão se execute, editExams. <br>

----------------------------------------- COMANDOS ----------------------------------------------- <br>
### Editar exame
~~~ python 
json = {
    "command": "edit_exams"
    "name": "name_id_prenatal"
}
~~~
Este comando funciona com auxilio de dados presentes no doctype Exames no campo "attach_edited".

### Salvar imagem
~~~ python 
json = {
    "command": "save_images"
    "name": "name_id_prenatal"
}
~~~
Este comando funciona com auxilio de dados presentes no doctype Exames no campo "attach_edited".
