# 🚧 SafeSite AI – AI-Powered Safety Compliance Monitoring System

SafeSite AI is a **FastAPI backend** that automates safety compliance monitoring for high-risk environments like construction sites, manufacturing plants, and industrial zones.  
It processes uploaded videos, detects whether workers are using proper **PPE (Personal Protective Equipment)**, and generates structured compliance reports using deep learning models.

---

## 🚀 Features

### 🔐 Authentication & Secure Access
- JWT-based login and token authentication  
- Role-based access control  
- Secure API endpoints  

### 📹 Video Upload & Processing
- Upload safety surveillance videos through REST API  
- Asynchronous background processing  
- Temporary and cloud storage support  

### 🧠 AI-Powered Violation Detection
- Detects PPE compliance:
  - Hard hats
  - Safety vests
  - Multiple violation types  
- Object detection model integration  
- Frame-wise and timestamp-based analysis  

### 📊 Structured Results & Reporting
- Time-stamped violation data  
- JSON-based structured API responses  
- Extendable for dashboards & analytics  

### ☁️ Cloud Storage Integration
- S3-compatible storage support  
- Secure file upload & retrieval  
- Scalable infrastructure design  

### 🛠 Modular & Scalable Architecture
- Clean FastAPI structure  
- Separation of concerns (auth, db, models, routes)  
- Production-ready backend foundation  

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| **Backend Framework** | FastAPI |
| **Language** | Python |
| **Database** | SQLite (Development) |
| **Validation** | Pydantic |
| **AI/ML** | Python Object Detection Model |
| **Cloud Storage** | AWS S3 / S3-compatible |
| **Server** | Uvicorn / Gunicorn |
| **Authentication** | JWT |

---

## 📁 Folder Structure

```plaintext
SafeSite_AI-Backend/
│
├── main.py                 # FastAPI entrypoint
├── auth.py                 # Authentication logic
├── crud.py                 # Database operations
├── models.py               # ORM models
├── schemas.py              # Pydantic schemas
├── deps.py                 # Dependency injection
├── database.py             # DB configuration
├── s3_client.py            # Cloud storage utilities
├── utils.py                # Helper functions
├── safesite_ai.db          # SQLite database
```

## 🧩 Module Overview

### 🔵 `main.py`
This is the main FastAPI application entry point.

**Responsible For:**
- Initializing the FastAPI app  
- Registering API routes  
- Configuring middleware and dependencies  
- Launching the backend server  

---

### 🔐 `auth.py`
Handles authentication and security mechanisms.

**Responsible For:**
- User authentication  
- JWT token generation  
- Token validation and protected routes  

---

### 📦 `crud.py`
Contains database interaction logic separated from route definitions.

**Responsible For:**
- Creating database records  
- Fetching and updating stored data  
- Maintaining clean separation of concerns  

---

### 🛠 `database.py`
Configures and manages the database connection.

**Responsible For:**
- Initializing database engine  
- Managing DB sessions  
- Connecting SQLite (development)  

---

### 📑 `schemas.py`
Defines structured request and response models using Pydantic.

**Responsible For:**
- Input validation  
- Response serialization  
- Data structure enforcement  

---

### ☁️ `s3_client.py`
Manages cloud storage integration.

**Responsible For:**
- Uploading videos to S3-compatible storage  
- Retrieving stored files  
- Handling secure storage access  

---

### 📌 `utils.py`
Contains reusable helper functions used across the application.

**Responsible For:**
- Utility operations  
- Model loading & preprocessing  
- Shared helper logic  

---

## 📡 API Endpoints (Example)

| Route | Method | Description |
|-------|--------|-------------|
| `/login` | POST | Authenticate user & receive JWT token |
| `/upload` | POST | Upload safety video for analysis |
| `/process` | POST | Trigger AI-based violation detection |
| `/results/{video_id}` | GET | Retrieve structured detection results |

---

## ▶️ Usage Instructions

### 1️⃣ Clone Repository
```bash
git clone https://github.com/MohdNazeeb/SafeSite_AI-Backend.git
cd SafeSite_AI-Backend