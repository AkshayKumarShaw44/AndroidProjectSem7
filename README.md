# 🎓 Centralized Campus Event Discovery & Reminder App

<p align="center">
  <img src="https://img.shields.io/badge/Android-Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" />
  <img src="https://img.shields.io/badge/Jetpack%20Compose-UI-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" />
  <img src="https://img.shields.io/badge/Material%203-Design-6750A4?style=for-the-badge&logo=materialdesign&logoColor=white" />
  <img src="https://img.shields.io/badge/MERN-Stack-3FA037?style=for-the-badge&logo=mongodb&logoColor=white" />
</p>

<p align="center">
  <strong>A centralized platform that helps students discover, track, save, and never miss important campus events.</strong>
</p>

<p align="center">
  📅 Events &nbsp; • &nbsp;
  🔔 Smart Reminders &nbsp; • &nbsp;
  🔍 Discovery &nbsp; • &nbsp;
  ❤️ Bookmarks &nbsp; • &nbsp;
  📱 Android &nbsp; • &nbsp;
  ☁️ MERN Backend
</p>

---

## 📌 About The Project

**Centralized Campus Event Discovery and Reminder App** is a full-stack mobile application designed to solve a common problem in colleges and universities: **campus event information is scattered across multiple platforms.**

Students often discover events through WhatsApp groups, Instagram, emails, notice boards, department announcements, and student clubs. Because information is distributed across different channels, students can easily miss important events.

This project brings campus events into **one centralized platform** where students can:

* 🔍 Discover upcoming campus events
* 📅 View complete event information
* ❤️ Save interesting events
* 🔔 Receive reminders before events
* 🏷️ Filter events by category
* 🔎 Search for specific events
* 📍 Find event venues
* 📲 Register for events
* 🔗 Share events with other students

The system consists of a **modern Android application** powered by a **MERN-based backend**.

---

# ✨ Core Features

### 🎓 Student Features

* 🔐 Secure user authentication
* 👤 Student profile
* 🔍 Search events
* 🏷️ Category-based filtering
* 📅 Upcoming events
* 📖 Event details
* ❤️ Bookmark/save events
* 🔔 Event reminders
* 📲 Push notifications
* 📍 Event venue information
* 📝 Event registration
* 🔗 Share events
* 🕒 Event history

### 🏢 Organizer Features

* 🔐 Organizer authentication
* ➕ Create events
* ✏️ Update events
* 🗑️ Delete events
* 📊 Manage registrations
* 👥 View registered students
* 🔔 Notify participants
* 📈 Event participation insights

### 🔔 Reminder System

Students can save events and configure reminders.

The application can notify users:

* Before the event starts
* On the event day
* For important event updates
* When event information changes

---

# 🏗️ System Architecture

```text
                    ┌─────────────────────────┐
                    │      Student / Admin    │
                    └────────────┬────────────┘
                                 │
                                 ▼
              ┌────────────────────────────────────┐
              │       Android Mobile Application   │
              │                                    │
              │     Kotlin + Jetpack Compose       │
              │                                    │
              │  UI → ViewModel → Repository      │
              └────────────────┬───────────────────┘
                               │
                         REST API / JSON
                               │
                               ▼
              ┌────────────────────────────────────┐
              │          Node.js + Express         │
              │                                    │
              │        Authentication              │
              │        Business Logic              │
              │        Event Management             │
              │        Notifications               │
              └────────────────┬───────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       MongoDB       │
                    │                     │
                    │ Users               │
                    │ Events              │
                    │ Registrations       │
                    │ Bookmarks            │
                    │ Notifications        │
                    └─────────────────────┘
```

---

# 🛠️ Tech Stack

## 📱 Android Application

| Technology                      | Purpose                         |
| ------------------------------- | ------------------------------- |
| **Kotlin**                      | Primary programming language    |
| **Jetpack Compose**             | Modern declarative UI           |
| **Material 3**                  | UI components & design system   |
| **Navigation Compose**          | Screen navigation               |
| **ViewModel**                   | UI state & business logic       |
| **StateFlow / Flow**            | Reactive state management       |
| **Coroutines**                  | Asynchronous programming        |
| **Repository Pattern**          | Data abstraction                |
| **MVVM**                        | Application architecture        |
| **Retrofit**                    | REST API communication          |
| **OkHttp**                      | Network layer                   |
| **Gson / Kotlin Serialization** | JSON serialization              |
| **Coil**                        | Image loading                   |
| **DataStore**                   | Local preferences/token storage |
| **WorkManager**                 | Background tasks                |
| **Notification API**            | Event reminders                 |

