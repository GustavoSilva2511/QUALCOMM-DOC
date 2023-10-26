[Voltar](../vmscripts.md)
# editExams
É necessário de auxilio de comandos nos doctypes de Exames, o codiga ira fazer uma varredura nos exames e os que estiverem sinalizados, serão feitas alterações 
## Comandos sinalizados no doctype exames
### Add attach
~~~ python 
attach_edited = str({
    "command": "add_attach",
    "name_img": image[0]["name"].split("/")[-1],
    "link_img": image[0]["link"],
    "attach_index": attach_index
})
~~~
Esses valores podem ser passados atravez da childtableapi com o subcommand edit_fields

### Delete attach 
~~~ python
attach_edited = str({
    "command" : "delete_attach",
    "field" : request.args.get("field"),
    "path" : request.args.get("link")
})
~~~
Esses valores podem ser passados atravez da childtableapi com o subcommand edit_fields

### Delete path
~~~ python
attach_edited = str({
        "command" : "delete_path",
        "exam_id": request.args.get("name")
})
~~~
Esses valores podem ser passados atravez da childtableapi com o subcommand edit_fields
