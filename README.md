# dockerfile-nginx
Hello-world form nginx server


---
Getting Started
These instructions will get a copy of the project up and running on your local machine for development and testing purposes.

Prerequisites
You'll need to have Docker installed on your machine.

Running the Application
Follow these steps to build and run the application using Docker:

Clone the Repository: Clone this repository to a local folder on your machine.

Bash

git clone [repository-url]
Navigate to the Project Directory: Go to the directory where the Dockerfile and index.html files are located.

Bash

cd [your-project-folder]
Build the Docker Image: Run the following command to build a Docker image named hello-nginx. The . at the end tells Docker to look for the Dockerfile in the current directory.

Bash

docker build -t hello-nginx .
Verify the Image: You can check if the image was successfully created by listing all local Docker images.

Bash

docker images
Run the Docker Container: Start a new container from your hello-nginx image. This command runs the container in detached mode (-d), maps port 8080 on your machine to port 80 in the container, and names the container hello-nginx-from-web.

Bash

docker run -d -p 8080:80 --name hello-nginx-from-web hello-nginx
View the Application: Open your web browser and navigate to http://localhost:8080 to see the index.html page.
