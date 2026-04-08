# MediSafe Healthcare Platform

![Status](https://img.shields.io/badge/Status-Completed-success) ![License](https://img.shields.io/badge/License-MIT-blue) ![Tech](https://img.shields.io/badge/Stack-PERN-orange)

An online medical appointment management platform designed to standardize the workflow of booking medical appointments and managing user information. This system was developed as part of the **Programming Integration Project (CO3103)** at the Faculty of Computer Science and Engineering, **Ho Chi Minh City University of Technology (HCMUT)**.

The platform serves three distinct user roles: **Patients**, **Doctors**, and **Administrators**, providing secure, stable, and scalable RESTful APIs along with a responsive Single Page Application (SPA) interface.

---

## 🌟 Key Features

### For Patients
* **Account Management:** Secure registration, login, and profile management.
* **Appointment Booking:** Search for doctors by department/specialty and book available time slots.
* **History Tracking:** View medical history and track appointment statuses (pending, confirmed, completed, cancelled).

### For Doctors
* **Schedule Management:** Define available time ranges and add, update, or remove working intervals.
* **Patient Management:** View daily appointment schedules, update appointment statuses, and write medical reports for completed visits.

### For Administrators
* **System Administration:** Manage user accounts, including creating, editing, or deleting doctor profiles.
* **Department Configuration:** Manage hospital departments, medical specialties, and overall system settings.

---

## 🏗️ System Architecture

The project is built on a highly scalable **Three-Tier Architecture**, ensuring clean separation of concerns:

1.  **Presentation Layer (Frontend):** A dynamic Single Page Application built with **React.js** and styled with **Tailwind CSS**.
2.  **Application Layer (Backend):** A RESTful API built with **Node.js** and **Express.js**, featuring modular routes for authentication, user management, and core booking logic.
3.  **Data Layer:** Hosted on **Supabase**, utilizing a **PostgreSQL** relational database and Supabase Storage for secure file and medical report uploads.

### Security & Authentication
* Custom authentication flow using **bcrypt** for secure password hashing.
* Stateless session management enforced via **JSON Web Tokens (JWT)**.
* **Role-Based Access Control (RBAC)** middleware (`authMiddleware`) to securely restrict endpoints based on user roles.

---

## 🚀 Getting Started

### Prerequisites
* **Node.js** (v16 or higher recommended)
* **npm** or **yarn**
* A **Supabase** project with the PostgreSQL database configured

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/VAENeverDle/DATH.git](https://github.com/VAENeverDle/DATH.git)
    cd DATH
    ```

2.  **Backend Setup:**
    ```bash
    cd backend
    npm install
    # Create a .env file and add your Supabase connection strings and JWT secrets
    npm run dev
    ```

3.  **Frontend Setup:**
    ```bash
    cd ../frontend
    npm install
    # Create a .env file and add your backend API URL
    # e.g., REACT_APP_API_URL=http://localhost:4000
    npm start
    ```

---

## 🧪 Testing

The backend business logic and API endpoints are fully tested using **Jest** and **Supertest**. The test suites utilize mocked environments (Supabase, bcrypt, JWT) to ensure isolated verification of authentication rules, appointment logic, and middleware enforcement.

* **Test Results:** 10 test suites, 41 tests passed successfully (0 failures).

**To run the test suite:**
```bash
cd backend
npm test
