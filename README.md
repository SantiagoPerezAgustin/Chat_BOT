🛒 BICTECH - E-Commerce Platform

BICTECH es una plataforma web de comercio electrónico moderna, escalable y full-stack orientada a la venta de productos tecnológicos y electrónicos. El proyecto fue desarrollado como Trabajo Integrador Final para la Tecnicatura Universitaria en Programación (UTN).

🚀 Características Principales

👤 Para Clientes

Autenticación y Perfil: Registro e inicio de sesión seguro con JWT.

Catálogo de Productos: Exploración dinámica por categorías y marcas con búsqueda y filtros.

Carrito de Compras: Gestión persistente de productos en tiempo real con validación de stock disponible.

Gestión de Pedidos: Confirmación de compras y seguimiento del historial de pedidos con estados actualizados (Pendiente, Confirmado, Enviado, Entregado).

🛠️ Para Administradores (Panel Admin)

Gestión de Catálogo (ABM/CRUD): Alta, baja y modificación de productos, categorías y marcas.

Control de Inventario: Gestión de stock en tiempo real y alerta de disponibilidad.

Administración de Pedidos: Monitoreo y actualización del flujo de estados de los pedidos de los usuarios.

Gestión de Usuarios: Control de roles y asignación de permisos (Cliente / Administrador).

🛠️ Arquitectura y Tecnologías

El proyecto fue diseñado aplicando principios de Clean Architecture (Arquitectura en Capas) para asegurar la mantenibilidad, legibilidad y modularidad del código.

Backend

Framework: .NET 8 (ASP.NET Core Web API)

ORM: Entity Framework Core

Base de Datos: SQL Server / PostgreSQL (compatible)

Autenticación & Seguridad: JWT (JSON Web Tokens) & Password Hashing

Documentación de API: Swagger / OpenAPI

Frontend

Librería UI: React + Vite

Estilos: Bootstrap 5 & Custom CSS

Manejo de Estado: Context API

Cliente HTTP: Axios

DevOps & Herramientas

Control de Versiones: Git & GitHub

Integración Continua: GitHub Actions (Pipelines de CI/CD para testing y build)

Pruebas: Postman / xUnit

📂 Estructura del Proyecto

TP-Final-BICTECH/
├── backend/
│   ├── Bictech.Domain/          # Entidades y Lógica de Negocio
│   ├── Bictech.Application/     # Casos de Uso, DTOs e Interfaces
│   ├── Bictech.Infrastructure/  # Persistencia de Datos y Entity Framework Core
│   └── Bictech.API/             # Controllers, Middlewares y Configuración API
│
└── frontend/
    ├── src/
    │   ├── components/          # Componentes reutilizables de UI
    │   ├── context/             # Estado Global (Carrito, Auth)
    │   ├── pages/               # Vistas principales (Home, Catalog, Admin, Checkout)
    │   ├── services/            # Llamadas a la API REST (Axios)
    │   └── styles/              # Archivos de estilos globales y temas
    └── package.json


⚙️ Instalación y Configuración Local

Prerrequisitos

.NET 8.0 SDK

Node.js (v18 o superior)

SQL Server o Docker con instancia SQL

1. Clonar el repositorio

git clone https://github.com/emi-pereyra17/TP-Final-BICTECH.git
cd TP-Final-BICTECH


2. Configurar el Backend (.NET 8)

Navega a la carpeta del backend:

cd backend/Bictech.API


Configura tu cadena de conexión en appsettings.json:

"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Database=BictechDb;Trusted_Connection=True;TrustServerCertificate=True;"
}


Aplica las migraciones e inicia la base de datos:

dotnet ef database update


Ejecuta la API:

dotnet run


La API estará corriendo en https://localhost:7123 (o el puerto configurado).

3. Configurar el Frontend (React)

En una nueva terminal, navega a la carpeta del frontend:

cd frontend


Instala las dependencias:

npm install


Inicia el servidor de desarrollo:

npm run dev


Abrí tu navegador en http://localhost:5173.

👨‍💻 Equipo de Desarrollo

Santiago Perez - Full Stack Developer (Frontend / Integración API / UI) - GitHub | LinkedIn

Emiliano Pereyra - Backend Developer (.NET / EF Core / Database) - GitHub

Máximo Jara - Full Stack Support & Testing

📄 Licencia

Este proyecto fue desarrollado con fines educativos dentro del marco de la UTN (Universidad Tecnológica Nacional).