---

# 🌐 Backend — MERN Stack

## 🍃 MongoDB

Used as the primary NoSQL database.

Stores:

* 👤 Users
* 📅 Events
* ❤️ Bookmarks
* 📝 Registrations
* 🔔 Notifications
* 🏢 Organizations
* 🏷️ Categories

---

## 🚂 Express.js

Used to build the RESTful API layer.

Responsibilities:

* API routing
* Authentication
* Authorization
* Request validation
* Error handling
* Middleware
* Event management
* User management

---

## 🟢 React.js

React can be used for the **Admin / Organizer Dashboard**.

The dashboard allows organizers and administrators to:

* Create events
* Update events
* Delete events
* Manage registrations
* View event statistics
* Manage users
* Send notifications

---

## 🟩 Node.js

Node.js powers the backend runtime.

Responsibilities:

* API execution
* Server-side business logic
* Authentication
* Database communication
* Real-time services
* Notification processing

---

# 🔐 Authentication & Security

The application will implement secure authentication using:

* 🔑 JWT Authentication
* 🔒 Password hashing
* 🛡️ Protected API routes
* 👤 Role-based authorization
* 🚦 Rate limiting
* 🌐 CORS configuration
* 🧹 Input validation
* 🔐 Secure environment variables
* 🛡️ Helmet security middleware

Example roles:

```text
STUDENT
ORGANIZER
ADMIN
```

---

# 📂 Project Structure

```text
Centralized-Campus-Event-App/
│
├── 📱 android/
│   ├── app/
│   │   └── src/
│   │       └── main/
│   │           ├── java/
│   │           │   └── com.campus.events/
│   │           │       ├── data/
│   │           │       ├── domain/
│   │           │       ├── presentation/
│   │           │       ├── navigation/
│   │           │       ├── utils/
│   │           │       └── MainActivity.kt
│   │           │
│   │           └── res/
│   │
│   └── build.gradle.kts
│
├── 🌐 web-admin/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── hooks/
│   │   ├── services/
│   │   └── utils/
│   │
│   └── package.json
│
├── ⚙️ backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── services/
│   ├── utils/
│   ├── config/
│   └── server.js
│
├── 📄 README.md
└── .gitignore
```

---

# 🧠 Android Architecture

The Android application follows **MVVM + Repository Architecture**.

```text
┌─────────────────────────┐
│       Compose UI        │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│       ViewModel         │
│                         │
│ UI State                │
│ Business Logic          │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│       Repository        │
└────────────┬────────────┘
             │
       ┌─────┴─────┐
       ▼           ▼
   Retrofit     DataStore
       │
       ▼
   REST API
       │
       ▼
   MERN Backend
```

---

# 🔄 Application Flow

```text
User Opens App
       │
       ▼
Authentication
       │
       ▼
Home Screen
       │
       ├──────────────► Search Events
       │
       ├──────────────► Filter Events
       │
       ├──────────────► View Event
       │                    │
       │                    ├──► Register
       │                    ├──► Bookmark
       │                    └──► Set Reminder
       │
       ▼
Saved Events
       │
       ▼
Reminder / Notification
       │
       ▼
Attend Event 🎓
```

---

# 🔔 Notification System

The reminder system is one of the core features of the application.

```text
Event Created
      │
      ▼
Event Date & Time Stored
      │
      ▼
Student Saves Event
      │
      ▼
Reminder Scheduled
      │
      ▼
Background Processing
      │
      ▼
🔔 Notification
      │
      ▼
Student Attends Event
```

---

# 🗄️ Database Design

### User

```text
User
├── _id
├── name
├── email
├── password
├── role
├── department
├── profileImage
└── createdAt
```

### Event

```text
Event
├── _id
├── title
├── description
├── category
├── date
├── startTime
├── endTime
├── venue
├── organizer
├── image
├── registrationRequired
└── createdAt
```

