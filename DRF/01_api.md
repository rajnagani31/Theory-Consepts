# API (Application Programming Interface)

is a set of rules that allows different software applications to communicate with each other.

is a set of rules that allows different software applications to communicate with each other.

API is bridge between of response and request.

API is talk to server after request and get data server and they give response to user

# REST API(Representational State Transfer)
A REST API uses HTTP methods to interact with resources (like users, posts, etc.).

GET ---> Get data to user 

POST ---> Create data to server

PUT ---> Update entire data to server

PATCH ---> Update Partial Data

DELETE ---> Delete data to server

## 🔸 REST API Key Features:

Stateless: No session saved on server.

JSON/XML format (mostly JSON today).

CRUD operations using HTTP methods.

# DRF(Django Rest Framework )

DRF is a powerful and flexible Python library to build REST APIs using Django.

### 🔸 DRF Advantages:
Automatically converts Django models to APIs.

Easy to use with serializers and viewsets.

Supports authentication, permissions, pagination, etc.

### 🔸 Example Flow in DRF:
Model: Create database structure.

Serializer: Convert model to JSON.

ViewSet: Define what actions to allow (GET, POST, etc.).

Router: Automatically generate URLs.

