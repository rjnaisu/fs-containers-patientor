# Patientor Docker

This is a containerized version of the Patientor application developed during the TypeScript chapter of Full Stack Open. Here we demonstrate use of both dev and production configurations for Docker and nginx in a full stack app of choice.

## Structure

```text
└── my-app
    ├── frontend
    |    ├── Dockerfile.dev
    |    └── Dockerfile
    ├── backend
    |    ├── Dockerfile.dev
    |    └── Dockerfile
    ├── nginx.dev.conf
    ├── nginx.conf
    ├── docker-compose.dev.yml
    └── docker-compose.yml
```

## Docker Commands

Run the development environment:

```bash
docker compose -f docker-compose.dev.yml up --build
```

Open the app at:

```text
http://localhost:8080
```

Stop the development environment:

```bash
docker compose -f docker-compose.dev.yml down
```

Run the production environment:

```bash
docker compose up --build
```

Stop the production environment:

```bash
docker compose down
```
