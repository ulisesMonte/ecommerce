# 🏦 Ecommerce API

> API ecommerce desarrollada con Node.js, Express y MongoDB, enfocada en gestión de productos, usuarios, carritos y flujos de compra mediante una arquitectura backend modular y escalable.

---

# 🚀 Características

- 🛒 Gestión de carritos
- 📦 CRUD completo de productos
- 🎟 Sistema de tickets de compra
- 📚 Paginación, filtros y ordenamiento
- 💬 Sistema de mensajería
- 📧 Envío de emails automáticos
- 🔄 Productos en tiempo real mediante WebSockets
- ⚡ API REST modular
- 🧩 Arquitectura desacoplada
- 🗄 Persistencia con MongoDB + archivos JSON

---

# 🛠 Stack Tecnológico

`Node.js` `Express.js` `MongoDB` `Mongoose` `Socket.io` `Nodemailer` `JavaScript` `REST API`

---

# 📂 Arquitectura del Proyecto

```bash
src/
├── config/
├── controllers/
├── dao/
├── dto/
├── middlewares/
├── models/
├── public/
├── repositories/
├── routes/
├── services/
├── views/
├── app.js
├── logger.js
└── utils.js
```

---

# 🧠 Arquitectura Backend

La aplicación implementa una arquitectura desacoplada utilizando:

- DAO Pattern
- Repository Pattern
- DTO Layer
- Services Layer
- MVC modular

```txt
Routes
   ↓
Controllers
   ↓
Services
   ↓
Repositories
   ↓
DAO
   ↓
MongoDB
```

---

# 📦 Funcionalidades Principales

## Productos

- CRUD completo
- Paginación dinámica
- Filtros por categoría
- Ordenamiento por precio
- Validaciones personalizadas
- Control de stock
- Actualización en tiempo real con WebSockets

---

## Usuarios

- Registro y login
- Recuperación de contraseña
- Gestión de documentos
- Tracking de última conexión

---

## Carritos

- Asociación de productos
- Manejo de cantidades
- Flujo de compra
- Generación automática de tickets

---

## Sistema de Tickets

El sistema genera tickets automáticamente luego de finalizar una compra:

- Código único de compra
- Fecha de compra
- Monto total
- Comprador asociado

---

## Emails Automáticos

Integración con Nodemailer para:

- Recuperación de contraseña
- Confirmación de compra
- Eliminación de cuentas inactivas
- Eliminación de productos

---

# 🔧 Persistencia de Datos

El proyecto utiliza:

- MongoDB con Mongoose
- Persistencia en archivos JSON
- DAO Layer para desacoplar acceso a datos

---

# ⚙️ Instalación

```bash
git clone https://github.com/ulisesMonte/eccomerce.git

cd eccomerce

npm install
```

---

# ▶️ Ejecución

```bash
npm run dev
```

---

# 🌐 Variables de Entorno

Crear un archivo `.env`

```env
PORT=8080
MONGO_URL=your_mongodb_connection

MAIL_USER=your_email
MAIL_PASSWORD=your_password
```

---

# 📌 Endpoints

## Productos

- `GET /api/products`
- `POST /api/products`
- `PUT /api/products/:id`
- `DELETE /api/products/:id`

## Carritos

- `GET /api/carts`
- `POST /api/carts`
- `POST /api/carts/:cid/products/:pid`
- `POST /api/carts/:cid/purchase`

## Usuarios

- `POST /api/sessions/register`
- `POST /api/sessions/login`
- `POST /api/sessions/forget-password`

---


