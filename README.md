# 🍼 DENNIBA – Maternal & Child Health Platform (Backend API)

## 📌 Project Overview

**DenNiBa** is a backend API designed to support Malian mothers throughout their maternal and child health journey.
It provides access to reliable health information, self-tracking tools, community support, and a directory of local healthcare services.

This project is developed as part of the **ALX Back-End Capstone Project**.

---

## 🚀 Features (MVP)

* **User & Profile Management**

  * Registration, login, and profile updates.

* **Health Education**

  * CRUD educational articles (pregnancy, nutrition, child development).

* **Health Tracking**

  * Store and retrieve health records (appointments, vaccinations, symptoms).

* **Community Support Forum**

  * CRUD posts and comments with categories.

* **Local Health Services Directory & Appointments**

  * Searchable directory of providers (clinics, pharmacies, gynecologists).
  * Appointment request and tracking.

---

## 🗂️ Project Structure

```
DenNiBa/
│── users/                 # User authentication & profiles
│── health_education/      # Educational articles
│── health_tracking/       # Health records
│── community_support/     # Forum posts & comments
│── service_directory/     # Providers & appointments
│── Den_Ba/  # Project settings & configs
│── manage.py
│── README.md
```

---

## 🛠️ Tech Stack

* **Backend Framework:** Django REST Framework (DRF)
* **Database:** PostgreSQL (can use SQLite for development)
* **Authentication:** Token-based (JWT)
* **Deployment (future):** Docker + Cloud (Heroku/AWS/Azure)

---

## 📖 API Endpoints (Version 1)

### Users

* `POST /api/users/register/` → Register a new user
* `POST /api/users/login/` → Login and get token
* `GET /api/users/me/` → Retrieve current user profile
* `PUT /api/users/me/` → Update current user profile

### Health Education

* `GET /api/education/articles/` → List articles
* `GET /api/education/articles/{id}/` → Get article details
* `POST /api/education/articles/` → Create article *(Admin/Expert only)*
* `PUT /api/education/articles/{id}/` → Update article *(Admin/Expert only)*
* `DELETE /api/education/articles/{id}/` → Delete article *(Admin/Expert only)*

### Health Tracking

* `POST /api/health_records/` → Add health record
* `GET /api/health_records/` → List user health records
* `GET /api/health_records/{id}/` → Get specific record
* `PUT /api/health_records/{id}/` → Update record
* `DELETE /api/health_records/{id}/` → Delete record

### Community Support

* `GET /api/forum/posts/` → List posts
* `POST /api/forum/posts/` → Create post
* `GET /api/forum/posts/{id}/` → Get post & comments
* `PUT /api/forum/posts/{id}/` → Update post *(Author only)*
* `DELETE /api/forum/posts/{id}/` → Delete post *(Author/Admin)*
* `POST /api/forum/posts/{post_id}/comments/` → Add comment

### Service Directory & Appointments

* `GET /api/services/providers/` → List providers
* `GET /api/services/providers/{id}/` → Get provider details
* `POST /api/services/appointments/` → Create appointment request
* `GET /api/services/appointments/` → List user appointments

---

## ⚡ Setup & Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/Den_Ba.git
   cd Den_Ba
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate   # Mac/Linux
   venv\Scripts\activate      # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply migrations**

   ```bash
   python manage.py migrate
   ```

5. **Create a superuser**

   ```bash
   python manage.py createsuperuser
   ```

6. **Run the server**

   ```bash
   python manage.py runserver
   ```

---

## ✅ Progress Tracking

* [x] ERD & API design
* [x] Django project setup
* [x] Models implementation
* [x] CRUD endpoints with DRF
* [ ] Authentication with JWT
* [ ] Unit tests
* [ ] Deployment

---

## 👨‍💻 Author

**Kalifa SENOU** – ALX Back-End Engineering Student (doc generete by AI)
