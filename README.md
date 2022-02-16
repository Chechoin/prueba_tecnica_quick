# pruebaTecnicaQuick
## _Por: Sergio Leguizamón_

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)]()

Aquí encontrarás información sobre cómo ejecutar la prueba técnica, e información sobre sus funcionalidades.

Colección postman para testear la - [api](https://go.postman.co/workspace/quickTest~365b9419-208a-4bde-94f7-76876db0c1b4/collection/17786365-aeaf5cdc-a047-48df-9bb8-cb87501cd352) 

## Comandos para instalación del proyecto
Siguiendo los comandos a continuación funcionará correctamente el proyecto

```sh
git clone https://github.com/SergioLeguizamon/prueba_tecnica_quick.git
cd pruebaTecnicaQuick
virtualenv -p python3 venv
source ./venv/bin/activate
pip install -r requirements.txt
```

## Comandos para la ejecución del proyecto

```
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
- [/excel/](http://localhost:8000/excel/) -POST- en la carpeta raíz del pryecto está el archivo archivoPruebaCargue.csv que puede ser cargado a través de post, seleccionando form-data, key=files, y en value se carga el archivo. Los datos se almacenan en la tabla api_clients y puede ser visualizada desde /admin. 


## License

MIT

**Free Software**
