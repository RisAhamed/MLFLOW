# MLFLOW Dockerized Flask Application

This repository contains a Dockerized Flask application for MLFLOW. It provides instructions on how to build, run, and deploy the application using Docker.

## Prerequisites

- Docker installed on your machine
- Docker Hub account
- Git (optional)

## Setup

### Clone the Repository

1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:
   ```bash
   cd <project-directory>
   ```

## Docker Instructions

### Building the Docker Image

To build the Docker image, run the following command in the project directory:

```bash
docker build -t your-username/flask-app:latest .
```

Replace `your-username` with your Docker Hub username.

### Running the Docker Container Locally

To run the Docker container locally, use the following command:

```bash
docker run -p 5000:5000 your-username/flask-app:latest
```

This will map port 5000 from the container to port 5000 on your host machine, allowing you to access the Flask application at `http://localhost:5000`.

### Docker Hub Operations

#### Login to Docker Hub

Before pushing your image to Docker Hub, ensure you are logged in:

```bash
docker login
```

#### Tagging the Docker Image

Tag your Docker image with your Docker Hub username:

```bash
docker tag flask-app your-username/flask-app:latest
```

#### Pushing to Docker Hub

Push your tagged image to Docker Hub:

```bash
docker push your-username/flask-app:latest
```

#### Pulling from Docker Hub

To pull the image from Docker Hub, use:

```bash
docker pull your-username/flask-app:latest
```

## Application Usage

Once the Docker container is running, you can access the application at: `http://localhost:5000`.

## Docker Image Structure

The Docker image is built using:
- **Base Image**: Python 3.8-slim
- **Web Framework**: Flask
- **Dependencies**: Installed from `requirements.txt`

## Environment Variables

- `FLASK_APP`: Set to `app.py`
- **Port**: 5000 (exposed)

## MLFLOW Configuration

To configure MLFLOW, set the following environment variables:

```bash
# Bash
export MLFLOW_TRACKING_URI=https://dagshub.com/RisAhamed/MLFLOW.mlflow
export MLFLOW_TRACKING_USERNAME=RisAhamed
export MLFLOW_TRACKING_PASSWORD=822dabf3de2f482e09baa3a4dd7259fafbc8bda8

# Windows CMD or Conda
set MLFLOW_TRACKING_URI=https://dagshub.com/RisAhamed/MLFLOW.mlflow
set MLFLOW_TRACKING_USERNAME=RisAhamed
set MLFLOW_TRACKING_PASSWORD=822dabf3de2f482e09baa3a4dd7259fafbc8bda8
```

## Contributing

Feel free to submit issues and enhancement requests!

## License

[Add your license here]