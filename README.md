# Financial Management System

A comprehensive web application for managing personal finances, built with React and Node.js.

## Escenarios de Historia de Usuario: Añadir Tarjeta

Basado en la implementación en `new-front/src/pages/AddCard.tsx` y `new-back/src/routes/credit-card.routes.ts`, los escenarios de prueba para la historia de usuario "Añadir Nueva Tarjeta" son los siguientes:

### Caminos Felices (Happy Paths):

- **Adición Exitosa con Todos los Campos Requeridos**: El usuario ingresa un número de tarjeta, nombre del titular y fecha de vencimiento válidos (y opcionalmente, marca y banco). La tarjeta se añade exitosamente, el formulario se limpia y el usuario es redirigido a la página de selección de tarjetas.

### Caminos Infelices (Unhappy Paths):

- **Campos Requeridos Vacíos**: El usuario intenta añadir una tarjeta dejando los campos `card_number`, `card_holder_name` o `expiry_date` vacíos. La aplicación debe mostrar un mensaje de error y la tarjeta no debe ser añadida.
- **Error del Servidor**: El servidor devuelve un error durante el proceso de adición de la tarjeta (por ejemplo, debido a un problema de conexión o una validación más compleja en el backend). La aplicación debe mostrar un mensaje de error apropiado al usuario.

Recomendación: Para más detalles sobre cómo escribir pruebas robustas, consulta la [Documentación de Jest](https://jestjs.io/docs/getting-started).

## Características

- Autenticación de usuario (inicio de sesión/registro)
- Seguimiento de gastos
- Gestión de presupuestos
- Informes y análisis financieros
- Panel de control con visualizaciones

## Pila Tecnológica

### Frontend
- React with TypeScript
- Material-UI for components
- Redux Toolkit for state management
- React Router for navigation
- Formik & Yup for form handling
- Chart.js for visualizations

### Backend
- Node.js with Express
- TypeScript
- PostgreSQL with Sequelize ORM
- JWT for authentication
- SOLID principles and design patterns

## Prerequisites

- Node.js (v14 or higher)
- PostgreSQL (v12 or higher)
- npm or yarn

## Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd <repository-name>
```

2. Set up the database:
- Create a PostgreSQL database named `software_db`
- Update the database credentials in `new-back/.env`

3. Install backend dependencies:
```bash
cd new-back
npm install
```

4. Install frontend dependencies:
```bash
cd ../new-front
npm install
```

## Running the Application

1. Start the backend server:
```bash
cd new-back
npm run dev
```

2. Start the frontend development server:
```bash
cd new-front
npm start
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend API: http://localhost:3001

## Project Structure

### Backend (`new-back/`)
```
src/
  ├── config/         # Configuration files
  ├── controllers/    # Route controllers
  ├── models/         # Database models
  ├── repositories/   # Data access layer
  ├── services/       # Business logic
  ├── middlewares/    # Custom middlewares
  ├── routes/         # API routes
  ├── utils/          # Utility functions
  ├── interfaces/     # TypeScript interfaces
  └── types/          # TypeScript types
```

### Frontend (`new-front/`)
```
src/
  ├── components/     # Reusable components
  ├── pages/         # Page components
  ├── services/      # API services
  ├── store/         # Redux store
  ├── utils/         # Utility functions
  ├── hooks/         # Custom hooks
  ├── types/         # TypeScript types
  └── assets/        # Static assets
```

## Development

- Backend API documentation is available at http://localhost:3001/api-docs
- Frontend development server includes hot reloading
- TypeScript compilation is handled automatically

## Testing

```bash
# Backend tests
cd new-back
npm test

# Frontend tests
cd new-front
npm test
```

## Contributing

1. Create a new branch for your feature
2. Make your changes
3. Submit a pull request

## License

This project is licensed under the MIT License. 