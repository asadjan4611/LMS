# 🎓 LMS - Learning Management System

<div align="center">

![LMS Banner](https://img.shields.io/badge/LMS-Learning%20Management%20System-blue?style=for-the-badge&logo=bookstack&logoColor=white)

[![Next.js](https://img.shields.io/badge/Next.js-15.5.5-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.1.0-61DAFB?style=flat-square&logo=react)](https://reactjs.org/)
[![Express](https://img.shields.io/badge/Express-5.2.1-000000?style=flat-square&logo=express)](https://expressjs.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-8.18.2-47A248?style=flat-square&logo=mongodb)](https://www.mongodb.com/)
[![Redis](https://img.shields.io/badge/Redis-5.8.0-DC382D?style=flat-square&logo=redis)](https://redis.io/)
[![Socket.io](https://img.shields.io/badge/Socket.io-4.8.3-010101?style=flat-square&logo=socket.io)](https://socket.io/)
[![Stripe](https://img.shields.io/badge/Stripe-20.1.0-008CDD?style=flat-square&logo=stripe)](https://stripe.com/)

[![License: ISC](https://img.shields.io/badge/License-ISC-green.svg?style=flat-square)](https://opensource.org/licenses/ISC)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

**A modern, full-stack Learning Management System for delivering high-quality online education**

[Features](#-key-features) • [Demo](#-demo) • [Installation](#-installation) • [Documentation](#-documentation) • [Contributing](#-contributing)

</div>

---

## 📋 Table of Contents

- [Problem Statement](#-problem-statement)
- [Our Solution](#-our-solution)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [System Architecture](#-system-architecture)
- [UML Diagrams](#-uml-diagrams)
- [Class Diagrams](#-class-diagrams)
- [Database Schema](#-database-schema)
- [API Documentation](#-api-documentation)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [Roadmap](#-roadmap)
- [License](#-license)
- [Author](#-author)
- [Acknowledgments](#-acknowledgments)

---

## 🎯 Problem Statement

### The Challenge in Online Education

The modern education landscape faces several critical challenges that hinder effective online learning:

| Problem | Impact |
|---------|--------|
| **Fragmented Learning Platforms** | Students juggle multiple tools for videos, assignments, discussions, and payments |
| **Poor User Experience** | Complex interfaces discourage learners and reduce course completion rates |
| **Limited Instructor-Student Interaction** | Lack of real-time communication creates disconnect in online learning |
| **Insecure Payment Processing** | Trust issues with payment handling reduce course enrollments |
| **No Centralized Progress Tracking** | Students and admins lack visibility into learning progress |
| **Scalability Issues** | Traditional platforms struggle with growing user bases |
| **Lack of Analytics** | Instructors can't measure course effectiveness or student engagement |

### Real-World Consequences

```
📉 60% of online learners drop out before completing courses
💸 $107 billion lost annually due to poor e-learning experiences  
⏰ Students spend 40% more time navigating platforms than learning
🔒 23% of potential students abandon purchases due to payment security concerns
```

---

## 💡 Our Solution

**LMS** addresses these challenges with a comprehensive, integrated platform:

```mermaid
mindmap
  root((LMS Solution))
    Unified Platform
      Single dashboard
      Seamless navigation
      Mobile responsive
    Secure Payments
      Stripe integration
      PCI compliant
      Multiple currencies
    Real-time Features
      Socket.io notifications
      Live Q&A
      Instant updates
    Analytics
      User tracking
      Course performance
      Revenue insights
    Scalable Architecture
      Redis caching
      MongoDB sharding
      CDN delivery
    Interactive Learning
      Video streaming
      Q&A discussions
      Review system
```

### How LMS Solves Each Problem

| Problem | LMS Solution |
|---------|--------------|
| **Fragmented Platforms** | All-in-one system: courses, payments, discussions, analytics in one place |
| **Poor UX** | Modern Next.js frontend with intuitive navigation and dark/light themes |
| **Limited Interaction** | Real-time Q&A, review replies, and Socket.io notifications |
| **Payment Security** | Stripe integration with PCI-DSS compliance and secure token handling |
| **No Progress Tracking** | User dashboard with enrolled courses and completion status |
| **Scalability** | Redis caching, MongoDB indexing, and Cloudinary CDN for media |
| **Lack of Analytics** | Comprehensive admin dashboard with Recharts visualizations |

---

## ✨ Key Features

<table>
<tr>
<td width="50%">

### 🎓 For Students
- ✅ Browse and search courses by category
- ✅ Secure Stripe payment checkout
- ✅ HD video streaming with VdoCipher
- ✅ Interactive Q&A with instructors
- ✅ Course reviews and ratings
- ✅ Personal profile management
- ✅ Social login (Google, GitHub)
- ✅ Email verification with OTP

</td>
<td width="50%">

### 👨‍💼 For Administrators
- ✅ Multi-step course creation wizard
- ✅ User management with role assignment
- ✅ Real-time purchase notifications
- ✅ Revenue and user analytics
- ✅ Layout customization (Hero, FAQ)
- ✅ Order and invoice management
- ✅ Review moderation and replies
- ✅ Category management

</td>
</tr>
</table>

### 🔐 Security Features
- **JWT Authentication** — Access tokens (30min) + Refresh tokens (7 days)
- **Password Hashing** — bcrypt with salt rounds
- **Role-Based Access** — User and Admin authorization
- **CORS Protection** — Configured origin whitelist
- **Rate Limiting** — API request throttling

### 🚀 Performance Features
- **Redis Caching** — Reduced database load
- **Cloudinary CDN** — Fast media delivery
- **Turbopack** — Lightning-fast Next.js builds
- **RTK Query** — Automatic request caching and deduplication

---

## 🛠 Tech Stack

### Frontend Architecture

```mermaid
graph LR
    subgraph "Frontend Stack"
        A[Next.js 15] --> B[React 19]
        B --> C[TypeScript]
        C --> D[Redux Toolkit]
        D --> E[RTK Query]
        
        F[Tailwind CSS] --> G[Material-UI]
        G --> H[Recharts]
        
        I[NextAuth] --> J[Socket.io Client]
        J --> K[Stripe.js]
    end
```

### Backend Architecture

```mermaid
graph LR
    subgraph "Backend Stack"
        A[Node.js 18+] --> B[Express 5]
        B --> C[TypeScript]
        
        D[Mongoose] --> E[MongoDB]
        F[ioredis] --> G[Redis]
        
        H[JWT] --> I[bcryptjs]
        J[Stripe SDK] --> K[Cloudinary]
        L[Socket.io] --> M[Nodemailer]
    end
```

### Complete Technology Matrix

| Layer | Technology | Version | Purpose |
|-------|------------|---------|---------|
| **Frontend Framework** | Next.js | 15.5.5 | React framework with App Router |
| **UI Library** | React | 19.1.0 | Component-based UI |
| **Type Safety** | TypeScript | 5.x | Static type checking |
| **State Management** | Redux Toolkit | 2.10.1 | Global state management |
| **API Layer** | RTK Query | - | Data fetching & caching |
| **Styling** | Tailwind CSS | 3.4.18 | Utility-first CSS |
| **Component Library** | Material-UI | 7.3.5 | Pre-built components |
| **Charts** | Recharts | 3.5.1 | Analytics visualizations |
| **Authentication** | NextAuth | 4.24.13 | OAuth & session management |
| **Real-time** | Socket.io | 4.8.3 | WebSocket communication |
| **Payments** | Stripe | 20.1.0 | Payment processing |
| **Backend Framework** | Express.js | 5.2.1 | REST API server |
| **Database** | MongoDB | - | Document database |
| **ODM** | Mongoose | 8.18.2 | MongoDB object modeling |
| **Caching** | Redis | 5.8.0 | In-memory data store |
| **Media Storage** | Cloudinary | 2.7.0 | Cloud media management |
| **Email** | Nodemailer | 7.0.6 | SMTP email service |
| **Video** | VdoCipher | - | Secure video streaming |

---

## 🏗 System Architecture

### High-Level Architecture

```mermaid
graph TB
    subgraph "Client Layer"
        Browser[Web Browser]
        NextJS[Next.js 15 App]
        Redux[Redux Store]
        SocketClient[Socket.io Client]
    end

    subgraph "API Gateway"
        Express[Express.js 5 Server]
        Middleware[Middleware Stack]
        SocketServer[Socket.io Server]
    end

    subgraph "Service Layer"
        UserService[User Service]
        CourseService[Course Service]
        OrderService[Order Service]
        NotificationService[Notification Service]
    end

    subgraph "Data Layer"
        MongoDB[(MongoDB)]
        Redis[(Redis Cache)]
    end

    subgraph "External Services"
        Stripe[Stripe API]
        Cloudinary[Cloudinary CDN]
        VdoCipher[VdoCipher]
        SMTP[SMTP Server]
    end

    Browser --> NextJS
    NextJS --> Redux
    Redux -->|REST API| Express
    SocketClient -->|WebSocket| SocketServer

    Express --> Middleware
    Middleware --> UserService
    Middleware --> CourseService
    Middleware --> OrderService
    Middleware --> NotificationService

    UserService --> MongoDB
    UserService --> Redis
    CourseService --> MongoDB
    CourseService --> Redis
    OrderService --> MongoDB
    NotificationService --> MongoDB

    OrderService --> Stripe
    CourseService --> Cloudinary
    CourseService --> VdoCipher
    UserService --> SMTP
```

### Request-Response Flow

```mermaid
sequenceDiagram
    autonumber
    participant Client as Browser
    participant Next as Next.js
    participant Redux as RTK Query
    participant API as Express API
    participant Auth as Auth Middleware
    participant Cache as Redis
    participant DB as MongoDB

    Client->>Next: User Action
    Next->>Redux: Dispatch Query/Mutation
    Redux->>API: HTTP Request + JWT
    API->>Auth: Validate Token
    
    alt Token Valid
        Auth->>Cache: Check Cache
        alt Cache Hit
            Cache-->>API: Return Cached Data
        else Cache Miss
            API->>DB: Query Database
            DB-->>API: Return Data
            API->>Cache: Update Cache
        end
        API-->>Redux: JSON Response
        Redux->>Next: Update State
        Next->>Client: Render UI
    else Token Invalid
        Auth-->>Client: 401 Unauthorized
    end
```

---

## 📐 UML Diagrams

### Use Case Diagram

```mermaid
graph TB
    subgraph "LMS System"
        UC1((Browse Courses))
        UC2((Purchase Course))
        UC3((Watch Videos))
        UC4((Ask Questions))
        UC5((Write Reviews))
        UC6((Manage Profile))
        UC7((Create Course))
        UC8((Manage Users))
        UC9((View Analytics))
        UC10((Edit Layout))
        UC11((Process Payments))
        UC12((Send Notifications))
    end

    Student[👤 Student]
    Admin[👨‍💼 Admin]
    System[⚙️ System]

    Student --> UC1
    Student --> UC2
    Student --> UC3
    Student --> UC4
    Student --> UC5
    Student --> UC6

    Admin --> UC7
    Admin --> UC8
    Admin --> UC9
    Admin --> UC10
    Admin --> UC1

    System --> UC11
    System --> UC12

    UC2 -.->|includes| UC11
    UC4 -.->|triggers| UC12
    UC5 -.->|triggers| UC12
```

### Activity Diagram - Course Purchase Flow

```mermaid
flowchart TD
    A([Start]) --> B[Browse Courses]
    B --> C[Select Course]
    C --> D{Already Purchased?}
    
    D -->|Yes| E[Access Course Content]
    D -->|No| F[View Course Details]
    
    F --> G{User Logged In?}
    G -->|No| H[Show Login Modal]
    H --> I[User Authenticates]
    I --> G
    
    G -->|Yes| J[Click Buy Now]
    J --> K[Open Stripe Checkout]
    K --> L[Enter Payment Details]
    L --> M{Payment Successful?}
    
    M -->|No| N[Show Error Message]
    N --> K
    
    M -->|Yes| O[Create Order Record]
    O --> P[Update User Courses]
    P --> Q[Send Confirmation Email]
    Q --> R[Notify Admin via Socket]
    R --> E
    
    E --> S[Watch Videos]
    S --> T[Participate in Q&A]
    T --> U[Submit Review]
    U --> V([End])
```

### State Diagram - User Authentication

```mermaid
stateDiagram-v2
    [*] --> Guest: Visit Site
    
    Guest --> Registering: Click Sign Up
    Registering --> PendingVerification: Submit Form
    PendingVerification --> Verified: Enter OTP
    PendingVerification --> Registering: Invalid OTP
    Verified --> Authenticated: Auto Login
    
    Guest --> Authenticating: Click Login
    Authenticating --> Authenticated: Valid Credentials
    Authenticating --> Guest: Invalid Credentials
    
    Guest --> SocialAuth: Click Google/GitHub
    SocialAuth --> Authenticated: OAuth Success
    SocialAuth --> Guest: OAuth Failed
    
    Authenticated --> TokenRefresh: Access Token Expired
    TokenRefresh --> Authenticated: Refresh Success
    TokenRefresh --> Guest: Refresh Failed
    
    Authenticated --> Guest: Logout
    Authenticated --> [*]: Session End
```

### Sequence Diagram - Video Access

```mermaid
sequenceDiagram
    participant User
    participant Frontend
    participant Backend
    participant VdoCipher
    participant MongoDB

    User->>Frontend: Click Play Video
    Frontend->>Backend: GET /get-course-content/:id
    Backend->>Backend: Verify JWT Token
    Backend->>MongoDB: Check User Enrollment
    
    alt User Enrolled
        MongoDB-->>Backend: Enrollment Confirmed
        Backend->>VdoCipher: Request OTP
        VdoCipher-->>Backend: Return OTP + Playback Info
        Backend-->>Frontend: Video Data + OTP
        Frontend->>VdoCipher: Initialize Player
        VdoCipher-->>User: Stream Video
    else Not Enrolled
        MongoDB-->>Backend: Not Enrolled
        Backend-->>Frontend: 403 Forbidden
        Frontend-->>User: Show Purchase Prompt
    end
```

---

## 📊 Class Diagrams

### Domain Model Class Diagram

```mermaid
classDiagram
    class User {
        +ObjectId _id
        +String name
        +String email
        +String password
        +Object avatar
        +String role
        +Boolean isVerified
        +Array~CourseRef~ courses
        +Date createdAt
        +Date updatedAt
        +comparePassword(password) Boolean
        +SignAccessToken() String
        +SignRefreshToken() String
    }

    class Course {
        +ObjectId _id
        +String name
        +String description
        +String categories
        +Number price
        +Number estimatedPrice
        +Object thumbnail
        +String tags
        +String level
        +String demoUrl
        +Array~Benefit~ benefits
        +Array~Prerequisite~ prerequisites
        +Array~Review~ reviews
        +Array~CourseData~ courseData
        +Number ratings
        +Number purchased
        +Date createdAt
        +Date updatedAt
    }

    class CourseData {
        +ObjectId _id
        +String title
        +String description
        +String videoUrl
        +String videoSection
        +Number videoLength
        +String videoPlayer
        +Array~Link~ links
        +Array~Question~ questions
    }

    class Review {
        +ObjectId _id
        +User user
        +Number rating
        +String comment
        +Array~Reply~ commentReplies
        +Date createdAt
    }

    class Question {
        +ObjectId _id
        +User user
        +String question
        +Array~Answer~ questionReplies
        +Date createdAt
    }

    class Order {
        +ObjectId _id
        +String courseId
        +String userId
        +Object payment_info
        +Date createdAt
    }

    class Notification {
        +ObjectId _id
        +String title
        +String message
        +String status
        +Date createdAt
    }

    class Layout {
        +ObjectId _id
        +String type
        +Object banner
        +Array~Category~ categories
        +Array~FAQ~ faq
    }

    User "1" --> "*" Order : places
    User "1" --> "*" Review : writes
    User "1" --> "*" Question : asks
    Course "1" --> "*" CourseData : contains
    Course "1" --> "*" Review : has
    CourseData "1" --> "*" Question : has
    Order "*" --> "1" Course : for
    Order "*" --> "1" User : by
```

### Service Layer Class Diagram

```mermaid
classDiagram
    class UserController {
        +registrationUser(req, res, next)
        +activateUser(req, res, next)
        +loginUser(req, res, next)
        +logoutUser(req, res, next)
        +updateAccessToken(req, res, next)
        +getUserInfo(req, res, next)
        +socialAuth(req, res, next)
        +updateUserInfo(req, res, next)
        +updateUserPassword(req, res, next)
        +updateUserAvatar(req, res, next)
        +getAllUsers(req, res, next)
        +updateUserRole(req, res, next)
        +deleteUser(req, res, next)
    }

    class CourseController {
        +uploadCourse(req, res, next)
        +editCourse(req, res, next)
        +getSingleCourse(req, res, next)
        +getAllCourses(req, res, next)
        +getCourseByUser(req, res, next)
        +addQuestion(req, res, next)
        +addAnswer(req, res, next)
        +addReview(req, res, next)
        +addReplyToReview(req, res, next)
        +deleteCourse(req, res, next)
    }

    class OrderController {
        +createOrder(req, res, next)
        +getAllOrders(req, res, next)
        +sendStripePublishableKey(req, res, next)
        +newPayment(req, res, next)
    }

    class UserService {
        +getUserById(id) User
        +createUser(data) User
        +updateUser(id, data) User
    }

    class CourseService {
        +createCourse(data) Course
        +getAllCourses() Course[]
    }

    class OrderService {
        +createOrder(data) Order
        +getAllOrders() Order[]
    }

    class AuthMiddleware {
        +isAuthenticated(req, res, next)
        +authorizeRoles(...roles)
    }

    class ErrorMiddleware {
        +errorHandler(err, req, res, next)
    }

    UserController --> UserService : uses
    CourseController --> CourseService : uses
    OrderController --> OrderService : uses
    
    UserController --> AuthMiddleware : protected by
    CourseController --> AuthMiddleware : protected by
    OrderController --> AuthMiddleware : protected by
```

### Frontend Component Hierarchy

```mermaid
classDiagram
    class RootLayout {
        +ThemeProvider
        +SessionProvider
        +ReduxProvider
        +Toaster
    }

    class Header {
        +NavItems
        +ThemeSwitcher
        +UserMenu
        +AuthModals
    }

    class HomePage {
        +Hero
        +Courses
        +Reviews
        +FAQ
        +Footer
    }

    class CoursePage {
        +CourseDetails
        +CourseContent
        +CheckoutForm
    }

    class AdminDashboard {
        +AdminSidebar
        +DashboardHeader
        +DashboardWidgets
    }

    class CourseManagement {
        +CreateCourse
        +EditCourse
        +AllCourses
    }

    class UserManagement {
        +AllUsers
        +UserAnalytics
    }

    RootLayout --> Header
    RootLayout --> HomePage
    RootLayout --> CoursePage
    RootLayout --> AdminDashboard
    
    AdminDashboard --> CourseManagement
    AdminDashboard --> UserManagement
```

---

## 🗄 Database Schema

### Entity Relationship Diagram

```mermaid
erDiagram
    USER {
        ObjectId _id PK
        string name "Required"
        string email UK "Required, Unique"
        string password "Min 6 chars"
        object avatar "public_id, url"
        string role "user | admin"
        boolean isVerified "Default: false"
        array courses "CourseRef[]"
        timestamp createdAt
        timestamp updatedAt
    }

    COURSE {
        ObjectId _id PK
        string name "Required"
        string description "Required"
        string categories "Required"
        number price "Required"
        number estimatedPrice "Optional"
        object thumbnail "public_id, url"
        string tags "Required"
        string level "Required"
        string demoUrl "Required"
        array benefits "title[]"
        array prerequisites "title[]"
        array reviews "Review[]"
        array courseData "CourseData[]"
        number ratings "Default: 0"
        number purchased "Default: 0"
        timestamp createdAt
        timestamp updatedAt
    }

    COURSE_DATA {
        ObjectId _id PK
        string title
        string description
        string videoUrl
        string videoSection
        number videoLength
        string videoPlayer
        array links "Link[]"
        array questions "Question[]"
    }

    ORDER {
        ObjectId _id PK
        string courseId FK "Required"
        string userId FK "Required"
        object payment_info "Stripe data"
        timestamp createdAt
        timestamp updatedAt
    }

    NOTIFICATION {
        ObjectId _id PK
        string title "Required"
        string message "Required"
        string status "Default: unread"
        timestamp createdAt
        timestamp updatedAt
    }

    LAYOUT {
        ObjectId _id PK
        string type "Banner | FAQ | Categories"
        object banner "image, title, subtitle"
        array categories "Category[]"
        array faq "FAQ[]"
    }

    REVIEW {
        ObjectId _id PK
        object user FK
        number rating "1-5"
        string comment
        array commentReplies
        timestamp createdAt
    }

    QUESTION {
        ObjectId _id PK
        object user FK
        string question
        array questionReplies
        timestamp createdAt
    }

    USER ||--o{ ORDER : "places"
    USER ||--o{ REVIEW : "writes"
    USER ||--o{ QUESTION : "asks"
    COURSE ||--o{ ORDER : "purchased_in"
    COURSE ||--|{ COURSE_DATA : "contains"
    COURSE ||--o{ REVIEW : "has"
    COURSE_DATA ||--o{ QUESTION : "has"
```

---

## 📡 API Documentation

### Authentication Endpoints

| Method | Endpoint | Description | Auth | Request Body |
|--------|----------|-------------|------|--------------|
| `POST` | `/api/v1/registration` | Register new user | ❌ | `{name, email, password}` |
| `POST` | `/api/v1/activate-user` | Verify OTP | ❌ | `{activation_token, activation_code}` |
| `POST` | `/api/v1/login` | User login | ❌ | `{email, password}` |
| `GET` | `/api/v1/logout` | User logout | ✅ | - |
| `GET` | `/api/v1/refresh` | Refresh token | ❌ | - |
| `GET` | `/api/v1/me` | Get current user | ✅ | - |
| `POST` | `/api/v1/social-auth` | OAuth login | ❌ | `{email, name, avatar}` |

### User Management Endpoints

| Method | Endpoint | Description | Auth | Role |
|--------|----------|-------------|------|------|
| `PUT` | `/api/v1/update-user-info` | Update profile | ✅ | User |
| `PUT` | `/api/v1/update-user-password` | Change password | ✅ | User |
| `PUT` | `/api/v1/update-user-avatar` | Update avatar | ✅ | User |
| `GET` | `/api/v1/get-all-users` | List all users | ✅ | Admin |
| `PUT` | `/api/v1/update-user-role` | Change user role | ✅ | Admin |
| `DELETE` | `/api/v1/delete-user/:id` | Delete user | ✅ | Admin |

### Course Endpoints

| Method | Endpoint | Description | Auth | Role |
|--------|----------|-------------|------|------|
| `POST` | `/api/v1/create-course` | Create course | ✅ | Admin |
| `PUT` | `/api/v1/edit-course/:id` | Update course | ✅ | Admin |
| `GET` | `/api/v1/get-course/:id` | Get course (public) | ❌ | - |
| `GET` | `/api/v1/get-courses` | List all courses | ❌ | - |
| `GET` | `/api/v1/get-course-content/:id` | Get full content | ✅ | Enrolled |
| `PUT` | `/api/v1/add-question` | Ask question | ✅ | User |
| `PUT` | `/api/v1/add-answer` | Answer question | ✅ | User |
| `PUT` | `/api/v1/add-review/:id` | Add review | ✅ | User |
| `PUT` | `/api/v1/add-reply/:id` | Reply to review | ✅ | Admin |
| `DELETE` | `/api/v1/delete-course/:id` | Delete course | ✅ | Admin |

### Order & Payment Endpoints

| Method | Endpoint | Description | Auth |
|--------|----------|-------------|------|
| `POST` | `/api/v1/create-order` | Create order | ✅ |
| `GET` | `/api/v1/get-all-orders` | List all orders | ✅ Admin |
| `GET` | `/api/v1/payment/stripePublishAbleKey` | Get Stripe key | ❌ |
| `POST` | `/api/v1/payment/process` | Process payment | ✅ |

---

## 🚀 Installation

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** 18.x or higher ([Download](https://nodejs.org/))
- **MongoDB** 6.x or higher ([Download](https://www.mongodb.com/try/download/community))
- **Redis** 7.x or higher ([Download](https://redis.io/download/))
- **Git** ([Download](https://git-scm.com/))

### Clone the Repository

```bash
git clone https://github.com/alishair/lms.git
cd lms
```

### Install Dependencies

```bash
# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install
```

### Quick Start

```bash
# Terminal 1: Start MongoDB (if not running as service)
mongod

# Terminal 2: Start Redis (if not running as service)
redis-server

# Terminal 3: Start Backend Server
cd server
npm run dev

# Terminal 4: Start Frontend
cd client
npm run dev
```

🎉 Open [http://localhost:3000](http://localhost:3000) to view the application!

---

## ⚙️ Configuration

### Server Environment Variables

Create a `.env` file in the `/server` directory:

```env
# Server Configuration
PORT=8000
NODE_ENV=development

# Database
MONGODB_URL=mongodb://localhost:27017/lms

# Redis
REDIS_URL=redis://localhost:6379

# JWT Secrets
ACCESS_TOKEN=your_access_token_secret_key_here
REFRESH_TOKEN=your_refresh_token_secret_key_here
ACCESS_TOKEN_EXPIRE=30
REFRESH_TOKEN_EXPIRE=7

# Cloudinary (Media Storage)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Stripe (Payments)
STRIPE_SECRET_KEY=sk_test_xxxxxxxxxxxxx
STRIPE_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxx

# SMTP (Email)
SMTP_HOST=smtp.gmail.com
SMTP_PORT=465
SMTP_SERVICE=gmail
SMTP_MAIL=your_email@gmail.com
SMTP_PASSWORD=your_app_password

# VdoCipher (Video)
VDOCIPHER_API_SECRET=your_vdocipher_secret

# Client URL
CLIENT_URL=http://localhost:3000
```

### Client Environment Variables

Create a `.env.local` file in the `/client` directory:

```env
# API Configuration
NEXT_PUBLIC_SERVER_URL=http://localhost:8000/api/v1/
NEXT_PUBLIC_SOCKET_SERVER_URI=http://localhost:8000

# NextAuth
NEXTAUTH_SECRET=your_nextauth_secret_key

# OAuth Providers
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret

# Stripe
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxx
```

---

## 📖 Usage

### For Students

1. **Register** — Create an account with email verification
2. **Browse** — Explore courses by category or search
3. **Purchase** — Secure checkout with Stripe
4. **Learn** — Watch videos, ask questions, track progress
5. **Review** — Rate and review completed courses

### For Administrators

1. **Login** — Access admin dashboard with admin credentials
2. **Create Courses** — Multi-step wizard for course creation
3. **Manage Users** — View, edit roles, or delete users
4. **Monitor** — Track analytics and real-time notifications
5. **Customize** — Edit hero banner, FAQ, and categories

---

## 📁 Project Structure

```
LMS/
├── 📂 client/                       # Next.js Frontend
│   ├── 📂 app/
│   │   ├── 📂 admin/                # Admin pages
│   │   │   ├── 📂 courses/
│   │   │   ├── 📂 users/
│   │   │   ├── 📂 create-course/
│   │   │   ├── 📂 edit-course/[id]/
│   │   │   ├── 📂 categories/
│   │   │   ├── 📂 faq/
│   │   │   ├── 📂 hero/
│   │   │   ├── 📂 invoices/
│   │   │   ├── 📂 team/
│   │   │   └── 📂 *-analytics/
│   │   ├── 📂 components/
│   │   │   ├── 📂 Admin/
│   │   │   ├── 📂 Auth/
│   │   │   ├── 📂 Courses/
│   │   │   ├── 📂 Payment/
│   │   │   ├── 📂 Profile/
│   │   │   ├── 📂 Review/
│   │   │   └── 📂 Route/
│   │   ├── 📂 course/[id]/
│   │   ├── 📂 course-access/[id]/
│   │   ├── 📂 courses/
│   │   ├── 📂 profile/
│   │   ├── 📂 hooks/
│   │   ├── 📂 styles/
│   │   └── 📂 utils/
│   ├── 📂 redux/
│   │   ├── 📂 features/
│   │   │   ├── 📂 api/
│   │   │   ├── 📂 auth/
│   │   │   ├── 📂 courses/
│   │   │   ├── 📂 orders/
│   │   │   ├── 📂 analytics/
│   │   │   ├── 📂 layout/
│   │   │   ├── 📂 notifications/
│   │   │   └── 📂 user/
│   │   └── 📄 store.ts
│   ├── 📂 public/
│   ├── 📄 package.json
│   └── 📄 tailwind.config.ts
│
├── 📂 server/                       # Express.js Backend
│   ├── 📂 controllers/
│   │   ├── 📄 user.controller.ts
│   │   ├── 📄 course.controller.ts
│   │   ├── 📄 order.controller.ts
│   │   ├── 📄 notification.controller.ts
│   │   ├── 📄 analytics.controller.ts
│   │   └── 📄 layout.controller.ts
│   ├── 📂 models/
│   │   ├── 📄 user.model.ts
│   │   ├── 📄 course.model.ts
│   │   ├── 📄 order.model.ts
│   │   ├── 📄 layout.model.ts
│   │   └── 📄 notificationModel.ts
│   ├── 📂 routes/
│   │   ├── 📄 user.route.ts
│   │   ├── 📄 course.route.ts
│   │   ├── 📄 order.route.ts
│   │   ├── 📄 notification.route.ts
│   │   ├── 📄 analytics.route.ts
│   │   └── 📄 layout.route.ts
│   ├── 📂 middleware/
│   │   ├── 📄 auth.ts
│   │   ├── 📄 error.ts
│   │   └── 📄 catchAsyncErrors.ts
│   ├── 📂 services/
│   │   ├── 📄 user.service.ts
│   │   ├── 📄 course.service.ts
│   │   └── 📄 order.service.ts
│   ├── 📂 utils/
│   │   ├── 📄 db.ts
│   │   ├── 📄 redis.ts
│   │   ├── 📄 jwt.ts
│   │   ├── 📄 sendMail.ts
│   │   ├── 📄 analytics.generator.ts
│   │   └── 📄 ErrorHandler.ts
│   ├── 📂 mails/
│   ├── 📂 @types/
│   ├── 📄 app.ts
│   ├── 📄 server.ts
│   ├── 📄 socketServer.ts
│   └── 📄 package.json
│
├── 📄 README.md
└── 📄 .gitignore
```

---

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### Getting Started

1. **Fork** the repository
2. **Clone** your fork: `git clone https://github.com/yourusername/lms.git`
3. **Create** a branch: `git checkout -b feature/amazing-feature`
4. **Make** your changes
5. **Commit**: `git commit -m 'Add amazing feature'`
6. **Push**: `git push origin feature/amazing-feature`
7. **Open** a Pull Request

### Contribution Guidelines

- Follow the existing code style and conventions
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

### Code of Conduct

Please read our [Code of Conduct](CODE_OF_CONDUCT.md) before contributing.

---

## 🗺 Roadmap

### Version 1.1 (Q2 2026)
- [ ] Course progress tracking
- [ ] Certificate generation
- [ ] Instructor dashboard
- [ ] Mobile app (React Native)

### Version 1.2 (Q3 2026)
- [ ] Live streaming classes
- [ ] Assignment submission
- [ ] Grading system
- [ ] Discussion forums

### Version 2.0 (Q4 2026)
- [ ] AI-powered recommendations
- [ ] Learning paths
- [ ] Gamification (badges, points)
- [ ] Multi-language support

---

## 📄 License

This project is licensed under the **ISC License**.

```
ISC License

Copyright (c) 2024-2026 Ali Shair

Permission to use, copy, modify, and/or distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
```

---

## 👨‍💻 Author

<div align="center">

### Ali Shair

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/alishair)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/alishair)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:alishair@example.com)

**Full-Stack Developer | Software Engineer**

*"Building solutions that make a difference, one commit at a time."*

</div>

---

## 🙏 Acknowledgments

Special thanks to:

- **Next.js Team** — For the amazing React framework
- **Vercel** — For hosting and deployment solutions
- **MongoDB** — For the flexible document database
- **Stripe** — For secure payment processing
- **VdoCipher** — For DRM-protected video streaming
- **Open Source Community** — For the countless libraries that made this possible

---

<div align="center">

**⭐ If you found this project helpful, please give it a star! ⭐**

Made with ❤️ by [Ali Shair](https://github.com/alishair)

</div>
