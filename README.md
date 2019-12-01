Aplicación web para la clinica "san juan bosco".
Trabajo práctico - Aspectos Legales y Profesionales.


Para correr el trabajo se deben ejecutar los siguientes comandos:

    docker-compose -f docker-compose.prod.yml up -d --build     

    docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput

    docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear

En este punto la aplicación ya esta corriendo en el puerto 1337.

Ingrese a su navegador y coloque la URL: localhost:1337



Para cerrar la aplicación correctamente debe ejecutar el siguiente comando:

    docker-compose -f docker-compose.prod.yml down -v