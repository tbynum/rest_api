# REST API

This is a simple REST API built with Django and Django REST Framework.

## Features

- User authentication
- CRUD operations for resources
- Token-based authentication for secure API access
- Input validation
- Error handling

## Technologies Used

- Python
- Django
- Django REST Framework
- PostgreSQL/SQLite (for database)

## Getting Started

### Prerequisites

- Python 3.x
- pip (Python package installer)
- A database (e.g., PostgreSQL, SQLite)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/tbynum/rest_api.git
   cd rest_api
   ```

2. Create a virtual environment and activate it:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   *(Note: You may need to create a `requirements.txt` file if it doesn't exist, containing `Django` and `djangorestframework`.)*

4. Create a `.env` file in the root directory and add your Django `SECRET_KEY` and database configuration.

### Running the Application

1. Apply database migrations:

   ```bash
   python manage.py migrate
   ```

2. Start the development server:

   ```bash
   python manage.py runserver
   ```

   The API will be accessible at `http://localhost:8000` (default Django port).

## API Endpoints

(This section would typically include a detailed list of API endpoints, HTTP methods, request/response formats, and authentication requirements, based on your Django REST Framework setup.)

### Example: User Authentication

- `POST /api/auth/register`: Register a new user.
- `POST /api/auth/login`: Log in a user and get an authentication token.

### Example: Resource Management (e.g., Items)

- `GET /api/items`: Get all items.
- `GET /api/items/:id`: Get a single item by ID.
- `POST /api/items`: Create a new item (requires authentication).
- `PUT /api/items/:id`: Update an item by ID (requires authentication).
- `DELETE /api/items/:id`: Delete an item by ID (requires authentication).

## Project Structure

```
.
├── manage.py
├── rest_api/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── venv/
├── .env.example
├── .gitignore
├── requirements.txt
└── README.md
```

- `manage.py`: Django's command-line utility for administrative tasks.
- `rest_api/`: The main Django project directory.
- `settings.py`: Django project settings.
- `urls.py`: URL declarations for the project.
- `wsgi.py`: WSGI configuration for serving the project.
- `venv/`: Python virtual environment (local).
- `requirements.txt`: Lists Python dependencies.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
