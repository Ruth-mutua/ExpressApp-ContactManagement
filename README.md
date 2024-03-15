# ExpressApp-ContactManagement
PROJECT DEVELOPMENT STRUCTURE:
1. REST API convention
2. Project setup of the contact management application
3. Creating an Express Server
4. Thunder Client Setup
5. Express Router and Contacts CRUD route setup
6. Creating contact controller for contacts CRUD Operations
7. Multiple HTTP Methods per Route
8. Built-in Middleware for POST Request body
9. Express- Throw error
10. Error Habdling Middleware
11. Express Asyncy Handler
12. MongoDB setup
13. Connecting Express App to MongoDB database
14. Mongoose schema for contacts
15. CRUD Get all contacts, CRUD create new contact, CRUD Get one contact, CRUD update contact, CRUD delete contact.
16. Adding user routes- for registration, login and current user
17. Adding user controller 
18. Mongoose schema for user
19. User registration and password hashing
20. JWT Access Token & User Login
21. Protecting routes for user
22. A middleware to verify JWT Token 
23. Handle relationship between user and contact schema
24. Protecting routes for contacts
25. Logged in User: Get all contacts, create new contact, update contact, and delete contact.

PROJECT OVERVIEW
This project focuses on building a backend API for a contact manager application, covering essential aspects like server setup, routing, controller logic, database interaction, authentication, error handling, and configuration. It covers setting up an Express project, creating an Express server, installing Thunder client for API testing, setting up Express router, handling errors, setting up middleware, and configuring MongoDB with Mongoose schema.

1. Project Setup:
Creation of a new directory for the backend APIs.
Initialization of the project with npm init to generate the package.json file.
Installation of Express and Nodemon as dependencies.
Setting up the server file (server.js) with basic Express server configuration and environment variable setup for the port.

2. Server Setup and Configuration:
   - server.js: Sets up the Express server, defines routes, and listens for incoming requests.
   - .env: Stores environment variables for configuration, such as the port number.

3. API Routing and Controllers:
   - routes/contactRoutes.js: Handles routing for contact-related APIs using Express Router.
   - routes/userRoutes.js: Hanldes routing for user-related APIs using Express Router. 
   - controllers/userController.js: Controller handling user-related operations such as registration, login, etc.
   - controllers/contactController.js: Contains logic for CRUD operations on contacts, interacting with MongoDB using Mongoose.

4. Models and Middleware:
   - models/contactModel.js: Defines Mongoose schema for the Contact model, specifying document structure.
   - models/contactModel.js: Define Mongoose schema for defining the user model.
   - middlewares/validateTokenHandler.js: Implements middleware for user authentication and authorization using JWT tokens. This middleware transforms  error responses into JSON format for consistency.
   - middlewares/errorMiddleware.js: Handles errors during request processing and formats error responses.

5. Additional Files and Folders:
   - config/dbConnection.js: Configuration file for database connection, including URL and JWT secret.
   - package.json and `package-lock.json: Manage project dependencies and scripts, ensuring consistency.
   - .gitignore: Specifies files and directories ignored by version control, such as node_modules.
   - README.md: Provides instructions, setup guidelines, and project overview for developers and contributors.

5. Async/Await and Express Async Handler:
Async/await syntax is adopted for managing asynchronous operations in the codebase.
The express-async-handler package is installed to simplify error handling in asynchronous Express routes.
Async handler middleware is imported and applied to all controller functions, ensuring consistent error handling throughout the application.

6. MongoDB Setup:
MongoDB is selected as the database solution, with a cluster created using MongoDB Atlas.
A cluster named "page cluster" is established with appropriate security configurations.
Within the cluster, a database named "my contacts backend" is created, along with a collection named "contacts" to store contact information.

7. Authentication:
JWT Implementation: Authentication is implemented using JSON Web Tokens (JWT). Tokens are generated upon successful login and used to authenticate subsequent requests.
Authorization:
Private Routes: Certain routes (e.g., contact-related endpoints) are protected and require a valid JWT for access. This is enforced using the authMiddleware.

