Resource Allocation Project
This is a Resource Allocation System developed with a React.js frontend, a Spring Boot backend, and a MySQL database. The project is designed to manage resources (such as employees, tasks, etc.) within an organization and enables various types of users to interact with the system according to their roles. It offers functionalities including user login, signup, and distinct dashboards for Admin, Manager, and Employee roles.

Project Overview
The Resource Allocation Project is designed to assist organizations in effectively managing their resources. The system enables users to sign up, log in, and access dashboards tailored to their roles (Admin, Manager, Employee). It manages employee tasks, allocates resources, and offers insights into resource utilization through user-friendly dashboards.

Frontend: Built with React.js for a responsive, interactive user interface.
Backend: Built with Spring Boot for a robust and scalable REST API.
Database: MySQL is used to store data about users, resources, and tasks.

Application Features:

Login Form:
- Enables users to log into the system.
- Users can access their respective dashboards based on their roles.

Signup Form:
- Allows new users to create an account.
- Supports basic user validation and role assignment (Admin, Manager, Employee).

Admin Dashboard:
- Admins can view and manage all users, resources, and tasks.
- Admins can assign resources to employees and manage the overall allocation of tasks.

Manager Dashboard:
- Managers can view the resources assigned to their team.
- Managers can assign or reallocate resources to employees.
- Managers can view the status of tasks and evaluate employee performance.

Employee Dashboard:
- Employees can view their assigned tasks.
- Employees can update the status of tasks and track their progress.
- Employees can view the resources allocated to them.


Technologies Used
Frontend:
React.js: A JavaScript library for building user interfaces.
React Router: For routing between pages.
Axios: For making HTTP requests to the Spring Boot backend.
Bootstrap: For responsive design and styling.
Backend:
Spring Boot: A Java-based framework used to build the REST API.
Spring Security: For securing the login and managing user authentication.
Spring Data JPA: To interact with the MySQL database.
JWT: JSON Web Tokens for secure authentication and authorization.
Database:
MySQL: A relational database to store user data, resources, tasks, and role information.
Database Schema
The MySQL database consists of several tables:
Users: Stores user information like username, password, role (Admin, Manager, Employee).
Resources: Stores data about resources (tasks, tools, etc.).
Assignments: Stores task assignments to employees.
Tasks: Stores details of tasks and their status (assigned, in progress, completed).
Roles: Stores roles and their associated permissions.

Prerequisites
Before running the project, make sure you have the following installed on your system:
Java (JDK 23) - Required for running the Spring Boot backend.
Download Java
Node.js (v14.x or higher) - Required to run the React frontend.
Download Node.js
MySQL - Required to set up the database for the project
Download MySQL
Maven - For managing backend dependencies and building the Spring Boot application (Usually comes with Spring Boot)
Download Maven
Git - To clone the repository.
Download Git
Setting Up the Project
1. Clone the Repository
Clone the repository to your local machine using Git:
git clone https://github.com/yourusername/resource-allocation-project.git
2. Setting Up the Backend (Spring Boot)
   
Step 1: Configure MySQL Database
Make sure MySQL is running on your machine.
Create a new database for the project, for example:
CREATE DATABASE resource_allocation;
Configure the MySQL connection in the application.properties file located in the backend/src/main/java/service/lasttryapplication directory. Update the connection settings to match your local MySQL setup:
spring.datasource.url=jdbc:mysql://localhost:3306/resource_allocation
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

Step 2: Build and Run the Backend
Open a terminal in the backend folder (where the pom.xml file is located).
Run the following Maven command to install dependencies and build the project:
mvn clean install
Start the Spring Boot application:
mvn spring-boot:run
The backend server should now be running at http://localhost:8080.

3. Setting Up the Frontend (React.js)
   
Step 1: Install Dependencies
Open a terminal in the frontend folder (where the package.json file is located).
Install the required dependencies:
npm install
Step 2: Configure API URL
In the frontend/src/utils/axios.js or any similar API-related file, ensure that the API base URL points to the backend URL:
const API_URL = "http://localhost:8080";  // Ensure this matches the backend server URL
Step 3: Run the Frontend
Once the dependencies are installed, you can start the frontend:
npm start
This will start the React application at http://localhost:3000.

How to Test the Project
Open http://localhost:3000 in your browser (this will load the React frontend).
You should be able to see the login/signup form.
Sign up as a new user or log in with an existing user.
Depending on the role assigned (Admin, Manager, Employee), you will be redirected to the respective dashboard where you can manage resources, tasks, and assignments.


# Resource_Allocation
