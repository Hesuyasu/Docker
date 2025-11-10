# 🌐 PSUSphere

![Python](https://img.shields.io/badge/Python-3.9+-blue?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-4.x-green?logo=django&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen)

> A Django-powered student organization management system designed for efficiency, scalability, and simplicity.

---

## ✨ Features

- 🏫 Manage **Colleges & Programs**  
- 🧑‍🤝‍🧑 Track **Organizations & Members**  
- ➕ Add **Students & Organization Memberships**  
- 🎲 Generate **Fake Data** using Faker for testing  
- ⚡ Enhanced **Django Admin Panel** with Search & Filters  

---

## Developed with ❤️ by
- [Edrian A. Bantog]
- GitHub: https://github.com/hesuyasu
- [Calaisha Mae S. Ducao]
- GitHub: https://github.com/PsychoQuake7

# Django Docker Project

This project containerizes a Django web application using Docker to provide a consistent and portable development environment.

## Prerequisites

- Install Docker Desktop: https://www.docker.com/products/docker-desktop
- (Optional) Create a Docker Hub account to share images: https://hub.docker.com/signup
- (Optional) Python 3.x and virtual env if working locally without Docker

## Setup Instructions

1. **Clone this repository:**
git clone https://github.com/yourusername/projectsite.git
cd projectsite

2. **Create `requirements.txt`** (if not already present):
pip freeze > requirements.txt

This file should list your project's Python dependencies.

3. **Review Dockerfile for environment variable syntax:**

Make sure `ENV` declarations are in the format:
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

4. **Build your Docker image:**
docker build -t my-django-applatest .

5. **Run Docker containers with Docker Compose:**
docker-compose up

Your Django app will be accessible at [http://localhost:8000](http://localhost:8000).

## Common Docker Commands

- Run migrations inside the container:
docker-compose exec web python manage.py migrate

- Create a superuser:
docker-compose exec web python manage.py createsuperuser

- Collect static files for production:
docker-compose exec web python manage.py collectstatic --noinput

- Run tests:
docker-compose exec web python manage.py test

- Stop containers:
docker-compose down

## Troubleshooting

- Make sure `requirements.txt` is in the root folder when building.
- Use modern `ENV` syntax as shown above to avoid Docker warnings.
- Check Docker and Docker Compose versions are up-to-date.
- If build or run fails, try:
docker system prune

## Pushing Docker Image to Docker Hub

1. Login to Docker Hub:
docker login

2. Tag your image:
docker tag my-django-applatest yourusername/django-applatest:latest

3. Push image:
docker push yourusername/django-applatest:latest

## Deploying to Another Machine

1. Pull the image on the target computer:
docker pull yourusername/django-applatest:latest

2. Run using a `docker-compose.yml` referencing the image.

3. Run migrations and other setup commands as needed.
