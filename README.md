Tienes razón, me pediste que **no quitara los `##` ni nada de eso**, y efectivamente lo mantuve así. Pero parece que mi respuesta fue interrumpida antes de completarse. Aquí va la **traducción completa**, fiel al formato que diste:

---

## Sistema de Gestión Financiera

Una aplicación web integral para gestionar finanzas personales, desarrollada con React y Node.js.

## Escenarios de Historia de Usuario: Añadir Tarjeta

Basado en la implementación en `new-front/src/pages/AddCard.tsx` y `new-back/src/routes/credit-card.routes.ts`, los escenarios de prueba para la historia de usuario "Añadir Nueva Tarjeta" son los siguientes:

### Caminos Felices (Happy Paths):

* **Adición Exitosa con Todos los Campos Requeridos**: El usuario ingresa un número de tarjeta, nombre del titular y fecha de vencimiento válidos (y opcionalmente, marca y banco). La tarjeta se añade exitosamente, el formulario se limpia y el usuario es redirigido a la página de selección de tarjetas.

### Caminos Infelices (Unhappy Paths):

* **Campos Requeridos Vacíos**: El usuario intenta añadir una tarjeta dejando los campos `card_number`, `card_holder_name` o `expiry_date` vacíos. La aplicación debe mostrar un mensaje de error y la tarjeta no debe ser añadida.
* **Error del Servidor**: El servidor devuelve un error durante el proceso de adición de la tarjeta (por ejemplo, debido a un problema de conexión o una validación más compleja en el backend). La aplicación debe mostrar un mensaje de error apropiado al usuario.

Recomendación: Para más detalles sobre cómo escribir pruebas robustas, consulta la [Documentación de Jest](https://jestjs.io/docs/getting-started).

## Características

* Autenticación de usuario (inicio de sesión/registro)
* Seguimiento de gastos
* Gestión de presupuestos
* Informes y análisis financieros
* Panel de control con visualizaciones

## Pila Tecnológica

### Frontend

* React con TypeScript
* Material-UI para componentes
* Redux Toolkit para gestión de estado
* React Router para navegación
* Formik y Yup para manejo de formularios
* Chart.js para visualizaciones

### Backend

* Node.js con Express
* TypeScript
* PostgreSQL con Sequelize ORM
* JWT para autenticación
* Principios SOLID y patrones de diseño

## Prerequisitos

* Node.js (v14 o superior)
* PostgreSQL (v12 o superior)
* npm o yarn

## Ejecución de la Aplicación

1. Inicia el servidor del backend:

```bash
cd new-back
npm run dev
```

2. Inicia el servidor de desarrollo del frontend:

```bash
cd new-front
npm start
```

La aplicación estará disponible en:

* Frontend: [http://localhost:3000](http://localhost:3000)
* API del Backend: [http://localhost:3001](http://localhost:3001)

## Estructura del Proyecto

### Backend (`new-back/`)

```
src/
  ├── config/         # Archivos de configuración
  ├── controllers/    # Controladores de rutas
  ├── models/         # Modelos de base de datos
  ├── repositories/   # Capa de acceso a datos
  ├── services/       # Lógica de negocio
  ├── middlewares/    # Middlewares personalizados
  ├── routes/         # Rutas de la API
  ├── utils/          # Funciones utilitarias
  ├── interfaces/     # Interfaces TypeScript
  └── types/          # Tipos TypeScript
```

### Frontend (`new-front/`)

```
src/
  ├── components/     # Componentes reutilizables
  ├── pages/          # Componentes de páginas
  ├── services/       # Servicios de API
  ├── store/          # Store de Redux
  ├── utils/          # Funciones utilitarias
  ├── hooks/          # Hooks personalizados
  ├── types/          # Tipos TypeScript
  └── assets/         # Recursos estáticos
```

## Desarrollo

* La documentación de la API del backend está disponible en [http://localhost:3001/api-docs](http://localhost:3001/api-docs)
* El servidor de desarrollo del frontend incluye recarga en caliente
* La compilación de TypeScript se maneja automáticamente

## Pruebas

```bash
# Pruebas del backend
cd new-back
npm test

# Pruebas del frontend
cd new-front
npm test
```
