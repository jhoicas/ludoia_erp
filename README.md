# Ludoia ERP

Bienvenido al repositorio principal de **Ludoia ERP**. Este repositorio funciona como un **monorepo** que integra tanto la API (Backend) como la interfaz de usuario (Frontend) del sistema de planificación de recursos empresariales.

## 📁 Estructura del Proyecto

El proyecto se divide en las siguientes áreas principales:

- **`/backend`**: Contiene la API REST desarrollada en **Go**. Gestiona la lógica de negocio, acceso a la base de datos (inventario y otros módulos).
- **`/frontend`**: Contiene la aplicación web desarrollada con **React** y **Vite**.

## 🚀 Requisitos Previos

Para ejecutar y contribuir a este proyecto, es recomendable tener instalado:

- [Docker](https://www.docker.com/) y [Docker Compose](https://docs.docker.com/compose/)
- [Go](https://go.dev/) (para desarrollo local del backend)
- [Node.js](https://nodejs.org/) (para desarrollo local del frontend)

## 🛠️ Cómo ejecutar el proyecto

La manera más sencilla de inicializar ambos servicios simultáneamente es mediante **Docker Compose**.

Desde la raíz del proyecto, ejecuta:

```bash
docker-compose up -d --build
```

Esto construirá las imágenes y levantará los contenedores según la configuración de los puertos en `docker-compose.yml`.

### Ejecución Local (Sin Docker)

Si deseas trabajar en los servicios de forma individual:

**Backend:**
```bash
cd backend
# Asegúrate de tener tu archivo .env configurado correctamente
go run main.go
```

**Frontend:**
```bash
cd frontend
npm install
npm run dev
```

## ⚙️ Configuración (.env)

Recuerda crear tus archivos `.env` basándote en los posibles `.env.example` dentro de cada carpeta (`/backend` y `/frontend`) para que los servicios tengan las credenciales y puertos de entorno correspondientes.
