# CivicIQ

**Domain**: Governance / Public Welfare  
**Tagline**: From Complaint to Intelligent Action 

>**Current systems stop at registering complaints. CivicIQ is designed to transform every complaint into the first step of an intelligent municipal decision**

## 🧠 Overview
  
**CivicIQ** is a full-stack web application designed to streamline the process of reporting, tracking, and resolving local civic issues such as potholes, broken streetlights, and uncollected garbage. It provides a bridge between citizens and municipal authorities, bringing accountability and transparency to local issue resolution. 

(image)
*Caption: Citizen view showing issue reporting interface*

## 🧠 Overview
CivicIQ is an AI-powered Smart Waste Management platform that bridges the gap between citizens and municipalities. Citizens can report waste by uploading an image and location, while AI automatically classifies the waste into categories such as Plastic, Organic, E-Waste, Construction Debris, or Mixed Waste.
Unlike traditional complaint management systems that stop at complaint registration, CivicIQ transforms every report into structured, actionable data for municipalities, laying the foundation for intelligent decision support.

**Our Vision**
> Report → Understand → Act
Future versions of CivicIQ will evolve beyond complaint management to help municipalities predict, prevent, and resolve urban waste challenges using AI. 

## 🚨 Problem Addressed
Despite the availability of digital complaint systems, urban waste management remains largely reactive.
Current challenges include:
- Manual waste categorization
- Delayed complaint prioritization
- Inefficient resource allocation
- Duplicate complaints
- Lack of AI-assisted decision making

Current systems digitize complaints.
CivicIQ digitizes decisions.

## ✨ Features  

(image)
*Caption: Step-by-step issue reporting process*

### 🧍 Citizens  
- 📍 **Report Issues**: Submit problems with a description, live location (via map), and an image   
- 👍 **Upvote Issues**: Support others' reports to highlight common concerns \
- 🔄 **Complaint Tracking**: Citizens can Track the progress 

### 🧑‍💼 Admins (City Workers)  
- 📊 **Dashboard**: View, filter, and manage all reported issues  
- 🔧 **Status Management**: Update progress and mark resolutions set priority  
- 🔒 **Smart Route Management**: Optimize the Best Route
- 📊 **Categorised Complaints**: Ai ctaegorizes waste and helps Minicipalities

### 📘 Civic Education & Rights  

CiviIQ now includes a fully frontend civic learning module to educate users—especially students and first-time voters—about their rights and responsibilities.

**Route**: `/civic-education`  
**File**: `src/Pages/CivicEducation.jsx`

## 🌟 What Makes CivicIQ Different?

| Traditional Waste Apps | CivicIQ |
|-------------------------|---------|
| Manual category selection | AI Waste Classification |
| Complaint registration | Structured complaint generation |
| Citizen-focused | Citizen + Municipality focused |
| Reactive | AI-ready |
| Report → Wait | Report → Understand → Act |

#### ✨ Highlights  
- 🧠 Interactive Quiz System with progress tracking and localStorage-based scores  
- 🏆 Gamified XP system, achievements, and level-ups  
- 🗂️ Tabbed layout for Overview, Learn, Quiz, and Resources  
- 🔖 Bookmark favorite sections and save them locally  
- 📊 Reading Progress Bar and Civic Journey visualization  
- 💡 Animated “Did You Know?” facts carousel  
- 📥 Downloadable PDFs and curated civic resources  
- 🎉 Celebration animations on milestone completions  

### 🧭 CivicIQ Simulator

CiviIQ now includes a standalone interactive simulator that allows users to step into civic leadership roles. Through animated dilemmas and slider-based decisions, users make trade-offs and explore the consequences of their choices—all within a frontend-only experience.

**Route**: `/civic-simulator`  
**File**: `src/Pages/CivicSimulator.jsx`

