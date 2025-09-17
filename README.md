# ToothTone – Dental Management System

This repository contains the **Graduation Project – ToothTone**, an **AI-integrated Dental Management System**.  
It includes both **Frontend** and **Backend** components, designed to streamline dental operations, support hands-free charting, and manage clinical data efficiently.

---

## 🌟 Key Features
- **AI-Powered Voice Recognition:** Hands-free periodontal charting using a fine-tuned Whisper Small model.
- **Comprehensive Management:** Appointments, Patients, Prescriptions, Attendance, and Analytics dashboards.
- **Role-Based Access:** Doctors, Managers, Patients, and Staff have tailored interfaces and permissions.
- **Modern Tech Stack:** React Frontend + ASP.NET Web API Backend + SQL Server.

---

## 🛠️ Tech Stack Overview

| Layer         | Technology                                          |
|---------------|-----------------------------------------------------|
| **Frontend**  | HTML, CSS, JavaScript, React                         |
| **Backend**   | ASP.NET Web API (C#), Entity Framework Core          |
| **Database**  | SQL Server                                           |
| **Real-Time** | WebSocket for voice recognition                      |
| **Tools**     | Swagger/OpenAPI for API testing & docs               |

---

## 🎨 Frontend Overview
The **Frontend** is built using **HTML, CSS, JavaScript, and React** to create a clean, modular, and responsive user interface.

### Structure & Styling
- HTML + CSS with Flexbox and Grid for responsive layouts.
- React component-based architecture with JSX for seamless UI logic.
- React Hooks for state and side-effect management.
- Server-side rendering applied where needed for SEO and performance.

### Periodontal Chart
- Built with **Canvas** (for high-performance rendering) and **SVG** (for interactive labels and selections).
- Efficient rendering with clear, scalable visuals.

---

## 🗂️ Backend Overview
The **Backend** is built using **ASP.NET Web API (C#)** with **Entity Framework Core** to manage all clinical data and system logic.

### Architecture
- Controllers handle logic and API requests.
- Models represent data entities.
- SQL Server stores structured clinical and user data.
- RESTful APIs are stateless, making the backend easier to scale.
- Database indexing improves response times for frequent queries.
- Swagger is integrated for API testing and live documentation.

### Real-Time Speech Recognition
- WebSocket support for hands-free dental charting.
- Fine-tuned Whisper Small model transcribes voice input into structured JSON.
- React UI reads JSON and updates the periodontal chart instantly.

---

## 🔗 Key API Endpoints

| Endpoint                               | Purpose                                  |
|----------------------------------------|------------------------------------------|
| **Appointments**                       |                                          |
| GET /api/Appointments                  | Fetch all appointments                   |
| POST /api/Appointments                 | Create new appointments                  |
| PUT /api/Appointments/{id}             | Update existing appointment              |
| DELETE /api/Appointments/{id}          | Delete appointment                       |
| **Doctors**                            |                                          |
| GET /api/Doctors                       | Get list of doctors                      |
| POST /api/Doctors                      | Add a new doctor (Manager only)          |
| **Patients**                           |                                          |
| GET /api/Patients                      | Retrieve all patient records             |
| POST /api/Patients                     | Add a new patient                        |
| PUT /api/Patients/{id}                 | Update patient info                      |
| **Prescriptions**                      |                                          |
| GET /api/Prescriptions                 | View prescriptions                       |
| POST /api/Prescriptions                | Create new prescription                  |
| **Bookings**                           |                                          |
| PUT /api/Bookings/{id}/status          | Update booking status                    |
| **Attendance**                         |                                          |
| GET /api/Attendance                    | View staff attendance                    |
| POST /api/Attendance                   | Record attendance entry                  |
| **Dashboard**                          |                                          |
| GET /api/Dashboard/stats/{doctorId}    | Fetch analytics for a specific doctor    |

---

## 🔐 Data Management & Security
- **Authentication & Authorization:** Role-based access control for doctors, managers, patients, and staff.
- **Data Encryption at Rest:** Sensitive information stored securely in SQL Server.
- **Healthcare Privacy Compliance:** Security measures align with healthcare data standards.

---

## 🧪 Deployment & Testing
- Tested in real-world conditions including multiple accents, background noise, and live voice interactions.
- Verified real-time performance of WebSocket connection between backend and frontend.
- Validated stability of RESTful APIs in the .NET backend.
- Deployed on a secure server setup supporting multiple user roles simultaneously.

---

## 🚀 Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/YourUsername/ToothTone-GradProj.git
cd ToothTone-GradProj
````

### 2. Frontend Setup

```bash
cd frontend
npm install
npm start
```

The React app will run at `http://localhost:3000`.

### 3. Backend Setup

```bash
cd backend
dotnet restore
dotnet ef database update
dotnet run
```

The API will be available at `https://localhost:5001` with Swagger UI at `/swagger`.

---

## 👩‍💻 Contributors

* **Reem Ahmed** – Lead Developer (Frontend & Backend)
