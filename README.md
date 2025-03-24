# StudentProject

## Project Overview
StudentProject is a Django-based web application that consists of multiple apps (App1 and App2) and provides a basic demonstration of Django's capabilities. The project is containerized using Docker and integrated with Jenkins for CI/CD automation.

## Features
- Homepage with navigation links to other pages.
- Sample pages in both apps displaying static content.
- Uses Django templates to render views.
- Dockerized for easy deployment.
- Jenkins setup for CI/CD automation.

## Installation & Setup

### Prerequisites
Ensure you have the following installed on your system:
- Python 3.10+
- Docker
- Git

### Clone the Repository
```sh
git clone https://github.com/your-username/StudentProject.git
cd StudentProject
```

### Running the Project with Docker
#### 1. Build the Docker Image
```sh
docker build -t studentproject .
```
#### 2. Run the Docker Container
```sh
docker run -p 8000:8000 studentproject
```
Access the application at: [http://localhost:8000](http://localhost:8000)

## Jenkins Setup

### 1. Build and Run Jenkins Container
```sh
docker build -t jenkins-python .
docker run -p 8080:8080 -p 50000:50000 jenkins-python
```
Access Jenkins at: [http://localhost:8080](http://localhost:8080)

### 2. Retrieve Initial Admin Password
```sh
docker exec -it <container_id> sh
cat /var/jenkins_home/secrets/initialAdminPassword
```
Use this password to complete the Jenkins setup.

## Project Structure
```
StudentProject/
│-- app1/
│-- app2/
│-- StudentProject/
│-- templates/
│-- static/
│-- Dockerfile
│-- requirements.txt
│-- manage.py
│-- README.md
```

## Contributing
Feel free to fork the repository and submit pull requests.

## License
This project is licensed under the MIT License.

