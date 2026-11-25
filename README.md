# Práctica 7 - API de productos con MongoDB

API REST de productos hecha con Express y Mongoose, conectada a MongoDB Atlas.

## Cómo ejecutar

1. Instalar dependencias:

```
npm install
```

2. Crear un archivo `.env` en la raíz (basado en `.env.example`) con tu cadena de conexión:

```
MONGODB_URI=tu_cadena_de_conexion_de_mongodb_atlas
PORT=3000
```

3. Iniciar el servidor:

```
npm start
```

El servidor corre en http://localhost:3000

## Endpoints

| Método | Ruta | Descripción | Respuestas |
|--------|------|-------------|------------|
| GET | /productos | Lista todos los productos | 200 |
| GET | /productos/:id | Obtiene un producto por id | 200, 400, 404 |
| POST | /productos | Crea un producto | 201, 400 |
| PUT | /productos/:id | Actualiza un producto | 200, 400, 404 |
| DELETE | /productos/:id | Elimina un producto | 200, 400, 404 |

Los datos se guardan en la base `tienda`, colección `productos`, y se conservan al reiniciar el servidor.