#### ✨ Highlights  
- 🎮 **Scenario Cards** – Solve dilemmas like budget allocation or policy conflicts using sliders and toggles  
- 🧠 **Outcome Feedback** – Dynamic responses based on user choices (public satisfaction, resource balance)  
- 📊 **Civic Style Profiling** – Discover civic personas like “Planner” or “Advocate” based on decisions  
- 🔁 **Replayable Challenges** – Rerun scenarios to improve your score and try alternate outcomes  
- 🏅 **XP & Badges** – Earn experience points and unlock achievement badges locally  
- 💡 **Frontend-Only Logic** – Built entirely in React with `localStorage` persistence for decision history and XP tracking

##📂 Project Structure

```
CivicIQ/
├── .github/              # GitHub Actions workflows and issue/PR templates
├── backend/              # The entire Node.js/Express.js backend API
│   ├── config/           # Database (MongoDB), Swagger, and other configs
│   ├── controllers/      # Business logic for API routes (e.g., auth, issues)
│   ├── middlewares/      # Custom middleware (e.g., auth, error handling, file uploads)
│   ├── models/           # Mongoose schemas for the database (e.g., User, Issue)
│   ├── routes/           # API endpoint definitions (e.g., auth.js, profileRoutes.js)
│   ├── __tests__/        # Backend tests (Jest)
│   ├── utils/            # Utility functions (e.g., email, token, file upload)
│   ├── .env.example      # Environment variable template for the backend
│   └── server.js         # Main backend server entry point
│
├── cypress/              # End-to-end (E2E) tests
│
├── public/               # Static assets for the frontend
│   ├── gtfs/             # Static data files (CSV, JSON) for app features
│   ├── index.html        # The main HTML template for the React app
│   └── *.png, *.svg      # Public images, logos, and favicons
│
├── src/                  # The main React frontend application source code
│   ├── Pages/            # All top-level page components (e.g., Home, About, ReportIssue)
│   ├── components/       # Reusable UI components (e.g., Navbar, Footer, Chatbot)
│   ├── assets/           # Images and logos imported into React components
│   ├── hooks/            # Custom React hooks (e.g., useProfileStatus)
│   ├── utils/            # Frontend utility functions
│   ├── App.jsx           # Main React app component (routing)
│   └── index.jsx         # React app entry point
│
├── .gitignore            # Files and folders to be ignored by Git
├── LICENSE               # Project's open-source license
├── README.md             # This file
├── package.json          # Frontend dependencies and scripts (React)
└── tailwind.config.js    # Tailwind CSS configuration
```

## 🛠️ Tech Stack  
### Frontend  
- React.js  
- Tailwind CSS – Modern responsive UI  
- Leaflet.js – Interactive maps for location tagging
- AI / ML
- Google Gemini Vision API
- Image Classification
- Prompt Engineering

### Backend  
- Node.js + Express.js  
- PostgreSQL – Relational DB for reports and user data  
- JWT Authentication – Secure role-based access
- Multer – File upload handling
- Swagger – API documentation
- Helmet.js – Security middleware
- Express Rate Limit – API protection

### Integrations  
- Cloudinary – Image uploads and hosting  
- JWT Authentication – Secure role-based access

## 🔧 Backend API Features

### 🔐 Authentication System
- **JWT-based authentication** with role management
- **Admin/User role separation** for different access levels
- **Secure password hashing** using bcrypt
- **Token expiration** and refresh handling

### 📡 RESTful API Endpoints
- **GET /api/issues** - Retrieve all civic issues
- **POST /api/issues** - Create new issue with file upload
- **PATCH /api/issues/:id/status** - Update issue status (Admin only)
- **POST /api/auth/signup** - User registration
- **POST /api/auth/login** - User authentication

### 🛡️ Security Features
- **Rate limiting** (100 requests per 15 minutes)
- **Input validation** using express-validator
- **XSS protection** and security headers
- **CORS configuration** for frontend integration
- **File upload security** with type validation

