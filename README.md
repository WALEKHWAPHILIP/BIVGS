# BIVGS: Beyond Individual Grades — Visual & Guided Stories  
_A High School Academic Reporting and Management System_

> Developed for ELE 3921 – Web Applications Development  
> BI Norwegian Business School – Oslo Campus  
> Hand-in date: 05.06.2025

[📺 Project Demo (YouTube)](https://www.youtube.com/watch?v=7P4s3DVCt-E)  
[🔗 GitHub Repository](https://github.com/WALEKHWAPHILIP/BIVGS)

---

## 🧭 Project Overview

**BIVGS** is a Django-based academic reporting and school management platform that goes *beyond individual grades*. It uses **data visualization and role-specific dashboards** to present performance narratives for students, parents, teachers, and school administrators.

---

## 🎯 Features

- ✅ Role-based dashboards: Student, Parent, Teacher, HOD, Principal, Vice Principal
- 📊 Real-time exam analytics and grade insights
- 🧾 Styled PDF report cards (WeasyPrint)
- 📁 Upload and manage CSV data (students, teachers, scores)
- 🖼️ Dynamic chart generation with Matplotlib
- 🔐 Secure login, routing, and dashboard segregation
- 📸 Profile photo & logo management (media handling)

---

## 📁 Project Structure

```

bivgs/
├── BIVGS/                      # Main project settings
├── enrollments/               # Enrollment logic & models
├── exams/                     # Exam score storage and grading logic
├── the\_school/                # Core school metadata & views
├── users/                     # All user dashboards & logic
│   ├── forms\_crud\_transactions/
│   ├── helpers/
│   ├── services/
│   ├── templates/
│   └── views/
├── media/                     # Profile photos, logos
├── static/                    # CSS/JS/images
├── templates/                 # Shared error pages
├── data/csv/                  # Sample CSV datasets
├── manage.py
└── requirements.txt

````

---

## 💻 Running Locally

### 1. Clone the repository

```bash
git clone https://github.com/WALEKHWAPHILIP/BIVGS.git
cd BIVGS
````

### 2. Create and activate a virtual environment

```bash
python -m venv venv
venv\Scripts\activate  # Windows
# or source venv/bin/activate  # Linux/macOS
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply migrations

```bash
python manage.py migrate
```

### 5. Load optional sample data

```bash
python manage.py loaddata sample_data.json  # If available
```

### 6. Run the development server

```bash
python manage.py runserver
```

---

## 📄 Sample & Extended Demo Users

These accounts are preloaded and mapped to specific dashboards for easy testing.

| Role              | Email / Username                                                          | Password     |
| ----------------- | ------------------------------------------------------------------------- | ------------ |
| Parent (2 kids)   | [elliot\_kedibone@aol.com](mailto:elliot_kedibone@aol.com)                | @0BusiaKenya |
| Student           | [maria\_kedibone@bivgs.no](mailto:maria_kedibone@bivgs.no)                | @0BusiaKenya |
| Subject Teacher   | [mary\_warlop@testteacher.no](mailto:mary_warlop@testteacher.no)          | @0BusiaKenya |
| Classroom Teacher | [lydia\_d\_canova@bivgs.no](mailto:lydia_d_canova@bivgs.no)               | @0BusiaKenya |
| HOD               | [mary\_r\_warlop@bivgs.no](mailto:mary_r_warlop@bivgs.no)                 | @0BusiaKenya |
| Principal         | [philip\_walekhwa\_admin@bivgs.no](mailto:philip_walekhwa_admin@bivgs.no) | @0BusiaKenya |
| Vice Principal    | [raymond\_y\_jumah@bivgs.no](mailto:raymond_y_jumah@bivgs.no)             | @0BusiaKenya |
| Administrator     | [admin@bivgs.edu](mailto:admin@bivgs.edu)                                 | @0BusiaKenya |

Each user is routed to a different dashboard, for example:

* `/dashboard/student/`
* `/dashboard/parent/`
* `/dashboard/principal/`
* etc.

> ⚠️ **Disclaimer**: These are test/demo users created for academic and demonstration purposes only. All identities are fictional or anonymized.

---

## 🛠️ Tech Stack

* **Python 3.11+**
* **Django 5.2.3**
* **HTML5, Tailwind, Bootstrap**
* **SQLite (dev-ready), PostgreSQL-ready**
* **Matplotlib** for charting
* **WeasyPrint** for PDF reports
* **Nginx + Gunicorn** for production deployment

---

## 📘 License

MIT License — see [LICENSE](LICENSE) for details.

---

## 👥 Authors

* **Acharya Puskar Raj**
* **Walekhwa Philip Leo Tambiti**
* **Maharjan Attit**

> Developed under ELE 3921 Web Applications Development, BI Norwegian Business School (Spring 2025)

---

## 📎 Additional Resources

* 📄 Full PDF Report: *Exam\_Report\_BIVGS\_Report\_final.pdf*
* 🌐 Live Demo: [https://bivgs.walsoftai.com](https://bivgs.walsoftai.com)

---

````

---

### ✅ Next Step for You

1. Copy and paste the full text above into a file called `README.md` in your project root.
2. Then run:

```bash
git add README.md
git commit -m "Add final README with extended roles and academic context"
git push
````

Would you like a **PDF version** of this README or help adding **badges** (e.g., Python version, license, deployment status)?
