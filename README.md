# Task Manager API

A simple API for managing tasks, built with FastAPI.

## Technologies

- **Python** 3.11+
- **FastAPI**  
- **Uvicorn** (ASGI server)
- **PostgreSQL** (via SQLAlchemy)
- **JWT** for authentication
- **Docker** for containerization

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/taskManagerAPI.git
    ```

2. Navigate to the project folder:
    ```bash
    cd taskManagerAPI
    ```

3. Create a virtual environment:
    ```bash
    python -m venv venv
    ```

4. Activate the virtual environment:
    - **Windows**:
      ```bash
      .\venv\Scripts\activate
      ```
    - **Linux/macOS**:
      ```bash
      source venv/bin/activate
      ```

5. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

6. Set up the database and apply migrations:
    ```bash
    alembic upgrade head
    ```

7. Run the application:
    ```bash
    uvicorn app.main:app --reload
    ```

## API Endpoints

- **POST /auth/register** - Register a new user.
- **POST /auth/login** - Log in and receive JWT token.
- **GET /tasks** - Get all tasks (with filters and pagination).
- **POST /tasks** - Create a new task.
- **PUT /tasks/{id}** - Update a task.
- **DELETE /tasks/{id}** - Delete a task.

## Docker

To run the app with Docker:

1. Build and run with Docker Compose:
    ```bash
    docker-compose up
    ```

2. The app will be available at `http://localhost:8000`.

## Tests

Run the tests with:
```bash
pytest