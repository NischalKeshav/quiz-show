# QuizSink

## Project overview

QuizSink is a real-time classroom quiz game with a NestJS backend and a Next.js frontend. The backend is server-authoritative, handles auth/quiz REST APIs plus game state, and communicates with clients over WebSockets. The frontend provides the host/player experiences and consumes the REST and socket endpoints.

## Tech Stack

Frontend: Next.js
Backend: NestJS
Database: SQLite
Realtime: WebSockets

## Key docs

- Backend REST endpoints: `backend/API.md`
- Backend system design + architecture: `backend/BackendDoc.md`
- Frontend Architecture: `frontend/FrontendDoc.md`

## Getting Started

### Using Docker (Recommended)

To run the entire stack (Frontend + Backend) with a single command:

1.  Make sure you have Docker and Docker Compose installed.
2.  Run the development stack:
    ```bash
    docker-compose up --build
    ```
3.  The frontend will be available at `http://localhost:8080` and the backend at `http://localhost:5200`.

### Manual Setup

1. Clone the repo
2. Install dependencies in frontend and backend folders
3. Run the dev servers
4. Open the app in your browser

Detailed setup lives in docs/onboarding.md

## Hosting

This project is optimized for containerized hosting.

- **Self-Hosting**: Deploy on a VPS with Docker Compose using the `docker-compose.prod.yml` file.
- **Render (Recommended)**:
    1. Sign in to [Render](https://dashboard.render.com).
    2. Click **New** > **Blueprint**.
    3. Connect this repository.
    4. Render will automatically detect the `render.yaml` and configure your services, including the persistent disk for your database.
- **SQLite Persistence**: Ensure you mount a persistent volume to `/app/data` in the backend container to maintain your quiz data between restarts. (Handled automatically on Render via the blueprint).
- **CI/CD**: GitHub Actions automatically builds multi-arch images and pushes them to Docker Hub on every push to `main`.

## How We Work

We use GitHub Issues to track work  
Branch out from the respective branch before making changes
Every change goes through Pull Requests  
Maintainers review before merge
**YOU CANNOT MERGE PR'S YOURSELF**  

> [!NOTE]
> Read `./CONTRIBUTING.md` before your first change

## Need Help

1. Post questions in GitHub Issues with the `help wanted` tag
2. Ask Cameron, Brett or Chloe during class
3. Email `gintherc@bentonvillek12.org` or `berrybr@bentonvillek12.org`
