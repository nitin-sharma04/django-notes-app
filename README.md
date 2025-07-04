# 📝 Django Notes App (Dockerized)

A simple Django-based Notes Application with MySQL and Nginx, fully containerized using Docker Compose.

---

## 🔧 Features

- Create, update, and delete notes  
- User login and registration  
- MySQL database integration  
- Dockerized using multi-container setup  
- Nginx as reverse proxy  
- Environment variables support using `.env`  

---

## 🛠 Tech Stack

- Django  
- MySQL  
- Nginx  
- Docker & Docker Compose  

---

## 📁 Project Structure

```
.
├── backend/               # Django project and app
├── nginx/                 # Nginx config files
├── docker-compose.yml     # Docker orchestration file
├── Dockerfile             # Django Dockerfile
├── .env                   # Environment variables
└── mysql_data/            # MySQL volume (auto-created)
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/nitin0412/django-notes-app.git
cd django-notes-app
```

### 2. Create `.env` file

Make a `.env` file in the root folder:

```
DB_NAME=test_db
DB_USER=root
DB_PASSWORD=root
DB_HOST=db
```

### 3. Build and run containers

```bash
docker-compose up --build
```

App will be available at: [http://localhost](http://localhost)

---

## 🐳 Docker Services

| Service | Description        | Port |
|---------|--------------------|------|
| Django  | Web app backend     | 8000 |
| MySQL   | Database            | 3306 |
| Nginx   | Reverse proxy       | 80   |

---

## 📌 Notes

- Admin panel is available at `/admin/`
- You can customize settings in `backend/settings.py`
- Static files are handled by Nginx

---

## 📤 Deployment

You can also push this project to Docker Hub:

```bash
docker image tag django-notes-app nitin0412/django-notes-app
docker push nitin0412/django-notes-app
```

---

## 👨‍💻 Author

Made with ❤️ by [Nitin Sharma](https://github.com/nitin0412)
