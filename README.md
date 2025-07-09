# Concursos MPD

Este proyecto permite gestionar los concursos del Ministerio Público de la Defensa (MPD).
Consta de dos partes principales:

- **concurso-backend**: servicio REST construido con Spring Boot.
- **mpd-concursos-app-frontend**: aplicación web desarrollada en Angular.

Los contenedores se orquestan mediante `docker-compose` para simplificar la puesta en marcha.

## Requisitos
- [Docker](https://docs.docker.com/get-docker/) y [Docker Compose](https://docs.docker.com/compose/install/).

## Puesta en marcha
1. Clonar este repositorio y situarse en la raíz del proyecto (donde se encuentra `docker-compose.yml`).
2. Ejecutar:
   ```bash
   docker-compose up --build
   ```
   Esto levantará MySQL, el backend y el frontend.

Una vez iniciado, la aplicación web quedará disponible en `http://localhost:8000` y el backend en `http://localhost:8080`.

## Pruebas básicas
- Acceder a `http://localhost:8000` para verificar que la interfaz cargue correctamente.
- Probar el endpoint del backend, por ejemplo:
  ```bash
  curl http://localhost:8080/actuator/health
  ```
  Debería devolver el estado de la aplicación.

## Estructura adicional
Para más detalles de cada módulo revisa:
- [`concurso-backend`](concurso-backend)
- [`mpd-concursos-app-frontend`](mpd-concursos-app-frontend)
