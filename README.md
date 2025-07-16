# NeuroScan - AI-Powered Brain Tumor Detection System

![NeuroScan Logo](https://via.placeholder.com/150x50?text=NeuroScan) 
*(Add your actual logo image here)*

## Overview

NeuroScan is an advanced medical diagnostic tool that uses artificial intelligence to detect brain tumors in MRI scans. This system provides healthcare professionals with a fast, accurate, and user-friendly interface for analyzing patient MRI images and generating comprehensive diagnostic reports.

## Key Features

- **AI-Powered Analysis**: Utilizes a trained VGG19 deep learning model for accurate tumor detection
- **Patient Management**: Complete patient information tracking and record-keeping
- **Secure Access**: Professional login system with security measures
- **Interactive Dashboard**: User-friendly interface for uploading and analyzing scans
- **Report Generation**: Automatic PDF report generation with patient details and results
- **Database Integration**: MySQL database for storing patient records and scan results

## Technology Stack

### Frontend
- HTML5, CSS3, JavaScript
- Animate.css for animations
- Font Awesome for icons
- html2pdf.js for PDF generation
- Poppins Google Font

### Backend
- Python with Flask framework
- Flask-CORS for cross-origin requests
- MySQL database
- TensorFlow/Keras for machine learning

### Image Processing
- OpenCV for image preprocessing
- NumPy for numerical operations

## System Architecture
NeuroScan/
├── frontend/ # Web interface
│ ├── login.html # Medical professional login
│ ├── Dashboard.html # Main application interface
│ ├── report.html # Report generation page
│ ├── style.css # Main stylesheet
│ └── login_css.css # Login page styles
├── backend/
│ ├── app.py # Flask application
│ └── vgg19_model_03.h5 # Trained ML model
├── database/ # Database scripts
└── README.md # This file

text

## Installation Guide

### Prerequisites
- Python 3.8+
- MySQL Server
- Node.js (for development)

### Backend Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/NeuroScan.git
   cd NeuroScan/backend
Create and activate a virtual environment:

bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:

bash
pip install flask flask-cors tensorflow opencv-python mysql-connector-python
Set up MySQL database:

Create a database named BrainTumorDB

Update the db_config in app.py with your MySQL credentials

Run the Flask application:

bash
python app.py
Frontend Setup
The frontend files can be served from any web server. For development:

bash
cd ../frontend
python -m http.server 8000
Access the application at http://localhost:8000/login.html

Usage Instructions
Login: Medical professionals log in using secure credentials

Username: abc

Password: abc@123

Patient Information: Enter patient details including:

Full name

Phone number

Age

Blood type

MRI Upload: Drag and drop or browse to upload an MRI scan image

Analysis: Click "Analyze MRI Scan" to process the image

Results: View the tumor detection results with confidence level

Report: Generate and download a PDF report with all patient information

Security Features
Right-click and developer tools disabled

Rate limiting for login attempts (5 attempts per minute)

Session timeout after 5 minutes of inactivity

Password complexity requirements

Secure content policies (CSP)

CSRF token protection

API Endpoints
POST /predict - Process MRI image and return tumor detection results

Required form data:

file: MRI image file

name: Patient name

phn: Patient phone number

age: Patient age

bloodType: Patient blood type
