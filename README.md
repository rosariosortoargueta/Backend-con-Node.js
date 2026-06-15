# 🚀 Backend con Node.js - Profe Rosario

Bienvenido al repositorio de Backend con **Node.js**, desarrollado bajo la guía, mentoría y tutoría de la **Profesora Rosario**. Este espacio está diseñado para consolidar el aprendizaje de la arquitectura de software del lado del servidor, buenas prácticas de desarrollo, y la construcción de APIs RESTful robustas, escalables y seguras.

---

## 📸 Vista Previa del Proyecto

Aquí puedes ver el flujo de la aplicación y el diseño de la arquitectura implementada en clase:

### Arquitectura General del Sistema
![Diagrama de Arquitectura](https://images.unsplash.com/photo-1555066931-4365d14bab8c?q=80&w=1200&auto=format&fit=crop)  
*Nota: Puedes reemplazar esta imagen por tu propio diagrama de arquitectura en `assets/arquitectura.png`.*

### Pruebas de Endpoints (Postman / Insomnia)
![Pruebas en Postman](https://images.unsplash.com/photo-1618401471353-b98aedd07871?q=80&w=1200&auto=format&fit=crop)  
*Nota: Captura de pantalla de las peticiones HTTP exitosas en el entorno de desarrollo.*

---

## 📋 Tabla de Contenidos
- [Descripción del Curso / Proyecto](#-descripción-del-curso--proyecto)
- [Características Principales](#-características-principales)
- [Tecnologías Utilizadas](#-tecnologías-utilizadas)
- [Arquitectura y Estructura de Capas](#-arquitectura-y-estructura-de-capas)
- [Requisitos Previos](#-requisitos-previos)
- [Instalación y Configuración](#%EF%B8%8F-instalación-y-configuración)
- [End-points de la API](#-end-points-de-la-api)
- [Flujo de Autenticación y Seguridad](#-flujo-de-autenticación-y-seguridad)
- [Pruebas (Testing)](#-pruebas-testing)
- [Buenas Prácticas Aplicadas](#-buenas-prácticas-aplicadas)
- [Contacto](#-contacto)

---

## 📝 Descripción del Curso / Proyecto
Este proyecto backend ha sido construido desde cero con el fin de asimilar los conceptos clave del ecosistema de Node.js. Bajo la supervisión de la Profe Rosario, nos enfocamos en resolver problemas del mundo real mediante código limpio, asincronía eficiente (Async/Await), y una correcta separación de responsabilidades.

La aplicación permite gestionar el ciclo de vida completo de los datos (CRUD) y cuenta con capas estrictas de seguridad para proteger la integridad de la información.

---

## ✨ Características Principales
* **Autenticación y Autorización:** Implementación de flujos seguros con JWT (JSON Web Tokens) y encriptación de contraseñas.
* **Validación de Datos:** Uso de middlewares especializados para asegurar que las peticiones cumplan con el formato requerido antes de llegar a la base de datos.
* **Manejo Centralizado de Errores:** Estructura global para capturar y responder de forma homogénea ante fallos del sistema.
* **Paginación y Filtros:** Endpoints optimizados para consultas de alto rendimiento en colecciones/tablas grandes.

---

## 🛠️ Tecnologías Utilizadas

| Categoría | Tecnología / Herramienta | Descripción |
| :--- | :--- | :--- |
| **Entorno** | [Node.js](https://nodejs.org/) | Entorno de ejecución para JavaScript en el servidor. |
| **Framework** | [Express.js](https://expressjs.com/) | Framework minimalista para direccionamiento y middlewares. |
| **BD** | MongoDB / PostgreSQL | Almacenamiento persistente de datos de la aplicación. |
| **ORM/ODM** | Mongoose / Sequelize | Modelado de objetos y mapeo de datos. |
| **Seguridad** | Bcrypt & JWT | Encriptación hashes y tokens de acceso por sesión. |
| **Pruebas** | Jest / Supertest | Testing unitario y de integración para endpoints. |

---

## 📐 Arquitectura y Estructura de Capas
El proyecto implementa una **Arquitectura en Capas** que aísla la lógica de las rutas, los controladores y el acceso a datos:

```text
├── src/
│   ├── config/          # Conexiones a bases de datos y variables globales
│   ├── controllers/     # Lógica de negocio (recibe req, envía res)
│   ├── models/          # Definición de esquemas y modelos de datos
│   ├── routes/          # Definición de rutas y mapeo de endpoints
│   ├── middlewares/     # Validaciones, interceptores y control de acceso
│   ├── utils/           # Funciones helper reutilizables
│   └── app.js           # Inicialización de Express y middlewares globales
├── tests/               # Archivos de pruebas automatizadas (.test.js)
├── .env.example         # Archivo de guía para variables de entorno
├── package.json         # Gestión de scripts y dependencias
└── README.md            # Documentación del proyecto
