User Management REST API with Flask

This project is a simple REST API built using **Flask** that manages user data.  
It supports basic CRUD operations (Create, Read, Update, Delete) using HTTP methods.

Features

- Get all users
- Get a specific user by ID
- Create a new user
- Update an existing user
- Delete a user

Tech Stack

- Python
- Flask
- Postman or Curl (for testing)

API Endpoints

GET /users
Get a list of all users.  
Response:

{
  "1": {"name": "Alice", "email": "alice@example.com"},
  "2": {"name": "Bob", "email": "bob@example.com"}
}
GET /users/<id>

Get a user by ID.
Response (200 OK):

{"name": "Alice", "email": "alice@example.com"}

If not found (404):

{"error": "User not found"}

POST /users
Create a new user.
Request Body:
{
  "name": "John Doe",
  "email": "john@example.com"
}

Response (201 Created):
{"id": 3, "message": "User created successfully"}

PUT /users/<id>
Update an existing user.
Request Body (any field):
{
  "name": "Updated Name"
}

Response:
{"message": "User updated successfully"}

DELETE /users/<id>
Delete a user by ID.
Response:
{"message": "User deleted successfully"}

How to Run
Clone this repository or copy the code into a file app.py.

Install Flask:
pip install flask

Run the Flask app:
python app.py

Open Postman or use curl to test the endpoints listed above.

Outcome
By completing this task, you will understand:
-REST API fundamentals
-Flask routing and HTTP methods
-In-memory data storage using dictionaries

