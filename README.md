# 🗄️ Módulo SQL — Repaso Personal

---

## 📁 Estructura del Repositorio

- `SQL_sentencias/`: Contiene scripts con sentencias SQL básicas y avanzadas.
- `SQL_requerist.txt`: Archivo con requisitos y ejercicios prácticos para reforzar el aprendizaje.


---

## 🧰 Sentencias SQL Básicas (`SQL_sentencias/`)

🔹 Conceptos Clave

- **SELECT**: Recuperar datos de una o más tablas.
- **INSERT**: Agregar nuevos registros a una tabla.
- **UPDATE**: Modificar registros existentes.
- **DELETE**: Eliminar registros de una tabla.

📌 Ejemplos de Código

```sql
-- Seleccionar todos los registros de la tabla 'clientes'
SELECT * FROM clientes;

-- Insertar un nuevo cliente
INSERT INTO clientes (nombre, email) VALUES ('Juan Pérez', 'juan.perez@example.com');

-- Actualizar el email de un cliente
UPDATE clientes SET email = 'juan.p@example.com' WHERE nombre = 'Juan Pérez';

-- Eliminar un cliente
DELETE FROM clientes WHERE nombre = 'Juan Pérez';

```

---

## 🧠 Consultas Avanzadas
🔹 Conceptos Clave

    JOIN: Combinar filas de dos o más tablas basadas en una relación entre ellas.

    GROUP BY: Agrupar resultados que tienen los mismos valores en columnas específicas.

    HAVING: Filtrar grupos de resultados.

    SUBQUERIES: Consultas dentro de otras consultas.

📌 Ejemplos de Código

```sql

-- Obtener el número de pedidos por cliente
SELECT cliente_id, COUNT(*) AS total_pedidos
FROM pedidos
GROUP BY cliente_id;

```

```sql

-- Seleccionar clientes que han realizado más de 5 pedidos
SELECT cliente_id
FROM pedidos
GROUP BY cliente_id
HAVING COUNT(*) > 5;

```

```sql

-- Subconsulta para obtener clientes sin pedidos
SELECT nombre
FROM clientes
WHERE id NOT IN (SELECT cliente_id FROM pedidos);

```

---

## 📝 Requisitos y Ejercicios (SQL_requerist.txt)

Este archivo contiene una serie de ejercicios prácticos diseñados para reforzar los conocimientos adquiridos. Algunos ejemplos incluyen:

  - Crear y modificar tablas.

    - Insertar y actualizar datos.

    - Realizar consultas con condiciones específicas.

    - Utilizar funciones agregadas y subconsultas.


---

## 🖼️ Recursos Visuales

Para facilitar la comprensión de las relaciones entre tablas y la estructura de la base de datos, se recomienda el uso de diagramas entidad-relación (ER). Herramientas como dbdiagram.io o draw.io pueden ser útiles para crear estos diagramas.
📚 Recursos Recomendados

Para profundizar en estos temas, te recomiendo los siguientes recursos:

  - Tutorial de SQL en W3Schools: w3schools.com/sql

    - Guía de SQL para Principiantes: sqlbolt.com

    - Curso de SQL en Español: youtube.com
