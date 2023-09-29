# notas-unigui
Mis notas personales de uniGui-Delphi
```
    {:::::::::::::::EJEMPLOS JAVASCRIPT:::::::::::::::::::}

    //Ejemplo de como asignar un ID para css y js en unigui
    BActualizar.JSControl.Id:= 'miID';


    //Ejemplo de como ejecutar codigo js desde el servidor...
    //...para usarlo para modificar el texto por js

    UniSession.AddJS('var button = Ext.getCmp("miID"); button.setText(''<i class="fa fa-arrows-rotate fa-lg" style="color: #64616B;"></i>'');');

    //Ejemplo cargar js desde un string:
    var codigoJS:= 'alert("Boom!")';
    UniSession.AddJS(codigoJS);


    //Ejemplo cargar js desde un archivo externo:
    var textoJS: TstringList;
    textoJS:= TStringList.Create;
    try
    textoJS.LoadFromFile(UniServerModule.FilesFolderPath+ '/js/miScript.js');
    UniSession.addJS(textoJS.Text);
    finally
    textoJS.Free
    end;

    {:::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::}
```
