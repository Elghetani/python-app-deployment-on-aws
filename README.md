# Patient Management System

## Overview

The Patient Management System is a web application built using Python and Django framework. It allows users to manage patient information by registering new patients and searching for existing ones. The system is deployed as a containerized application using Kubernetes for high availability, with a Django database backend. Continuous integration and deployment are automated using GitHub Actions. This README provides information on how to set up, deploy, and use the system.

C:\Users\abdlw\OneDrive\Desktop\ezgif-3-a0cae994e8.gif

## Prerequisites

- Python 3.x
- Django 3.x
- Docker
- Kubernetes
- AWS EC2
- GitHub repository

## Setup

1. Clone the repository:
```
git clone https://github.com/your-repo/patient-management-system.git
cd patient-management-system
```

2. Create a virtual environment and activate it:
```
python3 -m venv venv
source venv/bin/activate
```
3. Install dependencies:
```
pip install -r requirements.txt
```
4. Run database migrations:
```
python manage.py migrate
```

## Deployment

### Docker Container

1. Build the Docker image:
```
docker build -t patient-management-system .

```

2. Run the Docker container:
```
docker run -d -p 8000:8000 patient-management-system
```

### Kubernetes Deployment

1. Make sure you have a Kubernetes cluster set up and configured.

2. Apply the Kubernetes deployment and service files:

```
kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml
```

## GitHub Actions

Continuous integration and deployment are automated using GitHub Actions. The workflow is defined in `.github/workflows/main.yml`. It includes steps to build the Docker image, push it to a container registry, and deploy the application to Kubernetes.

## Usage

1. Access the application through the web browser or using the provided endpoint (e.g., `http://localhost:8000`).

2. Register a new patient by providing the required information.

3. Search for existing patients by entering their details or using the search functionality provided.

## High Availability

The system is deployed with a Kubernetes deployment configured for high availability. It uses a replicaset with three replicas to ensure redundancy and fault tolerance. In case of any failures, Kubernetes automatically manages the replicas to maintain the desired state.

## AWS EC2

The system can be deployed on AWS EC2 instances for scalability and reliability. Ensure that you have the necessary permissions and security groups configured to access the EC2 instances and deploy the Kubernetes cluster.

## Contributing

Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request on GitHub.





