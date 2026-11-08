# 🤖 AI Resume Analyzer

An AI-powered Resume Analyzer built using **Java 21, Spring Boot 3, React, and Google Gemini AI**. The application helps job seekers evaluate their resumes against job descriptions, identify missing skills, discover relevant ATS keywords, and receive AI-generated suggestions to improve their resumes.

## 📌 Project Overview

Finding the right job requires more than just having technical skills. A resume should also highlight the skills and qualifications that match the job requirements.

The AI Resume Analyzer simplifies this process by allowing users to upload their resumes in PDF format and provide a job description. The application processes the resume and uses Google's Gemini AI API to generate an analysis with useful feedback.

## ✨ Features

- 📄 **Resume Upload:** Upload resumes in PDF format.
- 🤖 **AI-Powered Analysis:** Uses Google Gemini AI to analyze resume content.
- 📊 **Resume Match Score:** Provides an AI-generated assessment of resume relevance to the job description.
- ✅ **Matched Skills:** Identifies skills that match the job requirements.
- ❌ **Missing Skills:** Highlights relevant skills that are missing from the resume.
- 🔍 **ATS Keywords:** Identifies important keywords from the job description.
- 💡 **Improvement Suggestions:** Provides recommendations to improve resume content.
- 📝 **Resume Summary:** Generates a summary of the resume analysis.
- 💻 **Interactive Interface:** React-based user interface for uploading resumes and viewing analysis results.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Java 21 | Backend programming language |
| Spring Boot 3 | Backend application framework |
| React | Frontend development |
| Vite | Frontend build tool |
| Google Gemini API | AI-powered resume analysis |
| REST APIs | Frontend-backend communication |
| PDF Parsing | Resume text extraction |
| Maven | Java dependency and build management |
| npm | Frontend package management |

## 🏗️ Project Architecture

The application follows a frontend-backend architecture.

```text
              USER
                |
                v
       REACT + VITE FRONTEND
                |
                | REST API
                v
       JAVA + SPRING BOOT
                |
                v
          PDF PROCESSING
                |
                v
         GOOGLE GEMINI API
                |
                v
         AI ANALYSIS RESULT
                |
                v
        REACT RESULTS DASHBOARD
```

## ⚙️ Application Workflow

1. The user opens the AI Resume Analyzer application.
2. The user uploads a resume in PDF format.
3. The user enters the target job description.
4. The React frontend sends the resume and job description to the Spring Boot backend.
5. The backend extracts text from the uploaded PDF.
6. The extracted resume text and job description are sent to Google Gemini AI.
7. Gemini analyzes the resume against the job requirements.
8. The backend processes the AI response and returns the analysis.
9. The frontend displays the resume match score, matched skills, missing skills, ATS keywords, summary, and suggestions.

## 📂 Project Structure

```text
AI-Resume-Analyzer/
│
├── backend/
│   └── resume-analyzer-api/
│       ├── src/
│       │   └── main/
│       │       ├── java/
│       │       └── resources/
│       │           └── application.properties
│       └── pom.xml
│
├── frontend/
│   └── resume-analyzer-ui/
│       ├── src/
│       ├── public/
│       ├── package.json
│       └── vite.config.js
│
└── README.md
```

*Note: This is the high-level project structure. Individual source files may vary.*

## 🚀 Getting Started

Follow these instructions to run the project locally.

### 1. Prerequisites

Install the following software:

- Java 21
- Apache Maven
- Node.js and npm
- Git
- Google Gemini API key

### 2. Clone the Repository

```bash
git clone https://github.com/Manikandan4411/AI-Resume-Analyzer.git
```

Navigate to the project directory:

```bash
cd AI-Resume-Analyzer
```

### 3. Backend Setup

Navigate to the backend directory:

```bash
cd backend/resume-analyzer-api
```

Configure your Gemini API key in:

`src/main/resources/application.properties`

Add the following configuration:

```properties
spring.application.name=resume-analyzer-api
server.port=8080

gemini.api.key=YOUR_GEMINI_API_KEY
```

Replace `YOUR_GEMINI_API_KEY` with your own API key.

**Important:** Never upload your actual API key to GitHub. Keep sensitive credentials private.

Start the Spring Boot application:

```bash
mvn spring-boot:run
```

Backend runs at:

`http://localhost:8080`

### 4. Frontend Setup

Open another terminal and navigate to:

```bash
cd frontend/resume-analyzer-ui
```

Install dependencies:

```bash
npm install
```

Start the frontend:

```bash
npm run dev
```

Frontend runs at:

`http://localhost:5173`

### 5. Access the Application

Open the following URL in your browser:

```text
http://localhost:5173
```

Make sure both the backend and frontend servers are running.

## 🔐 API Configuration and Security

- The Gemini API key is required for AI-based analysis.
- API credentials should be stored securely and excluded from version control.
- Uploaded resumes may contain personal information, so they should be handled securely.
- Validate uploaded files and handle API errors appropriately.

## 🗄️ Database

The current version does not include SQL or MySQL database integration. Resume analysis is performed through the backend and Gemini AI API.

Database integration is planned as a future enhancement.

## 🔮 Future Enhancements

- MySQL database integration.
- User registration and authentication.
- Save and retrieve previous resume analysis results.
- Resume analysis history.
- Downloadable analysis reports in PDF format.
- OCR support for scanned resumes.
- Support for additional resume file formats.
- Enhanced ATS matching and skill analysis.

## 🎯 Project Objectives

- Apply Java and Spring Boot concepts in a real-world application.
- Develop REST API-based backend functionality.
- Integrate external generative AI services.
- Understand frontend-backend communication.
- Build a practical AI-powered recruitment assistance tool.

**Built with Java, Spring Boot, React and Google Gemini AI.**
