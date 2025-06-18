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


## 📑 Sample User Credentials for BIVGS Testing

All users below share the **default password**: `@0BusiaKenya`

> These accounts are preloaded and mapped to specific dashboards for easy testing

---

### 👨‍👩‍👧‍👦 Parents

- **Parent with 2 children**: `elliot_kedibone@aol.com`  
- **Parent with 1 child**: `alex_binger@gmail.com`

---

### 👩‍🎓 Students

- **Maria Kedibone**: `maria_kedibone@bivgs.no`

---

### 🏫 Administrative Staff

- **Principal**: `simon_galle@testteacher.no`  
- **Vice Principal**: `benny_geys@testteacher.no`

---

### 🧑‍🏫 Heads of Department (HODs)

- `anna_nerstad@testteacher.no`  
- `rachel_wang@testteacher.no`  
- `leah_fieseler@testteacher.no`  
- `martha_andersen@testteacher.no`  
- `esther_brinch@testteacher.no`

---

### 👩‍🏫 Classroom Teachers

- `naomi_bruno@testteacher.no`  
- `lydia_canova@testteacher.no`  
- `joanna_eriksen@testteacher.no`  
- `abigail_fiva@testteacher.no`

---

### 📚 Subject Teachers

- `mary_warlop@testteacher.no`  
- `elizabeth_ehling@testteacher.no`  
- `sarah_stauskas@testteacher.no`  
- `hannah_kisser@testteacher.no`  
- `rebecca_silkoset@testteacher.no`  
- `david_kreiberg@testteacher.no`  
- `lin_ma@testteacher.no`  
- `espen_moen@testteacher.no`  
- `knut_mork@testteacher.no`  
- `plamen_nenov@testteacher.no`  
- `christian_riis@testteacher.no`  
- `alessia_russo@testteacher.no`  
- `erling_larsen@testteacher.no`  
- `albert_satorra@testteacher.no`  
- `genaro_sucarrat@testteacher.no`  
- `anders_tveit@testteacher.no`  
- `adrien_vigier@testteacher.no`  
- `deborah_cross@testteacher.no`  
- `francisco_martinez@testteacher.no`  
- `gisle_natvik@testteacher.no`

---

> ⚠️ **Disclaimer**: All sample accounts were created for academic, demonstration, and development purposes only. All names and email addresses are fictional or anonymized.
                               | @0BusiaKenya |

Each user is routed to a different dashboard, for example:

* `/dashboard/student/`
* `/dashboard/parent/`
* `/dashboard/principal/`
* etc.



---

## 🛠️ Technology Stack

The BIVGS platform is developed using a modern, modular, and extensible technology stack. This stack balances security, scalability, clarity, personalization, and future-readiness, while ensuring a clean user experience and efficient system performance.

### 🔹 Core Development Stack

| Layer              | Technology / Tool       | Purpose                                                                 |
|--------------------|--------------------------|-------------------------------------------------------------------------|
| **Backend Framework** | Django (Python)           | Core web framework for routing, models, role-based views, permissions, and RBAC |
| **Frontend Styling**  | Tailwind CSS             | Utility-first CSS framework enabling responsive, modern, and minimal UIs |
| **Templating Engine** | Django Templates         | Server-side HTML rendering with context-driven dynamic logic           |
| **Database**         | SQLite                   | Lightweight relational DB used for development and testing             |
| **Authentication**   | Django Auth System       | Session management and built-in role-based user access                 |
| **Forms & Validation** | Django Forms           | Validates and processes data (login, assignments, grading, etc.)       |
| **Visualization**     | Chart.js, Plotly.js     | Graphs for grade trends, GPA insights, and performance analysis        |
| **PDF Generation**    | xhtml2pdf (pisa)        | Converts HTML dashboards into branded, print-ready PDF report cards    |
| **PDF Templates**     | Custom HTML Layouts     | Optimized for A4 printing and embedded branding                        |
| **Media Handling**    | MEDIA_ROOT, MEDIA_URL   | Manages uploads: student photos, school logos, and documents           |
| **Static Files**      | Django staticfiles app  | Manages Tailwind CSS, JavaScript, images, and custom styles            |
| **Custom CSS**        | bootstrap_overrides.css | Legacy Bootstrap integration and theme overrides                       |

---

### 🧾 Styling & Print Design Principles

- **Tailwind Themes**: Consistent typography, spacing, color palettes (e.g., `bg-green-500` for success).
- **Role-Based Layouts**: Custom interfaces for each user type (student, parent, teacher, HOD, principal).
- **Print Styles**: Dedicated A4-optimized templates for exportable PDFs.
- **Minimal JavaScript**: Reduced client-side complexity for faster load times and HTMX integration readiness.

---

### 🚧 Planned & Future Technologies

| Technology     | Purpose                                                              |
|----------------|----------------------------------------------------------------------|
| **HTMX**        | Partial page updates with server interaction (AJAX-like, minimal JS) |
| **PostgreSQL**  | Production-grade DB with indexing, concurrency, scalability          |
| **Docker**      | Containerized development and deployment environments                |
| **Celery + Redis** | Asynchronous task queues for background jobs (emails, GPA calc)   |


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

