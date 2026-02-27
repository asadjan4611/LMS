# LMS Client - Next.js Frontend

The frontend application for the **Learning Management System**, built with **Next.js 15**, **React 19**, and **TypeScript**.

## Tech Stack

- **Next.js 15.5.5** - React framework with App Router & Turbopack
- **React 19.1.0** - UI library
- **TypeScript 5** - Type safety
- **Redux Toolkit 2.10.1** - State management
- **RTK Query** - API data fetching & caching
- **Tailwind CSS 3.4.18** - Utility-first styling
- **Material-UI 7.3.5** - Component library
- **NextAuth 4.24.13** - Authentication (Google, GitHub)
- **Socket.io Client 4.8.3** - Real-time notifications
- **Stripe.js 8.6.0** - Payment processing
- **Recharts 3.5.1** - Analytics charts
- **Formik + Yup** - Form handling & validation

## Project Structure

```
client/
├── app/
│   ├── admin/                   # Admin dashboard pages
│   │   ├── courses/             # Course management
│   │   ├── users/               # User management
│   │   ├── create-course/       # Course creation
│   │   ├── edit-course/[id]/    # Course editing
│   │   ├── categories/          # Category management
│   │   ├── faq/                 # FAQ management
│   │   ├── hero/                # Hero section editor
│   │   ├── invoices/            # Order invoices
│   │   ├── team/                # Team management
│   │   └── *-analytics/         # Analytics dashboards
│   ├── components/
│   │   ├── Admin/               # Admin components
│   │   ├── Auth/                # Login, SignUp, Verification
│   │   ├── Courses/             # Course display components
│   │   ├── Payment/             # Stripe checkout
│   │   ├── Profile/             # User profile
│   │   ├── Review/              # Review cards
│   │   └── Route/               # Landing page sections
│   ├── course/[id]/             # Course detail page
│   ├── course-access/[id]/      # Purchased course access
│   ├── courses/                 # Course catalog
│   ├── profile/                 # User profile page
│   ├── hooks/                   # Custom React hooks
│   ├── styles/                  # Style utilities
│   └── utils/                   # Helper components
├── redux/
│   ├── features/
│   │   ├── api/apiSlice.ts      # Base API configuration
│   │   ├── auth/                # Authentication state
│   │   ├── courses/             # Course API endpoints
│   │   ├── orders/              # Order API endpoints
│   │   ├── analytics/           # Analytics API
│   │   ├── layout/              # Layout API
│   │   ├── notifications/       # Notifications API
│   │   └── user/                # User API endpoints
│   └── store.ts                 # Redux store config
└── public/                      # Static assets
```



### Installation

```bash
# Install dependencies
npm install

# Run development server with Turbopack
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

## Features

### Public Pages
- **Landing Page** - Hero section, featured courses, reviews, FAQ
- **Course Catalog** - Browse and search courses with category filtering
- **Course Details** - View course info, curriculum, reviews before purchase

### User Features
- **Authentication** - Email/password, Google, GitHub login
- **Profile Management** - Update info, avatar, password
- **Course Access** - Video player, Q&A, resources for purchased courses
- **Reviews** - Rate and review completed courses

### Admin Dashboard
- **Course Management** - Create, edit, delete courses
- **User Management** - View users, update roles, delete accounts
- **Analytics** - User, course, and order analytics with charts
- **Layout Customization** - Edit hero banner, FAQ, categories
- **Real-time Notifications** - Purchase and review alerts via Socket.io

## Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with Turbopack |
| `npm run build` | Build for production |
| `npm start` | Start production server |
| `npm run lint` | Run ESLint |

## Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Redux Toolkit](https://redux-toolkit.js.org/)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [Material-UI](https://mui.com/material-ui/)
