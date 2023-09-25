# Utiliza la imagen base de Python con una versión específica
FROM python:3.9

# Establece el directorio de trabajo en el contenedor
WORKDIR /app

# Copia el archivo de requisitos y lo instala en el contenedor
COPY requirements.txt /app/
RUN ls -al /app              # Listar todos los archivos y directorios en /app
RUN pip install -r requirements.txt

# Copia todo el contenido de tu proyecto al contenedor
COPY . /app/

# Expone el puerto en el que se ejecutará la aplicación Django
EXPOSE 8000

# Comando para ejecutar la aplicación Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
