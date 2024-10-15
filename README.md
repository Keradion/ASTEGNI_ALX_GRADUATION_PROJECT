# ASTEGNI_ALX_GRADUATION_PROJECT
A web application to connect parents with tutors.

I understand you might be facing issues copying and pasting the content into GitHub. Below, I've provided the README content in a plain text format to make it easier for you to copy:

```
# 🧑‍🏫 Tutor Finder Web Application

## Overview

**Tutor Finder** is a Django-based web application that allows **parents** to search for **tutors** based on various criteria, view tutor profiles, and submit requests to hire them. The application includes user authentication with **JWT** and **OAuth**, allows **tutor ratings**, and integrates **email notifications**. The backend is designed with **MongoDB** for scalability, and the app supports **load balancing** across multiple servers using **Redis**.

---

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Features Breakdown](#features-breakdown)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)

---

## 🎯 Features

- **User Authentication**: Sign up/login using email and password or via **Google OAuth**.
- **JWT-Based Security**: Protects the application using **JSON Web Tokens** for API security.
- **Tutor Listings**: Browse and filter through a list of tutors, categorized by their field of study, experience, and more.
- **Tutor Request**: Parents can request a tutor by submitting a form, which notifies the tutor.
- **Tutor Rating System**: Rate tutors based on your experience.
- **Email Notifications**: Automatic emails to tutors and parents upon request submission.
- **Load Balancing**: Ensure smooth performance using multiple servers, distributed via **Redis**.
- **MongoDB**: Handles tutor and parent data in a scalable NoSQL database.

---

## 🚀 Technologies Used

- **Frontend**:
  - HTML5, CSS3 (For Login, Signup pages, and basic UI)
  - JavaScript (with jQuery/AJAX)
  
- **Backend**:
  - Django (REST Framework for APIs)
  - JWT (JSON Web Tokens for authentication)
  - OAuth (Google OAuth for social login)
  
- **Database**:
  - MongoDB (for tutor and parent data)
  
- **Caching**:
  - Redis (for caching and session management)
  
- **Load Balancing**:
  - Multiple server instances with load balancing
  
- **Email**:
  - SMTP (for sending email notifications)

---

## 🛠️ Installation

### Prerequisites
- Python 3.x
- MongoDB
- Redis
- Node.js (optional, if using npm for frontend dependencies)

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/tutor-finder.git
   cd tutor-finder
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv env
   source env/bin/activate   # On Windows use: env\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up MongoDB and Redis**:
   - Make sure **MongoDB** and **Redis** are running on your local machine or in the cloud.

5. **Create environment variables**:
   - Create a `.env` file to store sensitive data like your database connection string, Redis config, and API keys.
   ```bash
   SECRET_KEY=<your-django-secret-key>
   MONGODB_URI=<your-mongodb-uri>
   REDIS_URL=<your-redis-url>
   ```

6. **Run the Django app**:
   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

---

## 🏃 Usage

### Running the Application

- Visit `http://127.0.0.1:8000` to access the home page.
- Sign up as a **parent** or **tutor** using either an email/password combination or **Google OAuth**.
- Search for available tutors, filter by subject, and click the "Request Tutor" button to submit your interest.
- After submitting a request, both the parent and the tutor will receive email notifications.

---

## 📊 API Endpoints

Here are the key API endpoints available in the app:

### **Authentication**:
- `POST /api/auth/register/`: Register a new user.
- `POST /api/auth/login/`: Login with email and password.
- `POST /api/auth/oauth/google/`: Login or register via Google OAuth.
- `POST /api/auth/refresh-token/`: Refresh JWT tokens.

### **Tutor Listings**:
- `GET /api/tutors/`: List all available tutors.
- `GET /api/tutors/<id>/`: Get detailed information about a specific tutor.
- `POST /api/tutors/<id>/request/`: Submit a request to hire a tutor.

### **Rating**:
- `POST /api/tutors/<id>/rate/`: Submit a rating for a tutor.
  
---

## 📝 Features Breakdown

### 1. **Authentication**
   - **JWT** and **OAuth** are used for secure user authentication.
   - The registration/login process uses **email** or **Google OAuth**.
   - Sessions are managed through **JWT** to ensure security.

### 2. **Tutor Listings**
   - The tutor listings include details like **name**, **field of study**, **rating**, and a **request button**.
   - Filter tutors based on various fields (e.g., subjects, ratings).

### 3. **Request Tutor**
   - Parents can request a tutor by clicking the "Request Tutor" button on a tutor's profile.
   - Once a request is submitted, an **email notification** is sent to both the tutor and the parent.

### 4. **Tutor Rating System**
   - After using a tutor, parents can submit a **rating** which is averaged to create the tutor's overall rating.
   - The rating system will adjust based on the number of ratings and the overall score.

### 5. **Notifications**
   - **Email notifications** are sent when a tutor request is made or a rating is submitted. These notifications can CC your team as needed.

---

## 🚧 Future Improvements

- **Mobile Responsiveness**: Create a mobile-friendly version of the app.
- **Real-Time Notifications**: Integrate WebSockets for real-time tutor notifications.
- **Payment Integration**: Add the ability for parents to pay tutors directly through the app using services like **Telebirr**.
- **Chat System**: Add a feature where parents and tutors can chat directly through the platform.

---

## 🤝 Contributing

Contributions are welcome! Here's how you can contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/new-feature`).
3. Commit your changes (`git commit -m 'Add a new feature'`).
4. Push to the branch (`git push origin feature/new-feature`).
5. Open a **Pull Request**.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
```

### Instructions to Copy and Paste:

1. **Select the Text**: Click and drag your mouse from the beginning to the end of the text to highlight it.
2. **Copy**: Right-click and select **Copy** or use `Ctrl+C` (Windows) or `Command+C` (Mac).
3. **Paste in GitHub**: Go to your GitHub repository, click on the `Add file` button, select `Create new file`, name it `README.md`, and paste the copied content using `Ctrl+V` (Windows) or `Command+V` (Mac).

This should help you integrate the README into your GitHub repository without any issues. Let me know if you need further assistance!
