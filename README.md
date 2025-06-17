
# 🏫 BIVGS: BI-Driven Virtual Grading System

**Django-based school data dashboard and academic reporting platform.**  
Includes role-based dashboards for students, parents, teachers, principals, and administrators — all powered by exam analytics, PDF reports, and real-time data visualization.

---

## 🎯 Features

- ✅ Student, Parent, Teacher, HOD, Principal, and Vice Principal dashboards
- 📊 Exam analytics and grade insights
- 🧾 PDF report cards
- 📁 Upload and manage CSV school data (students, teachers, subjects, etc.)
- 🖼️ Dynamic chart generation using Matplotlib
- 🔐 Role-based authentication & routing
- 📸 Support for user profile photos and school logos

---

## 📂 Project Structure

```

bivgs/
│
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
├── media/                     # Profile photos & logos
├── static/                    # Static CSS/JS/images
├── templates/                 # Shared error templates
├── data/csv/                  # Preloaded CSV school datasets
├── manage.py
└── requirements.txt

````

---

## 🚀 Running Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/WALEKHWAPHILIP/BIVGS.git
   cd BIVGS
````

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply migrations and load sample data**

   ```bash
   python manage.py migrate
   python manage.py loaddata sample_data.json  # If available
   ```

5. **Run the server**

   ```bash
   python manage.py runserver
   ```

---

## 📄 Sample and Extended Users

Below are sample credentials for testing different user roles. These accounts are preloaded and mapped to actual dashboard views.

| Role              | Username / Email                                                 | Password     |
| ----------------- | ---------------------------------------------------------------- | ------------ |
| Parent (2 kids)   | [elliot\_kedibone@aol.com](mailto:elliot_kedibone@aol.com)       | @0BusiaKenya |
| Student           | [maria\_kedibone@bivgs.no](mailto:maria_kedibone@bivgs.no)       | @0BusiaKenya |
| Subject Teacher   | [mary\_warlop@testteacher.no](mailto:mary_warlop@testteacher.no) | @0BusiaKenya |
| Classroom Teacher | \[See full list below]                                           | @0BusiaKenya |

### 🔐 Extended User Accounts (Testing Various Dashboards)

| Role                  | Email                                                                     | Dashboard Route                |
| --------------------- | ------------------------------------------------------------------------- | ------------------------------ |
| **Classroom Teacher** | [lydia\_d\_canova@bivgs.no](mailto:lydia_d_canova@bivgs.no)               | /dashboard/classroom\_teacher/ |
| **HOD Teacher**       | [mary\_r\_warlop@bivgs.no](mailto:mary_r_warlop@bivgs.no)                 | /dashboard/hod\_teacher/       |
| **Subject Teacher**   | [maria\_r\_kedibone@bivgs.no](mailto:maria_r_kedibone@bivgs.no)           | /dashboard/subject\_teacher/   |
| **Principal**         | [philip\_walekhwa\_admin@bivgs.no](mailto:philip_walekhwa_admin@bivgs.no) | /dashboard/principal/          |
| **Vice Principal**    | [raymond\_y\_jumah@bivgs.no](mailto:raymond_y_jumah@bivgs.no)             | /dashboard/vice\_principal/    |
| **Parent**            | [elliot\_kedibone@bivgs.no](mailto:elliot_kedibone@bivgs.no)              | /dashboard/parent/             |
| **Student**           | [alex\_walekhwa@bivgs.no](mailto:alex_walekhwa@bivgs.no)                  | /dashboard/student/            |

📝 **Note:** All users share the same password: `@0BusiaKenya`.

> **Disclaimer:** These accounts were created strictly for demonstration and testing. All names, emails, and details are fictional or anonymized. Any resemblance to real individuals is purely coincidental.

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

````

---

### 🔄 Next Step

1. Save this content in a file named `README.md` in the root of your local project.
2. Then run:

```bash
git add README.md
git commit -m "Add complete project README with extended user roles"
git push
````


