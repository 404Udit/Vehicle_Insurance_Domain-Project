

# 🚀 End-to-End MLOps Project: Vehicle Insurance Prediction System

> **A full-stack MLOps pipeline** that takes a machine learning model from raw data ingestion to production deployment using modern MLOps best practices, cloud services, CI/CD, and scalable architecture.


>🧩 Project Overview

This project is a Vehicle Insurance Prediction System that aims to predict whether a customer is likely to purchase vehicle insurance based on historical and behavioral data. The model uses customer and vehicle-related features such as Gender, Age, Driving License status, Region Code, Previous Insurance history, Annual Premium, Policy Sales Channel, Customer Vintage, Vehicle Age indicators, and Vehicle Damage history to estimate the probability of insurance uptake.

The objective of this system is to help insurance companies identify high-potential customers, optimize marketing strategies, and reduce operational costs by focusing outreach on users who are more likely to convert. By analyzing past customer behavior and vehicle conditions, the system transforms raw data into actionable insights that support data-driven decision-making.

The project is implemented as a production-ready machine learning pipeline, ensuring reliable data ingestion, validation, transformation, model training, evaluation, and deployment. Designed with real-world scalability in mind, the system supports automated retraining, consistent inference, and seamless integration into business workflows, making it suitable for enterprise-level insurance analytics and deployment.

---


This project demonstrates:

✔ Modular & scalable architecture
✔ Cloud-native (AWS + MongoDB Atlas)
✔ CI/CD with GitHub Actions & Docker
✔ End-to-end automation (Training → Evaluation → Deployment)
✔ Production-grade logging & exception handling

---

## 🧠 Tech Stack & Tools

### 🧩 Core Technologies

* **Python 3.10**
* **MongoDB Atlas** (Data source)
* **AWS (S3, ECR, EC2, IAM)**
* **Docker**
* **GitHub Actions (CI/CD)**

### 📦 MLOps Libraries

* NumPy, Pandas, Scikit-Learn
* PyYAML
* Logging & Exception handling
* Custom ML Pipelines

---

## 📁 Project Architecture

```bash
proj1/
│
├── src/
│   ├── components/          # Data Ingestion, Validation, Transformation, Trainer
│   ├── configuration/       # MongoDB & AWS connections
│   ├── entity/              # Config & Artifact entities
│   ├── cloud_storage/       # AWS S3 interaction
│   ├── data_access/         # MongoDB data fetch logic
│   ├── utils/               # Reusable utility functions
│
├── notebook/                # EDA & MongoDB demo notebooks
├── templates/               # HTML templates (Flask)
├── static/                  # Static assets
│
├── app.py                   # Prediction pipeline API
├── demo.py                  # Pipeline testing
├── Dockerfile
├── requirements.txt
├── pyproject.toml
├── setup.py
└── README.md
```

---

## ⚙️ Setup & Installation

### 1️⃣ Create Project Template

```bash
python template.py
```

---

### 2️⃣ Local Package Management

Configured using:

* `setup.py`
* `pyproject.toml`

📌 Enables importing project modules as a package.

---

### 3️⃣ Virtual Environment Setup



#### venv

```bash
python -m venv proj1
proj1\Scripts\activate
pip install -r requirements.txt
```

---

### 4️⃣ Verify Installation

```bash
pip list
```

---

## 🗄️ MongoDB Atlas Integration

✔ Cloud-hosted NoSQL database
✔ Secure environment variable usage

### Steps:

1. Create MongoDB Atlas account & project
2. Create **M0 Cluster**
3. Add DB user credentials
4. Allow network access: `0.0.0.0/0`
5. Copy **Python connection string**
6. Push dataset using Jupyter Notebook
7. Verify data via **Atlas → Browse Collections**

📁 Notebooks used:

* `mongoDB_demo.ipynb`
* `EDA & Feature Engineering.ipynb`

---

## 🧾 Logging & Exception Handling

✔ Centralized logging
✔ Custom exception classes
✔ Fully tested via `demo.py`

---

## 🔄 MLOps Pipeline Components

### ✅ Data Ingestion

* MongoDB → Pandas DataFrame
* Config-driven architecture
* Artifact & config entities

### ✅ Data Validation

* Schema validation via `schema.yaml`
* Missing values & data drift checks

### ✅ Data Transformation

* Feature engineering
* Preprocessing pipelines

### ✅ Model Trainer

* Modular estimator design
* Serialized model artifacts

---

## ☁️ AWS Integration (Model Registry)

### Services Used

* **S3** → Model storage
* **IAM** → Secure access
* **EC2** → Deployment server
* **ECR** → Docker image registry

Environment variables:

```bash
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
```

---

## 📊 Model Evaluation & Pusher

✔ Compare new model vs production model
✔ Threshold-based promotion logic
✔ Automatic S3 model push

---

## 🔮 Prediction Pipeline

* Flask-based API (`app.py`)
* `/predict` route for inference
* `/training` route for retraining

---

## 🐳 Docker & CI/CD (Production Ready)

### CI/CD Highlights

* Dockerized application
* GitHub Actions workflow
* Self-hosted EC2 runner
* Auto build → push → deploy

### Deployment Flow

```text
GitHub Commit
   ↓
GitHub Actions
   ↓
Docker Image Build
   ↓
AWS ECR
   ↓
EC2 Deployment
```

---


## 🎯 Key MLOps Concepts Demonstrated In this project are:

* Modular ML pipelines
* Artifact tracking
* Cloud model registry
* CI/CD automation
* Production inference API
* Secure credential management
* Scalable deployment


## 👤 Author

**Udit Srivastava**

