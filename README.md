# FastAPI Full-Stack Todo App (JWT Auth)

A simple full-stack Todo application built with FastAPI (backend) and a frontend (static files served from static/). Authentication uses JSON Web Tokens (JWT).

### Features

- User registration & login
- JWT-based authentication (access token)
- CRUD operations for Todo items
- Static & Templates files served from /static (can host SPA or simple HTML/CSS/JS)
- SQLite (default) or any SQLAlchemy-supported DB
- Basic tests using pytest for auth and route behavior

## Tech stack

- Python 3.10+
- FastAPI
- Uvicorn
- SQLAlchemy (ORM)
- jose (JWT encode/decode)
- Alembic (optional, for migrations)
- pytest / pytest-asyncio (for tests)
- Frontend: simple static HTML/JS in TodoApp/static & jinja2 tamplates

## Project structure (example)
.
├── TodoApp
│   ├── __init__.py
│   ├── main.py              # FastAPI app + mounts
│   ├── models.py            # SQLAlchemy models + Base
│   ├── database.py          # engine, SessionLocal
│   ├── routers
│   │   ├── auth.py
│   │   ├── todos.py
│   │   ├── users.py
│   │   └── admin.py
│   └── static                   # static frontend files
│   └── templates               # html frontend files
├── tests
│   └── test_auth.py
│   ├── test_todos.py
│   ├── test_users.py
│   ├── test_admin.py
├── alembic
├── requirements.txt
└── README.md
