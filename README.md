# in.orbit

**in.orbit** is a full-stack goal scheduling application developed during the Rocketseat event, **NLW Pocket: JavaScript - Full-stack Intermediate**.

## Features

The application allows users to:
- Set weekly goals
- Track pending goals for the week
- Mark goals as completed
- View a weekly summary of goal progress

## Technologies Used

### Backend
- **Node.js** with **TypeScript**
- **Fastify** framework
- **DrizzleORM** for database interaction
- **PostgreSQL** as the database
- **Docker** for containerization
- **Zod** for schema validation

### Frontend
- **ReactJS** with **TypeScript**
- **Vite** for tooling
- **TailwindCSS** for responsive styling
- **TanStack Query** for asynchronous data management
- Integration with the Node.js API

## API Endpoints

Visit the `requests.http` file in the root of the project to test the API using the **REST Client** extension for VSCode, **Postman**, or other API testing tools.

### Goals

```bash
curl -X POST http://localhost:3333/goals \
-H "Content-Type: application/json" \
-d '{"title": "Fazer nada", "desiredWeeklyFrequency": 7}'
```

### Get week pending goals

```bash
curl -X GET http://localhost:3333/pending-goals
```

### Create goal completion

```bash
curl -X POST http://localhost:3333/completions \
-H "Content-Type: application/json" \
-d '{"goalId": "the_goal_id_here"}'
```

### Get week summary

```bash
curl -X GET http://localhost:3333/summary
```