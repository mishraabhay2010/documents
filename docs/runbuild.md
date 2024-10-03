# Onboarding Tutorial for New Joiners

## Part 2: Project Run, Build, and Deployment

### Introduction
- Overview of the steps involved in running, building, and deploying the project
- Importance of understanding the build and deployment process.

### Running the Project

#### Running Locally
- Open the project in Visual Studio or Visual Studio Code.
- Ensure all dependencies are installed.
- Use the following command to run the project locally:
  ```bash
  dotnet run
- Access the application at http://localhost:5000 (or the configured port)

#### Running with Docker
- Ensure Docker Desktop is running.
- Build the Docker image:
  ```bash
  docker build -t your-project-name .
- Run the Docker container:
  ```bash
  docker run -p 5000:80 your-project-name
- Access the application at http://localhost:5000.

### Building the Project
#### Building Locally
- Open a terminal or command prompt in the project directory.
- Use the following command to build the project
  ```bash
  dotnet build
- Ensure the build completes without errors.
#### Building with Docker
- Ensure Docker Desktop is running.
- Use the following command to build the Docker image
### Deployment
#### Deploying to a Server
- Ensure the server is configured to run .NET applications.
- Copy the build output to the server.
- Use the following command to run the application on the server:
  ```bash
  dotnet your-project-name.dll
#### Deploying with Docker
- Ensure the server is configured to run Docker containers.
- Push the Docker image to a container registry
  ```bash
   docker tag your-project-name your-registry/your-project-name
   docker push your-registry/your-project-name
- Pull and run the Docker image on the server:
  ```bash
  docker pull your-registry/your-project-name
  docker run -p 5000:80 your-registry/your-project-name
