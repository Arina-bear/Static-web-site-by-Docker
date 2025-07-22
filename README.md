# Static-web-site-by-Docker+Django+PostgreSQL
------------------------------
The focus of this project is specifically on gaining experience in backend development.The frontend remains primitive.
To secure database queries, it is also worth developing an API.
---------------------------
✨ Features

-User Authentication – Sign up, login, and profile management
- Posts – Create, edit, and delete blog posts
- Comments – Discuss posts with threaded replies
- Image Uploads – Add images to posts (via Pillow)
- Responsive Design – Works on mobile & desktop

Built with:

Backend: Django + PostgreSQL
Frontend: HTML/CSS, Bootstrap
Deployment: Docker-ready

📦 Backend (Django)
Service: web (main application)
Role: Request handling, API, page rendering
Technologies:
Django (Python framework)
Gunicorn (WSGI server for production)
Pillow (image processing)

🗃 Database (PostgreSQL)
Service: db
Role: Data storage (posts, comments, users)
Configuration:
Login/password: postgres (configured in docker-compose.yml)
Automatic volume creation for data persistence

🖥 Frontend (optional)
HTML/CSS

How It Works:

web Service:
Built from Dockerfile (with Python dependencies installed)
Mounts code volume for hot-reload during development
Uses Gunicorn to run Django in production

db Service:
Uses the official PostgreSQL 13 image
Data persists in postgres_data volume (survives container restarts)

Volumes:
postgres_data – stores database files
static_volume – shared volume for static files (CSS/JS)

Structure
<img width="368" height="144" alt="image" src="https://github.com/user-attachments/assets/7570d32f-f117-4f2c-8535-76adc0f11c6c" />

<img width="202" height="416" alt="image" src="https://github.com/user-attachments/assets/81be0dd4-aa12-4023-9749-f3c5c14bebf9" />

<img width="200" height="258" alt="image" src="https://github.com/user-attachments/assets/96d3a6bf-7d1b-4bd0-b10a-ae58f320b12e" />

<img width="183" height="82" alt="image" src="https://github.com/user-attachments/assets/ce4d46f5-b200-4d49-876a-0b841e8fdc64" />

Design

<img width="460" height="254" alt="image" src="https://github.com/user-attachments/assets/ab4b42c1-41d8-4727-9756-425d86dbd5f5" />

<img width="1198" height="499" alt="image" src="https://github.com/user-attachments/assets/30186b76-d665-4bf4-a3bd-75c755f6e5df" />


Commands for building docker containers

1. docker-compose build
2. docker-compose up -d
3. docker-compose exec web python manage.py makemigrations
4. docker-compose exec web python manage.py migrate
5. docker-compose exec web python manage.py createsuperuser


Creating an user by superuser
1.Users--->2.username-->3.password


<img width="1191" height="344" alt="image" src="https://github.com/user-attachments/assets/e47c8652-a48e-4af3-a687-50b46d97f3cb" />

2.-3.

<img width="871" height="471" alt="image" src="https://github.com/user-attachments/assets/81c2c97c-cdd7-4623-895c-3d274b5c7060" />







