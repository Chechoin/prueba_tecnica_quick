# pruebaTecnicaQuick
## _Por: Sergio Leguizamón_

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)]()

Aquí encontrarás información sobre cómo ejecutar la prueba técnica, e información sobre sus funcionalidades.

- Type some Markdown on the left
- See HTML in the right
- ✨Magic ✨

## Comandos para ejecución del proyecto
Siguiendo los comandos a continuación funcionará correctamente el proyecto

```sh
git clone ######
cd pruebaTecnicaQuick
virtualenv -p python3 venv
source ./venv/bin/activate
pip install -r requirements.txt
pip install pandas
python manage.py runserver
python manage.py makemigrations
python manage.py migrate 
```
## ENDPOINTS

Aquí se explican los endpoints y modo de uso en la aplicación. Luego de ejecutar los comandos de la sección anterior se tendrá acceso a las siguientes rutas:

- [/clientes](http://localhost:8000/client/) - Listado y creación de clientes.
- [/products](http://localhost:8000/products/) - Listado y creación de productos.
- [/products/ud](http://localhost:8000/products/ud/) - Actualizar y eliminar productos usando su id.
- [/bills/](http://localhost:8000/bills/) - Listado y creación de facturas
- [/bills/ud](http://localhost:8000/bills/ud/) - Actualizar y eliminar una factura especificada a través del id
- [/bills/products/](http://localhost:8000/bills/products/) - Lista facturas-productos
- [/api/create_user/1.0/](http://localhost:8000/api/create_user/1.0/) - configurar en el header Content-Type:application/json y enviar en el body un json de con la siguiente estructura: 
{
    "first_name": "",
    "last_name": "",
    "username": "",
    "email": "",
    "password":"" 
}
- [/login](http://localhost:8000/login/) - Iniciar sesión usuario:sergio password:sergio
- [/api_generate_token/](http://localhost:8000/api_generate_token/) - generar token usuario:sergio password:sergio
- [/excel/](http://localhost:8000/excel/) -GET- Mediante el método GET de esta url automáticamente se creara un reporte en csv de los clientes creados, este archivo se guardará en la carpeta static/excel.
- [/excel/](http://localhost:8000/excel/) -POST- enviando en el body los datos key-value lo siguiente:
key: files, value: archivo.csv()
A través de postman se puede realizar una prueba sencilla, se realiza un POST a la url http://localhost:8000/excel/ en el body se establece que se enviará en form-data y en el valor key se define que será un archivo (file) lo que permitirá cargar un archivo a través de un input file. Al hacer el POST se guardará una copia del documento en la carpeta static/excel y se cargarán a la tabla Clientes los registros. **NOTA: en el proyecto hay un archivo llamado archivoPruebaCargue.csv con datos nuevos para ser cargados.


## License

MIT

**Free Software, Hell Yeah!**