### 📊 API Documentation
- **Interactive Swagger UI** at `/api-docs`
- **Complete endpoint documentation** with examples
- **Schema definitions** for request/response objects
- **Authentication testing** directly in browser

### 🗄️ Database Integration
- **PostgreSQL** for reliable data storage
- **Optimized queries** with proper indexing
- **User management** with secure credential storage
- **Issue tracking** with status management

### 📁 File Management
- **Image upload** support for issue reporting
- **File validation** and security checks
- **Organized storage** in uploads directory
- **Efficient file handling** with Multer middleware  


## 🌗 Dark Mode Toggle  
**Implementation**:  
- `darkMode: 'class'` in `tailwind.config.js`  
- User preference saved via `localStorage`  
- Toggle switch: `src/ThemeToggle.jsx` (used in `Home.jsx`)  

**How to Use**:  
1. Locate the toggle button (🌙/☀️) in the header  
2. Click to switch between:  
   - **Light Mode**: White/light gray backgrounds (`bg-slate-50`) with dark text (`text-gray-900`)  
   - **Dark Mode**: Dark gray backgrounds (`dark:bg-gray-800`) with light text (`dark:text-gray-100`)  

## 🚀 Getting Started  

()
*Caption: Admin dashboard with issue management tools*

### Prerequisites  
- Node.js 16+  
- npm 8+  
- PostgreSQL 14+  
- Cloudinary account (for image uploads)

## 📡 API Usage Examples

### Authentication
```bash
# Register new user
curl -X POST http://localhost:5000/api/auth/signup \
  -H "Content-Type: application/json" \
  -d '{"username":"john_doe","email":"john@example.com","password":"password123"}'

# Login user
curl -X POST http://localhost:5000/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{"email":"john@example.com","password":"password123"}'
```

### Issue Management
```bash
# Get all issues
curl -X GET http://localhost:5000/api/issues
```
# Create new issue with image
curl -X POST http://localhost:5000/api/issues \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -F "title=Pothole on Main Street" \
  -F "description=Large pothole causing traffic issues" \
  -F "location=Main Street & 5th Ave" \
  -F "category=road" \
  -F "file=@/path/to/image.jpg"

# Update issue status (Admin only)
curl -X PATCH http://localhost:5000/api/issues/1/status \
  -H "Authorization: Bearer ADMIN_JWT_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"status":"in-progress"}'


### API Documentation
- **Swagger UI**: `http://localhost:5000/api-docs`
- **Interactive testing** of all endpoints
- **Complete schema documentation**
- **Authentication examples**  




### Testing
*   **Backend Testing:** Jest, Supertest, MongoDB Memory Server
*   **Frontend Unit/Component Testing:** Vitest, React Testing Library
*   **Frontend E2E Testing:** Cypress


## 📌 Roadmap / Future Enhancements  

## 🚀 CivicIQ Roadmap

### Phase 1 (Current MVP)

 AI Waste Classification
 Waste Reporting
 Complaint Tracking
 Municipal Dashboard

---

### Phase 2

 AI Severity Assessment
 Duplicate Complaint Detection
 AI Priority Score
 Cleanup Action Plans

---

### Phase 3

 Smart Route Optimization
 Waste Hotspot Prediction
 Smart Bin IoT Integration
 Crew & Vehicle Recommendation
 Predict → Prevent → Resolve

--- 

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss your ideas.

--- 

--- 

## 🙏 Acknowledgements

CivicIQ is built upon the open-source Civix project, licensed under the MIT License.

Our team extended the platform by redesigning it specifically for AI-powered waste management, introducing AI-based waste classification, waste-specific workflows, and a roadmap toward intelligent municipal decision support.

<p align="center">
  <a href="#top" style="font-size: 18px; padding: 8px 16px; display: inline-block; border: 1px solid #ccc; border-radius: 6px; text-decoration: none;">
    ⬆️ Back to Top
  </a>
</p>

