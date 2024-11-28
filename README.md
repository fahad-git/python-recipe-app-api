# Python Recipe App API

Welcome to the Python Recipe App API, a Django-based backend API for managing recipes. This project provides a RESTful service allowing users to perform CRUD operations on recipes, manage ingredients and tags, and upload images. The application is containerized using Docker for seamless deployment and scalability.

---

## Features

- **User Authentication**
  - Secure user registration and login with token-based authentication.
  
- **Recipe Management**
  - Create, Read, Update, and Delete (CRUD) operations on recipes.
  
- **Ingredient and Tag Management**
  - Organize recipes with custom tags and manage ingredient lists.
  
- **Image Upload**
  - Upload images for recipes to enhance the visual experience.

---

## Technology Stack

- **Frameworks:** Django, Django REST Framework
- **Database:** PostgreSQL
- **Containerization:** Docker
- **Testing:** Test-Driven Development (TDD) with unit tests
- **Continuous Integration:** Travis CI

---

## Prerequisites

Before running the application, ensure the following are installed on your system:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

---

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/fahad-git/python-recipe-app-api.git
```

### Navigate to the Project Directory

```bash
cd python-recipe-app-api
```

### Build and Start Docker Containers

```bash
docker-compose up --build
```

### Run Migrations

```bash
docker-compose run app sh -c "python manage.py migrate"
```

### Create a Superuser (Optional)

```bash
docker-compose run app sh -c "python manage.py createsuperuser"
```

### Access the Application

- Open your browser and navigate to: [http://localhost:8000](http://localhost:8000)
- Use tools like Postman or curl to interact with the API.

---

## API Endpoints

### Authentication

- **Register User:** `/api/user/create/` (POST)
- **Login:** `/api/user/token/` (POST)
- **Manage User:** `/api/user/me/` (GET/PUT)

### Recipes

- **List Recipes:** `/api/recipe/recipes/` (GET)
- **Create Recipe:** `/api/recipe/recipes/` (POST)
- **Retrieve Recipe:** `/api/recipe/recipes/<id>/` (GET)
- **Update Recipe:** `/api/recipe/recipes/<id>/` (PATCH)
- **Delete Recipe:** `/api/recipe/recipes/<id>/` (DELETE)

### Tags

- **List Tags:** `/api/recipe/tags/` (GET)
- **Create Tag:** `/api/recipe/tags/` (POST)

### Ingredients

- **List Ingredients:** `/api/recipe/ingredients/` (GET)
- **Create Ingredient:** `/api/recipe/ingredients/` (POST)

### Uploads

- **Upload Recipe Image:** `/api/recipe/recipes/<id>/upload-image/` (POST)

---

## Testing

Run the comprehensive test suite to ensure application reliability:

```bash
docker-compose run app sh -c "python manage.py test"
```

---

## Continuous Integration

This repository integrates with Travis CI to automate testing and ensure code quality. On every push, the test suite is executed, and results are displayed in the CI pipeline.

---

## Project Structure

```
python-recipe-app-api/
├── app/
│   ├── core/          # Core Django app for database models
│   ├── recipe/        # Recipe app for API logic
│   ├── user/          # User app for authentication
│   ├── tests/         # Unit tests
│   ├── Dockerfile     # Docker configuration
│   ├── manage.py      # Django management script
├── docker-compose.yml # Docker Compose configuration
└── README.md          # Documentation file
```

---

## Contributing

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

Special thanks to the Django and Docker communities for their amazing tools and documentation.
