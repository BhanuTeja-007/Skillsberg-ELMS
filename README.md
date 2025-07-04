
# 📚 Skillsberg ELMS - Language Learning Management System


## 🚀 Overview

**Skillsberg ELMS (E-Learning Management System)** is a robust web-based platform focused on helping learners acquire new languages efficiently and effectively. Built as part of an academic capstone project, Skillsberg combines modular software architecture with rich feature sets like course management, content creation, quizzes, and progress tracking.

The platform is engineered with a **microservices-inspired modular structure**, integrated with **Firebase (NoSQL)** for real-time capabilities, and deploys on **Google Cloud Platform (GCP)** for scalable delivery.

---

## 🎯 Key Features

- 🧑‍🎓 **User Management**: Seamless registration, login, profile editing, and role-based dashboard.
- 📚 **Course Catalog & Enrollment**: Browse and enroll in language courses with structured modules.
- 📝 **Quiz & Assignment Management**: Auto-grading, manual grading, submission tracking.
- 💬 **Messaging & Support**: In-app messaging and support ticketing system.
- 🛡️ **Authentication & Access Control**: Role-based access (Student, Instructor, Admin).
- 📊 **Progress Tracking**: Track learning scores, submissions, and grades in real time.

---

## 🧱 Tech Stack

| Layer        | Technologies Used         |
|--------------|---------------------------|
| Frontend     | React.js                  |
| Backend      | Node.js + Firebase SDK    |
| Database     | Firebase Realtime DB      |
| Hosting      | GCP                       |
| Auth & Sec   | Username & Password       |
| CMS          | Custom-built              |

---

## 🧠 Architecture Overview

Skillsberg’s architecture is designed around modular responsibilities and follows key software design principles like **SRP** and **OCP** for maintainability and extensibility.

### ⚙️ Logical View

Each subsystem is defined by responsibility and interface:

- **User Management** → Register/Login/Profile
- **Content Design** → Create & Manage Learning Modules
- **Course Catalog** → Enroll/View Courses
- **Quiz/Assignment** → Upload, Submit, Grade
- **Dashboard** → Role-specific views and analytics

![Architecture Logical View](https://github.com/user-attachments/assets/bdf4b0e7-3328-4f15-a20b-424afbe9016e)

---

### 🔁 Behavioral View

This project contains 5 key UML Activity Diagrams:
1. Student Registration & Login
2. Course Enrollment
3. Instructor Adding Module
4. Password Update
5. Secure User Management

![Architecture Behavior View](https://github.com/user-attachments/assets/9c6751ef-76fe-4022-9581-5280bc39e851)

---

### 🧪 Design Patterns Used

- **SRP (Single Responsibility Principle)**: Isolated modules like `UserRepository`, `Authenticator`.
- **OCP (Open-Closed Principle)**: Interfaces for `ContentService`, `QuizHandler`, allowing extensions.

---

## 🧰 Detailed Component Designs

Each component adheres to best practices and encapsulation:

### 👤 User Registration (Class Diagram)
> ![User Registration - Class Diagram](https://github.com/user-attachments/assets/4c7e186b-fc9b-4f4d-a90a-4b281e325caa)


### 📑 Content Design (Class Diagram)
> ![image](https://github.com/user-attachments/assets/04adaec4-f8b8-43fc-b3df-c0c6441d5c15)

---

## 🔐 Access Control & Security

- Authentication validates credentials.
- Authorization checks user roles for permissions.

> ![Access Control and Security - Class Diagram](https://github.com/user-attachments/assets/5c552094-7b8b-434e-a897-e0e4042e0b7a)


---

## 🧪 UML Sequence Diagrams

1. **User Registration**  
   ![User Registration - Sequence Diagram](https://github.com/user-attachments/assets/5f57c6bf-0a10-4955-93e8-0ed5e323d1ca)


2. **Content Creation**  
   ![Content Management - Seq Design](https://github.com/user-attachments/assets/e3b29ffa-eada-4deb-9950-6a9020e83157)


3. **User Authentication**  
   ![image](https://github.com/user-attachments/assets/4886094e-e5c1-43bc-bf44-b6267d4d88e6)


4. **Course Enrollment**  
   ![image](https://github.com/user-attachments/assets/f3d833f2-1776-475d-9c09-85b87ca0c581)


---

## 🗂️ Firebase Data Models

### 👩‍🏫 Instructor Model

```json
{
  "id": "string",
  "name": "string",
  "courses": ["courseId1", "courseId2"],
  "profileImage": "url",
  "bio": "string",
  "email": "string",
  "phoneNo": "string"
}
```

### 👨‍🎓 Student Model + Subcollections

- `/students/{id}`
- `/students/{id}/courses/{courseId}/quizzes`
- `/students/{id}/courses/{courseId}/assignments`

### ❓ Questions

- Supports MCQ, Numerical, Subjective types

---

## ⚙️ Deployment Architecture

> ![image](https://github.com/user-attachments/assets/d827d8df-c0c6-4122-9314-faff370561d1)


---

## 📍 Responsibilities by Team Members

| Name                  | Modules Owned                                       |
|-----------------------|-----------------------------------------------------|
| Bhanu Teja Panguluri  | Auth, Course Design, Database, Quizzes              |
| Revanth Maturu        | Messaging, Assignments, Testing                     |
| Sai Pranathi Vadrevu  | User Support, Enrollment, Testing                   |
| Sudhanshu Dubey       | Dashboard, Grading                                  |
| Tarang Nair           | User Registration, Content Design, Course Catalog   |

---

## ✅ Setup Instructions

1. Clone the repository
```bash
git clone https://github.com/your-username/skillsberg-elms.git
```
2. Install dependencies
```bash
npm install
```
3. Add your Firebase config in `/config/firebase.js`

4. Start the development server
```bash
npm start
```

---

## 📌 Future Enhancements

- 🌍 Multilingual support
- 📈 Advanced analytics for instructors
- 🤖 AI-based quiz recommendations
- 🧩 SCORM compatibility


