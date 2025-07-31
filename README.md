# Pruebas Automatizadas - Reqres API con Postman

Este repositorio contiene una colección de pruebas automatizadas realizadas con **Postman** para la API pública de [Reqres](https://reqres.in/). Con este repositorio busco mostrar cómo desarrollar pruebas automatizadas centradas en las respuestas (`post response`) de los distintos endpoints de esta API.

---

## ¿Qué contiene este proyecto?

Una colección Postman organizada en carpetas según los endpoints de la API Reqres:

- Get Users  
- Create User  
- Update User (PUT)  
- Update User (PATCH)  
- Delete User  
- Register  
- Login  

Cada endpoint tiene:

- Múltiples pruebas configuradas con assertions en JavaScript.  
- Validación de código de estado, estructura y datos de respuesta.  

---

## Cómo importar la colección en Postman

1. Clona este repositorio o descarga los archivos `.json`.  
2. Abre **Postman**.  
3. Haz clic en `Import` (parte superior izquierda).  
4. Selecciona la pestaña **"File"** y carga ambos archivos:

   - `Reqres API.postman_collection.json`  
   - `Reqres QA.postman_environment.json`  

> ⚠️ **Nota:** Es importante importar tanto la colección como las variables de entorno para que las pruebas funcionen correctamente.


##  Ejecución con Newman (opcional)

Newman permite ejecutar pruebas desde la terminal.

###  Requisitos previos
Debes tener [Node.js](https://nodejs.org/) instalado.

###  Instalación de Newman
```
npm install -g newman
```
### Ejecutar la coleccion con las variables de entorno
```
newman run "Reqres API.postman_collection.json" -e "Reqres QA.postman_environment.json" -r htmlextra
```
##  Estructura del repositorio

```
📂reqres-api-postman-tests
├── Reqres API.postman_collection.json
└── Reqres QA.postman_environment.json 
```
