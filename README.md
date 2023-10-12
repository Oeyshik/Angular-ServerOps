# Angular-ServerOps
This repository showcases a RESTful API-driven full-stack CRUD system for server management, built with Spring Boot, Angular, and MongoDB.

## Table of Contents
- [Video Demo](#video-demo)
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [How the Task Is Made](#how-the-task-is-made)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Project Setup](#project-setup)
- [Screenshots](#screenshots)

## Video Demo

### Click on the thumbnail to Watch:

[![Click to Watch](https://drive.google.com/uc?id=1UoHixYMcrRS9MT7aRSjrKEx9Lql7Cvs-)](https://drive.google.com/file/d/12cyhpt7bs9L7qsMU79UEkJaYBNHLHONX/view?usp=sharing)

## Key Features
- Create new servers with specific details.
- Edit server information, including name, language, and framework.
- Delete individual servers or all servers.
- View a list of servers with their details.
- Interactive user interface for seamless server management.

## Technologies Used
- Angular: A powerful and popular web application framework.
- TypeScript: A statically typed superset of JavaScript.
- Angular Material: A UI component library for Angular applications.
- Bootstrap 4: A responsive and customizable CSS framework.
- RESTful API: Communicates with the backend using RESTful web services.

## How the Task Is Made

### Backend

1. Create a Server (POST Request):

To create a new server, send a POST request to the /api/servers endpoint. The request body should be in JSON format and include the following attributes:

- id (String): The unique ID for the server.
- name (String): The name of the server.
- language (String): The programming language used on the server.
- framework (String): The framework used on the server.

Example JSON request body:
    
    {
    "id": "123",
    "name": "Test Server",
    "language": "Java",
    "framework": "Spring Boot"
    }

2. Get Servers (GET Request):

To retrieve a list of all servers, send a GET request to the /api/servers endpoint. If no parameters are provided, this endpoint will return a list of all servers stored in the database.

3. Get Server by ID (GET Request):

To retrieve a specific server by its ID, send a GET request to the /api/servers/{id} endpoint, where {id} should be replaced with the server's unique ID. If the server with the specified ID exists, it will be returned; otherwise, a "404 Not Found" response will be returned.

4. Update Server by ID (PUT Request):

To update an existing server by its ID, send a PUT request to the /api/servers/{id} endpoint, where {id} should be replaced with the server's unique ID. The request body should contain the updated server information in JSON format. If the server with the specified ID exists, it will be updated with the provided data; otherwise, a "404 Not Found" response will be returned.

5. Delete Server by ID (DELETE Request):

To delete a server by its ID, send a DELETE request to the /api/servers/{id} endpoint, where {id} should be replaced with the server's unique ID. If the server with the specified ID exists, it will be deleted from the database; otherwise, a "404 Not Found" response will be returned.

6. Find Servers by Name (GET Request)
To search for servers by name, send a GET request to the /api/servers/findByName endpoint with the name query parameter. The server controller will search for servers whose names contain the provided string. If one or more servers are found, they will be returned; otherwise, a "404 Not Found" response will be returned.

These endpoints collectively provide the basic CRUD (Create, Read, Update, Delete) operations for managing server objects in the MongoDB database.

You can customize and extend these endpoints to fit your specific requirements and business logic.

### Frontend
The next task consists of creating a web-based frontend using Angular that interacts with a REST API implemented using Spring Boot. The frontend provides functionality to view a list of servers, create new servers, edit existing servers, and delete servers.

The application uses Angular components to separate different parts of the user interface:

- **Create Server Component**: Allows users to create a new server by providing server details.
- **Edit Server Component**: Provides a form for editing server details.
- **Server List Component**: Displays a list of servers, and users can edit or delete individual servers.

The frontend communicates with the backend using HTTP requests to perform CRUD (Create, Read, Update, Delete) operations on the server data.


## Project Structure
- backend/-
  - `src/`: This directory contains the source code and resources for the project.
    - `main/`: The main application code.
      - `java/`: All Java source files are located here.
      - `resources/`: This directory holds resource files, such as configuration files.
    - `test/`: Contains test code to ensure the reliability of the application.
      - `java/`: Test source files are organized here.
      - `resources/`: You can find test-related resource files in this directory.
  - `target/`: This directory stores compiled bytecode and built artifacts.
  - `.gitignore`: The Gitignore file specifies which files and directories should be excluded from version control.
  - `pom.xml`: The Project Object Model (POM) file, which is used for Maven configuration.
- frontend/
  - `src/`: This directory contains the source code and resources for the project.
      - `app/`: The main application code.
          - `create-server/`: This directory contains the Create Server Component.
          - `edit-server/`: This directory contains the Edit Server Component.
          - `server/`: This directory contains the Server List Component.
          - `server.service.ts`: This TypeScript file is the Server Service.
          - `app.component.ts`: The main component of the Angular application.
          - `app.module.ts`: The main module of the Angular application.
          - `app.component.html`: The main HTML template for the Angular application.
          - `...`  Other Angular components and modules.
      -  `assets/`: This directory holds static assets like images.
          - `images/`: Subdirectory for image assets.
              - `logo.png`: The logo image used in the application.
  - `...`  Other Angular configuration and setup files.

## Prerequisites
- Java Development Kit (JDK)
- Maven
- Spring Boot
- MongoDB
- Postman (for testing)
  
- Node.js and npm (Node Package Manager)
- Angular CLI

## Project Setup
1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/Oeyshik/Angular-ServerOps.git

2. Open the project in your preferred IDE.

3. Ensure that you have MongoDB installed and running locally.

### Database Configuration
In the 'application.properties' file, configure your MongoDB database settings:

        spring.data.mongodb.host=localhost
        spring.data.mongodb.port=27017
        spring.data.mongodb.database=task1
        
Before running the application, make sure you have the following:

1. Node.js and npm installed. You can download them from [here](https://nodejs.org/).
2. Angular CLI installed globally. You can install it using npm:

   ```bash
   npm install -g @angular/cli

3. Navigate to the project folder:

4. Install the project dependencies:

    ```bash
    npm install

5. Start the Angular development server:

    ```bash
    ng serve

6. Open a web browser and access the application at 
    ```bash
    http://localhost:4200/.

## Screenshots
### Web UI FrontEnd
![App Screenshot](https://drive.google.com/uc?id=1UoHixYMcrRS9MT7aRSjrKEx9Lql7Cvs-)

### Creating Server
![App Screenshot](https://drive.google.com/uc?id=184m-NEBRuuvguFR5A-RzAQ2Vw5b9kmPG)

### New Server Added
![App Screenshot](https://drive.google.com/uc?id=1kLCpWm8wADm5P9c84Wh87fFeYdbx6gt9)

### MongoDB Database Gets Updated
![App Screenshot](https://drive.google.com/uc?id=1O5ya0b4oMVFwImVl4SmZbHavgjOFLbre)

### Change is reflected in http://localhost:8080/api/server
![App Screenshot](https://drive.google.com/uc?id=141ENnpVMIFdPO4Hs-R4-8P9e9wh-GbJl)

### Deleting a Server
![App Screenshot](https://drive.google.com/uc?id=1EBrguKKMbyIDiUDZrFBeL6M7mKazfZpN)

### Server is Deleted
![App Screenshot](https://drive.google.com/uc?id=1egFY-Hl3rPXsRQKtewOHWWDyz5DMcFCO)

### Server Gets Deleted from MongoDB Database
![App Screenshot](https://drive.google.com/uc?id=1Jnq3WIkCGXtUyiA_3U7cTkrE5m1BPfhk)

### Deleting All Servers
![App Screenshot](https://drive.google.com/uc?id=1EDlyCy7MbuqNXFSFWh2wiUZ-75IO70dc)

### All servers gets deleted
![App Screenshot](https://drive.google.com/uc?id=1Db3gmn8xJ6o3xaLV13mgJ6-LHMmBsrmx)

### Servers Gets Deleted from MongoDB Database
![App Screenshot](https://drive.google.com/uc?id=1rVABJCIPltGZOReCWJocp9LNJHbO5e3v)
