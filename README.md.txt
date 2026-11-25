# Proyecto de Integración Continua (GitHub + Docker + Jenkins)

Este repositorio contiene la estructura y configuración base para el flujo de Integración Continua (CI) desarrollado para las Entregas 1 y 2 del módulo.

## Arquitectura del Entorno
* **Control de Versiones:** GitHub
* **Contenerización:** Docker Desktop (Windows x86_64)
* **Contenedores de Trabajo:** `ubuntu1` y `ubuntu2` comunicados mediante la red interna `red_ci`
* **Orquestador CI:** Jenkins (`jenkins/jenkins:lts`)

## Estructura del Repositorio
* `README.md`: Documentación técnica y guía de despliegue.
* `Dockerfile`: Definición de imagen personalizada basada en Ubuntu.
* `Jenkinsfile`: Pipeline declarativo para la automatización de pruebas y construcción.