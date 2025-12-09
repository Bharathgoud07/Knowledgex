

# Knowledgex – Student Resource Sharing Portal 📚

Knowledgex is a Django-based web app where students can upload, share and discover:

- Notes & handwritten notes
- Important questions
- Diagrams / charts
- Reference material

It also has favorites, comments, ratings, leaderboards, and basic analytics.

---

## 🧩 Features

- 🔐 **Authentication**
  - Email/username + password login
  - Profile page with avatar, bio, college, branch, links
  - Login streak & longest streak tracking

- 📤 **Resource Uploads**
  - Upload PDF, images, DOCX, PPT/PPTX, ZIP
  - Tag by subject, semester, resource type
  - Basic file preview for:
    - Images
    - PDFs
    - DOCX (first few lines)
    - PPT/PPTX (slide titles)
    - ZIP (file list)

- ⭐ **Engagement**
  - Favorites (Saved resources)
  - Comments + threaded replies
  - Star ratings (1–5)
  - Notifications for comments, replies, ratings, reports

- ✅ **Moderation & Verification**
  - Report resources (wrong / illegal / duplicate)
  - Staff dashboard to approve/reject resources
  - “Trusted” badge for approved content

- 📊 **Analytics**
  - My activity dashboard (views, downloads, uploads, ratings)
  - Subject-wise analytics
  - Admin analytics: uploads per day, visits per day, top subjects, active users
  - Basic leaderboard (top contributors)

---

## 🛠 Tech Stack

- **Backend:** Django 5.x
- **Frontend:** Bootstrap 5 + Bootstrap Icons
- **Database:** SQLite (local dev)
- **Auth:** Django’s built-in auth (`User` + `Profile` model)
- **Other:** Chart.js for charts, Pillow/docx/pptx for previews

---

## 🚀 Running the project locally

### 1. Clone the repo

```bash
git clone https://github.com/<your-username>/knowledgex-django.git
cd knowledgex-django

2. Create & activate a virtual environment (Windows)
python -m venv venv
venv\Scripts\activate

3. Install dependencies
pip install -r requirements.txt


If requirements.txt is not present yet, install Django manually first:

pip install django

4. Run migrations
python manage.py migrate

5. Create a superuser (admin)
python manage.py createsuperuser

6. Run the development server
python manage.py runserver


Visit: http://127.0.0.1:8000/

📁 Important apps

accounts/ – registration, login, profile, streaks, email verification (planned)

resources/ – uploads, comments, ratings, notifications, analytics, leaderboard

core/ – home page, dashboard, common views

🌐 Deployment (Render – planned)

The project is prepared for deployment on Render.com:

requirements.txt – Python dependencies

Procfile – Gunicorn entry point:

web: gunicorn knowledgex.wsgi:application


STATIC_ROOT and MEDIA_ROOT are configured in settings.py.

Deployment steps (short):

Push code to GitHub.

Create a new Web Service on Render from this repo.

Set environment variables (DJANGO_SECRET_KEY, PYTHON_VERSION etc.).

Use a build command that runs migrate + collectstatic.

Use Gunicorn as the start command.

🧑‍💻 Author

Built by Bharath goud – B.Tech CSE student (MRCET COLLEGE), focusing on Django, Python, and real-world student tools.



