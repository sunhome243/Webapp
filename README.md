# The Hangman Game

## Project Description

Welcome to my very first project—a fully functional web application for the popular word game, Hangman. This application features a user-friendly front end built with JavaScript, CSS, and HTML, and a robust backend powered by Python. For containerization and orchestration, Docker and Minikube have been utilized. The application has been tested both in a local environment and within a Minikube setup.

## Technologies Used

- **Frontend:** JavaScript, CSS, HTML
- **Backend:** Python
- **Containerization:** Docker
- **Orchestration:** Minikube

## Setup Instructions

### Prerequisites

1. **Minikube:** Ensure Minikube is installed and running.
2. **Docker:** Ensure Docker is installed and running.

### Steps to Set Up

1. **Download the Code Files:**
   - Clone the repository or download the code files to your local machine.

2. **Create Docker Image:**
   - Navigate to the directory containing the Dockerfile.
   - Build the Docker image:
     ```bash
     docker build -t hangman-image .
     ```
   - Alternatively, you can load the pre-built image:
     ```bash
     docker load -i hangman-image.tar
     ```
     (Ensure the tar file is unzipped before running this command.)

3. **Deploy to Minikube:**
   - Apply the deployment configuration:
     ```bash
     kubectl apply -f deployment.yaml
     ```
     (Adjust the directory path if necessary.)
   - Verify that the pods are running:
     ```bash
     kubectl get pods
     ```

4. **Expose the Service:**
   - Apply the service configuration:
     ```bash
     kubectl apply -f service.yaml
     ```
   - Verify that the service is running:
     ```bash
     kubectl get service
     ```

5. **Access the Application:**
   - Start the Hangman service in Minikube:
     ```bash
     minikube service hangman-service
     ```
   - Minikube will automatically open the web browser, directing you to the Hangman game application.

Enjoy playing the Hangman game on your newly set up web application!
