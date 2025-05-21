# django-cms-secured

A secure content management system built with Django. Designed as a hands-on project to understand user roles, dynamic content handling, and common web security flaws.

---

## 🎯 Learning Objectives

- ✅ Build a Django CMS with Posts, Comments, and Markdown support
- ✅ Implement manual Role-Based Access Control (RBAC)
- ✅ Harden against XSS via form inputs and markdown rendering
- ✅ Secure admin routes and access control
- ✅ Audit for common misconfigurations

## 🔒 Security Focus

This project includes:
- Input sanitization for comment/post fields
- Restricted access to admin-only views
- Manual permissions layer (`permissions.py`)
- Markdown safely rendered via `bleach` or `markdown2`
- Checklist in `audit-checklist.md` to track security fixes

## 🤝 Contributions
Pull requests are welcome! If you’d like to add features, improve security hardening, optimize code, or extend functionality, feel free to open an issue or PR. This is a learning-focused lab project, and collaboration is encouraged.

## 📦 Setup

```bash
git clone https://github.com/yourusername/django-cms-secured.git
cd django-cms-secured
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver

🧪 Test Accounts
 Username  Role    Access Notes                 
 admin     Admin   Full access to admin + posts 
 editor    Editor  Can create/edit posts only   
 viewer    Viewer  Read-only access to posts

📄 Bonus Features
✅ Markdown support in post bodies
✅ Manual RBAC using decorators or middleware
✅ Templates with role-based visibility
✅ Expandable model structure for categories/tags
