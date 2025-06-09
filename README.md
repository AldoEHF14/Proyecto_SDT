# UEA: Sistemas Distribuidos

## 🖥️ TUXEDO

Su objetivo es demostrar la integración de **interfaces gráficas** con una **base de datos Oracle**, haciendo uso de **Oracle Tuxedo** para gestionar la comunicación entre cliente e infraestructura distribuida.

---

## 🎯 Objetivo del Proyecto

Diseñar una aplicación distribuida que permita al usuario realizar operaciones sobre una base de datos a través de una interfaz gráfica intuitiva, aprovechando los servicios de middleware de **Oracle Tuxedo** para conectarse con una **BD Oracle**.

---

##  📌  Arquitectura general

- **Cliente Java** con interfaz gráfica (Swing)
- **Middleware Tuxedo** (archivos `.ud32`, `.fml`)
- **Base de Datos Oracle**
- Comunicación mediante servicios de Tuxedo para cada operación CRUD

---

## ⚙️ Funcionalidades implementadas

La interfaz gráfica permite realizar todas las operaciones básicas de una base de datos desde una aplicación distribuida:

### ✅ Insertar producto

- Permite agregar un nuevo registro a la tabla `Dulceria`
- Se especifican: `id_clave`, `nombre_dulce`, `tipo_dulce`, `descripcion`, `precio`

### 🔍 Buscar producto

- Permite buscar un dulce por su `id_clave` y mostrar sus detalles.

### 📋 Ver todos los productos

- Muestra todos los registros de la tabla `Dulceria` en una `JTextArea` o tabla.

### 🗑 Eliminar producto

- Elimina un dulce de la base de datos mediante su `id_clave`.

### ✏️ Actualizar producto

- Actualiza los datos de un dulce existente usando su `id_clave` como identificador.

---

## 🧾 Estructura de la tabla

```sql
CREATE TABLE Dulceria (
  id_clave NUMBER(20),
  nombre_dulce VARCHAR2(20),
  tipo_dulce VARCHAR2(20),
  descripcion VARCHAR2(20),
  precio NUMBER(20)
);
```

## 🔗 Recursos y bibliografía

- Oracle Tuxedo: https://www.oracle.com/middleware/technologies/tuxedo.html
- Oracle SQL Developer: https://www.oracle.com/database/sqldeveloper/
- Tutorial Java - Archivos de texto: https://decodigo.com/java-crear-archivos-de-texto
