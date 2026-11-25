# Imagen base oficial de Ubuntu
FROM ubuntu:latest

# Evitar preguntas interactivas durante la instalación de paquetes
ENV DEBIAN_FRONTEND=noninteractive

# Actualizar repositorios e instalar herramientas básicas de red y diagnóstico
RUN apt-get update && apt-get install -y \
    curl \
    iputils-ping \
    git \
    && rm -rf /var/lib/apt/lists/*

# Directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar los archivos del repositorio al contenedor
COPY . /app

# Mantener el contenedor activo
CMD ["bash"]