# 📘 Tasca S2.03. Estructura de dades – MongoDB (NOU)

## 🧩 Descripción

Este repositorio contiene los ejercicios correspondientes a la **Tasca S2.03 – Estructura de dades (MongoDB)** del **Sprint 2** de la especialización en **Java** de la **IT Academy**.

El objetivo de esta práctica es **aprender a diseñar y modelar bases de datos no relacionales** utilizando **MongoDB**, aplicando los principios de las **estructuras de datos tipo documento** y comprendiendo cómo representar relaciones entre entidades en formato **JSON**.  

Se trabajan distintos escenarios prácticos para adquirir soltura en el diseño de modelos de datos en MongoDB a partir de casos reales.

---

## 💾 Bases de datos creadas

### 🏥 Nivel 1 – Òptica “Cul d’Ampolla”

Una óptica desea informatizar la gestión de sus **clientes**, **empleados**, **proveedores** y **ventas de gafas**.  

#### Objetivos del modelo
- Representar las relaciones entre clientes, empleados, gafas y proveedores.  
- Registrar qué empleado realiza cada venta y en qué fecha/hora.  
- Permitir almacenar la información de clientes recomendados por otros clientes.  

#### Entidades principales
- **Proveedor**: nombre, dirección (calle, número, piso, puerta, ciudad, código postal, país), teléfono, fax, NIF.  
- **Gafa**: marca, graduación de cada vidrio, tipo de montura (flotante, pasta o metálica), color de montura, color de cristales, precio, proveedor asociado.  
- **Cliente**: nombre, dirección postal, teléfono, correo electrónico, fecha de registro, cliente que lo recomendó (opcional).  
- **Empleado**: nombre, apellidos, identificador de empleado.  
- **Venta**: referencia a la gafa vendida, cliente, empleado y fecha/hora de la transacción.  

#### Ejercicios
- **Ejercicio 1:** Diseño del modelo de base de datos desde el punto de vista del cliente.  
- **Ejercicio 2:** Diseño del modelo desde el punto de vista de las gafas.  

---

### 🍕 Nivel 2 – Comandes de menjar a domicili

Diseño de una base de datos para una **web de pedidos de comida a domicilio**, donde se gestionan clientes, pedidos, productos, tiendas y empleados.

#### Entidades principales
- **Cliente**: identificador único, nombre, apellidos, dirección, código postal, localidad, provincia, teléfono.  
- **Comanda**: identificador, fecha/hora, tipo (reparto o recogida), lista de productos, cantidad, precio total, nota adicional.  
- **Producto**: identificador, nombre, descripción, imagen, precio.  
  - Subtipos: `pizza`, `hamburguesa`, `bebida`.  
- **Tienda**: identificador, dirección, código postal, localidad, provincia.  
- **Empleado**: identificador, nombre, apellidos, NIF, teléfono, rol (`cuiner/a` o `repartidor/a`).  

#### Relaciones destacadas
- Un cliente puede realizar muchas comandes.  
- Una comanda pertenece a un único cliente y una única tienda.  
- Un repartidor realiza la entrega de la comanda (si es a domicilio).  
- Una tienda puede tener múltiples empleados y gestionar muchas comandes.  

---

### ▶️ Nivel 3 – Mini YouTube

Diseño de un modelo de datos que simula una versión reducida de **YouTube**, gestionando usuarios, vídeos, canales, comentarios y playlists.

#### Entidades principales
- **Usuario/a**: email, contraseña, nombre de usuario, fecha de nacimiento, sexo, país, código postal.  
- **Vídeo**: título, descripción, tamaño, nombre del archivo, duración, miniatura (thumbnail), reproducciones, likes, dislikes, estado (`público`, `oculto`, `privado`), etiquetas, usuario creador, fecha/hora de publicación.  
- **Canal**: nombre, descripción, fecha de creación, usuario propietario.  
- **Like/Dislike**: registro de usuarios que interactúan con un vídeo y la fecha/hora.  
- **Playlist**: nombre, fecha de creación, estado (`pública` o `privada`), lista de vídeos.  
- **Comentario**: texto, usuario autor, vídeo asociado, fecha/hora.  

#### Relaciones destacadas
- Un usuario publica muchos vídeos y puede tener un canal.  
- Un usuario puede suscribirse a los canales de otros usuarios.  
- Cada usuario puede dar like/dislike una sola vez por vídeo.  
- Un usuario puede crear varias playlists y dejar comentarios en distintos vídeos.

---

## 💻 Tecnologías utilizadas

- **MongoDB 6.x**
- **MongoDB Compass**
- ** Moon modeler
- **Git & GitHub**

---

## 📚 Contenido del repositorio

El repositorio incluye:
- Archivos `.json` con los **modelos de datos** de cada nivel.  
- Diagramas de estructura en formato `.png`  

---

## 🛠️ Instalación

Abre los archivos `.json` en **MongoDB Compass** o en tu editor de código y analiza la estructura de las bases de datos.

---

## ▶️ Ejecución

1. Inicia el servidor de **MongoDB**.  
2. Importa los documentos o inserta los modelos mediante los comandos `insertOne()` o `insertMany()`.  
3. Ejecuta consultas `find()` o `aggregate()` para explorar los datos.  
4. Visualiza las relaciones mediante `lookup` o diagramas E-R adaptados a MongoDB.

---

## 🤝 Autoría

Proyecto desarrollado por **Jordi**  
como parte del itinerario de especialización en **Java – IT Academy**.
