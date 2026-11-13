# Full-Stack Web Technology (WT) Resume Project

**Student Name:** VASIYA. P  
**Semester:** 5th Semester  
**Course:** B.E. Computer Science & Engineering (Web Technology Lab)  

---

## 🏗️ Architecture Overview

This project is structured into clear **Front-End** and **Back-End** modules:

```
WT/
├── frontend/                     # Client-side presentation layer
│   ├── index.html                # Semantic HTML5 UI layout
│   ├── style.css                 # CSS3 styling (Flexbox, Grid, Print rules)
│   └── app.js                    # JavaScript ES6+ fetch API & DOM manipulation
├── backend/                      # Server-side business logic & data layer
│   ├── server.ps1                # Native Windows HTTP backend (zero install required)
│   ├── server.js                 # Node.js + Express REST API alternative
│   ├── package.json              # Node.js dependencies
│   ├── app.py                    # Python Flask alternative
│   └── data/
│       └── resume.json           # JSON Database (profile, skills, projects, messages)
├── start-server.bat              # 1-Click launcher to run backend & open frontend
└── README.md                     # Documentation
```

---

## 🎨 Front-End (Client Layer)
- **HTML5 (`frontend/index.html`)**: Semantic markup with structured sections (`<header>`, `<nav>`, `<aside>`, `<main>`, `<article>`, `<section>`, `<footer>`), edit modal, and interactive contact form.
- **CSS3 (`frontend/style.css`)**: Responsive layout utilizing CSS Grid and Flexbox, custom color tokens, modern typography (`Plus Jakarta Sans`), and `@media print` rules for clean PDF export.
- **JavaScript (`frontend/app.js`)**:
  - Asynchronously communicates with backend REST APIs via `fetch()`.
  - Dynamic client-side DOM rendering for skills, education, and full-stack projects.
  - Interactive section filters (Front-End, Back-End, Projects, Education, Contact).
  - Modal editor with `POST /api/resume` to update candidate details live.
  - Form validation with `POST /api/contact` to submit feedback to backend.

---

## ⚙️ Back-End (Server & API Layer)
- **REST API Endpoints**:
  - `GET /api/resume`: Returns JSON containing profile, skills, education, and projects.
  - `POST /api/resume` (or `PUT`): Receives updated resume payload and writes it to `backend/data/resume.json`.
  - `POST /api/contact`: Saves incoming inquiries and messages into `resume.json`.
  - `GET /api/health`: Health status probe for monitoring.
- **Server Implementations Provided**:
  1. **PowerShell Native (`backend/server.ps1`)**: Powered by .NET `System.Net.HttpListener`. Works right out of the box on Windows with zero setup.
  2. **Node.js Express (`backend/server.js`)**: Standard Node.js backend (`npm install && npm start`).
  3. **Python Flask (`backend/app.py`)**: Python backend option (`python app.py`).

---

## 🚀 How to Run

### Method 1: Instant 1-Click Launch (Recommended on Windows)
Double-click `start-server.bat`. It will start the backend server and open `http://localhost:3000` automatically in your browser.

### Method 2: Manual PowerShell Launch
Open PowerShell in the project directory and run:
```powershell
powershell -ExecutionPolicy Bypass -File .\backend\server.ps1
```
Then navigate to `http://localhost:3000` in your browser.

### Method 3: Node.js (If Node is installed)
```bash
cd backend
npm install
npm start
```
