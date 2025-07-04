
# 📚 Skillsberg ELMS - Language Learning Management System

![Skillsberg Logo](insert-your-logo-here.png)

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

📌 *[Insert Logical View Diagram here]*  
> `![Logical Architecture Diagram](./diagrams/logical-architecture.png)`

---

### 🔁 Behavioral View

This project contains 5 key UML Activity Diagrams:
1. Student Registration & Login
2. Course Enrollment
3. Instructor Adding Module
4. Password Update
5. Secure User Management

📌 *[Insert Sample Behavior Diagram]*  
> `![User Registration Flow](./diagrams/user-registration-activity.png)`

---

### 🧪 Design Patterns Used

- **SRP (Single Responsibility Principle)**: Isolated modules like `UserRepository`, `Authenticator`.
- **OCP (Open-Closed Principle)**: Interfaces for `ContentService`, `QuizHandler`, allowing extensions.

---

## 🧰 Detailed Component Designs

Each component adheres to best practices and encapsulation:

### 👤 User Registration (Class Diagram)
> `![User Registration UML](./diagrams/user-registration-class.png)`

### 📑 Content Design (Class Diagram)
> `![Content Design UML](./diagrams/content-design-class.png)`

---

## 🔐 Access Control & Security

- Authentication validates credentials.
- Authorization checks user roles for permissions.

> `![Access Control UML](./diagrams/auth-access-class.png)`

---

## 🧪 UML Sequence Diagrams

1. **User Registration**  
   `![Sequence - Registration](./diagrams/sequence-registration.png)`

2. **Content Creation**  
   `![Sequence - Content](./diagrams/sequence-content.png)`

3. **User Authentication**  
   `![Sequence - Auth](./diagrams/sequence-auth.png)`

4. **Course Enrollment**  
   `![Sequence - Enrollment](./diagrams/sequence-enrollment.png)`

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

> `![Deployment Diagram](./diagrams/deployment.png)`

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

---

## 📜 License

This project is licensed under the MIT License.

---

## 🤝 Acknowledgements

Thanks to our mentors and instructors at [Your University Name] for their support.

---
