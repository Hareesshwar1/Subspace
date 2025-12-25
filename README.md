----------------------------------------**CLUESO CLONE**--------------------------------------------------


#A full-stack clone of Clueso.io, built as part of an assignment to replicate core product flows, architecture, and user experience using modern web technologies.
#This project demonstrates frontend engineering, backend API design, authentication, database integration, and system architecture.


//--------------------------------------------------------------------------------------------------//
                                         **#KEY FEATURES#**
                                     
1. User onboarding & authentication
2. Secure session handling using JWT
3. Feedback collection system
4. Dashboard view for logged-in users
5. AI Insights (mocked)
6. Modern landing page with animations
7. Clean UX flows similar to Clueso.io
//--------------------------------------------------------------------------------------------------//
                                            **#Tech Stack#**

----------
Frontend
----------
React.js
React Router DOM
Framer Motion (animations)
Fetch API
CSS Modules / Custom CSS
----------
Backend
----------
**Node.js
Express.js
MongoDB
Mongoose
JWT Authentication
Bcrypt.js
Nodemailer (email verification support)
dotenv**
//--------------------------------------------------------------------------------------------------//
                                              **Tools**
**VS Code
MongoDB Compass
Thunder Client / Postman
Git & GitHub**
//--------------------------------------------------------------------------------------------------//
Frontend (React)
   |
   | HTTP (JSON + JWT)
   |
Backend (Express API)
   |
   | Mongoose ODM
   |
MongoDB


//--------------------------------------------------------------------------------------------------//
backend/
├── server.js
├── src/
│   ├── app.js
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── auth.controller.js
│   │   ├── feedback.controller.js
│   │   └── ai.controller.js
│   ├── middlewares/
│   │   └── auth.middleware.js
│   ├── models/
│   │   ├── User.js
│   │   └── Feedback.js
│   ├── routes/
│   │   ├── auth.routes.js
│   │   ├── feedback.routes.js
│   │   └── ai.routes.js
│   └── utils/
│       └── sendEmail.js

//--------------------------------------------------------------------------------------------------//
frontend/
├── src/
│   ├── components/
│   │   ├── Navbar.jsx
│   │   ├── Hero.jsx
│   │   ├── Workflow.jsx
│   │   ├── AnimatedGrid.jsx
│   │   └── ProtectedRoute.jsx
│   ├── pages/
│   │   ├── Login.jsx
│   │   ├── Signup.jsx
│   │   ├── Dashboard.jsx
│   │   └── Feedback.jsx
│   ├── assets/
│   │   ├── images/
│   │   └── workflow/
│   ├── App.jsx
│   └── index.js

//--------------------------------------------------------------------------------------------------//
                                          **Authentication Flow**
                User submits name, email, password

**Password hashed using bcrypt
User stored in MongoDB
JWT generated and returned
Email verification via Nodemailer**
//--------------------------------------------------------------------------------------------------//
                                            **Login**

**Credentials verified
Password compared using bcrypt
JWT issued
Token stored in localStorage
Redirect to dashboard**
//--------------------------------------------------------------------------------------------------//
**Protected Routes**
1.Dashboard & Feedback pages require JWT
2.Unauthorized users redirected to /login
//--------------------------------------------------------------------------------------------------//
                                        **Feedback System**

**Features
Create feedback (text/video type)
Fetch feedback per user
Delete feedback
Secure user isolation**
//--------------------------------------------------------------------------------------------------//
                                        **UI & UX Highlights**


**Landing page inspired by Clueso.io
Scroll-based CTA interactions
Animated workflow cards
Sticky editor preview
Clean SaaS-style layout
Responsive design principles**
//--------------------------------------------------------------------------------------------------//

┌──────────────┐        HTTP / JWT        ┌──────────────┐
│   Frontend   │  ───────────────────▶   │   Backend    │
│   (React)    │                          │ (Node.js)   │
└──────────────┘                          └──────┬──────┘
                                                       │
                                                       ▼
                                                ┌───────────┐
                                                │ MongoDB   │
                                                └───────────┘

//--------------------------------------------------------------------------------------------------//
src/
├── components/        # Reusable UI components
│   ├── Hero
│   ├── Navbar
│   ├── Workflow
│   ├── AnimatedGrid
│   ├── StickyEditor
│   ├── ImpactMatrix
│   ├── Trust
│   └── ... (30+ components)
│
├── pages/             # Route-level pages
│   ├── Home
│   ├── Login
│   ├── Signup
│   ├── Dashboard
│   ├── Feedback
│   └── LoginSuccess
│
├── assets/
│   ├── images
│   ├── gifs
│   └── logos
│
├── utils/
│   ├── api.js         # Centralized API calls
│   └── auth.js        # Token helpers
│
├── App.js             # Routing & layout
└── index.js


