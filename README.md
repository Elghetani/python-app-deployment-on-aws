# Patient Management System

## Overview

The Patient Management System is a web application built using Python and Django framework. It allows users to manage patient information by registering new patients and searching for existing ones. The system is deployed as a containerized application using Kubernetes for high availability, with a Django database backend. Continuous integration and deployment are automated using GitHub Actions. This README provides information on how to set up, deploy, and use the system.

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





