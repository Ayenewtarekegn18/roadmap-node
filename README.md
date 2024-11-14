#Roadmap Backend Application
This is a backend application built with Node.js and Express.js, utilizing Sequelize as the ORM for database interactions. The application handles user authentication, course management, and roadmap generation.

##Project Structure

.gitignore
config/
    db.js
controllers/
    authControllers.js
    courseController.js
    roadmapController.js
    userController.js
index.js
middleware/
    authMiddleaware.js
    tokenBlackList.js
models/
    courseModel.js
    lessonModel.js
    resourceModel.js
    roadmap.js
    userModel.js
package.json
routes/
    authRoutes.js
    courseRoutes.js
    roadmapRoutes.js
    userRoutes.js
services/
    Database.js
    ExpressApp.js
utils/
    example_json.json
    passwordUtility.js
    validationUtility.js
    
##Key Components
Controllers
authControllers.js: Handles user authentication, including registration, login, and logout.
courseController.js: Manages course-related operations such as creating, updating, deleting, and fetching courses.
roadmapController.js: Generates learning roadmaps using Google Generative AI.
userController.js: Manages user-related operations such as fetching, updating, and deleting users.
Middleware
authMiddleaware.js: Middleware for authenticating requests using JWT tokens.
tokenBlackList.js: Manages a blacklist of JWT tokens to handle logout functionality.
Models
courseModel.js: Defines the schema for the Course model.
lessonModel.js: Defines the schema for the Lesson model.
resourceModel.js: Defines the schema for the Resource model.
roadmap.js: Defines the schema for the Roadmap model.
userModel.js: Defines the schema for the User model.
Routes
authRoutes.js: Routes for authentication-related endpoints.
courseRoutes.js: Routes for course-related endpoints.
roadmapRoutes.js: Routes for roadmap-related endpoints.
userRoutes.js: Routes for user-related endpoints.
Services
Database.js: Configures and connects to the database using Sequelize.
ExpressApp.js: Sets up the Express application with middleware and routes.
Utilities
example_json.json: Example JSON data for courses.
passwordUtility.js: Utility functions for hashing and validating passwords.
validationUtility.js: Utility functions for validating email, username, and password strength.
Running the Project
To run the project, follow these steps:

Install the dependencies:

Create a .env file with the necessary environment variables (e.g., database credentials, JWT secret key).

Start the server:

The server will start and listen on port 8000 by default. You can access the API endpoints via http://localhost:8000.

Example API Endpoints
POST /api/auth/register: Register a new user.
POST /api/auth/login: Login a user.
POST /api/auth/logout: Logout a user.
GET /api/course: Fetch all courses.
POST /api/course/new: Create a new course.
PATCH /api/course/update: Update a course.
DELETE /api/course/:id: Delete a course by ID.
GET /api/roadmap: Fetch a learning roadmap.
POST /api/roadmap: Create a new learning roadmap.
Dependencies
The project relies on several npm packages, including but not limited to:

express: Web framework for Node.js.
sequelize: Promise-based ORM for Node.js.
jsonwebtoken: For generating and verifying JWT tokens.
bcryptjs: For hashing and validating passwords.
dotenv: For loading environment variables from a .env file.
cors: For enabling Cross-Origin Resource Sharing.
