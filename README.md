# 🍎 Nutrify - AI-Powered Nutrition & Health Monitoring Platform

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green)](https://nodejs.org/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue)](https://www.python.org/)
[![React](https://img.shields.io/badge/React-18+-61DAFB?logo=react)](https://reactjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.0+-green?logo=mongodb)](https://www.mongodb.com/)
[![Status: Active](https://img.shields.io/badge/Status-Active-success)](https://github.com)

**Nutrify** is an intelligent nutrition and health monitoring platform that leverages artificial intelligence to help users analyze food intake, receive personalized health recommendations, and maintain optimal nutrition with an interactive AI chatbot.

[Features](#-features) • [Installation](#-installation) • [Architecture](#-system-architecture) • [Team](#-team-responsibilities) • [Contributing](#-contributors)

</div>

---

## 📋 Project Overview

Nutrify is a comprehensive capstone project designed to demonstrate the integration of modern web technologies, machine learning, and data science to create a user-centric health and nutrition platform. The platform enables users to:

- **Scan & Analyze** food items using advanced image recognition AI
- **Track Nutrition** intake with real-time dashboard visualization
- **Receive Personalized** health recommendations based on their health profile
- **Interact** with an intelligent nutrition chatbot for health guidance
- **Manage** food preferences, allergies, and dietary restrictions
- **Monitor** nutrition history and health trends

Whether you're a fitness enthusiast, healthcare professional, or someone looking to improve your dietary habits, Nutrify provides intelligent, data-driven insights to support your health journey.

---

## ✨ Features

### 🎯 Core Features

| Feature | Description |
|---------|-------------|
| 📸 **Food Image Recognition** | Advanced AI-powered image recognition to identify food items and estimate portion sizes |
| 📊 **Nutrition Analysis** | Comprehensive nutritional breakdown including calories, macros, and micronutrients |
| 🎯 **Personalized Recommendations** | AI-driven health recommendations based on user profile, health conditions, and dietary preferences |
| 💬 **AI Nutrition Chatbot** | Real-time conversational AI for nutrition guidance and health questions |
| 📈 **Daily Nutrition Dashboard** | Visual representation of daily nutrition intake vs. recommended values |
| 📝 **Nutrition History Tracking** | Complete history of scanned foods and nutrition trends over time |
| 👤 **Health Personalization Profile** | Comprehensive user profile including age, health conditions, dietary preferences, and allergies |
| 🏥 **Disease-Based Recommendations** | Specialized nutrition recommendations for specific health conditions (diabetes, hypertension, etc.) |
| ⚠️ **Food Preference & Allergy Management** | Track allergies, intolerances, and food preferences for safe recommendations |

---

## 📁 Repository Structure

```
Project-Utama/
├── 🤖 AI/
│   └── AI/                          # AI/ML models and API integration
│       ├── app/
│       │   ├── main.py              # FastAPI application entry point
│       │   ├── core/                # Configuration and logging
│       │   ├── models/              # CNN model architecture
│       │   ├── routers/             # API endpoints
│       │   ├── schemas/             # Data validation schemas
│       │   └── services/            # Business logic
│       ├── nutrify_model.keras      # Trained food recognition model
│       ├── class_names.json         # Food classification labels
│       ├── indonesian_food_clean.csv # Training dataset
│       ├── requirements.txt         # Python dependencies
│       ├── Dockerfile              # Container configuration
│       └── README.md               # AI module documentation
│
├── 📊 Datascience/
│   └── Data/                        # Data science and analytics
│       ├── dashboard/
│       │   ├── app.py              # Streamlit analytics dashboard
│       │   └── clean_dataset.csv   # Processed nutrition dataset
│       ├── data_dictionary.md      # Dataset documentation
│       ├── requirements.txt        # Python dependencies
│       └── README.md              # Data science documentation
│
└── 🌐 Fullstack/
    └── Full-Stack/                  # Complete web application
        ├── backend-nutrify/         # Node.js/Express REST API
        │   ├── src/
        │   │   ├── config/          # Database and seed configuration
        │   │   ├── controllers/     # Request handlers
        │   │   ├── middlewares/     # Authentication and logging
        │   │   ├── models/          # MongoDB schemas
        │   │   ├── routes/          # API routes
        │   │   └── services/        # Business logic
        │   ├── csv/                 # Data files
        │   ├── app.js              # Express app setup
        │   ├── server.js           # Server entry point
        │   ├── package.json        # Node dependencies
        │   └── vercel.json         # Deployment configuration
        │
        └── frontend-nutrify/        # React/Vite web application
            ├── src/
            │   ├── components/      # Reusable UI components
            │   ├── features/        # Feature modules (Auth, Dashboard, etc.)
            │   ├── hooks/           # Custom React hooks
            │   ├── layout/          # Page layouts
            │   ├── utils/           # Utility functions
            │   ├── config/          # Firebase and API config
            │   ├── App.jsx         # Root component
            │   └── main.jsx        # Application entry point
            ├── public/             # Static assets
            ├── index.html          # HTML template
            ├── vite.config.js      # Vite configuration
            ├── package.json        # Node dependencies
            ├── vercel.json         # Deployment configuration
            └── README.md           # Frontend documentation
```

---

## 🛠️ Technology Stack

### Frontend Development
```
Framework:     React 18+
Build Tool:    Vite
Styling:       Tailwind CSS
State:         Context API / Custom Hooks
UI Components: shadcn/ui
Auth:          Firebase Authentication
Deployment:    Vercel
```

### Backend Development
```
Runtime:       Node.js 18+
Framework:     Express.js
Database:      MongoDB Atlas
Authentication: JWT
API Format:    RESTful
Deployment:    Vercel / Cloud Services
```

### Artificial Intelligence & ML
```
Food Recognition:      Gemini API + Custom CNN
AI Chatbot:           Gemini API
ML Framework:         TensorFlow/Keras
Model Type:           Convolutional Neural Network (CNN)
Training Data:        Indonesian Food Dataset
Languages:            Python 3.8+
API Framework:        FastAPI
```

### Data Science
```
Data Processing:      Pandas, NumPy
Visualization:        Streamlit, Matplotlib, Plotly
Datasets:            Nutrition, Food, Health Recommendations
Analysis Tools:       Jupyter Notebooks
```

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                      Client Layer (Frontend)                      │
│                     React 18 + Vite + Tailwind                    │
│                    (Deployed on Vercel)                           │
└──────────────────────────┬──────────────────────────────────────┘
                           │ HTTP/REST API Calls
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│                    API Gateway Layer (Backend)                    │
│              Node.js + Express.js (Vercel Deployment)             │
│                                                                    │
│  ┌──────────────────┐  ┌──────────────────┐  ┌──────────────┐   │
│  │  User Routes     │  │  Food Routes     │  │  Chat Routes │   │
│  ├──────────────────┤  ├──────────────────┤  ├──────────────┤   │
│  │  Auth Middleware │  │  History Routes  │  │ Scan Routes  │   │
│  └──────────────────┘  └──────────────────┘  └──────────────┘   │
│                                                                    │
└──────────┬─────────────────────────────────────┬──────────────────┘
           │                                     │
           ▼                                     ▼
┌──────────────────────────────┐  ┌─────────────────────────────┐
│    Data Layer (MongoDB)      │  │  AI Services Layer (Python)  │
│   - User Profiles            │  │                              │
│   - Nutrition History        │  │  ┌──────────────────────┐   │
│   - Food Database            │  │  │ Food Recognition API │   │
│   - Chat History             │  │  │ (FastAPI + CNN)      │   │
│   - Health Recommendations   │  │  └──────────────────────┘   │
└──────────────────────────────┘  │                              │
                                  │  ┌──────────────────────┐   │
                                  │  │ Chatbot Service      │   │
                                  │  │ (Gemini API)         │   │
                                  │  └──────────────────────┘   │
                                  └─────────────────────────────┘
                                           │
                                           ▼
                            ┌──────────────────────────┐
                            │  External AI Services    │
                            │  - Google Gemini API     │
                            │  - Food Recognition API  │
                            └──────────────────────────┘
```

### Data Flow

1. **Food Scanning**: User captures image → Frontend sends to Backend → Backend calls AI Service → CNN model identifies food → Nutrition data retrieved
2. **Chatbot**: User message → Backend → Gemini API → Response generation → Real-time streaming
3. **Recommendations**: User profile + Health history → Recommendation Engine → Personalized advice based on health conditions

---

## 📦 Installation Guide

### Prerequisites

Before you begin, ensure you have installed:

- **Node.js** (v18 or higher) - [Download](https://nodejs.org/)
- **Python** (v3.8 or higher) - [Download](https://www.python.org/)
- **MongoDB Atlas** account - [Sign up](https://www.mongodb.com/cloud/atlas)
- **Google Gemini API** key - [Get API Key](https://makersuite.google.com/app/apikey)
- **Git** - [Download](https://git-scm.com/)

### Clone the Repository

```bash
# Clone the repository
git clone https://github.com/yourusername/nutrify.git

# Navigate to project directory
cd nutrify
```

### Backend Setup

```bash
# Navigate to backend directory
cd Fullstack/Full-Stack/backend-nutrify

# Install dependencies
npm install

# Create .env file (see Environment Variables section below)
cp .env.example .env

# Start backend server
npm start
# Server runs at http://localhost:3000
```

### Frontend Setup

```bash
# Navigate to frontend directory (from project root)
cd Fullstack/Full-Stack/frontend-nutrify

# Install dependencies
npm install

# Create .env file (see Environment Variables section below)
cp .env.example .env

# Start development server
npm run dev
# Application runs at http://localhost:5173
```

### AI Service Setup

```bash
# Navigate to AI directory
cd AI/AI

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start API server
python -m uvicorn app.main:app --reload
# API runs at http://localhost:8000
```

### Data Science Dashboard Setup

```bash
# Navigate to Data Science directory
cd Datascience/Data

# Create virtual environment
python -m venv venv

# Activate virtual environment
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run Streamlit dashboard
streamlit run dashboard/app.py
# Dashboard opens at http://localhost:8501
```

---

## 🔐 Environment Variables

### Backend (.env) - `backend-nutrify/.env`

```env
# Server Configuration
PORT=3000
NODE_ENV=development

# Database
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/nutrify?retryWrites=true&w=majority

# Firebase
FIREBASE_API_KEY=your_firebase_api_key
FIREBASE_AUTH_DOMAIN=your_firebase_project.firebaseapp.com
FIREBASE_PROJECT_ID=your_firebase_project_id
FIREBASE_STORAGE_BUCKET=your_firebase_project.appspot.com
FIREBASE_MESSAGING_SENDER_ID=your_firebase_sender_id
FIREBASE_APP_ID=your_firebase_app_id

# AI Services
GEMINI_API_KEY=your_gemini_api_key
AI_SERVICE_URL=http://localhost:8000
FOOD_RECOGNITION_API=your_food_recognition_api_key

# JWT
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d

# CORS
CORS_ORIGIN=http://localhost:5173
```

### Frontend (.env) - `frontend-nutrify/.env`

```env
# API Configuration
VITE_API_BASE_URL=http://localhost:3000/api
VITE_AI_SERVICE_URL=http://localhost:8000

# Firebase
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_firebase_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_firebase_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_firebase_sender_id
VITE_FIREBASE_APP_ID=your_firebase_app_id

# Gemini API
VITE_GEMINI_API_KEY=your_gemini_api_key

# Environment
VITE_ENV=development
```

### AI Service (.env) - `AI/AI/.env`

```env
# Server Configuration
HOST=127.0.0.1
PORT=8000
DEBUG=True

# Model Configuration
MODEL_PATH=./nutrify_model.keras
CLASS_NAMES_PATH=./class_names.json

# API Keys
GEMINI_API_KEY=your_gemini_api_key

# Database
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/nutrify

# CORS
CORS_ORIGINS=["http://localhost:5173", "http://localhost:3000"]
```

---

## 🚀 Running the Application

### Development Mode (All Services)

#### Terminal 1 - Backend
```bash
cd Fullstack/Full-Stack/backend-nutrify
npm start
```

#### Terminal 2 - Frontend
```bash
cd Fullstack/Full-Stack/frontend-nutrify
npm run dev
```

#### Terminal 3 - AI Service
```bash
cd AI/AI
source venv/bin/activate  # or venv\Scripts\activate
python -m uvicorn app.main:app --reload
```

#### Terminal 4 - Data Science Dashboard (Optional)
```bash
cd Datascience/Data
source venv/bin/activate  # or venv\Scripts\activate
streamlit run dashboard/app.py
```

### Access Points

| Service | URL | Purpose |
|---------|-----|---------|
| Frontend | `http://localhost:5173` | Web Application |
| Backend API | `http://localhost:3000/api` | REST API Endpoints |
| AI Service Docs | `http://localhost:8000/docs` | API Documentation |
| Data Dashboard | `http://localhost:8501` | Analytics Dashboard |

---

## 🤖 AI Integration Overview

### Food Image Recognition

The platform utilizes a **Convolutional Neural Network (CNN)** model trained on Indonesian food dataset to recognize food items from images.

**Workflow:**
1. User uploads food image via mobile/web app
2. Image sent to AI FastAPI service
3. CNN model processes and identifies food
4. Nutrition data retrieved from database
5. Results returned to frontend

**Model Details:**
- **Framework**: TensorFlow/Keras
- **Model File**: `nutrify_model.keras`
- **Training Data**: `indonesian_food_clean.csv`
- **Accuracy**: >85% on test dataset
- **Classes**: 100+ Indonesian food items

### AI Nutrition Chatbot

Powered by **Google Gemini API**, the chatbot provides real-time nutrition and health guidance.

**Capabilities:**
- Answer nutrition questions
- Provide dietary recommendations
- Suggest meal plans
- Alert about allergies and dietary restrictions
- Track conversation history for personalized advice

**Integration:**
- Real-time streaming responses
- Context-aware recommendations
- History tracking in MongoDB

### Personalized Recommendation Engine

**Algorithm:**
1. Analyze user health profile (age, conditions, preferences)
2. Review nutrition history
3. Apply disease-specific nutrition rules
4. Generate personalized recommendations
5. Consider allergies and food preferences

---

## 👥 Team Responsibilities

### 🤖 AI Team (AI Module)

**Ownership**: Food recognition AI and food-related APIs

**Responsibilities:**
- Develop and train CNN food recognition model
- Maintain FastAPI service for image processing
- Integrate Gemini API for chatbot functionality
- Manage food classification system
- API documentation and testing
- Performance optimization for image processing
- Model version management and updates

**Key Deliverables:**
- `nutrify_model.keras` - Trained CNN model
- FastAPI application with endpoints:
  - `POST /api/predict` - Food recognition
  - `GET /api/nutrition/{food_id}` - Nutrition data
- Integration with Gemini API for chatbot

### 📊 Data Science Team (Datascience Module)

**Ownership**: Nutrition dataset, analysis, and recommendations

**Responsibilities:**
- Maintain nutrition and food datasets
- Create and manage recommendation algorithms
- Build analytics dashboard
- Generate health insights and statistics
- Data validation and quality assurance
- Create visualizations for nutrition trends
- Develop disease-based recommendation rules

**Key Deliverables:**
- `indonesian_food_clean.csv` - Food nutrition database
- Recommendation algorithm implementation
- Streamlit analytics dashboard
- Data documentation and dictionary

### 🌐 Full Stack Team (Fullstack Module)

**Ownership**: Web application, backend API, and user experience

**Responsibilities:**
- Develop and maintain Express.js REST API
- Build responsive React frontend
- Manage MongoDB database schema and queries
- Implement user authentication and authorization
- Integrate with AI and Data Science services
- Deploy frontend and backend applications
- Performance optimization and security
- API documentation and testing

**Key Deliverables:**
- RESTful API with endpoints for:
  - User management (registration, profile)
  - Food scanning history
  - Nutrition tracking
  - Chat functionality
  - Recommendations
- React web application with features:
  - User authentication
  - Food scanning interface
  - Nutrition dashboard
  - History tracking
  - Chatbot interface
  - Personalization settings

**Sub-team Structure:**

- **Backend (Node.js/Express)**
  - API design and implementation
  - Database modeling
  - Authentication/authorization
  - Service integration
  - API testing

- **Frontend (React/Vite)**
  - UI/UX implementation
  - Component architecture
  - State management
  - API integration
  - Performance optimization

---

## 🔮 Future Development

### Phase 2 Features

- 🏋️ **Advanced Health Metrics**
  - Integration with wearable devices (Fitbit, Apple Watch)
  - Real-time biometric tracking
  - Sleep and exercise monitoring

- 👥 **Social Features**
  - Community nutrition challenges
  - Shared meal plans
  - Social sharing and achievements
  - Friend nutrition comparison

- 📱 **Mobile Application**
  - Native iOS app (Swift)
  - Native Android app (Kotlin)
  - Offline food recognition capability
  - Push notifications for health reminders

- 🔬 **Advanced AI Features**
  - Predictive health analytics
  - Meal plan generation based on health goals
  - Natural language understanding improvements
  - Multi-language support

- 🏥 **Healthcare Integration**
  - Integration with medical professionals
  - Prescription medication tracking
  - Medical history integration
  - Professional nutrition consultation

- 💾 **Data & Analytics**
  - Machine learning model improvements
  - Advanced nutrition algorithms
  - Predictive health recommendations
  - Research-grade data exports

---

## 📚 Documentation

Each module includes detailed documentation:

- [AI Module Documentation](./AI/AI/README.md)
- [Data Science Documentation](./Datascience/Data/README.md)
- [Backend Documentation](./Fullstack/Full-Stack/backend-nutrify/README.md)
- [Frontend Documentation](./Fullstack/Full-Stack/frontend-nutrify/README.md)

---

## 🤝 Contributors

### Project Team Members

**AI/ML Engineering**
- [Team Member Names]

**Data Science**
- [Team Member Names]

**Full Stack Development**
- [Team Member Names]

**Project Coordination**
- [Team Lead/Advisor Names]

### How to Contribute

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines

- Follow project coding standards
- Add tests for new features
- Update documentation accordingly
- Ensure code quality with linting
- Write meaningful commit messages

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 📞 Support & Contact

For questions, issues, or suggestions:

- **Issues**: [GitHub Issues](https://github.com/yourusername/nutrify/issues)
- **Email**: [your-email@example.com]
- **Discord**: [Join our Discord community]
- **Project Advisor**: [Advisor Name]

---

## 🙏 Acknowledgments

- Indonesian Food Dataset providers
- Google Gemini API team
- MongoDB Atlas for database services
- Vercel for deployment infrastructure
- Open-source community for libraries and tools

---

<div align="center">

Made with ❤️ by the Nutrify Team

⭐ If you find this project helpful, please give it a star!

[Back to Top](#-nutrify---ai-powered-nutrition--health-monitoring-platform)

</div>