### Registration

```text
Registration
├── _id
├── user
├── event
├── registeredAt
└── status
```

---

# 📡 API Overview

Example REST API structure:

```text
/api/auth
    POST   /register
    POST   /login
    GET    /me

/api/events
    GET    /
    GET    /:id
    POST   /
    PUT    /:id
    DELETE /:id

/api/bookmarks
    GET    /
    POST   /:eventId
    DELETE /:eventId

/api/registrations
    POST   /:eventId
    GET    /:eventId
    DELETE /:eventId

/api/notifications
    GET    /
    POST   /
```

---

# 🎨 UI & UX

The Android application focuses on a clean and modern user experience using **Jetpack Compose + Material 3**.

Planned screens include:

```text
📱 Splash Screen
      ↓
🔐 Login / Register
      ↓
🏠 Home
      ↓
┌───────────────────────────────┐
│ 🔍 Search                     │
│                               │
│ 📅 Upcoming Events            │
│                               │
│ 🎓 Academic                  │
│ 💻 Technical                 │
│ 🎭 Cultural                  │
│ ⚽ Sports                    │
│ 🏆 Competitions              │
└───────────────────────────────┘
      ↓
📄 Event Details
      ↓
❤️ Save / 📝 Register / 🔔 Remind
```

---

# 🧪 Testing

Testing will include:

* Unit Testing
* ViewModel Testing
* Repository Testing
* API Testing
* UI Testing
* Integration Testing

Tools:

* JUnit
* AndroidX Test
* Compose UI Testing
* Postman

---

# 🚀 Development Roadmap

* [x] Project initialization
* [x] Android project setup
* [x] Kotlin + Jetpack Compose setup
* [ ] Authentication
* [ ] MongoDB database
* [ ] REST API
* [ ] Event management
* [ ] Event search & filtering
* [ ] Bookmark system
* [ ] Event registration
* [ ] Reminder system
* [ ] Push notifications
* [ ] React admin dashboard
* [ ] Analytics
* [ ] Testing
* [ ] Deployment

---

# 🔮 Future Improvements

Future versions may introduce:

* 🤖 AI-powered event recommendations
* 📍 GPS-based campus navigation
* 🗺️ Interactive campus map
* 📊 Advanced analytics
* 🎯 Personalized event feeds
* 📱 QR-based event check-in
* 🤝 Social event sharing
* 🧠 Recommendation system
* ☁️ Cloud image storage
* 🔄 Real-time event updates

---

# ⚙️ Development Tools

<p align="center">

<img src="https://img.shields.io/badge/Android%20Studio-3DDC84?style=for-the-badge&logo=androidstudio&logoColor=white" />
<img src="https://img.shields.io/badge/IntelliJ%20IDEA-000000?style=for-the-badge&logo=intellijidea&logoColor=white" />
<img src="https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" />

</p>

---

# 📦 Installation

## 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/Centralized-Campus-Event-App.git

cd Centralized-Campus-Event-App
```

## 2️⃣ Backend Setup

```bash
cd backend
npm install
npm run dev
```

Create a `.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

## 3️⃣ Android Setup

Open the `android` folder in **Android Studio**.

Then:

```text
Sync Gradle
        ↓
Connect Emulator / Android Device
        ↓
Run ▶️
```

## 4️⃣ Admin Dashboard

```bash
cd web-admin
npm install
npm run dev
```

---

# 🌟 Project Goals

The project aims to demonstrate practical knowledge of:

```text
Kotlin
   +
Jetpack Compose
   +
Modern Android Architecture
   +
REST APIs
   +
MERN Stack
   +
MongoDB
   +
Authentication
   +
Notifications
   +
Cloud Integration
```

More importantly, the goal is to build a **real-world solution rather than just a demonstration application**.

---

# 👨💻 Author

**Akshay Kumar Shaw**

B.Tech Computer Science & Engineering
Full Stack Web Development • Android Development

---

# ⭐ Support

If you find this project useful or interesting, consider giving it a ⭐ on GitHub!

---

<p align="center">
  <strong>🎓 Discover. Save. Remember. Attend.</strong>
</p>

<p align="center">
  Made with ❤️ using Kotlin, Jetpack Compose & MERN
</p>
