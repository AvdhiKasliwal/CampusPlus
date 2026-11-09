# CampusPlus – Digital Campus Ecosystem 🎓

CampusPlus is a centralized digital campus platform designed to simplify and enhance student life by bringing essential academic and campus-related services together in one place.

The platform provides students with access to academic resources, campus clubs, events, placement opportunities, and accommodation listings through a unified web-based application. It also includes dedicated interfaces for club heads and administrators to manage campus activities and content efficiently.

## 🚀 Features

### 👨‍🎓 Student Portal
- Student registration and login with email OTP verification.
- Personalized student dashboard.
- Browse campus clubs and their details.
- Explore upcoming college events and activities.
- View and share accommodation listings.
- Access placement opportunities and company information.
- Submit requests for additional user roles.
- Upload and share campus-related content.

### 📚 Academic Resource Management
- Course-wise academic resource organization.
- Subject-wise notes and previous year question papers (PYQs).
- Academic project sharing and uploads.
- Centralized access to learning materials.

### 🏛️ Club Management
- Dedicated dashboard for club heads.
- Manage club information and details.
- Upload and manage club gallery images.
- Create and manage club events.

### 🛠️ Admin Dashboard
- Manage registered users and their roles.
- Approve or reject role requests.
- Moderate uploaded content.
- Add, edit, and delete clubs.
- Manage courses and subjects.
- Manage company and placement information.
- Maintain administrative activity logs.

### 🏠 Accommodation & Placement
- Browse accommodation listings.
- Add accommodation details and reviews.
- Explore placement drives and company information.
- Access centralized placement-related updates.

## 🧰 Tech Stack

| Category | Technologies |
|---|---|
| Backend | Python, Flask |
| Frontend | HTML5, CSS3 |
| Database | PostgreSQL |
| Database Connectivity | Psycopg2 |
| Email Services | Flask-Mail |
| File & Image Storage | Cloudinary |
| Environment Management | Python Dotenv |
| Version Control | Git, GitHub |

## 📁 Project Structure

```text
CampusPlus/
│
├── app.py
├── helpers.py
├── requirements.txt
│
├── routes/
│   ├── __init__.py
│   ├── auth.py
│   ├── student.py
│   ├── academics.py
│   ├── club_head.py
│   └── admin.py
│
├── templates/
│   ├── academics/
│   ├── login.html
│   ├── signup.html
│   ├── dashboard.html
│   ├── clubs.html
│   ├── events.html
│   ├── accommodations.html
│   ├── placements.html
│   └── admin templates
│
├── static/
│   └── css/
│
├── schema.sql
├── seed.sql
├── seed_events.py
├── seed_accommodations.py
└── test_academic_routes.py
```

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/AvdhiKasliwal/CampusPlus.git
cd CampusPlus
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows:**
```bash
venv\Scripts\activate
```

**Mac/Linux:**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
pip install cloudinary
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory and configure the following variables:

```env
SECRET_KEY=your_secret_key

DB_HOST=localhost
DB_PORT=5432
DB_NAME=campusplus
DB_USER=postgres
DB_PASSWORD=your_database_password

MAIL_SERVER=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your_email
MAIL_PASSWORD=your_app_password

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

**Note:** Never upload your `.env` file or expose database credentials, email passwords, or API keys publicly.

### 5. Configure PostgreSQL Database

Create a PostgreSQL database named `campusplus`.

```sql
CREATE DATABASE campusplus;
```

Initialize the database schema:

```bash
psql -U postgres -d campusplus -f schema.sql
```

Load the initial database records:

```bash
psql -U postgres -d campusplus -f seed.sql
```

### 6. Run the Application

```bash
python app.py
```

Open your browser and visit:

```text
http://127.0.0.1:5000/
```

## 🎯 Project Objectives

- Create a unified digital platform for campus activities and academic resources.
- Improve communication and information accessibility among students.
- Simplify the management of clubs, events, and placement opportunities.
- Provide centralized academic resource sharing.
- Enable efficient administration through role-based access.

## 🔮 Future Scope

- Cloud deployment using AWS services.
- Mobile application integration.
- Real-time notifications for campus events and announcements.
- Advanced analytics for student engagement.
- Integration with additional university services.

## 👩‍💻 Developer

**Avdhi Kasliwal**

B.Tech – Electronics and Communication Engineering (AI & ML)

MIT World Peace University, Pune

## 📄 License

This project is developed as an academic project. All rights reserved to the project developer.
