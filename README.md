# dockerfile-nginx
Hello-world form nginx server


---
# Getting Started

These instructions will get a copy of the project up and running on your local machine for development and testing purposes.

## Prerequisites
- Docker must be installed on your machine.

## Running the Application
Follow these steps to build and run the application using Docker:

### 1. Clone the Repository
Clone this repository to a local folder on your machine:

```bash
git clone https://github.com/SatishShreeram/dockerfile-nginx.git
```

### 2. Navigate to the Project Directory
Go to the directory where the `Dockerfile` and `index.html` files are located:

```bash
cd [your-project-folder]
```

### 3. Build the Docker Image
Run the following command to build a Docker image named `hello-nginx`. The `.` at the end tells Docker to look for the Dockerfile in the current directory:

```bash
docker build -t hello-nginx .
```

### 4. Verify the Image
Check if the image was successfully created by listing all local Docker images:

```bash
docker images --filter "reference=hello-nginx"
```

### 5. Run the Docker Container
Start a new container from your `hello-nginx` image. This command runs the container in detached mode (`-d`), maps port 8080 on your machine to port 80 in the container, and names the container `hello-nginx-from-web`:

```bash
docker run -d -p 8080:80 --name hello-nginx-from-web hello-nginx
```

### 6. View the Application
Open your web browser and navigate to [http://localhost:8080](http://localhost:8080) to see the `index.html` page.

