# 🎬📚📺 DelFlo

Esta es una aplicación web que permite a los usuarios llevar un registro personalizado de su progreso al ver **series**, **películas** y leer **libros**. Cada recurso puede ser añadido, editado, eliminado y visualizado desde la interfaz, con una valoración y reseña personal al terminarlo.

---

## 📝 Descripción del Repositorio

Este repositorio contiene el desarrollo completo del proyecto web para la gestión de recursos de entretenimiento (series, películas y libros). Aquí encontrarás:

- Archivo `.json` con los datos organizados por tipo de recurso.
- Archivo `.json` con los datos organizados por cada usuario.
- Comandos necesarios para crear e importar la base de datos en MongoDB.

### 📌 Generalidades

- El proyecto usa **MongoDB** como base de datos NoSQL.
- Se realizaron dos archivos `.json` para la creación de datos tanto para registros como para usuarios.
- Se creó un Id para cada usuario para relacionarlo con una serie, pelicula o libro.
- Se agregó el Id del usuario al documento de registros para hacer referencia a quienes hayan visto o leido el recurso y su opinión.


### 🧭 Indicaciones para uso

1. Leer los comandos de instalación y carga de base de datos en MongoDB.
2. Usar los archivos `.json` incluidos para importar datos de ejemplo.
3. Empezar búsqueda de datos y filtrado en MongoDB.

---

## 🚀 Funcionalidades Principales

### ✅ CRUD de Recursos

Cada recurso (serie, película o libro) cuenta con los siguientes campos:

- 📌 **Nombre del recurso**
- 🎭 **Género**
- 🌐 **Plataforma** (Netflix, Amazon, HBO, Kindle, etc.)
- 🔁 **Estado** (En progreso, Terminado, Pendiente)
- 🎞️ **Formato** (Serie, Película, Libro)
- 📅 **Fecha de terminación**
- ⭐ **Valoración final** (1 a 5 estrellas)
- 📝 **Reseña personal** (comentarios del usuario)

### 🛠️ Operaciones disponibles

- **Crear:** Agregar nuevos recursos con todos los campos anteriores.
- **Leer:** Ver la lista de recursos registrados con toda la información detallada.
- **Actualizar:** Editar información de un recurso existente.
- **Eliminar:** Eliminar un recurso de la base de datos.

---

## 🧱 Modelo de Datos – MongoDB

### 📂 Colección: `recursos`

Ejemplo de documento para registros:

```json
{
    "id_usuario":"01",
    "nombre": "Siempre a tu lado",
    "genero":"drama",
    "plataforma":"youtube",
    "formato":"pelicula",
    "fecha_terminacion":"03-08-2025",
    "valoracion_final":"5",
    "reseña":"Muy linda, Lloré mucho"
}
```


Ejemplo de documento para usuarios:
```json
{
    "id_usuario": "01",
    "nombre": "valentina",
    "correo": "valen@gmail.com",
    "nombre_user": "valendr"
}
```

### Importar datos de series, peliculas y libros
mongoimport --db recursosDelFlo --collection recursosDelFlo --file "./Base de datos App DelFlo/registros.json" --jsonArray


## 🤝 Participantes

- **Valentina Delgado**
- **Camila Florez** 
---

## 📜 Contacto GitHub
- https://github.com/ValentinaDelgadoRincon
- https://github.com/CamilaFlorez12
