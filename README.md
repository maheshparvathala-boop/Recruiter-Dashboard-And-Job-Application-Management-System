🛠 Tech Stack
Backend

Java 17

Spring Boot 3

Spring Security (JWT Auth)

Spring Data JPA

MySQL Database

Maven

Frontend

React 18

Axios

React Router

Tailwind/Bootstrap (optional UI styling)

✨ Features
👤 User Features

Register/Login using JWT

Role-based login (Applicant/Recruiter)

Edit profile & upload profile picture

🧑‍💼 Recruiter Features

Post new job positions

View only their posted jobs

View all applications for a job

Change application status (Accepted/Rejected/Pending)

📝 Applicant Features

Browse all jobs

View job details

Apply for jobs

Upload resume (PDF/DOC)

Track application status

🔐 Security

JWT Token Authentication

Role-based authorization

Secured API endpoints

📁 Project Folder Structure
project/
├── backend/
│   ├── src/main/java/com/project/
│   │   ├── controller/
│   │   ├── service/
│   │   ├── repository/
│   │   ├── model/
│   │   ├── security/
│   │   └── RecruiterJobApplication.java
│   └── src/main/resources/application.properties
│
└── frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── api.js
    │   └── App.js

🗄 Database Schema
Users Table
Field	Type	Description
id	int	Primary Key
name	varchar	User name
email	varchar	Login email
password	varchar	Encrypted
role	varchar	APPLICANT / RECRUITER
profilePhoto	varchar	Uploaded image URL
Jobs Table
Field	Description
id	Job ID
title	Job Title
description	Full Job Description
location	City/State
skills	Required Skills
postedBy	Recruiter ID
Applications Table
Field	Description
id	Application ID
jobId	Linked Job
applicantId	Linked Applicant
resumeUrl	Uploaded Resume
status	Pending/Accepted/Rejected
⚙ Backend Setup
Update application.properties:
server.port=5000
spring.datasource.url=jdbc:mysql://localhost:3306/jobportal
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
spring.jpa.hibernate.ddl-auto=update

app.jwt.secret=YOUR_SECRET_KEY

Run Backend:
cd backend
mvn spring-boot:run


Backend runs at:
👉 http://localhost:5000

🌐 Frontend Setup
cd frontend
npm install
npm start


Frontend runs at:
👉 http://localhost:3000

🔗 API Endpoints (Quick View)
Authentication

POST /api/auth/register

POST /api/auth/login

Jobs

POST /api/jobs (Recruiter only)

GET /api/jobs

GET /api/jobs/{id}

GET /api/jobs/mine (Recruiter)

Applications

POST /api/apply

GET /api/applications/mine

PUT /api/applications/{id}/status

🧪 Testing Instructions

Login using recruiter credentials → Post job

Login using applicant credentials → Apply

Check recruiter dashboard → View applications

🚀 Future Enhancements

Admin Dashboard

Email Notifications

AI-based Resume Screening

Chat between Recruiter & Applicant

🤝 Contribution

Pull requests are welcome.
Feel free to open issues for bugs or enhancements.
