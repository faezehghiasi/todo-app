# 📝 Flask To-Do App (Dockerized)

This is a simple To-Do web application built using **Flask** and containerized with **Docker**.

It provides basic task management with a Jinja2-rendered UI.  
This fork adds full Docker support for easy setup, testing, and portability.

---

## 🚀 Getting Started (with Docker Compose)

### 📦 Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

---

### 🛠 Steps to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/YOUR_USERNAME/todo-app.git
   cd todo-app
   ```

2. **Switch to the dockerized branch**:
   ```bash
   git checkout dockerize
   ```

3. **Build and run the containers**:
   ```bash
   docker-compose up --build
   ```

4. **Visit the app in your browser**:
   [http://localhost:5000](http://localhost:5000)

---

## 📁 Project Structure

```
.
├── app.py               # Main Flask application
├── db_create.py         # Database initializer
├── requirements.txt     # Python dependencies
├── templates/           # HTML templates (Jinja2)
├── docker/
│   └── Dockerfile       # Dockerfile for building the app image
├── docker-compose.yml   # Compose configuration
└── README.md            # You're reading it!
```

---

## 🐳 Docker Overview

| Component        | Description                                 |
|------------------|---------------------------------------------|
| Base Image       | `python:3.12-slim`                          |
| Web Server       | Flask's built-in development server        |
| App Port         | Exposes port `5000`                        |
| Dockerfile Path  | `./docker/Dockerfile`                     |
| Volume (optional)| `/app/data` (can be used for persistence)  |

> Note: The app listens on `0.0.0.0` inside the container to be accessible from host.

---

## 📌 Notes

- This setup is **intended for development/demo purposes**.
- For production deployment:
  - Replace `flask run` with `gunicorn` or `uWSGI`.
  - Use a production-ready WSGI server.
  - Configure environment variables and database security.

---

## 📄 License & Attribution

- Original project: [pj8912/todo-app](https://github.com/pj8912/todo-app)
- Dockerized and maintained by: [YOUR_USERNAME](https://github.com/YOUR_USERNAME)
