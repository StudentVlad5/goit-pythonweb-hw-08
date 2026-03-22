Contacts REST API (FastAPI)
This is a RESTful API for managing contacts, built with FastAPI, SQLAlchemy, and PostgreSQL. 
The project is fully containerized using Docker and managed with Poetry.

FeaturesFull CRUD Operations: Create, Read, Update, and Delete contacts.
Advanced Search: Filter contacts by first name, last name, or email using query parameters.
Upcoming Birthdays: Specialized endpoint to retrieve contacts with birthdays in the next 7 days.
Automatic Documentation: Interactive Swagger UI and ReDoc.
Data Validation: Strict type checking and validation using Pydantic.

Tech StackFramework: 

- Framework: FastAPI
- Database: PostgreSQL
- ORM: SQLAlchemy
- Dependency Management: Poetry
- Containerization: Docker & Docker Compose


Installation & Setup

Prerequisites
Docker and Docker Compose installed on your machine.(Optional) Poetry installed for local development.

1. Clone the repository
```
git clone https://github.com/YOUR_USERNAME/goit-pythonweb-hw-08.git
cd goit-pythonweb-hw-08
```

2. Configure Environment Variables
The application uses the following connection string (update it in database.py or create a .env file):
postgresql://vlad:qwertyd@db:5432/contacts_db

3. Run with Docker Compose
The easiest way to start the project is using Docker. This will spin up the PostgreSQL database and the FastAPI application automatically.
'''
docker-compose up --build
'''

The API will be available at: http://localhost:8000

API Documentation
Once the server is running, you can access the interactive documentation:
Swagger UI: http://localhost:8000/docs
ReDoc: http://localhost:8000/redocKey 

Key Endpoints
Method,        Endpoint,               Description
POST,         /contacts/,            Create a new contact
GET,          /contacts/,            List all contacts (supports name, last_name, email filters)
GET,         /contacts/{id},         Get a specific contact by ID
PUT,         /contacts/{id},         Update an existing contact
DELETE,      /contacts/{id},         Delete a contact
GET,         /contacts/birthdays/,   Get contacts with birthdays in the next 7 days

Project Structure:

├── models.py          # SQLAlchemy database models
├── schemas.py         # Pydantic data validation schemas
├── database.py       # Database connection and session management
├── Dockerfile         # Docker image configuration
├── docker-compose.yaml # Multi-container orchestration
├── pyproject.toml     # Poetry dependencies
└── README.md          # Project documentation

 License
 This project was created as a homework assignment for the GoIT Python Web course.
