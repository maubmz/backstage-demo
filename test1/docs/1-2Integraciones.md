# Requisitos e Integraciones para Backstage

Este documento detalla los requisitos e integraciones necesarias para ejecutar backstage.

---

## Requisitos del Sistema

Asegúrate de tener instalados los siguientes componentes en tu entorno antes de comenzar:

### Herramientas necesarias

- **Node.js** (v16 o superior recomendado): Entorno de ejecución para JavaScript.
- **yarn**: Gestor de paquetes preferido por Backstage.
- **Docker**: Utilizado para contenedores de servicios auxiliares (como bases de datos o servicios externos).
- **Git**: Para clonar repositorios y gestionar control de versiones.
- **curl** o **wget**: Herramientas de línea de comandos para hacer peticiones HTTP.

### Puertos requeridos

- **Puerto 3000**: Interfaz de desarrollo del frontend.
- **Puerto 7007**: API backend del catálogo y otros servicios de Backstage.  

## Instalación
### Pasos para instalación
1. Crear la aplicación de Backstage ejecutando el siguiente comando:  
   `npx @backstage/create-app@latest`  
   La aplicación va a generar una estructura de Backstage donde se va a instalar lo necesario para su funcionamiento.

2. Acceder al directorio que generó Backstage con el siguiente comando:  
   `cd {nombre-proyecto}`

3. Estando dentro de nuestra aplicación, ejecutar el siguiente comando para levantar la aplicación:  
   `yarn start`  
   Cuando se termine de levantar la aplicación, nos va a enviar a la página principal de Backstage que es ejecuta en el puerto **3000**.




[Regresar a Indice](./index.md)
