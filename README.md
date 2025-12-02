# API REST - Taller de Backend con Node.js
Este repositorio contiene el proyecto final desarrollado para el taller de API REST. El objetivo principal es demostrar la implementación de un servicio web backend funcional capaz de procesar solicitudes HTTP (CRUD) utilizando Javascript en el servidor.

## Tecnologías y Dependencias
El proyecto está construido utilizando las siguientes herramientas clave:

* Node.js: Entorno de ejecución para Javascript.
* Express (v5.1.0): Framework para gestionar rutas y middleware.
* Nodemon (v3.1.11): Dependencia de desarrollo para reinicio automático del servidor.

## Estructura del Proyecto
La organización de archivos del repositorio es la siguiente:

Taller_API_REST/  
├── index.js  
├── package.json  
├── package-lock.json  
└── README.md  

## Instrucciones de Instalación y Ejecución
Sigue estos pasos para poner en marcha el servidor en tu entorno local:

Clonar el repositorio:
```Bash
git clone https://github.com/JCriss06/Taller_API_REST.git
```

Instalar dependencias: Es necesario descargar los módulos requeridos (Express y Nodemon) antes de iniciar:
```Bash
npm install
```

Ejecutar el servidor: El proyecto cuenta con un script configurado para iniciar en modo desarrollo:
```Bash
npm run dev
```

Una vez ejecutado, verás el mensaje: Servidor corriendo exitosamente en http://localhost:3000

## Endpoints de la API  
A continuación se detallan las rutas disponibles para interactuar con la API. Puedes utilizar herramientas como Postman, Insomnia o Thunder Client para probarlas. 

| Método | Ruta | Descripción | Body (JSON) Requerido |
| :--- | :--- | :--- | :--- |
| **GET** | `/` | Ruta raíz. Verifica que el servidor responde. | N/A |
| **GET** | `/saludo` | Retorna un objeto JSON informativo. | N/A |
| **GET** | `/user` | Obtiene la lista completa de usuarios. | N/A |
| **POST** | `/user` | Agrega un nuevo usuario. | `{ "nombre": "...", "edad": 0 }` |
| **PUT** | `/user/:id` | Actualiza un usuario existente por su ID. | `{ "nombre": "...", "edad": 0 }` |
| **DELETE**| `/user/:id` | Elimina un usuario por su ID. | N/A |

## Ejemplos de Peticiones
### Crear un usuario (POST)  
URL: http://localhost:3000/user
```JSON
{
  "nombre": "Juan Perez",
  "edad": 30
}
```
### Actualizar un usuario (PUT)  
URL: http://localhost:3000/user/1
```JSON
{
  "edad": 31
}
```
