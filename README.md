# Generador de decretos municipales

Esta aplicación genera Decretos municipales en base a informes de evaluación para adjudicar servicios o productos necesarios en las Direcciones.

# Herramientas utilizadas
- Python Flask
- Regex (Palabras claves)
- Api GPT
- Sql Server

## Requisitos previos.
- Tener instalado GIT
- Tener instalado Python
- Tener instalado SQLServer



## Instalación y levantamiento de la aplicación.

1. Clonar el repositorio:
   
```
git clone https://github.com/germanDitec/generador-decretos.git
cd generador-decretos
```

2. Instalar entorno virtual de Python:

```
pip install virtualenv
```

3. Crear entorno de virtual de Python:

```
virtualenv venv
```

4. Activar entorno virtual de Python:

```
.\venv\Scripts\activate
```

5. Instalar librerias necesarios del proyecto:

```
pip install -r requirements.txt
```
puede que surga algún error en un entorno windows, por ende sigue las siguientes instrucciones para solventar esto:
```
pip install setuptools
pip install aiohttp frozenlist multidict tiktoken yarl
```

6. Crea un archivo .env y coloca tus variables de entorno (basate en .env.example)

```
   DATABASE_HOST=localhost | host de la base de datos
   DATABASE_USER=sa o cualquier otro
   DATABASE_PASSWORD=password DB
   SECRET_KEY=clavesecreta
   OPENAI_API_KEY=TOKEN DE OPENAI
   MAIL_SERVER=smtp.office365.com
   MAIL_USERNAME=correo
   MAIL_DEFAULT_SENDER=mismocorreo
   MAIL_PASSWORD=PASSWORD

```

7. Levantar el servidor Flask:

```
flask run
```
Si quieres utilizar un modo debug para ver los cambios que hagas, ejecuta el siguiente comando en vez del anterior:
```
flask --debug run
```

# Actualizar cambios en producción

Para poder actualizar los cambios que se hagan en producción se debe acceder al servidor y realizar los siguientes comandos:
``` Obtener los cambios nuevos del repositorio
git pull
```
```Actualizar el servicio de la aplicación
sudo systemctl restart Generador-decretos.service
```


