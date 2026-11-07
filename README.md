
# Repair Shop Management API

A RESTful backend application designed to manage the daily operations of a repair shop. The system provides authentication, role-based access control, device management, spare-parts inventory, repair tracking, and technician intervention management.

## Features

- **Authentication and Authorization**
  - User authentication using JWT.
  - Password hashing with bcrypt.
  - Role-based access control.
  - Two user roles: ADMIN and TECH.

- **Device Management**
  - Manage customer devices registered for repair.
  - Store and retrieve device information.

- **Spare Parts Management**
  - Manage spare-parts inventory.
  - Track available stock quantities.
  - Update inventory when parts are used.

- **Repair Management**
  - Create and manage repair records.
  - Track repair progress and related information.
  - Associate repairs with devices and technicians.

- **Technician Interventions**
  - Record technician interventions.
  - Associate interventions with repairs.
  - Manage spare-parts consumption during interventions.
  - Update inventory through transactional operations.

## Technologies Used

| Technology | Purpose |
|---|---|
| Node.js | Runtime environment |
| NestJS 11 | Backend framework |
| TypeScript | Programming language |
| MySQL | Relational database |
| TypeORM | Database ORM |
| JWT | Authentication |
| Passport | Authentication strategy |
| bcrypt | Password hashing |
| Jest | Testing framework |

## Project Structure

```text
repair-backend-api/
├── src/
│   ├── auth/
│   ├── users/
│   ├── devices/
│   ├── repairs/
│   ├── spare-parts/
│   ├── interventions/
│   └── ...
├── test/
├── package.json
├── tsconfig.json
└── nest-cli.json
```

*The structure above summarizes the main application modules.*

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/chahbaniomar/repair-backend-api.git
cd repair-backend-api
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root and configure the database connection and authentication settings.

Example:

```env
DB_HOST=localhost
DB_PORT=3306
DB_USERNAME=root
DB_PASSWORD=your_password
DB_DATABASE=repair_shop

JWT_SECRET=your_jwt_secret
```

Make sure the variable names match those expected by the application configuration.

### 4. Start the application

Development mode:

```bash
npm run start:dev
```

Production mode:

```bash
npm run build
npm run start:prod
```

## Testing

Run the automated tests using:

```bash
npm run test
```

## Main Modules

| Module | Responsibility |
|---|---|
| Authentication | Login, JWT authentication, and access control |
| Users | User management and roles |
| Devices | Device records and information |
| Repairs | Repair tracking and management |
| Spare Parts | Inventory and stock management |
| Interventions | Technician work and spare-parts consumption |

## Future Improvements

- Add API documentation using Swagger.
- Implement more advanced repair status tracking.
- Add customer notifications.
- Improve reporting and inventory analytics.
- Expand automated test coverage.

## Author

**Chahbani Omar**

GitHub: [@chahbaniomar](https://github.com/chahbaniomar)
