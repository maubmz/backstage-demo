# 1. ¿Qué es Backstage?

[Backstage](https://backstage.io/) es una plataforma de código abierto desarrollada por Spotify que permite construir un **portal para desarrolladores (IDP - Internal Developer Platform)** personalizado. Su objetivo es centralizar todas las herramientas, servicios y documentación que un equipo de desarrollo necesita para trabajar de forma más eficiente, segura y estandarizada.

## Características clave:

- **Catálogo de Software**: organiza y visualiza todos los componentes (microservicios, bibliotecas, herramientas internas) de la organización.
- **Templating con Software Templates**: permite a los desarrolladores crear proyectos nuevos siguiendo estándares definidos por la organización.
- **Integración con herramientas DevOps**: como Jenkins, GitHub, GitLab, Kubernetes, Azure DevOps, Prometheus, entre otros.
- **Plugins Personalizables**: Backstage tiene un sistema de plugins que permite extender su funcionalidad e integrarlo con el stack tecnológico existente.
- **Documentación Viva**: incluye Docs-as-Code con soporte para Markdown y generación automática con TechDocs.

Backstage **no es un portal IDP en sí**, sino la **plataforma base para construirlo**. 

---

# 2. Diseño de Arquitectura del Portal IDP y Manual de Instalación

## Diseño de arquitectura del portal IDP

El portal IDP basado en Backstage se compone de los siguientes elementos clave:

### Componentes principales

- **Frontend Backstage App**: aplicación React generada con el CLI de Backstage, sirve como interfaz para los usuarios.
- **Backend de Backstage**: servidor Node.js con plugins que proveen APIs internas y conexión con herramientas externas.
- **Base de Datos**: comúnmente PostgreSQL, usada para almacenar metadatos del catálogo y estados de plugins. Al instalar backstage es una base de datos en memoria (no persisten los datos).
- **Plugins personalizados**: desarrollos internos que amplían las capacidades de Backstage (por ejemplo: generación de pipelines, onboarding de microservicios).
- **Auth y SSO**: integración con proveedores de identidad (OIDC, Azure AD, Okta) para autenticación y autorización.

## Instalación
### Pasos para instalación
1. Crear la aplicación de Backstage ejecutando el siguiente comando:  
   `npx @backstage/create-app@latest`  
   La aplicación va a generar una estructura de Backstage donde se va a instalar lo necesario para su funcionamiento.

2. Acceder al directorio que generó Backstage con el siguiente comando:  
   `cd {nombre-proyecto}`

3. Estando dentro de nuestra aplicación, ejecutar el siguiente comando para levantar la aplicación:  
   `yarn start`  
   Cuando se termine de levantar la aplicación, nos va a enviar a la página principal de Backstage.


[Regresar al indice](./index.md)
