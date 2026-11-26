
# MediVision

An AI-powered web application for kidney stone image classification built using Flask and TensorFlow.

## Overview

MediVision is a web application that accepts medical images and uses a trained deep learning model to classify kidney images. It also includes an admin dashboard for managing posts and a contact form with email functionality.

## Features

- Kidney image classification using a trained deep learning model
- Image upload and prediction interface
- Admin authentication
- Admin dashboard for post management
- Create, read, update, and delete posts (CRUD)
- Contact form with email integration
- MySQL database integration

## Tech Stack

- **Backend:** Python, Flask
- **Machine Learning:** TensorFlow, Keras
- **Database:** MySQL / MariaDB
- **Frontend:** HTML, CSS, JavaScript, Bootstrap
- **Email:** Flask-Mail
- **Image Processing:** Pillow

## Project Structure

```text
MediVision/
├── models/
│   └── kidney_model.h5
├── static/
│   ├── assets/
│   ├── css/
│   ├── img/
│   └── js/
├── templates/
├── orgapp.py
├── posts.sql
├── requirements.txt
├── .gitignore
├── .env.example
└── README.md
```

## Installation & Setup

### 1. Clone the repository

```bash
git clone <repository-url>
cd flaskapi
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```powershell
.\venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set up the database

- Start MySQL/MariaDB using XAMPP or another database server.
- Create the database `resourcesharing`.
- Import `posts.sql` using phpMyAdmin or the MySQL command line.

### 5. Configure environment variables

Create a `.env` file in the project root using `.env.example` as a template.

Configure your own:

- Gmail credentials
- Admin username and password
- Flask secret key

Do not commit `.env` or personal configuration files.

### 6. Run the application

```bash
python orgapp.py
```

Open in your browser:

```text
http://127.0.0.1:5000/
```

## Machine Learning Model

The application uses the trained model located at:

```text
models/kidney_model.h5
```

The model is loaded using TensorFlow/Keras for image classification.

## Disclaimer

This project is intended for educational purposes. Predictions are not medical diagnoses and should not replace professional medical advice or evaluation.
